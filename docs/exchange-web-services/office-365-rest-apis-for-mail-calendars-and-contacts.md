---
title: 用于邮件、日历和联系人的 Microsoft Graph Outlook API
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: 查找有关可用于访问 Office 365 或 Exchange Online 中的邮件、日历和联系人的 Microsoft Graph API 的信息。
localization_priority: Priority
ms.openlocfilehash: 7ca77596afb59ffab76001abd495de7328d2dd29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463865"
---
# <a name="microsoft-graph-rest-apis-for-mail-calendars-and-contacts"></a>针对邮件、日历和联系人的 Microsoft Graph REST API

查找有关可用于在混合部署中访问 Office 365、Exchange Online 或 Exchange Server 中的邮件、日历和联系人的 Microsoft Graph Api 的信息。

在混合部署中，Office 365、Exchange Online 和 Exchange Server 提供了一种使用电子邮件、日历和联系人的新方法。 Microsoft Graph 邮件、日历和联系人 REST Api 提供了一种强大且易于使用的方法来访问和操作 Exchange 数据。 这些 Api 基于开放标准：用于身份验证的 OAuth 版本2.0，以及用于数据抽象的 OData 版本4.0 和 JSON。 这具有以下优点：

- 由于这些 Api 需要 OAuth 进行身份验证，因此应用程序不需要处理或存储用户凭据。

- 通过 OAuth，可以向用户数据请求严格范围的权限。 例如，您可以将应用程序设计为请求权限并只读取用户的日历。

## <a name="work-with-email-and-mail-folders"></a>使用电子邮件和邮件文件夹

您可以使用[邮件 API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview)来获取、创建、更新、删除、移动、复制和发送电子邮件。 您还可以获取、创建、更新和删除邮件文件夹。 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a>使用事件、日历和日历组

您可以使用[日历 API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview)来获取、创建、更新和删除事件。 您还可以获取、创建、更新和删除日历组和日历。 
  
## <a name="work-with-contacts-and-contact-folders"></a>使用联系人和联系人文件夹

您可以使用[联系人 API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview)来获取、创建、更新和删除用户邮箱中的联系人。 您还可以获取联系人文件夹。 
  
## <a name="next-steps"></a>后续步骤

转到[Microsoft Graph 文档](https://developer.microsoft.com/graph/docs/concepts/overview)页面，以获取有关邮件、日历和联系人 api 的详细信息，包括有关设置环境和开始使用 api 的指南。 

此外，请务必查看[快速入门](https://developer.microsoft.com/graph/quick-start)和[代码示例](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph)，以查看这些 api 的操作。 
  
## <a name="see-also"></a>另请参阅

- [Microsoft Graph 文档](https://developer.microsoft.com/graph/docs/concepts/overview)   
- [REST API 的本地要求](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api)   

