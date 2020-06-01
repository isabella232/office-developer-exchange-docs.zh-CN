---
title: Exchange 备份和还原
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: 查找有关为 Exchange 2013 创建备份和还原应用程序的信息。
ms.openlocfilehash: 1c5d99be60501fd1c4414ea22294bd05645bb0a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455238"
---
# <a name="backup-and-restore-for-exchange"></a>Exchange 备份和还原
  
Exchange Server 2013 提供了数据库可用性组（Dag），可帮助保持存储数据的安全和可用性，并减少对自定义备份和还原应用程序的需求。 Dag 启用非现场数据冗余，以帮助确保您不会丢失数据。 但是，许多灾难恢复计划继续包含更传统的备份和还原方法以及系统（包括自定义应用程序），以实现 DAG 的冗余。 为了帮助确保组织中的数据可用性和冗余，您可以创建使用 Exchange Server 和 Windows Server 操作系统技术来备份和还原 Exchange 数据的自定义应用程序。

<a name="bk_plugin"> </a>

## <a name="backup-technologies-in-exchange-2013"></a>Exchange 2013 中的备份技术

Exchange 2013 包括 Windows Server 备份的插件，管理员可使用该插件进行 Exchange 数据的基于 VSS 的备份。 管理员还可以使用 Windows Server 备份来备份和还原 Exchange 数据库。 如果要为 Exchange 2013 创建备份和还原应用程序，您需要创建支持 exchange 2013 VSS 编写器的 Exchange 感知应用程序，并使用 CHKSGFILES API 验证该备份的一致性。 有关详细信息，请参阅[使用 Exchange 2013 中的 CHKSGFILES API 验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)。

<a name="bk_vsswriter"> </a>

## <a name="vss-writer-in-exchange-2013"></a>Exchange 2013 中的 VSS 编写器

Exchange 2013 在 Exchange Server 2010 和 Exchange Server 2007 中引入了对 VSS 写入器体系结构的重大更改。 Exchange 2010 和 Exchange 2007 包括两个 VSS 编写器：一个在 Exchange 信息存储服务（store.exe）中，一个在 Exchange 复制服务（msexchangerepl）内。 在 Exchange 2013 中，VSS 编写器功能位于 Exchange 复制服务中。 您的备份和还原应用程序使用新的 VSS 编写器（称为 Microsoft Exchange 编写器）来备份主动数据库副本和被动数据库副本，并还原备份的数据库副本。 尽管新的 VSS 编写器在 Exchange 复制服务中运行，但必须运行 Exchange 信息存储服务，编写器才能使用。 因此，为了能够备份或还原 Exchange 数据库，这两项服务都是必需的。
  
虽然 Exchange 2013 中更新了 VSS 编写器体系结构，但基础功能尚未更改。 如果为 Exchange 2010 创建了备份和还原应用程序，则无需对 Exchange 2013 的应用程序进行任何更改。 请务必使用最新文件重新编译应用程序以确保兼容性。 对于为 Exchange 2007 或更早版本创建的备份和还原应用程序，需要重写您的代码以使用最新的 CHKSGFILES API。
  
## <a name="what-you-need-to-know-about-vss-backup-and-restore"></a>您需要了解的有关 VSS 备份和还原的内容

|如果你想要了解 .。。|请参阅这个|
|:-----|:-----|
|应用程序体系结构  <br/> |使用 VSS 备份 Exchange 数据库的备份和还原应用程序通常由执行备份、计划服务的后台服务以及控制和配置备份和还原系统的 Windows GUI 应用程序控制台组成。  <br/> |
|远程使用情况  <br/> |使用 VSS 备份 Exchange 服务器的应用程序必须在运行 Exchange 存储进程的 Windows Server 2008 计算机上运行。 由于大型存储系统的灵活性，承载存储卷的硬件可能不会物理上是运行 Windows Server 2008 的计算机的一部分。  <br/> |
|语言和工具  <br/> |可以使用任何 COM 兼容的语言来使用 VSS。 它最常用于用 c + + 编写的应用程序。 因为您必须让 Exchange 存储脱机创建卷影副本，所以备份应用程序通常是时间敏感的，在大多数情况下，使用 Visual Basic 或 VBScript 这样的语言就会变得不切实际。  <br/> |
|托管实现  <br/> |您可以通过 COM 互操作程序集在托管代码环境中使用 VSS Api。  <br/> |
|可脚本化  <br/> |可以，但不建议这样做。  <br/> |
|可用测试和调试工具  <br/> |调试使用 Windows VSS 的应用程序不需要任何特殊工具。  <br/> |
   
## <a name="in-this-section"></a>本节内容

- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    
- [为 Exchange 2013 生成备份和还原应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [CChkSGFiles 类参考](cchksgfiles-class-reference.md)
    
## <a name="see-also"></a>另请参阅

- [卷影复制服务（Windows）](https://msdn.microsoft.com/library/windows/desktop/bb968832%28v=vs.85%29.aspx)   
- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange 命令行管理程序](../management/exchange-management-shell.md)   
- [Exchange 中的传输代理](../transport-agents/transport-agents-in-exchange-2013.md) 
    

