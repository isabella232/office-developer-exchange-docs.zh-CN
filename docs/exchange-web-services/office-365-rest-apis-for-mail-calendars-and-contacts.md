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
# <a name="microsoft-graph-rest-apis-for-mail-calendars-and-contacts"></a><span data-ttu-id="d30b6-103">针对邮件、日历和联系人的 Microsoft Graph REST API</span><span class="sxs-lookup"><span data-stu-id="d30b6-103">Microsoft Graph REST APIs for mail, calendars, and contacts</span></span>

<span data-ttu-id="d30b6-104">查找有关可用于在混合部署中访问 Office 365、Exchange Online 或 Exchange Server 中的邮件、日历和联系人的 Microsoft Graph Api 的信息。</span><span class="sxs-lookup"><span data-stu-id="d30b6-104">Find information about the Microsoft Graph APIs that you can use to access mail, calendars, and contacts in Office 365, Exchange Online, or Exchange Server in hybrid deployments.</span></span>

<span data-ttu-id="d30b6-105">在混合部署中，Office 365、Exchange Online 和 Exchange Server 提供了一种使用电子邮件、日历和联系人的新方法。</span><span class="sxs-lookup"><span data-stu-id="d30b6-105">Office 365, Exchange Online, and Exchange Server in hybrid deployments provide a new way to work with email, calendars, and contacts.</span></span> <span data-ttu-id="d30b6-106">Microsoft Graph 邮件、日历和联系人 REST Api 提供了一种强大且易于使用的方法来访问和操作 Exchange 数据。</span><span class="sxs-lookup"><span data-stu-id="d30b6-106">The Microsoft Graph Mail, Calendar, and Contact REST APIs provide a powerful, easy-to-use way to access and manipulate Exchange data.</span></span> <span data-ttu-id="d30b6-107">这些 Api 基于开放标准：用于身份验证的 OAuth 版本2.0，以及用于数据抽象的 OData 版本4.0 和 JSON。</span><span class="sxs-lookup"><span data-stu-id="d30b6-107">These APIs are based on open standards: OAuth version 2.0 for authentication, and OData version 4.0 and JSON for data abstraction.</span></span> <span data-ttu-id="d30b6-108">这具有以下优点：</span><span class="sxs-lookup"><span data-stu-id="d30b6-108">This provides the following advantages:</span></span>

- <span data-ttu-id="d30b6-109">由于这些 Api 需要 OAuth 进行身份验证，因此应用程序不需要处理或存储用户凭据。</span><span class="sxs-lookup"><span data-stu-id="d30b6-109">Because these APIs require OAuth for authentication, your application does not have to handle or store user credentials.</span></span>

- <span data-ttu-id="d30b6-110">通过 OAuth，可以向用户数据请求严格范围的权限。</span><span class="sxs-lookup"><span data-stu-id="d30b6-110">OAuth makes it possible to request tightly scoped permissions to user data.</span></span> <span data-ttu-id="d30b6-111">例如，您可以将应用程序设计为请求权限并只读取用户的日历。</span><span class="sxs-lookup"><span data-stu-id="d30b6-111">For example, you might design your application to request permission and read only a user's calendar.</span></span>

## <a name="work-with-email-and-mail-folders"></a><span data-ttu-id="d30b6-112">使用电子邮件和邮件文件夹</span><span class="sxs-lookup"><span data-stu-id="d30b6-112">Work with email and mail folders</span></span>

<span data-ttu-id="d30b6-113">您可以使用[邮件 API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview)来获取、创建、更新、删除、移动、复制和发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="d30b6-113">You can use the [Mail API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview) to get, create, update, delete, move, copy, and send email.</span></span> <span data-ttu-id="d30b6-114">您还可以获取、创建、更新和删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="d30b6-114">You can also get, create, update, and delete mail folders.</span></span> 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a><span data-ttu-id="d30b6-115">使用事件、日历和日历组</span><span class="sxs-lookup"><span data-stu-id="d30b6-115">Work with events, calendars, and calendar groups</span></span>

<span data-ttu-id="d30b6-116">您可以使用[日历 API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview)来获取、创建、更新和删除事件。</span><span class="sxs-lookup"><span data-stu-id="d30b6-116">You can use the [Calendar API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview) to get, create, update, and delete events.</span></span> <span data-ttu-id="d30b6-117">您还可以获取、创建、更新和删除日历组和日历。</span><span class="sxs-lookup"><span data-stu-id="d30b6-117">You can also get, create, update, and delete calendar groups and calendars.</span></span> 
  
## <a name="work-with-contacts-and-contact-folders"></a><span data-ttu-id="d30b6-118">使用联系人和联系人文件夹</span><span class="sxs-lookup"><span data-stu-id="d30b6-118">Work with contacts and contact folders</span></span>

<span data-ttu-id="d30b6-119">您可以使用[联系人 API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview)来获取、创建、更新和删除用户邮箱中的联系人。</span><span class="sxs-lookup"><span data-stu-id="d30b6-119">You can use the [Contacts API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview) to get, create, update, and delete contacts in a user's mailbox.</span></span> <span data-ttu-id="d30b6-120">您还可以获取联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="d30b6-120">You can also get contact folders.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="d30b6-121">后续步骤</span><span class="sxs-lookup"><span data-stu-id="d30b6-121">Next steps</span></span>

<span data-ttu-id="d30b6-122">转到[Microsoft Graph 文档](https://developer.microsoft.com/graph/docs/concepts/overview)页面，以获取有关邮件、日历和联系人 api 的详细信息，包括有关设置环境和开始使用 api 的指南。</span><span class="sxs-lookup"><span data-stu-id="d30b6-122">Head over to the [Microsoft Graph documentation](https://developer.microsoft.com/graph/docs/concepts/overview) page to get more information about the Mail, Calendar, and Contacts APIs, including guidance for setting up your environment and getting started with the APIs.</span></span> 

<span data-ttu-id="d30b6-123">此外，请务必查看[快速入门](https://developer.microsoft.com/graph/quick-start)和[代码示例](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph)，以查看这些 api 的操作。</span><span class="sxs-lookup"><span data-stu-id="d30b6-123">Also be sure to check out the [quick starts](https://developer.microsoft.com/graph/quick-start) and [code samples](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph) to see these APIs in action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d30b6-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d30b6-124">See also</span></span>

- [<span data-ttu-id="d30b6-125">Microsoft Graph 文档</span><span class="sxs-lookup"><span data-stu-id="d30b6-125">Microsoft Graph documentation</span></span>](https://developer.microsoft.com/graph/docs/concepts/overview)   
- [<span data-ttu-id="d30b6-126">REST API 的本地要求</span><span class="sxs-lookup"><span data-stu-id="d30b6-126">On-premises requirements for the REST API</span></span>](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api)   

