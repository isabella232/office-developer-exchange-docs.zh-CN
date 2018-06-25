---
title: 备份和还原 exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: 查找信息创建备份和还原 Exchange 2013 的应用程序。
ms.openlocfilehash: 9eceb3d512a73ad9cb07a01864fb8b029d5b5772
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752685"
---
# <a name="backup-and-restore-for-exchange"></a>备份和还原 exchange
  
Exchange Server 2013 提供数据库可用性组 (Dag) 帮助保持存储的数据安全和可用，并减少需要自定义备份和还原应用程序。 Dag 启用非现场数据冗余，以帮助确保您不会丢失数据。 但是，许多灾难恢复计划继续包括更传统的备份和还原方法和系统，包括自定义应用程序，与 DAG 的冗余。 为了帮助确保数据可用性和您的组织中的冗余，您可以创建自定义应用程序使用 Exchange Server 和 Windows Server 操作系统技术备份和还原 Exchange 数据。

<a name="bk_plugin"> </a>

## <a name="backup-technologies-in-exchange-2013"></a>Exchange 2013 中的备份技术

Exchange 2013 包括插件管理员可用于基于 VSS 备份 Exchange 数据的 Windows Server Backup。 管理员还可以使用 Windows 服务器备份来备份和还原 Exchange 数据库。 如果您所创建的备份和还原 Exchange 2013 的应用程序，您需要创建的 Exchange 感知应用程序支持的 Exchange 2013 VSS 编写器并使用 CHKSGFILES API 以验证该备份的一致性。 有关详细信息，请参阅[使用 CHKSGFILES API 在 Exchange 2013 验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)。

<a name="bk_vsswriter"> </a>

## <a name="vss-writer-in-exchange-2013"></a>Exchange 2013 中的 VSS 编写器

Exchange 2013 到 Exchange Server 2010 和 Exchange Server 2007 中的 VSS 编写器体系结构引入了重大更改。 Exchange 2010 和 Exchange 2007 包括两个 VSS 编写器： 一个内部 Exchange 信息存储服务 (store.exe) 和一个内部 Exchange 复制服务 (msexchangerepl.exe)。 在 Exchange 2013 VSS 编写器功能位于 Exchange 复制服务。 备份和还原应用程序使用名为 Microsoft Exchange Writer，新 VSS 编写器备份主动和被动数据库副本，并还原备份数据库副本。 虽然在 Exchange 复制服务运行新 VSS 编写器，Exchange 信息存储服务必须运行编写器可顺序。 因此，这两种服务所需备份或还原 Exchange 数据库。
  
虽然 Exchange 2013 中已更新 VSS 编写器体系结构，但未更改的基本功能。 如果您创建的 Exchange 2010 的备份和还原应用程序，您不需要对 Exchange 2013 的应用程序进行任何更改。 请务必使用最新的文件，以确保兼容编译应用程序。 备份和还原应用程序，为 Exchange 2007 或早期版本创建，您将需要重写代码以使用最新的 CHKSGFILES API。
  
## <a name="what-you-need-to-know-about-vss-backup-and-restore"></a>您需要了解 VSS 备份和还原

|如果您想知道有关...|请参阅这个|
|:-----|:-----|
|应用程序体系结构  <br/> |使用 VSS 备份 Exchange 数据库通常组成执行备份的背景服务、 计划服务和 Windows 图形用户界面应用程序控制台的控件，并将配置备份和还原系统备份和还原应用程序。  <br/> |
|远程使用情况  <br/> |使用 VSS 备份 Exchange 服务器的应用程序必须在其运行 Exchange 存储进程在 Windows Server 2008 计算机上运行。 由于在大型存储系统的灵活性，承载存储卷的硬件可能不从物理上隔离是计算机的运行 Windows Server 2008 的一部分。  <br/> |
|语言和工具  <br/> |您可以使用任何 COM 兼容语言使用 vss。 在 c + + 编写的应用程序中最常使用它。 由于您必须采取 Exchange 存储脱机创建卷影副本，备份应用程序将是通常时效性，在大多数情况下使使用 Visual Basic 或 VBScript 不切实际类似的语言。  <br/> |
|托管实现  <br/> |您可以通过 COM 互操作程序集的托管的代码环境中使用 VSS Api。  <br/> |
|可脚本化  <br/> |是，但不是建议这样做。  <br/> |
|可用测试和调试工具  <br/> |没有特殊工具所需调试应用程序使用 Windows vss。  <br/> |
   
## <a name="in-this-section"></a>本节内容

- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    
- [构建备份和还原 Exchange 2013 的应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [CChkSGFiles 类参考 （英文）](cchksgfiles-class-reference.md)
    
## <a name="see-also"></a>另请参阅

- [卷影复制服务 (Windows)](http://msdn.microsoft.com/en-us/library/windows/desktop/bb968832%28v=vs.85%29.aspx)   
- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange 命令行管理程序](../management/exchange-management-shell.md)   
- [在 Exchange 传输代理](../transport-agents/transport-agents-in-exchange-2013.md) 
    

