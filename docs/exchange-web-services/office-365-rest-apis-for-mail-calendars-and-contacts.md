---
title: Microsoft Graph Outlook API 的邮件、 日历和联系人
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: 查找有关 Microsoft Graph API 可用于访问邮件、 日历和 Office 365 或 Exchange Online 中的联系人的信息。
ms.openlocfilehash: 3065de389157345afd5ed07e302ace99e2048bdf
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353292"
---
# <a name="microsoft-graph-rest-apis-for-mail-calendars-and-contacts"></a><span data-ttu-id="00942-103">Microsoft Graph REST Api 的邮件、 日历和联系人</span><span class="sxs-lookup"><span data-stu-id="00942-103">Microsoft Graph REST APIs for mail, calendars, and contacts</span></span>

<span data-ttu-id="00942-104">查找有关 Microsoft Graph Api 可用于访问邮件、 日历和 Office 365 或 Exchange Online 中的联系人的信息。</span><span class="sxs-lookup"><span data-stu-id="00942-104">Find information about the Microsoft Graph APIs that you can use to access mail, calendars, and contacts in Office 365 or Exchange Online.</span></span>

<span data-ttu-id="00942-105">Office 365 和 Exchange Online 提供的新方法，以使用电子邮件、 日历和联系人。</span><span class="sxs-lookup"><span data-stu-id="00942-105">Office 365 and Exchange Online provide a new way to work with email, calendars, and contacts.</span></span> <span data-ttu-id="00942-106">Microsoft Graph 邮件、 日历和联系人 REST Api 提供强大的简单易用的方式来访问和操作 Exchange 数据。</span><span class="sxs-lookup"><span data-stu-id="00942-106">The Microsoft Graph Mail, Calendar, and Contact REST APIs provide a powerful, easy-to-use way to access and manipulate Exchange data.</span></span> <span data-ttu-id="00942-107">这些 Api 基于开放标准： OAuth 2.0 版的身份验证和 OData 版本 4.0 和 JSON 的数据抽象化。</span><span class="sxs-lookup"><span data-stu-id="00942-107">These APIs are based on open standards: OAuth version 2.0 for authentication, and OData version 4.0 and JSON for data abstraction.</span></span> <span data-ttu-id="00942-108">这可以提供以下优点：</span><span class="sxs-lookup"><span data-stu-id="00942-108">This provides the following advantages:</span></span>

- <span data-ttu-id="00942-109">这些 Api 需要 OAuth 身份验证，因为您的应用程序没有处理或存储用户凭据。</span><span class="sxs-lookup"><span data-stu-id="00942-109">Because these APIs require OAuth for authentication, your application does not have to handle or store user credentials.</span></span>

- <span data-ttu-id="00942-110">OAuth 使可以请求对用户数据紧密范围的权限。</span><span class="sxs-lookup"><span data-stu-id="00942-110">OAuth makes it possible to request tightly scoped permissions to user data.</span></span> <span data-ttu-id="00942-111">例如，您可能设计应用程序请求权限并读取仅用户的日历。</span><span class="sxs-lookup"><span data-stu-id="00942-111">For example, you might design your application to request permission and read only a user's calendar.</span></span>

## <a name="work-with-email-and-mail-folders"></a><span data-ttu-id="00942-112">使用电子邮件和邮件文件夹</span><span class="sxs-lookup"><span data-stu-id="00942-112">Work with email and mail folders</span></span>

<span data-ttu-id="00942-113">[邮件 API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview)可用于获取、 创建、 更新、 删除、 移动、 复制和发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="00942-113">You can use the [Mail API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview) to get, create, update, delete, move, copy, and send email.</span></span> <span data-ttu-id="00942-114">您可以获取、 创建、 更新和删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="00942-114">You can also get, create, update, and delete mail folders.</span></span> 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a><span data-ttu-id="00942-115">处理事件、 日历和日历组</span><span class="sxs-lookup"><span data-stu-id="00942-115">Work with events, calendars, and calendar groups</span></span>

<span data-ttu-id="00942-116">您可以使用[日历 API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview)获取、 创建、 更新和删除事件。</span><span class="sxs-lookup"><span data-stu-id="00942-116">You can use the [Calendar API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview) to get, create, update, and delete events.</span></span> <span data-ttu-id="00942-117">您可以获取、 创建、 更新和删除日历组和日历。</span><span class="sxs-lookup"><span data-stu-id="00942-117">You can also get, create, update, and delete calendar groups and calendars.</span></span> 
  
## <a name="work-with-contacts-and-contact-folders"></a><span data-ttu-id="00942-118">使用联系人和联系人文件夹</span><span class="sxs-lookup"><span data-stu-id="00942-118">Work with contacts and contact folders</span></span>

<span data-ttu-id="00942-119">您可以使用[联系人 API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview)获取、 创建、 更新和删除用户的邮箱中的联系人。</span><span class="sxs-lookup"><span data-stu-id="00942-119">You can use the [Contacts API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview) to get, create, update, and delete contacts in a user's mailbox.</span></span> <span data-ttu-id="00942-120">您可以获取联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="00942-120">You can also get contact folders.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="00942-121">后续步骤</span><span class="sxs-lookup"><span data-stu-id="00942-121">Next steps</span></span>

<span data-ttu-id="00942-122">通过头到[Microsoft Graph 文档](https://developer.microsoft.com/graph/docs/concepts/overview)页以获取有关邮件、 日历和联系人 Api，包括有关设置您的环境和 Api 入门指南的详细信息。</span><span class="sxs-lookup"><span data-stu-id="00942-122">Head over to the [Microsoft Graph documentation](https://developer.microsoft.com/graph/docs/concepts/overview) page to get more information about the Mail, Calendar, and Contacts APIs, including guidance for setting up your environment and getting started with the APIs.</span></span> 

<span data-ttu-id="00942-123">此外务必签出的[快速启动](https://developer.microsoft.com/graph/quick-start)和[代码示例](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph)以查看这些 Api 在操作。</span><span class="sxs-lookup"><span data-stu-id="00942-123">Also be sure to check out the [quick starts](https://developer.microsoft.com/graph/quick-start) and [code samples](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph) to see these APIs in action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00942-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="00942-124">See also</span></span>

- [<span data-ttu-id="00942-125">Microsoft Graph 文档</span><span class="sxs-lookup"><span data-stu-id="00942-125">Microsoft Graph documentation</span></span>](https://developer.microsoft.com/graph/docs/concepts/overview)   

