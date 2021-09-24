---
title: 迁移到 Exchange 技术
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: 如果要从早期版本的 Exchange 进行迁移，请使用本文中的信息了解当前产品版本中支持哪些开发技术，以及要迁移到的技术。
ms.openlocfilehash: 3885d6789cedf5de028b64a0658b336bd021b9ee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526999"
---
# <a name="migrating-to-exchange-technologies"></a>迁移到 Exchange 技术

如果要从早期版本的 Exchange 进行迁移，请使用本文中的信息了解当前产品版本中支持哪些开发技术，以及要迁移到的技术。
  
## <a name="determine-if-your-technology-is-available-in-current-versions"></a>确定你的技术在当前版本中是否可用

使用下表确定开发技术在 2019 年 3 月Exchange Online Exchange受支持。 如果技术不受支持，请参阅选择要迁移到 [的开发技术](#bk_choose)。

<br/> 

**Exchange开发技术和产品版本**

|技术|Office 365 和 Exchange Online|Exchange 2019|Exchange 2016|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|[Office 365 API 平台概述](https://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> |X×  <br/> |X¹ ¹  <br/> ||
|[EWS 托管 API](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[ExchangeWeb 服务 (EWS) ](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Outlook 邮件应用程序](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[OutlookOOM (对象) ](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[备份和还原](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[传输代理](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Active Directory 服务接口 (ADSI)  <br/> ||||||X  <br/> |
|CDOEX Exchange (协作数据)   <br/> ||||||X  <br/> |
|2000 Windows CDOSYS (协作数据)   <br/> ||||||X  <br/> |
|ExchangeOLE DB Provider (EXOLEDB)   <br/> ||||||X  <br/> |
|Exchange 存储事件接收器  <br/> ||||||X  <br/> |
|增量更改同步 (ICS)  <br/> ||||||X  <br/> |
|轻型目录访问协议 (LDAP)  <br/> ||||||X  <br/> |
|[MAPI (消息 API) ](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> | 
|Outlook Web App自定义  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Web 分布式创作和版本 (WebDAV)   <br/> ||||||X  <br/> |

<a name="bk_choose"> </a>

¹REST API 和 Graph API 需要 2016 年 2 月累积更新 3 Exchange 3。

1Only 混合客户能够利用本地邮箱和本地Office 365 REST API。

## <a name="choose-a-development-technology-to-migrate-to"></a>选择要迁移到的开发技术

如果您的应用程序使用的技术在 Exchange Online 或 Exchange 2013 中不受支持或未经过强调，请使用下表确定要迁移到的技术。
  
**推荐的技术迁移路径**

|**技术**|**在 Office 365、Exchange Online 和 Exchange 2019 中受支持？**|**迁移到**|**更多信息**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |是，但强调 <br/>|[Exchange 命令行管理程序](management/exchange-management-shell.md)<br/> |无。  <br/> |
|CDOEX  <br/> |否  <br/> |[EWS 托管 API 或 EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |EWS 托管 API 和 EWS 可以访问Exchange CDOEX 提供的相同存储。 与使用 CDOEX 构建的客户端应用程序不同，您可以在本地或远程计算机上运行 EWS 应用程序。  <br/> |
|CDOEXM  <br/> |否 <br/> |[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |Exchange命令行管理程序Exchange控制服务器、存储组、数据库和用户，比相应的 CDOEXM API 要简单。 此外，您还可以轻松地将 CDOEXM 应用程序迁移到命令行Exchange命令行管理程序命令。  <br/> |
|CDOSYS<br/> |否<br/> |[传输代理](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |从 2010 年 10 月Exchange基于通知的应用程序使用Exchange代理。<br/><br/> CDOSYS 包含在当前版本的 Windows。 CDOSYS 中的功能在 .NET Framework。  <br/> |
|CDOWF  <br/> |否  <br/> |[WindowsWorkflow Foundation (WWF) ](https://msdn.microsoft.com/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |您可以使用 WWF 创建与 Exchange 2007 一起运行的高级工作流应用程序。   <br/> |
|ExOLEDB  <br/> |否  <br/> |[EWS 托管 API 或 EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |EWS 托管 API 和 EWS 提供对 exOLEDB Exchange存储的相同访问权限。 与使用 ExOLEDB 构建的客户端应用程序不同，您可以在本地或远程计算机上运行 EWS 应用程序。  <br/> |
|ICS  <br/> |是，但强调  <br/> |EWS 托管 API 或 EWS<br/> |您可以使用 EWS 托管 API 或 EWS 订阅[通知并](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)[同步邮箱数据](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)。  <br/> |
|LDAP  <br/> |是，但强调  <br/> |[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |无。  <br/> |
|MAPI  <br/> |是，但强调  <br/> |Office 365API 平台概述， EWS 托管 API， EWS <br/> |虽然 MAPI 当前是受支持的开发技术，但最终必须重新设计 MAPI 应用程序以使用较新的技术。<br/><br/>如果您的 MAPI 应用程序对邮件、日历或联系人对象执行简单的读取、写入和更新操作，并且针对 Office 365、Exchange 2019¹ 或 Exchange 2016¹ ¹，您可以将[Office 365 REST API](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)用于邮件、日历和联系人。<br/><br/>如果你面向本地Exchange，并且需要访问 MAPI 可以访问的所有属性，可以使用 EWS 托管 API 或 EWS 以及架构化属性或[扩展属性](https://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx)。<br/><br/>**注意**[：ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx)类提供从 EWS 托管 API 访问 MAPI 的访问权限 [，ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素提供对 EWS 中的 MAPI 属性的访问权限。           |
|Outlook Web App自定义  <br/> |否  <br/> |[邮件应用程序](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |无。  <br/> |
|存储事件接收器  <br/> |否  <br/> |EWS 托管 API 或 EWS <br/> |您可以使用 EWS 托管 API 或 EWS 订阅[通知并](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)[同步邮箱数据](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)。<br/><br/>EWS 中的通知提供对存储事件接收器Exchange存储的相同访问权限。 您可以使用 Visual Studio工具简化使用 EWS 的应用商店事件感知客户端应用程序的开发。  <br/> |
|流式备份和还原  <br/> |否  <br/> |[卷影复制服务 (VSS) 编写器](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |无。  <br/> |
|WebDAV  <br/> |否  <br/> |Office 365API 平台概述、EWS 托管 API 或 EWS <br/> |如果 WebDAV 应用程序对邮件、日历或联系人对象执行简单的读取、写入和更新操作，并且您将面向 Office 365、Exchange 2019¹ 或 Exchange 2016¹ ¹，您可以使用[Office 365 REST](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)API 进行邮件、日历和联系人。<br/><br/>否则，如果要Exchange内部部署，并且您需要访问 WebDAV 提供的 Exchange 存储中的相同属性，请使用 EWS 托管 API 或 EWS。  <br/> |
|WebDAV 通知  <br/> |否  <br/> |EWS 托管 API 或 EWS<br/> |您可以使用 EWS 托管 API 或 EWS 订阅 [通知](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)。  <br/> |
|Web 表单  <br/> |否  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |切换到 ASP.NET 应用程序，以使用 EWS 访问邮箱和服务器信息。  <br/> |
|WMI 提供程序  <br/> |否  <br/> |[Exchange 命令行管理程序](management/exchange-management-shell.md) <br/> |无。  <br/> |
   
¹REST API 和 Graph API 需要 2016 年 2 月累积更新 3 Exchange 3。

1Only 混合客户能够利用本地邮箱和本地Office 365 REST API。

## <a name="see-also"></a>另请参阅

- [选择某个 API 或技术开发适用于 Outlook 的解决方案](https://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
- [针对 REST API 的本地体系结构要求](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api/)    
