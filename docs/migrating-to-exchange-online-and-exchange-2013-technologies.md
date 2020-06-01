---
title: 迁移到 Exchange 技术
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: 如果要从早期版本的 Exchange 进行迁移，请使用本文中的信息来确定当前产品版本支持的开发技术，以及要迁移到的技术。
ms.openlocfilehash: d82f1b305fd1cc30e48cddbf9bf2981d3d829a5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459151"
---
# <a name="migrating-to-exchange-technologies"></a>迁移到 Exchange 技术

如果要从早期版本的 Exchange 进行迁移，请使用本文中的信息来确定当前产品版本支持的开发技术，以及要迁移到的技术。
  
## <a name="determine-if-your-technology-is-available-in-current-versions"></a>确定您的技术在当前版本中是否可用

使用下表确定是否支持 Exchange Online 或 Exchange 2019 中的开发技术。 如果技术不受支持，请参阅[选择要迁移到的开发技术](#bk_choose)。

<br/> 

**Exchange 开发技术和产品版本**

|技术协会|Office 365 和 Exchange Online|Exchange 2019|Exchange 2016|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|[Office 365 API 平台概述](https://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> |X ²  <br/> |X ¹²  <br/> ||
|[EWS Managed API](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange Web 服务（EWS）](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Outlook 邮件应用程序](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Outlook 对象模型（OOM）](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[备份和还原](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[传输代理](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Active Directory 服务接口 (ADSI)  <br/> ||||||X  <br/> |
|Exchange 的协作数据对象（CDOEX）  <br/> ||||||X  <br/> |
|适用于 Windows 2000 的协作数据对象（CDOSYS）  <br/> ||||||X  <br/> |
|Exchange OLE DB 提供程序（EXOLEDB）  <br/> ||||||X  <br/> |
|Exchange 存储事件接收器  <br/> ||||||X  <br/> |
|增量更改同步 (ICS)  <br/> ||||||X  <br/> |
|轻型目录访问协议 (LDAP)  <br/> ||||||X  <br/> |
|[消息处理 API （MAPI）](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> | 
|Outlook Web App 自定义  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Web 分布式创作和版本控制（WebDAV）  <br/> ||||||X  <br/> |

<a name="bk_choose"> </a>

¹ REST API 和 Graph API 需要累积更新3的 Exchange 2016。

仅限²混合客户可以利用适用于 Office 365 和内部部署邮箱的 REST Api。

## <a name="choose-a-development-technology-to-migrate-to"></a>选择要迁移到的开发技术

如果您的应用程序使用的技术不受支持或 deemphasized 在 Exchange Online 或 Exchange 2013 中，请使用下表来决定要迁移到的技术。
  
**推荐的技术迁移途径**

|**技术协会**|**在 Office 365、Exchange Online 和 Exchange 2019 中是否受支持？**|**迁移到**|**更多信息**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |是，但 deemphasized <br/>|[Exchange 命令行管理程序](management/exchange-management-shell.md)<br/> |无。  <br/> |
|CDOEX  <br/> |否  <br/> |[EWS 托管 API 或 EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |EWS 托管 API 和 EWS 可以访问 CDOEX 提供的同一 Exchange 存储。 与使用 CDOEX 生成的客户端应用程序不同，您可以在本地或远程计算机上运行 EWS 应用程序。  <br/> |
|CDOEXM  <br/> |否 <br/> |[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |Exchange 命令行管理程序命令控制 Exchange 服务器、存储组、数据库和用户，而不仅仅是对应的 CDOEXM Api。 此外，您可以轻松地将 CDOEXM 应用程序迁移到 Exchange 命令行管理程序命令。  <br/> |
|CDOSYS<br/> |否<br/> |[传输代理](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |将传输代理用于与 Exchange 2010 中的 Exchange 版本一起使用的基于通知的应用程序。<br/><br/> CDOSYS 包含在 Windows 的当前版本中。 CDOSYS 中的功能在 .NET Framework 中可用。  <br/> |
|CDOWF  <br/> |否  <br/> |[Windows Workflow Foundation （WWF）](https://msdn.microsoft.com/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |您可以使用 WWF 创建适用于 Exchange 2007 的高级工作流应用程序。   <br/> |
|ExOLEDB  <br/> |否  <br/> |[EWS 托管 API 或 EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |EWS 托管 API 和 EWS 提供了与 ExOLEDB 提供的 Exchange 存储相同的访问权限。 与使用 ExOLEDB 构建的客户端应用程序不同，您可以在本地或远程计算机上运行 EWS 应用程序。  <br/> |
|用作  <br/> |是，但 deemphasized  <br/> |EWS 托管 API 或 EWS<br/> |您可以使用 EWS 托管 API 或 EWS[订阅通知](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)并[同步邮箱数据](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)。  <br/> |
|LDAP  <br/> |是，但 deemphasized  <br/> |[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |无。  <br/> |
|MAPI  <br/> |是，但 deemphasized  <br/> |Office 365 Api 平台概述、EWS 托管 API、EWS <br/> |尽管 MAPI 目前是一种受支持的开发技术，但最终必须将 MAPI 应用程序重新设计为使用较新的技术。<br/><br/>如果 MAPI 应用程序对邮件、日历或联系人对象执行简单的读取、写入和更新操作，并面向 Office 365，则 Exchange 2019 ² or Exchange 2016 ¹²可以[对邮件、日历和联系人使用 Office 365 REST api](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)。<br/><br/>如果您针对的是本地 Exchange，并且您需要访问 MAPI 可以访问的所有属性，则可以使用 EWS 托管 API 或 EWS 以及[架构化属性或扩展属性](https://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx)。<br/><br/>**注意**： [ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx)类提供了对来自 EWS 托管 API 的 mapi 的访问权限，而[ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素提供了对来自 ews 的 mapi 属性的访问权限。           |
|Outlook Web App 自定义  <br/> |否  <br/> |[邮件应用程序](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |无。  <br/> |
|存储事件接收器  <br/> |否  <br/> |EWS 托管 API 或 EWS <br/> |您可以使用 EWS 托管 API 或 EWS[订阅通知](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)并[同步邮箱数据](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)。<br/><br/>EWS 中的通知与存储事件接收器的 Exchange 存储提供相同的访问权限。 您可以使用 Visual Studio 工具来简化使用 EWS 的 microsoft store 事件感知客户端应用程序的开发。  <br/> |
|流式备份和还原  <br/> |否  <br/> |[卷影复制服务（VSS）编写器](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |无。  <br/> |
|WebDAV  <br/> |否  <br/> |Office 365 Api 平台概述、EWS 托管 API 或 EWS <br/> |如果您的 WebDAV 应用程序对邮件、日历或联系人对象执行简单的读取、写入和更新操作，并且您将针对 Office 365、Exchange 2019 ²或 Exchange 2016 ¹²，则可以将[office 365 REST api 用于邮件、日历和联系人](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)。<br/><br/>否则，如果您针对的是本地 Exchange，并且您需要访问 WebDAV 提供的 Exchange 存储中的相同属性，请使用 EWS 托管 API 或 EWS。  <br/> |
|WebDAV 通知  <br/> |否  <br/> |EWS 托管 API 或 EWS<br/> |您可以使用 EWS 托管 API 或 EWS[订阅通知](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)。  <br/> |
|Web 表单  <br/> |否  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |切换到 ASP.NET 并更新应用程序，以使用 EWS 访问邮箱和服务器信息。  <br/> |
|WMI 提供程序  <br/> |否  <br/> |[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |无。  <br/> |
   
¹ REST API 和 Graph API 需要累积更新3的 Exchange 2016。

仅限²混合客户可以利用适用于 Office 365 和内部部署邮箱的 REST Api。

## <a name="see-also"></a>另请参阅

- [选择某个 API 或技术开发适用于 Outlook 的解决方案](https://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
- [针对 REST API 的本地体系结构要求](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api/)    
