---
title: Exchange 备份和还原
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: 查找有关为 Exchange 2013 创建备份和还原应用程序的信息。
ms.openlocfilehash: 2be8295985651319860ab2d2a143d69f663bf932
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514898"
---
# <a name="backup-and-restore-for-exchange"></a>Exchange 备份和还原
  
Exchange Server 2013 提供了数据库可用性组 (DAG) ，帮助保持存储数据的安全和可用，并减少对自定义备份和还原应用程序的需要。 使用 DAG 可实现场外数据冗余，以帮助确保不会丢失数据。 但是，许多灾难恢复计划仍包括更多传统的备份和还原方法和系统，包括自定义应用程序，以实现 DAG 的冗余。 为了帮助确保数据在组织中的可用性和冗余性，您可以创建使用 Exchange Server 和 Windows Server 操作系统技术来备份和还原 Exchange 数据。

<a name="bk_plugin"> </a>

## <a name="backup-technologies-in-exchange-2013"></a>2013 年 Exchange 中的备份技术

Exchange 2013 包含一个 Windows Server Backup 插件，管理员可使用该插件对数据进行基于 VSS Exchange备份。 管理员还可使用 Windows 备份来备份和还原Exchange数据库。 如果要为 Exchange 2013 创建备份和还原应用程序，则需要创建支持适用于 Exchange 2013 的 VSS 编写器且可感知 Exchange 的应用程序，并使用 CHKSGFILES API 验证该备份的一致性。 有关详细信息，请参阅 Validate [backup integrity by using the CHKSGFILES API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)。

<a name="bk_vsswriter"> </a>

## <a name="vss-writer-in-exchange-2013"></a>2013 Exchange VSS 编写器

Exchange 2013 年 2 月对 2010 和 2007 Exchange Server VSS 编写器体系结构Exchange Server重大更改。 Exchange 2010 和 Exchange 2007 包含两个 VSS 编写器：一个位于 Exchange 信息存储服务 (store.exe) 内部，另一个位于 Exchange 复制服务 (msexchangerepl.exe) 。 在 Exchange 2013 中，VSS 编写器功能位于 Exchange 复制服务中。 备份和还原应用程序使用称为 Microsoft Exchange 编写器的新 VSS 编写器来备份主动和被动数据库副本，并还原备份的数据库副本。 尽管新的 VSS 编写器在 Exchange 复制服务中运行，Exchange信息存储服务必须运行，以便编写器可用。 因此，为了能够备份或还原 Exchange 数据库，这两项服务都是必需的。
  
尽管 VSS 编写器体系结构在 2013 Exchange进行了更新，但基础功能没有更改。 如果为 Exchange 2010 创建了备份和还原应用程序，则无需对 Exchange 2013 的应用程序进行更改。 请务必使用最新文件重新编译应用程序以确保兼容性。 对于为 Exchange 2007 或早期版本创建的备份和还原应用程序，你将需要重写代码以使用最新的 CHKSGFILES API。
  
## <a name="what-you-need-to-know-about-vss-backup-and-restore"></a>您需要了解的 VSS 备份和还原信息

|如果你想知道...|请参阅这个|
|:-----|:-----|
|应用程序体系结构  <br/> |使用 VSS 备份 Exchange 数据库的备份和还原应用程序通常包含一个执行备份的后台服务、一个计划服务和一个控制并配置备份和还原系统的 Windows GUI 应用程序控制台。  <br/> |
|远程使用情况  <br/> |使用 VSS 备份 Exchange 服务器的应用程序必须在 Windows Server 2008 计算机上运行Exchange存储进程。 由于大型存储系统的灵活性，承载存储卷的硬件实际上可能并不属于运行 Windows Server 2008 的计算机。  <br/> |
|语言和工具  <br/> |可以使用任何 COM 兼容的语言来使用 VSS。 它最常用于用 C++ 编写的应用程序中。 由于您必须使 Exchange 存储脱机以创建卷影副本，因此备份应用程序通常区分时间，这在大多数情况下使使用 Visual Basic 或 VBScript 等语言不切实际。  <br/> |
|托管实现  <br/> |您可以通过 COM 互操作程序集在托管代码环境中使用 VSS API。  <br/> |
|可脚本化  <br/> |可以，但不建议这样做。  <br/> |
|可用测试和调试工具  <br/> |调试使用 VSS 的应用程序不需要任何特殊Windows。  <br/> |
   
## <a name="in-this-section"></a>本节内容

- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    
- [构建适用于 Exchange 2013 的备份和还原应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [CChkSGFiles 类参考](cchksgfiles-class-reference.md)
    
## <a name="see-also"></a>另请参阅

- [卷影复制服务 (Windows) ](https://msdn.microsoft.com/library/windows/desktop/bb968832%28v=vs.85%29.aspx)   
- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange 命令行管理程序](../management/exchange-management-shell.md)   
- [Exchange 中的传输代理](../transport-agents/transport-agents-in-exchange-2013.md) 
    

