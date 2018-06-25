---
title: Office 365 的邮件、 日历和联系人 REST Api
manager: sethgros
ms.date: 4/29/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: 查找有关 Office 365 Api 的可用来访问邮件、 日历和 Office 365 或 Exchange Online 中的联系人信息。
ms.openlocfilehash: d42d3ff0b68dfbf23d5a4eebb826a6d39a4ac116
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753001"
---
# <a name="office-365-rest-apis-for-mail-calendars-and-contacts"></a>Office 365 的邮件、 日历和联系人 REST Api

查找有关 Office 365 Api 的可用来访问邮件、 日历和 Office 365 或 Exchange Online 中的联系人信息。
  
Office 365 和 Exchange Online 提供的新方法，以使用电子邮件、 日历和联系人。 邮件、 日历和联系人 REST Api 提供强大的简单易用的方式来访问和操作 Exchange 数据。 这些 Api 基于开放标准： OAuth 2.0 版的身份验证和 OData 版本 4.0 和 JSON 的数据抽象化。 这可以提供以下优点：
  
- 这些 Api 需要 OAuth 身份验证，因为您的应用程序没有处理或存储用户凭据。
    
- OAuth 使可以请求对用户数据紧密范围的权限。 例如，您可能设计应用程序请求权限并读取仅用户的日历。
    
## <a name="work-with-email-and-mail-folders"></a>使用电子邮件和邮件文件夹

[邮件 API](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx)可用于获取、 创建、 更新、 删除、 移动、 复制和发送电子邮件。 您可以获取、 创建、 更新和删除邮件文件夹。 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a>处理事件、 日历和日历组

您可以使用[日历 API](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx)获取、 创建、 更新和删除事件。 您可以获取、 创建、 更新和删除日历组和日历。 
  
## <a name="work-with-contacts-and-contact-folders"></a>使用联系人和联系人文件夹

您可以使用[联系人 API](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx)获取、 创建、 更新和删除用户的邮箱中的联系人。 您可以获取联系人文件夹。 
  
## <a name="work-with-file-providers"></a>使用文件提供程序

您可以使用[文件提供程序 REST API](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx)获取、 创建、 更新和删除有关受支持的文件提供程序，如邮箱、 收存箱，等信息。 
  
## <a name="next-steps"></a>后续步骤

头转移到[Office 365 平台上的开发](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx)页以获取有关邮件、 日历和联系人 Api，包括有关设置您的环境和 Api 入门指南的详细信息。 此外务必签出的[起始项目和代码示例](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx)以查看这些 Api 在操作。 
  
## <a name="see-also"></a>另请参阅


- [在 Office 365 平台上开发](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx)
    
- [构建一个 Office 365 ASP.NET MVC 应用](http://msdn.microsoft.com/office/office365/howto/Build-your-first-ASPNET-MVC-app%28Office.15%29.aspx)
    
- [邮件 REST 操作](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx)
    
- [日历 REST 操作](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx)
    
- [联系人 REST 操作](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx)
    
- [Office 365 API 入门项目和代码示例](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx)
    

