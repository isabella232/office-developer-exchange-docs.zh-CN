---
title: EWS 托管 API 的再分发要求
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: 了解如何使用应用程序重新分发 EWS 托管 API 程序集。
ms.openlocfilehash: e64b4cdb8938caa819ba30621112a25946ef0424
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463823"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a><span data-ttu-id="099fc-103">EWS 托管 API 的再分发要求</span><span class="sxs-lookup"><span data-stu-id="099fc-103">Redistribution requirements for the EWS Managed API</span></span>

<span data-ttu-id="099fc-104">了解如何使用应用程序重新分发 EWS 托管 API 程序集。</span><span class="sxs-lookup"><span data-stu-id="099fc-104">Find out how you can redistribute the EWS Managed API assemblies with your application.</span></span>
  
<span data-ttu-id="099fc-105">在设计 EWS 托管 API 应用程序时，您还需要考虑将其发布给用户的方式。</span><span class="sxs-lookup"><span data-stu-id="099fc-105">As you design your EWS Managed API application, you'll also want to consider how you will release it to your users.</span></span> 
  
## <a name="redistributing-your-ews-managed-api-application"></a><span data-ttu-id="099fc-106">重新分发您的 EWS 托管 API 应用程序</span><span class="sxs-lookup"><span data-stu-id="099fc-106">Redistributing your EWS Managed API application</span></span>

<span data-ttu-id="099fc-107">除非您的应用程序位于 Exchange 服务器上，否则您将需要重新发布 EWS 托管 API 程序集。</span><span class="sxs-lookup"><span data-stu-id="099fc-107">Unless your application is located on the Exchange server, you will need to redistribute the EWS Managed API assemblies.</span></span> <span data-ttu-id="099fc-108">EWS 托管 API 下载包含两个可以重新发布的程序集： WebServices 和 WebServices。. "。</span><span class="sxs-lookup"><span data-stu-id="099fc-108">The EWS Managed API download contains two assemblies that you can redistribute: Microsoft.Exchange.WebServices.dll and Microsoft.Exchange.WebServices.Auth.dll.</span></span> <span data-ttu-id="099fc-109">在设计如何释放 EWS 托管 API 应用程序时，请记住以下信息：</span><span class="sxs-lookup"><span data-stu-id="099fc-109">Keep the following information in mind when you design how you will release your EWS Managed API application:</span></span>
  
- <span data-ttu-id="099fc-110">EWS 托管 API 的设计使您可以下载它，并将其与面向 Exchange server 的应用程序一起分发。</span><span class="sxs-lookup"><span data-stu-id="099fc-110">The EWS Managed API was designed such that you can download it and distribute it with your application that targets an Exchange server.</span></span> <span data-ttu-id="099fc-111">或者，您的应用程序可以下载 EWS 托管 API。</span><span class="sxs-lookup"><span data-stu-id="099fc-111">Alternatively, your application can download the EWS Managed API.</span></span>
    
- <span data-ttu-id="099fc-112">您可以使用 EWS 托管 API 与运行 Exchange Online 的 Exchange 服务器、作为 Office 365 的一部分的 Exchange Online 或从 Exchange Server 2007 开始的 Exchange 内部部署版本进行通信。</span><span class="sxs-lookup"><span data-stu-id="099fc-112">You can use the EWS Managed API to communicate with an Exchange server running Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2007.</span></span>
    
- <span data-ttu-id="099fc-113">在从版本2.1 开始的 EWS 托管 API 的各个版本中，您可以在全局程序集缓存（GAC）中安装 API。</span><span class="sxs-lookup"><span data-stu-id="099fc-113">In versions of the EWS Managed API starting with version 2.1, you can install the API in the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="099fc-114">MSI 将自动将 DLL 添加到 GAC 中，并且可以在每台计算机上访问，而不是每个用户都可以访问。</span><span class="sxs-lookup"><span data-stu-id="099fc-114">The MSI will automatically add the DLL to the GAC and will be accessible on per computer basis, not on a per user basis.</span></span>
    
<span data-ttu-id="099fc-115">该许可条款包含在 EWS 托管 API 下载中。</span><span class="sxs-lookup"><span data-stu-id="099fc-115">The license terms are included in the EWS Managed API download.</span></span> <span data-ttu-id="099fc-116">查看有关可以使用 EWS 托管 API 执行的操作的权威信息的术语。</span><span class="sxs-lookup"><span data-stu-id="099fc-116">Review the terms for the authoritative information about what you can do with the EWS Managed API.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="099fc-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="099fc-117">See also</span></span>


- [<span data-ttu-id="099fc-118">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="099fc-118">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    
- [<span data-ttu-id="099fc-119">EWS 托管 API （下载）</span><span class="sxs-lookup"><span data-stu-id="099fc-119">EWS Managed API (download)</span></span>](https://aka.ms/ews-managed-api-readme)
    

