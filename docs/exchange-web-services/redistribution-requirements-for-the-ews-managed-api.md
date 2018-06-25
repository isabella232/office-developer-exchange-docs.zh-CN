---
title: EWS 托管 API 的重新分发要求
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: 了解如何在应用程序再发行 EWS 托管 API 程序集。
ms.openlocfilehash: d8fc57c4a2b3ed7d6218aeeed0fe88c2d3e0fbe0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753004"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a><span data-ttu-id="e91af-103">EWS 托管 API 的重新分发要求</span><span class="sxs-lookup"><span data-stu-id="e91af-103">Redistribution requirements for the EWS Managed API</span></span>

<span data-ttu-id="e91af-104">了解如何在应用程序再发行 EWS 托管 API 程序集。</span><span class="sxs-lookup"><span data-stu-id="e91af-104">Find out how you can redistribute the EWS Managed API assemblies with your application.</span></span>
  
<span data-ttu-id="e91af-105">在设计 EWS 托管 API 应用程序时，您还需要考虑如何您将其释放到您的用户。</span><span class="sxs-lookup"><span data-stu-id="e91af-105">As you design your EWS Managed API application, you'll also want to consider how you will release it to your users.</span></span> 
  
## <a name="redistributing-your-ews-managed-api-application"></a><span data-ttu-id="e91af-106">重新分发 EWS 托管 API 应用程序</span><span class="sxs-lookup"><span data-stu-id="e91af-106">Redistributing your EWS Managed API application</span></span>

<span data-ttu-id="e91af-107">除非您的应用程序位于 Exchange 服务器上，您将需要重新分发本 EWS 托管 API 的程序集。</span><span class="sxs-lookup"><span data-stu-id="e91af-107">Unless your application is located on the Exchange server, you will need to redistribute the EWS Managed API assemblies.</span></span> <span data-ttu-id="e91af-108">EWS 托管 API 下载包含两个程序集，您可以重新分发本： Microsoft.Exchange.WebServices.dll 和 Microsoft.Exchange.WebServices.Auth.dll。</span><span class="sxs-lookup"><span data-stu-id="e91af-108">The EWS Managed API download contains two assemblies that you can redistribute: Microsoft.Exchange.WebServices.dll and Microsoft.Exchange.WebServices.Auth.dll.</span></span> <span data-ttu-id="e91af-109">如何将发布 EWS 托管 API 应用程序在设计时，请牢记以下信息：</span><span class="sxs-lookup"><span data-stu-id="e91af-109">Keep the following information in mind when you design how you will release your EWS Managed API application:</span></span>
  
- <span data-ttu-id="e91af-110">EWS 托管 API 旨在以便您可以下载它并将其与您的 Exchange 服务器的应用程序。</span><span class="sxs-lookup"><span data-stu-id="e91af-110">The EWS Managed API was designed such that you can download it and distribute it with your application that targets an Exchange server.</span></span> <span data-ttu-id="e91af-111">此外，您的应用程序可以下载 EWS 托管 API。</span><span class="sxs-lookup"><span data-stu-id="e91af-111">Alternatively, your application can download the EWS Managed API.</span></span>
    
- <span data-ttu-id="e91af-112">EWS 托管 API 可用于与运行 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 开头 Exchange Server 2007 的本地版本的 Exchange 服务器进行通信。</span><span class="sxs-lookup"><span data-stu-id="e91af-112">You can use the EWS Managed API to communicate with an Exchange server running Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2007.</span></span>
    
- <span data-ttu-id="e91af-113">EWS 托管 API 开头 2.1 版的版本中，您可以安装在全局程序集缓存 (GAC) 中的 API。</span><span class="sxs-lookup"><span data-stu-id="e91af-113">In versions of the EWS Managed API starting with version 2.1, you can install the API in the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="e91af-114">MSI 将自动添加到 GAC DLL，并将访问每个计算机为基础，而不上每个用户分别。</span><span class="sxs-lookup"><span data-stu-id="e91af-114">The MSI will automatically add the DLL to the GAC and will be accessible on per computer basis, not on a per user basis.</span></span>
    
<span data-ttu-id="e91af-115">许可条款都包含在 EWS 托管 API 下载。</span><span class="sxs-lookup"><span data-stu-id="e91af-115">The license terms are included in the EWS Managed API download.</span></span> <span data-ttu-id="e91af-116">查看有关如何使用 EWS 托管 API 的权威信息条款。</span><span class="sxs-lookup"><span data-stu-id="e91af-116">Review the terms for the authoritative information about what you can do with the EWS Managed API.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e91af-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e91af-117">See also</span></span>


- [<span data-ttu-id="e91af-118">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="e91af-118">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    
- [<span data-ttu-id="e91af-119">EWS 托管 API （下载）</span><span class="sxs-lookup"><span data-stu-id="e91af-119">EWS Managed API (download)</span></span>](http://aka.ms/ews-managed-api-readme)
    

