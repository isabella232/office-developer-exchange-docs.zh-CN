---
title: 迁移到 Exchange 技术
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: 如果您正在从早期版本的 Exchange 迁移的使用本文中的信息以找出哪些开发技术支持在当前的产品版本和要迁移到的技术。
ms.openlocfilehash: 82362b7bcdb79d6ca43603335d51a8bd8c1df239
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753052"
---
# <a name="migrating-to-exchange-technologies"></a>迁移到 Exchange 技术

如果您正在从早期版本的 Exchange 迁移的使用本文中的信息以找出哪些开发技术支持在当前的产品版本和要迁移到的技术。
  
## <a name="determine-if-your-technology-is-available-in-current-versions"></a>确定您的技术是否在当前版本中可用

下表用于确定是否开发技术支持在 Exchange Online 或 Exchange 2013。 如果不支持这种技术，请参阅[Choose 迁移到开发技术](#bk_choose)。

<br/> 

**Exchange 开发技术和产品版本**

|技术|Office 365 和 Exchange Online|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|
|[Office 365 Api 平台概述](http://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> ||||
|[EWS Managed API](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange Web 服务 (EWS)](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Outlook 邮件应用程序](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |||
|[Outlook 对象模型 (OOM)](http://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[备份和还原](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |
|[传输代理](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |
|Active Directory 服务接口 (ADSI)  <br/> ||||X  <br/> |
|协作数据对象 (CDOEX) Exchange  <br/> ||||X  <br/> |
|对于 Windows 2000 (CDOSYS) 的协作数据对象  <br/> ||||X  <br/> |
|Exchange OLE DB 提供程序 (EXOLEDB)  <br/> ||||X  <br/> |
|Exchange 存储事件接收器  <br/> ||||X  <br/> |
|增量更改同步 (ICS)  <br/> ||||X  <br/> |
|轻型目录访问协议 (LDAP)  <br/> ||||X  <br/> |
|[消息处理 API (MAPI)](http://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Outlook Web App 自定义  <br/> |||X  <br/> ||
|Web 分布式创作和版本管理 (WebDAV)  <br/> ||||X  <br/> |

<a name="bk_choose"> </a>

## <a name="choose-a-development-technology-to-migrate-to"></a>选择身份验证迁移到开发技术

如果您的应用程序使用的技术不受支持或 deemphasized 在 Exchange Online 或 Exchange 2013，请使用下表确定哪种技术迁移到。
  
**建议使用的技术的迁移路径**

|**技术**|**Office 365，Online，Exchange 和 Exchange 2013 中受支持？**|**迁移到**|**更多信息**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |是，但 deemphasized <br/>|[Exchange 命令行管理程序](management/exchange-management-shell.md)<br/> |无。  <br/> |
|CDOEX  <br/> |否  <br/> |[EWS 托管 API 或 EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |EWS 托管 API 和 EWS 可以访问同一 Exchange 存储 CDOEX 提供。 与使用 CDOEX 构建的客户端应用程序，您可以在本地或远程计算机上运行 EWS 应用程序。  <br/> |
|CDOEXM  <br/> |否 <br/> |[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |Exchange 命令行管理程序命令地控制 Exchange 服务器、 存储组、 数据库和用户比相应 CDOEXM Api。 此外，您可以轻松地迁移到 Exchange 命令行管理程序命令 CDOEXM 应用程序。  <br/> |
|CDOSYS<br/> |否<br/> |[传输代理](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |使用基于通知的应用程序与 Exchange 2010 开头的 Exchange 版本一起使用的传输代理。<br/><br/> CDOSYS 包含在当前版本的 Windows 中。 CDOSYS 中的功能是.NET Framework 中可用。  <br/> |
|CDOWF  <br/> |否  <br/> |[Windows Workflow Foundation (WWF)](http://msdn.microsoft.com/en-us/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |您可以使用 WWF 创建使用 Exchange 2007 的高级工作流应用程序。   <br/> |
|ExOLEDB  <br/> |否  <br/> |[EWS 托管 API 或 EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |EWS 托管 API 和 EWS 提供 ExOLEDB 提供的 Exchange 存储到相同的访问。 与使用 ExOLEDB 构建的客户端应用程序，您可以在本地或远程计算机上运行 EWS 应用程序。  <br/> |
|ICS  <br/> |是，但 deemphasized  <br/> |EWS 托管 API 或 EWS<br/> |您可以使用 EWS 托管 API 或 EWS[订阅通知](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)并[同步邮箱数据](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)。  <br/> |
|LDAP  <br/> |是，但 deemphasized  <br/> |[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |无。  <br/> |
|MAPI  <br/> |是，但 deemphasized  <br/> |Office 365 Api 平台概述，EWS 托管 API EWS <br/> |尽管 MAPI 当前是受支持的开发技术，您将最终需要重新设计您的 MAPI 应用程序能够使用较新的技术。<br/><br/>如果您的 MAPI 应用程序执行简单的读取、 写入和更新操作对邮件、 日历或联系对象和目标 Office 365，您可以使用[Office 365 REST Api 的邮件、 日历和联系人](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)。<br/><br/>如果您面向的 Exchange 内部部署，您需要访问 MAPI 可以访问的所有属性，您可以使用 EWS 托管 API 或 EWS 和[架构化属性或扩展属性](http://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx)。<br/><br/>**注意**： [ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx)类提供对 MAPI 从 EWS 托管 API 的访问并[ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素提供对 MAPI 属性从 EWS 的访问。           |
|Outlook Web App 自定义  <br/> |否  <br/> |[邮件应用程序](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |无。  <br/> |
|存储事件接收器  <br/> |否  <br/> |EWS 托管 API 或 EWS <br/> |您可以使用 EWS 托管 API 或 EWS[订阅通知](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)并[同步邮箱数据](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)。<br/><br/>通知中的 ews 提供对 Exchange 存储的同一访问存储事件接收器提供。 Visual Studio 工具可用于简化开发使用 EWS 的存储事件感知客户端应用程序。  <br/> |
|流式备份和还原  <br/> |否  <br/> |[卷影复制服务 (VSS) 编写器](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |无。  <br/> |
|WebDAV  <br/> |否  <br/> |Office 365 Api 平台概述，EWS 托管 API 或 EWS <br/> |如果您 WebDAV 应用程序的执行简单的读取、 写入和更新操作对邮件、 日历或联系对象，您将面向 Office 365 使用的[Office 365 REST Api 的邮件、 日历和联系人](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)。<br/><br/>否则，如果您面向的 Exchange 内部部署并且您需要在 Exchange 存储中的相同属性访问该 WebDAV 提供，使用 EWS 托管 API 或 EWS。  <br/> |
|WebDAV 通知  <br/> |否  <br/> |EWS 托管 API 或 EWS<br/> |您可以使用 EWS 托管 API 或 EWS 来[订阅通知](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)。  <br/> |
|Web 窗体  <br/> |否  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |切换到 ASP.NET 并更新应用程序使用 EWS 访问邮箱和服务器的信息。  <br/> |
|WMI 提供程序  <br/> |否  <br/> |[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |无。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [选择的 API 或技术来开发 Outlook 解决方案](http://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
    

