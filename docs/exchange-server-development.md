---
title: Exchange Online 和 Exchange 开发
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: f33d1093-75ba-4ff2-8d15-b0bf73a401bf
description: 查找 Exchange Server 的深入开发人员文档，包括作为 Office 365 的一部分的 Exchange Online 和 Exchange Server 内部部署版本。
localization_priority: Priority
ms.openlocfilehash: 12a29ca07801561e7a746603d795468d9cb7491f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528494"
---
# <a name="exchange-online-and-exchange-development"></a>Exchange Online 和 Exchange 开发

查找 Exchange Server 的深入开发人员文档，包括作为 Office 365 的一部分的 Exchange Online 和 Exchange Server 内部部署版本。

您可以使用 how to、入门、新功能和 API 参考文档来开发工具来访问和管理来自服务、网站、桌面计算机和移动设备的邮箱数据，并为存储在 Exchange Online 或 Exchange 2010、2013、2016和2019服务器上的电子邮件、日历、联系人和其他项目创建自定义解决方案。

您可以使用 Graph API、REST API、Exchange Web 服务（EWS）、自动发现、Outlook 外接程序或其他 Api 来开发应用程序。 此页面可帮助你选择正确的 Exchange 技术。

## <a name="exchange-developer-content"></a>Exchange 开发人员内容

使用下表找出将帮助你实现自己的开发目标的技术和相关 API 内容。

> [!IMPORTANT]
> 我们建议使用 Microsoft Graph 这一 API 来访问 Exchange Online 数据。 为访问 Exchange Online 数据而设计的新应用程序应使用 Microsoft Graph。

|如果正在构建…|从这里开始|
|:-----|:-----|
|基于 REST 的应用，可访问作为 Office 365 的一部分的 Exchange Online|[针对邮件、日历和联系人的 Microsoft Graph REST API](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md) |
|用于在 Outlook、Outlook Web App 或适用于设备的 OWA 中显示信息的上下文敏感型应用 |[Outlook 加载项和 Exchange 中的 EWS](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) |
|不基于 .NET Framework 或 Java 的邮箱客户端 |[在 Exchange 中探索 EWS 托管 API、EWS 和 Web 服务](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) |
|使用 .NET Framework 访问 EWS 的邮箱客户端 |[EWS 托管 API 客户端应用程序入门](exchange-web-services/get-started-with-ews-managed-api-client-applications.md) |
|使用 Java 访问 EWS 的邮箱客户端 |[GitHub 上的 EWS Java API](https://github.com/OfficeDev/ews-java-api) |
|会自定义 Outlook 用户界面或依赖于 Outlook 业务逻辑的应用程序  |[Outlook VBA 参考](https://msdn.microsoft.com/VBA/VBA-Outlook) |
|适用于 Exchange Online 或 Exchange 2013 且您需从之前的 Exchange 版本迁移的应用程序  |[迁移到 Exchange 技术](migrating-to-exchange-online-and-exchange-2013-technologies.md) |
|从托管代码使用 Windows PowerShell 的自定义管理工具   |[Exchange 命令行管理程序](management/exchange-management-shell.md) |
|备份或还原 Exchange 数据的解决方案  |[Exchange 备份和还原](backup-restore/backup-and-restore-for-exchange-2013.md) |
|支持访问传输管道中的邮件的扩展   |[Exchange 中的传输代理](transport-agents/transport-agents-in-exchange-2013.md)  |
|适用于移动设备的邮箱客户端   |[Exchange ActiveSync](https://technet.microsoft.com/library/aa998357.aspx) |

## <a name="exchange-interactions-with-custom-applications"></a>与自定义应用程序的 Exchange 交互

您可以通过一部分这些技术使应用程序使用存储在 Exchange 中的数据，另一部分技术用于管理和控制 Exchange 服务器。大多数情况下，您可以使用多种编程技术或语言来完成任务，这就让您可以使用熟悉的技术和语言。例如，可以通过邮件 REST API、EWS 或 EWS 托管 API 为 Exchange 存储中的项目设置属性。

Exchange 通过多种方式与自定义应用程序交互，具体取决于应用程序的体系结构和功能。其核心是，Exchange 不仅传输邮件，还维护邮箱、执行基于表单的应用程序，等等。

|Exchange 交互|说明|
|:-----|:-----|
|**邮件传输**|Exchange 可作为发送邮件的应用程序的标准邮件服务器。<br/>Exchange 包括多个传输邮件的 API，如 REST、EWS 和 EWS 托管 API。<br/>此外，在使用 Exchange 处理和发送邮件时，应用程序可以使用传输代理来进行回复。 |
|**邮箱存储** |针对访问存储在邮箱中的数据的应用程序，Exchange 会提供分层的文件夹、项目和属性结构。<br/>您可以使用数据库和组件对象样式的组合访问该存储信息。<br/>您可以执行有关数据的查询，并且 Exchange 将基于用户和存储权限管理对存储数据的访问权限。<br/>处理邮箱数据的应用程序通常使用 REST、EWS 或 EWS 托管 API。|
|**托管的企业服务器** |对于管理 Exchange 服务器和存储的应用程序，Exchange 可作为其托管服务器。<br/>应用程序可以配置、控制和监视整个组织中的 Exchange 服务器的当前活动及运行状况。<br/>Exchange 管理应用程序使用 Exchange 命令行管理程序来管理 Exchange 服务器。 |

## <a name="see-also"></a>另请参阅

- 
  [Exchange 的服务器 API 参考](https://msdn.microsoft.com/library/dn186243(v=exchg.150).aspx)
- [在 Office 博客上阅读有关 Exchange 的文章](https://www.microsoft.com/microsoft-365/blog/)
- [获取 Exchange 2013 的 101 代码示例](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)
- [获取 EWS 托管 API (GitHub)](https://github.com/OfficeDev/ews-managed-api/blob/master/README.md)
- [获取 Exchange Server 支持](https://support.microsoft.com/getsupport?oaspworkflow=start_1.0.0.0&wf=0&wfname=productselection&gprid=730&x=13&y=7&st=1&wfxredirect=1&sd=gn&ccsid=635890984021344661&forceorigin=esmc)
