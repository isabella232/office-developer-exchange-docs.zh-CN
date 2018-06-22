---
title: Exchange Online 和 Exchange 开发
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f33d1093-75ba-4ff2-8d15-b0bf73a401bf
description: 查找 Exchange Server 的详细开发人员文档，包括 Office 365、Exchange Online、Exchange 2013、EWS 托管 API、Exchange 2010 和 Exchange 2007 中的 Exchange Online。
ms.openlocfilehash: b933bd1bdc6dfcbe4941f23dbee9a587745c7bd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752703"
---
# <a name="exchange-online-and-exchange-development"></a>Exchange Online 和 Exchange 开发

查找 Exchange Server 的详细开发人员文档，包括 Office 365、Exchange Online、Exchange 2013、EWS 托管 API、Exchange 2010 和 Exchange 2007 中的 Exchange Online。 

您可以使用如何，获取开始、 新建功能和 API 参考文档，以开发工具来访问和管理服务、 网站、 台式计算机和移动设备中的邮箱数据以及创建自定义解决方案的电子邮件、 日历、 联系人和在 Exchange Online 或 Exchange 2013 服务器上存储其他项目。 

您可以使用 Exchange Web 服务 (EWS)、自动发现、适用于 Office 的邮件应用程序或其他 API 开发应用程序。 此页面可帮助您选择正确的 Exchange 技术。

## <a name="exchange-developer-content"></a>Exchange 开发人员内容  

使用下表识别将帮助您实现开发目标的技术和相关 API 内容。  
  
|如果您正在构建…|从这里开始|
|:-----|:-----|
|用于访问 Exchange Online 作为 Office 365 的一部分的基于 REST 的应用程序|[Office 365 REST Api 的邮件、 日历和联系人](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md) |
|在 Outlook、 Outlook Web App 或适用于设备的 OWA 中显示信息的上下文相关应用程序 |[Outlook 和 Exchange 中的 EWS 的邮件应用程序](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) |
|不基于.NET Framework 或 Java 邮箱客户端 |[在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) |
|使用.NET Framework 访问 EWS 的邮箱客户端 |[EWS 托管 API 客户端应用程序入门](exchange-web-services/get-started-with-ews-managed-api-client-applications.md) |
|使用 Java 访问 EWS 的邮箱客户端 |[GitHub 上的 EWS Java API](https://github.com/OfficeDev/ews-java-api) |
|自定义 Outlook 用户界面或依赖 Outlook 业务逻辑的应用程序  |[Outlook VBA 参考](https://msdn.microsoft.com/en-us/VBA/VBA-Outlook) |
|针对 Exchange Online 的应用程序或 Exchange 2013 所需从以前版本的 Exchange 迁移  |[迁移到 Exchange 技术](migrating-to-exchange-online-and-exchange-2013-technologies.md) |
|使用 Windows PowerShell 从托管代码的自定义管理工具   |[Exchange 命令行管理程序](management/exchange-management-shell.md) |
|要备份或还原 Exchange 数据解决方案  |[备份和还原 exchange](backup-restore/backup-and-restore-for-exchange-2013.md) |
|在传输管道中支持访问邮件扩展   |[在 Exchange 传输代理](transport-agents/transport-agents-in-exchange-2013.md)  |
|适用于移动设备邮箱客户端   |[Exchange ActiveSync](https://technet.microsoft.com/en-us/library/aa998357.aspx) |
   
## <a name="exchange-interactions-with-custom-applications"></a>Exchange 与自定义应用程序的交互

您可以通过一部分这些技术使应用程序使用存储在 Exchange 中的数据，另一部分技术用于管理和控制 Exchange 服务器。大多数情况下，您可以使用多种编程技术或语言来完成任务，这就让您可以使用熟悉的技术和语言。例如，可以通过邮件 REST API、EWS 或 EWS 托管 API 为 Exchange 存储中的项目设置属性。
  
Exchange 通过多种方式与自定义应用程序交互，具体取决于应用程序的体系结构和功能。其核心是，Exchange 不仅传输邮件，还维护邮箱、执行基于表单的应用程序，等等。

|Exchange 交互|说明|
|:-----|:-----|
|**邮件传输**|Exchange 充当发送邮件的应用程序的标准邮件服务器。<br/>Exchange 包括多个传输邮件的 API，如 REST、EWS 和 EWS 托管 API。<br/>此外，在 Exchange 处理和传递邮件时，应用程序可以使用传输代理作出响应。 |
|**邮箱存储** |Exchange 为访问存储在邮箱中的数据的应用程序提供了文件夹、项目和属性的层次结构。<br/>您可以使用数据库和组件对象样式的组合访问该存储信息。<br/>您可以执行有关数据的查询，并且 Exchange 将基于用户和存储权限管理对存储数据的访问权限。<br/>处理邮箱数据的应用程序通常使用 REST、EWS 或 EWS 托管 API。|
|**管理的企业服务器** |对于管理 Exchange 服务器和存储的应用程序，Exchange 起着托管服务器的作用。<br/>应用程序可以配置、控制和监视整个组织中的 Exchange 服务器的当前活动及运行状况。<br/>Exchange 管理应用程序使用 Exchange Management Shell 来管理 Exchange 服务器。 |
   
## <a name="see-also"></a>另请参阅

- [Exchange server API 参考](https://msdn.microsoft.com/en-us/library/dn186243(v=exchg.150).aspx)
- [阅读 Office 上的 Exchange 博客](https://www.microsoft.com/en-us/microsoft-365/blog/) 
- [获取 Exchange 2013 的 101 个代码示例](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)
- [获取 EWS 托管的 API (GitHub)](https://github.com/OfficeDev/ews-managed-api/blob/master/README.md)
- [获取 Exchange Server 支持](https://support.microsoft.com/en-us/getsupport?oaspworkflow=start_1.0.0.0&wf=0&wfname=productselection&gprid=730&x=13&y=7&st=1&wfxredirect=1&sd=gn&ccsid=635890984021344661&forceorigin=esmc)


