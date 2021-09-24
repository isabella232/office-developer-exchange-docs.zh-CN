---
title: 构建适用于 Exchange 2013 的备份和还原应用程序
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e5e952a5-add1-417c-a3c2-230f4dc99b00
description: 查找有关 Exchange 2013 备份和还原应用程序的组件和体系结构的信息，以及创建备份和还原应用程序的系统要求。
ms.openlocfilehash: 590ac029e157196d370cbcbe54e5df75bc1a830b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513876"
---
# <a name="build-backup-and-restore-applications-for-exchange-2013"></a>构建适用于 Exchange 2013 的备份和还原应用程序

查找有关 Exchange 2013 备份和还原应用程序的组件和体系结构的信息，以及创建备份和还原应用程序的系统要求。
  
**适用于：Exchange Server** 2013 
  
可以从 Windows Windows Server 2008 开始，在 Windows Server 版本中使用卷影复制服务 ([VSS](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx)) 来创建备份和还原 Exchange Server 2013 数据的应用程序。 VSS 提供了一个基础结构，使您能够跨第三方存储管理系统、业务应用程序和硬件创建和管理卷影副本。 您可以创建基于 VSS 基础结构的解决方案，这些基础结构使用卷影副本在 2013 数据库中备份和还原Exchange一个或多个。 
  
## <a name="backup-and-restore-application-prerequisites"></a>备份和还原应用程序先决条件
<a name="bk_systemrequirements"> </a>

为了使自定义备份和还原应用程序和 VSS 在 2013 Exchange备份和还原，您的环境必须包括：
  
- 从 Windows Server 2008 Windows版本的 Windows Server 
    
- Exchange 2013
    
此外，如果您要创建备份和还原应用程序，您应该了解对开发环境的以下限制：
  
- VSS 是一种非托管 COM API，可通过 COM 互操作程序集.NET Framework托管代码访问它。
    
- 命令行Exchange程序是一个托管应用程序，可通过托管代码.NET Framework访问。
    
- 随 2013 Exchange CHKSGFILES API 是 64 位本机代码 DLL。 不支持将 Exchange 2007 32 位 CHKSGFILES DLL 与 Exchange 2013 数据库一同使用。
    
## <a name="backup-and-restore-application-overview"></a>备份和还原应用程序概述
<a name="bk_components"> </a>

VSS 协调以下组件之间的通信： 
  
- VSS 请求程序，即您的备份应用程序
    
- VSS 编写器
    
- VSS 提供程序，它是创建卷影副本的系统、软件或硬件组件
    
若要使用 VSS 备份 Exchange 2013 数据，您的备份应用程序必须是 2013 Exchange 2013 感知的 VSS 请求程序。 Exchange 2013 包括一个 VSS 编写器（称为 Microsoft Exchange 编写器），用于 Windows Server 备份程序;但是，Exchange编写器仅备份整个卷。 它不会备份 2013 Exchange单个数据库。 如果您需要更大的灵活性，可以使用具有可处理单个 Exchange 数据库的 Exchange 感知 VSS 编写器的第三方备份应用程序，也可以创建自定义 VSS 请求程序。
  
在应用程序调用 VSS 以启动备份之前，它必须获取有关要备份的 Exchange 2013 系统的存储配置的信息。 该信息存储在 Active Directory 域服务 (AD DS) 。 备份应用程序可以使用命令行Exchange命令行管理程序命令获取Exchange配置数据。 有关详细信息，请参阅 Exchange Server [PowerShell (Exchange Management Shell) ](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。 
  
Exchange 2013 备份应用程序调用 VSS COM API 来创建数据库的完整、复制、差异和增量Exchange备份;它们不直接与 VSS 编写器交互。 Exchange 中的数据库可用性组 (DAG) 功能还允许应用程序创建完全一致的备份，即使初始完整备份和稍后的增量备份来自 DAG 中的不同服务器。 VSS 创建数据副本Exchange，备份应用程序会将数据存储到预期媒体上。
  
若要还原 Exchange 2013 数据库，还原应用程序会从备份媒体检索数据库和日志文件，将它们存储在 Exchange 服务器的活动磁盘存储中。 各个数据库不与特定数据库Exchange关联。 
  
备份和还原应用程序必须指定许多特定于 Exchange 2013 的参数，以正确控制和管理 VSS 针对 Exchange 2013 数据库运行的操作。 例如，由于 Exchange 2013 最多支持 100 个同时处于活动状态的数据库，因此备份应用程序必须正确指定并处理数据库文件、事务日志文件和检查点文件数据库组件。
  
若要重新构造自上次完整备份以来发生更改的数据库，还原应用程序需要不同备份中的数据库和日志文件。 例如，可能需要每周完整备份和一个或多个每日增量备份。 在使用 DAG 的 Exchange 2013 系统中，还原应用程序可以使用来自同一 DAG 中不同服务器上不同数据库副本的备份来重新生成数据库。 但是，从备份还原 DAG 数据库的唯一受支持的方法就是使用相同的数据还原数据库的所有主动和被动副本。
  
所有数据就位后，还原应用程序Exchange检查数据库和日志文件的完整性。 如果数据库和日志文件已正确还原，Exchange服务器可以重播数据库日志文件，使数据库更新并装入。 如果数据库已恢复到已装入数据库的活动副本的服务器，则数据库将被视为恢复数据库。 如果数据库已恢复到其他服务器上，则数据库可以独立装入，也可以将副本添加到 DAG 中。
  
## <a name="backup-and-restore-system-architecture"></a>备份和还原系统体系结构
<a name="bk_ExchangeVSS"> </a>

VSS 通过第三Windows提供程序或自定义存储提供程序与 Windows Server 文件系统和大容量存储设备驱动程序)  (通信。 硬件提供商确定将在何处创建卷影副本。 VSS 将硬件特定的卷影副本抽象化，以便备份和还原应用程序可以访问卷影副本，而无需了解有关硬件实现详细信息的信息。 下图显示了备份和还原应用程序如何与 Exchange 2013 和 Windows Server 进行交互。
  
**图 1.备份和还原系统体系结构**

![此图显示备份和恢复应用程序如何进行交互。在 Exchange、Windows Server 和客户端应用程序之间存在双向通信。Windows Server 还会与大容量存储设备或备份媒体交互。](media/VSS_architecture_E2k7.gif)
  
备份和还原应用程序将用作 VSS 请求程序。 请求者与 VSS 通信，以获取有关 Exchange 2013 的信息、启动卷影副本的创建以及获取数据访问权限以用于备份。 
  
Exchange存储是 Exchange 2013 的组件，Exchange Windows Server 文件系统访问 Windows 2013 数据库。 在文件系统内，每台 Exchange 服务器可同时装入多达 100 个数据库及其附带的数据库 (.edb) 文件、事务日志文件和检查点文件。
  
为了支持 VSS，Exchange 2013 Exchange内置到 VSS Exchange编写器。 Exchange 编写器与 Exchange 存储 (代表请求程序) 进行协调，以在备份数据库之前冻结和卸除数据库，然后在备份完成后解除冻结并装入数据库。 在还原过程中，备份和还原应用程序会指示 Exchange 编写器与 Exchange 存储进行协调，以卸除数据库、替换数据库文件、装入数据库，然后根据需要重播 (日志) 。
  
在还原过程中，请求程序还会与 VSS 通信，为还原准备系统，然后将数据放回到大容量存储设备。 备份和还原应用程序还负责与 Windows Server 一起读取数据，以及将数据写入备份存储媒体，无论是磁带存档、存储区域网络还是其他备份媒体。
  
还原的数据库可以装入为常规的活动数据库，也可以作为 Exchange 2013 恢复数据库装入。 只能将一个装入的数据库指定为每台服务器上Exchange数据库。
  
成功完成 Exchange 2013、VSS 和备份和还原应用程序之间的备份和还原操作所需的信息作为 Exchange 编写器元数据的一部分进行传输。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [Exchange 2013 的备份操作类型](types-of-backup-operations-for-exchange-2013.md)
    
- [还原 Exchange 2013 数据库](restoring-exchange-2013-databases.md)
    
- [在 2013 年 6 月使用 CHKSGFILES API Exchange完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [使用 2013 年 10 月中的 Eseutil 工具Exchange完整性](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 备份和还原](backup-and-restore-for-exchange-2013.md) 
- [CChkSGFiles 类参考](cchksgfiles-class-reference.md) 
- [卷影复制服务](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx) 
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

