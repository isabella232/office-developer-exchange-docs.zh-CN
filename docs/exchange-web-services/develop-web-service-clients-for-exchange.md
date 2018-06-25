---
title: 开发 Exchange Web 服务客户端
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 899ba15b-336d-4f9b-8563-318c61e43713
description: 寻找信息以帮助您开发适用于 Exchange 的 EWS 和 Web 服务客户端应用程序。
ms.openlocfilehash: 2b8b032124e45dda7c83932d519ffb87bcdb5514
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752701"
---
# <a name="develop-web-service-clients-for-exchange"></a><span data-ttu-id="c1094-103">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="c1094-103">Develop web service clients for Exchange</span></span>

<span data-ttu-id="c1094-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 寻找信息以帮助您开发适用于 Exchange 的 EWS 和 Web 服务客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="c1094-104">Find information to help you develop EWS and web service client applications for Exchange.</span></span>
  
<span data-ttu-id="c1094-105">本节中的文章介绍如何将 Exchange 客户端应用程序中的 EWS 和 Web 服务用于 Exchange Online、作为 Office 365 一部分的 Exchange Online，以及从 Exchange 2013 开始的本地 Exchange 版本，并提供向您展示如何执行特定任务的示例。</span><span class="sxs-lookup"><span data-stu-id="c1094-105">The articles in this section explain how to use EWS and web services in your Exchange client applications for Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange 2013, and provide examples that show you how to perform specific tasks.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="c1094-106">本节中</span><span class="sxs-lookup"><span data-stu-id="c1094-106">In this section</span></span>

- [<span data-ttu-id="c1094-107">在 Exchange 中 EWS 存档</span><span class="sxs-lookup"><span data-stu-id="c1094-107">Archiving in EWS in Exchange</span></span>](archiving-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-108">附件和 EWS Exchange 中</span><span class="sxs-lookup"><span data-stu-id="c1094-108">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-109">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1094-109">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-110">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c1094-110">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-111">通讯组和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c1094-111">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-112">在交换中 EWS eDiscovery</span><span class="sxs-lookup"><span data-stu-id="c1094-112">eDiscovery in EWS in Exchange</span></span>](ediscovery-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-113">电子邮件和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c1094-113">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-114">文件夹和交换中的 EWS 中的项目</span><span class="sxs-lookup"><span data-stu-id="c1094-114">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-115">Exchange 中的标识符</span><span class="sxs-lookup"><span data-stu-id="c1094-115">Identifiers in Exchange</span></span>](ews-identifiers-in-exchange.md)
    
- [<span data-ttu-id="c1094-116">Impersonation and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1094-116">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-117">Inbox management and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1094-117">Inbox management and EWS in Exchange</span></span>](inbox-management-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-118">Notification subscriptions, mailbox events, and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1094-118">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-119">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="c1094-119">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-120">在交换 EWS 持久应用程序设置</span><span class="sxs-lookup"><span data-stu-id="c1094-120">Persistent application settings in EWS in Exchange</span></span>](persistent-application-settings-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-121">属性和交换中的 EWS 中的扩展的属性</span><span class="sxs-lookup"><span data-stu-id="c1094-121">Properties and extended properties in EWS in Exchange</span></span>](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-122">属性集和响应形状在 EWS 在 Exchange</span><span class="sxs-lookup"><span data-stu-id="c1094-122">Property sets and response shapes in EWS in Exchange</span></span>](property-sets-and-response-shapes-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-123">使用 EWS 在 Exchange 公用文件夹访问。</span><span class="sxs-lookup"><span data-stu-id="c1094-123">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-124">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c1094-124">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-125">邮箱同步和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c1094-125">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-126">时区和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c1094-126">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c1094-127">工具和资源来解决 exchange 的 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="c1094-127">Tools and resources for troubleshooting EWS applications for Exchange</span></span>](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    
- [<span data-ttu-id="c1094-128">验证 EWS 或 EWS 托管 API 调用的结果</span><span class="sxs-lookup"><span data-stu-id="c1094-128">Verifying the results of an EWS or EWS Managed API call</span></span>](verifying-the-results-of-an-ews-or-ews-managed-api-call.md)
    
## <a name="see-also"></a><span data-ttu-id="c1094-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c1094-129">See also</span></span>

- [<span data-ttu-id="c1094-130">在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务</span><span class="sxs-lookup"><span data-stu-id="c1094-130">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)     
- [<span data-ttu-id="c1094-131">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1094-131">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)  
- [<span data-ttu-id="c1094-132">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="c1094-132">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)  
- [<span data-ttu-id="c1094-133">Exchange web 服务引用</span><span class="sxs-lookup"><span data-stu-id="c1094-133">Web services reference for Exchange</span></span>](../web-service-reference/web-services-reference-for-exchange.md)
    

