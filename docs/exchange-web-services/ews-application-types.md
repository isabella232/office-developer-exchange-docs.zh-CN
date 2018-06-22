---
title: EWS 应用程序类型
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ca4e8b90-d0d8-4d55-aa92-19e21659d4f5
description: 了解有关您可以使用 EWS 在 Exchange 中创建的应用程序的最常见类型。
ms.openlocfilehash: 1ce739f453ba1bc6f1b5d38edae3776daa562ffb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752711"
---
# <a name="ews-application-types"></a><span data-ttu-id="58e40-103">EWS 应用程序类型</span><span class="sxs-lookup"><span data-stu-id="58e40-103">EWS application types</span></span>

<span data-ttu-id="58e40-104">了解有关您可以使用 EWS 在 Exchange 中创建的应用程序的最常见类型。</span><span class="sxs-lookup"><span data-stu-id="58e40-104">Find out about the most common types of applications that you can create by using EWS in Exchange.</span></span>
  
<span data-ttu-id="58e40-105">[EWS 和 Exchange 体系结构](ews-applications-and-the-exchange-architecture.md)提供统一的开发模型，可用来创建最常见类型的应用程序中以一致的方式，其中包括：</span><span class="sxs-lookup"><span data-stu-id="58e40-105">The [EWS and Exchange architecture](ews-applications-and-the-exchange-architecture.md) provides a uniform development model that you can use to create the most common types of applications in a consistent way, including the following:</span></span> 
  
- <span data-ttu-id="58e40-106">[客户端应用程序](#bk_clientapps)— 使用 EWS 访问 Exchange 数据的独立应用程序。</span><span class="sxs-lookup"><span data-stu-id="58e40-106">[Client applications](#bk_clientapps) — Standalone applications that use EWS to access Exchange data.</span></span> <span data-ttu-id="58e40-107">Outlook 和 Outlook Web App 是客户端应用程序的示例。</span><span class="sxs-lookup"><span data-stu-id="58e40-107">Outlook and Outlook Web App are examples of client applications.</span></span> 
    
- <span data-ttu-id="58e40-108">[门户应用程序](#bk_portalapps)— 包括的信息来扩展现有 web 页的应用程序检索 exchange，例如忙/闲或联系人信息。</span><span class="sxs-lookup"><span data-stu-id="58e40-108">[Portal applications](#bk_portalapps) — Applications that extend an existing web page by including information retrieved from Exchange, such as free/busy or contact information.</span></span> <span data-ttu-id="58e40-109">检索 Exchange 数据的 SharePoint web 部件是门户应用程序的示例。</span><span class="sxs-lookup"><span data-stu-id="58e40-109">A SharePoint web part that retrieves Exchange data is an example of a portal application.</span></span> 
    
- <span data-ttu-id="58e40-110">[服务应用程序](#bk_serviceapps)— 背景用于集成或同步到现有系统从交换数据的作业。</span><span class="sxs-lookup"><span data-stu-id="58e40-110">[Service applications](#bk_serviceapps) — Background jobs used to integrate or synchronize data from Exchange into an existing system.</span></span> <span data-ttu-id="58e40-111">例如，应用程序同步 Exchange 到 CRM 应用程序的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="58e40-111">For example, an application that synchronizes contact information from Exchange into a CRM application.</span></span> 
    
<span data-ttu-id="58e40-112">这些应用程序模型中的每个可用基本的常见代码来检索信息交换-从，因此不需要更改用于检索客户端、 门户或服务应用程序之间的项信息的 EWS 代码。</span><span class="sxs-lookup"><span data-stu-id="58e40-112">Each of these application models can use a common code base to retrieve information from Exchange - so you don't need to change the EWS code used to retrieve item information between a client, portal, or service application.</span></span> <span data-ttu-id="58e40-113">从到下一个应用程序可能更改的内容是邮箱访问和身份验证机制。</span><span class="sxs-lookup"><span data-stu-id="58e40-113">What might change from one application to the next is the mailbox access and authentication mechanism.</span></span> <span data-ttu-id="58e40-114">例如，客户端应用程序通常使用用户直接访问和基本或 NTLM 身份验证，而服务应用程序可能使用模拟的邮箱访问和 OAuth 身份验证。</span><span class="sxs-lookup"><span data-stu-id="58e40-114">For example, client applications commonly use direct user access and basic or NTLM authentication, whereas a service application likely uses impersonation for mailbox access and OAuth authentication.</span></span>
  
## <a name="client-applications"></a><span data-ttu-id="58e40-115">客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="58e40-115">Client applications</span></span>
<span data-ttu-id="58e40-116"><a name="bk_clientapps"> </a></span><span class="sxs-lookup"><span data-stu-id="58e40-116"></span></span>

<span data-ttu-id="58e40-117">EWS 客户端应用程序是任何独立应用程序使用 EWS 检索从 Exchange 存储的信息。</span><span class="sxs-lookup"><span data-stu-id="58e40-117">An EWS client application is any standalone application that uses EWS to retrieve information from the Exchange store.</span></span> <span data-ttu-id="58e40-118">EWS 客户端应用程序使用直接客户端访问或委派从邮箱存储检索数据的访问权限。</span><span class="sxs-lookup"><span data-stu-id="58e40-118">EWS client applications use direct client access or delegate access to retrieve data from the mailbox store.</span></span> <span data-ttu-id="58e40-119">以下是使用 EWS 的客户端应用程序的一些示例：</span><span class="sxs-lookup"><span data-stu-id="58e40-119">The following are some examples of client applications that use EWS:</span></span>
  
- <span data-ttu-id="58e40-120">Outlook 的邮件提示、 可用性和用户 OOF 状态等功能</span><span class="sxs-lookup"><span data-stu-id="58e40-120">Outlook, in features such as MailTips, availability, and user OOF status</span></span>
    
- <span data-ttu-id="58e40-121">适用于设备的 OWA</span><span class="sxs-lookup"><span data-stu-id="58e40-121">OWA for Devices</span></span>
    
- <span data-ttu-id="58e40-122">Outlook for Mac 2011</span><span class="sxs-lookup"><span data-stu-id="58e40-122">Outlook for Mac 2011</span></span>
    
- <span data-ttu-id="58e40-123">Lync 的可用性信息</span><span class="sxs-lookup"><span data-stu-id="58e40-123">Lync, for availability information</span></span>
    
<span data-ttu-id="58e40-124">客户端应用程序通常使用直接访问和基本或 NTLM 身份验证，以便用户仅限于访问自己的登录凭据自己邮箱中的信息。</span><span class="sxs-lookup"><span data-stu-id="58e40-124">Client applications commonly use direct access and basic or NTLM authentication, so that users are limited to accessing information in their own mailbox with their own logon credentials.</span></span> <span data-ttu-id="58e40-125">此外应支持客户端应用程序代理的有权访问其他用户的邮箱的权限的用户的访问。</span><span class="sxs-lookup"><span data-stu-id="58e40-125">Client applications should also support delegate access for users who have been given permission to access another user's mailbox.</span></span>
  
## <a name="portal-applications"></a><span data-ttu-id="58e40-126">门户应用程序</span><span class="sxs-lookup"><span data-stu-id="58e40-126">Portal applications</span></span>
<span data-ttu-id="58e40-127"><a name="bk_portalapps"> </a></span><span class="sxs-lookup"><span data-stu-id="58e40-127"></span></span>

<span data-ttu-id="58e40-128">门户应用程序扩展现有 web 页或门户以包括页上的个性化组件的 Exchange 邮箱信息。</span><span class="sxs-lookup"><span data-stu-id="58e40-128">A portal application extends an existing web page or portal to include Exchange mailbox information as a personalized component of the page.</span></span> <span data-ttu-id="58e40-129">SharePoint web 部件的最常见的门户应用程序和向用户提供个性化体验通过提供到 Exchange 邮箱数据，例如未读的邮件、 最新邮件和日历事件，用于在其常查看的视图SharePoint 门户页面。</span><span class="sxs-lookup"><span data-stu-id="58e40-129">SharePoint web parts are the most common portal applications and provide users with a personalized experience by providing views into Exchange mailbox data, such as unread messages, most recent messages, and calendar events, alongside their commonly viewed SharePoint portal page.</span></span> <span data-ttu-id="58e40-130">EWS 门户应用程序可以使用直接客户端访问、 代理访问或模拟从邮箱存储检索数据。</span><span class="sxs-lookup"><span data-stu-id="58e40-130">EWS portal applications can use direct client access, delegate access, or impersonation to retrieve data from the mailbox store.</span></span> <span data-ttu-id="58e40-131">Exchange 2013 和 SharePoint 2013 支持的服务器到服务器身份验证的 OAuth 授权协议，因为 OAuth 提供的最无缝且安全的身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="58e40-131">Because Exchange 2013 and SharePoint 2013 both support the OAuth authorization protocol for server-to-server authentication, OAuth provides the most seamless and secure authentication method.</span></span>
  
## <a name="service-applications"></a><span data-ttu-id="58e40-132">服务应用程序</span><span class="sxs-lookup"><span data-stu-id="58e40-132">Service applications</span></span>
<span data-ttu-id="58e40-133"><a name="bk_serviceapps"> </a></span><span class="sxs-lookup"><span data-stu-id="58e40-133"></span></span>

<span data-ttu-id="58e40-134">服务应用程序通常是内置的现有应用程序扩展到要关联之间系统和 Exchange 存储的数据交换后台作业。</span><span class="sxs-lookup"><span data-stu-id="58e40-134">A service application is usually a background job built into an existing application that extends to Exchange to correlate data between the system and the Exchange store.</span></span> <span data-ttu-id="58e40-135">服务应用程序通常不具有用户界面和使用模拟或 OAuth 身份验证和访问。</span><span class="sxs-lookup"><span data-stu-id="58e40-135">Service applications typically do not have a user interface and use impersonation or OAuth for authentication and access.</span></span> <span data-ttu-id="58e40-136">创建模拟用户的服务帐户是 EWS 服务应用程序中常见，因为这样可以授予一个单个帐户的权限模拟用户组，并执行这些帐户的邮箱操作。</span><span class="sxs-lookup"><span data-stu-id="58e40-136">Creating a service account to impersonate users is common in EWS service apps because you can grant a single account permission to impersonate a set of users and perform mailbox operations for those accounts.</span></span> <span data-ttu-id="58e40-137">例如，EWS 服务应用程序可同步之间使用的服务帐户和模拟营销中 CRM 解决方案和 Exchange 通讯组列表的数据。</span><span class="sxs-lookup"><span data-stu-id="58e40-137">For example, an EWS service application can synchronize data between marketing lists in a CRM solution and Exchange distribution groups by using a service account and impersonation.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58e40-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="58e40-138">See also</span></span>


- [<span data-ttu-id="58e40-139">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="58e40-139">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="58e40-140">EWS 应用程序和 Exchange 体系结构</span><span class="sxs-lookup"><span data-stu-id="58e40-140">EWS applications and the Exchange architecture</span></span>](ews-applications-and-the-exchange-architecture.md)
    
- [<span data-ttu-id="58e40-141">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="58e40-141">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

