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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753001"
---
# <a name="office-365-rest-apis-for-mail-calendars-and-contacts"></a><span data-ttu-id="5d8cd-103">Office 365 的邮件、 日历和联系人 REST Api</span><span class="sxs-lookup"><span data-stu-id="5d8cd-103">Office 365 REST APIs for mail, calendars, and contacts</span></span>

<span data-ttu-id="5d8cd-104">查找有关 Office 365 Api 的可用来访问邮件、 日历和 Office 365 或 Exchange Online 中的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-104">Find information about the Office 365 APIs that you can use to access mail, calendars, and contacts in Office 365 or Exchange Online.</span></span>
  
<span data-ttu-id="5d8cd-105">Office 365 和 Exchange Online 提供的新方法，以使用电子邮件、 日历和联系人。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-105">Office 365 and Exchange Online provide a new way to work with email, calendars, and contacts.</span></span> <span data-ttu-id="5d8cd-106">邮件、 日历和联系人 REST Api 提供强大的简单易用的方式来访问和操作 Exchange 数据。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-106">The Mail, Calendar, and Contact REST APIs provide a powerful, easy-to-use way to access and manipulate Exchange data.</span></span> <span data-ttu-id="5d8cd-107">这些 Api 基于开放标准： OAuth 2.0 版的身份验证和 OData 版本 4.0 和 JSON 的数据抽象化。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-107">These APIs are based on open standards: OAuth version 2.0 for authentication, and OData version 4.0 and JSON for data abstraction.</span></span> <span data-ttu-id="5d8cd-108">这可以提供以下优点：</span><span class="sxs-lookup"><span data-stu-id="5d8cd-108">This provides the following advantages:</span></span>
  
- <span data-ttu-id="5d8cd-109">这些 Api 需要 OAuth 身份验证，因为您的应用程序没有处理或存储用户凭据。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-109">Because these APIs require OAuth for authentication, your application does not have to handle or store user credentials.</span></span>
    
- <span data-ttu-id="5d8cd-110">OAuth 使可以请求对用户数据紧密范围的权限。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-110">OAuth makes it possible to request tightly scoped permissions to user data.</span></span> <span data-ttu-id="5d8cd-111">例如，您可能设计应用程序请求权限并读取仅用户的日历。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-111">For example, you might design your application to request permission and read only a user's calendar.</span></span>
    
## <a name="work-with-email-and-mail-folders"></a><span data-ttu-id="5d8cd-112">使用电子邮件和邮件文件夹</span><span class="sxs-lookup"><span data-stu-id="5d8cd-112">Work with email and mail folders</span></span>

<span data-ttu-id="5d8cd-113">[邮件 API](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx)可用于获取、 创建、 更新、 删除、 移动、 复制和发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-113">You can use the [Mail API](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx) to get, create, update, delete, move, copy, and send email.</span></span> <span data-ttu-id="5d8cd-114">您可以获取、 创建、 更新和删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-114">You can also get, create, update, and delete mail folders.</span></span> 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a><span data-ttu-id="5d8cd-115">处理事件、 日历和日历组</span><span class="sxs-lookup"><span data-stu-id="5d8cd-115">Work with events, calendars, and calendar groups</span></span>

<span data-ttu-id="5d8cd-116">您可以使用[日历 API](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx)获取、 创建、 更新和删除事件。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-116">You can use the [Calendar API](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx) to get, create, update, and delete events.</span></span> <span data-ttu-id="5d8cd-117">您可以获取、 创建、 更新和删除日历组和日历。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-117">You can also get, create, update, and delete calendar groups and calendars.</span></span> 
  
## <a name="work-with-contacts-and-contact-folders"></a><span data-ttu-id="5d8cd-118">使用联系人和联系人文件夹</span><span class="sxs-lookup"><span data-stu-id="5d8cd-118">Work with contacts and contact folders</span></span>

<span data-ttu-id="5d8cd-119">您可以使用[联系人 API](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx)获取、 创建、 更新和删除用户的邮箱中的联系人。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-119">You can use the [Contacts API](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx) to get, create, update, and delete contacts in a user's mailbox.</span></span> <span data-ttu-id="5d8cd-120">您可以获取联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-120">You can also get contact folders.</span></span> 
  
## <a name="work-with-file-providers"></a><span data-ttu-id="5d8cd-121">使用文件提供程序</span><span class="sxs-lookup"><span data-stu-id="5d8cd-121">Work with file providers</span></span>

<span data-ttu-id="5d8cd-122">您可以使用[文件提供程序 REST API](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx)获取、 创建、 更新和删除有关受支持的文件提供程序，如邮箱、 收存箱，等信息。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-122">You can use the [File Providers REST API](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx) to get, create, update, and delete information about supported file providers, such as mailbox, Dropbox, and so on.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="5d8cd-123">后续步骤</span><span class="sxs-lookup"><span data-stu-id="5d8cd-123">Next steps</span></span>

<span data-ttu-id="5d8cd-124">头转移到[Office 365 平台上的开发](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx)页以获取有关邮件、 日历和联系人 Api，包括有关设置您的环境和 Api 入门指南的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-124">Head over to the [Developing on the Office 365 platform](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx) page to get more information about the Mail, Calendar, and Contacts APIs, including guidance for setting up your environment and getting started with the APIs.</span></span> <span data-ttu-id="5d8cd-125">此外务必签出的[起始项目和代码示例](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx)以查看这些 Api 在操作。</span><span class="sxs-lookup"><span data-stu-id="5d8cd-125">Also be sure to check out the [starter projects and code samples](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx) to see these APIs in action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d8cd-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d8cd-126">See also</span></span>


- [<span data-ttu-id="5d8cd-127">在 Office 365 平台上开发</span><span class="sxs-lookup"><span data-stu-id="5d8cd-127">Developing on the Office 365 platform</span></span>](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx)
    
- [<span data-ttu-id="5d8cd-128">构建一个 Office 365 ASP.NET MVC 应用</span><span class="sxs-lookup"><span data-stu-id="5d8cd-128">Building an Office 365 ASP.NET MVC app</span></span>](http://msdn.microsoft.com/office/office365/howto/Build-your-first-ASPNET-MVC-app%28Office.15%29.aspx)
    
- [<span data-ttu-id="5d8cd-129">邮件 REST 操作</span><span class="sxs-lookup"><span data-stu-id="5d8cd-129">Mail REST operations</span></span>](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx)
    
- [<span data-ttu-id="5d8cd-130">日历 REST 操作</span><span class="sxs-lookup"><span data-stu-id="5d8cd-130">Calendar REST operations</span></span>](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx)
    
- [<span data-ttu-id="5d8cd-131">联系人 REST 操作</span><span class="sxs-lookup"><span data-stu-id="5d8cd-131">Contacts REST operations</span></span>](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx)
    
- [<span data-ttu-id="5d8cd-132">Office 365 API 入门项目和代码示例</span><span class="sxs-lookup"><span data-stu-id="5d8cd-132">Office 365 APIs starter projects and code samples</span></span>](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx)
    

