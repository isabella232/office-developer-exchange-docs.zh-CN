---
title: Exchange 的统一消息 web 服务参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Unified
api_type:
- schema
ms.assetid: 83afea8a-c716-41df-9eb2-e1000357afb6
description: 在 Exchange 中查找统一消息（UM） web 服务的引用内容。
ms.openlocfilehash: e4bb63f34650dae8fc28016196c97a6b79e69df0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467373"
---
# <a name="unified-messaging-web-service-reference-for-exchange"></a><span data-ttu-id="a386e-103">Exchange 的统一消息 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="a386e-103">Unified Messaging web service reference for Exchange</span></span>

<span data-ttu-id="a386e-104">在 Exchange 中查找统一消息（UM） web 服务的引用内容。</span><span class="sxs-lookup"><span data-stu-id="a386e-104">Find reference content for the Unified Messaging (UM) web service in Exchange.</span></span>
  
<span data-ttu-id="a386e-105">统一消息（UM） web 服务提供了一个扩展性点，使客户端能够读取和更改有关 UM 属性的信息，并请求对邮箱存储项进行分析并通过电话设备决定。</span><span class="sxs-lookup"><span data-stu-id="a386e-105">The Unified Messaging (UM) web service provides an extensibility point that enables clients to read and change information about UM properties and request that mailbox store items be parsed and dictated over a telephony device.</span></span> <span data-ttu-id="a386e-106">本节包含有关组成 UM web 服务的 XML 消息的操作和元素的信息。</span><span class="sxs-lookup"><span data-stu-id="a386e-106">This section contains information about the operations and elements that make up the XML messages for the UM web service.</span></span> <span data-ttu-id="a386e-107">此内容适用于类似于 https:// \<yourclientaccessserver\> /EWS/UM2007Legacy 的服务终结点 URL。</span><span class="sxs-lookup"><span data-stu-id="a386e-107">This content applies to the service endpoint URL that is similar to https://\<yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span></span> 
  
<span data-ttu-id="a386e-108">您可以使用自动发现服务获取指向 UM web 服务终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="a386e-108">You can use the Autodiscover service to get the URL to the UM web service endpoint.</span></span> <span data-ttu-id="a386e-109">有关自动发现的详细信息，请参阅[Exchange 的自动发现](../exchange-web-services/autodiscover-for-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="a386e-109">For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="a386e-110">对于从 Exchange 2010 开始的 Exchange 版本，我们建议使用[Exchange Web 服务（EWS）](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx)而不是 UM Web 服务中提供的统一消息操作，原因如下：</span><span class="sxs-lookup"><span data-stu-id="a386e-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the UM web service, for the following reasons:</span></span> 
> - <span data-ttu-id="a386e-111">基于 EWS 的 UM 功能在 EWS 托管 API 中具有一流支持。</span><span class="sxs-lookup"><span data-stu-id="a386e-111">The EWS-based UM features have first-class support in the EWS Managed API.</span></span> 
> - <span data-ttu-id="a386e-112">在从 Exchange 2010 开始的 Exchange 版本中，新的 UM 功能将添加到 EWS，但不添加到统一消息 web 服务中。</span><span class="sxs-lookup"><span data-stu-id="a386e-112">In versions of Exchange starting with Exchange 2010, new UM features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
<span data-ttu-id="a386e-113">UM web 服务没有显式架构。</span><span class="sxs-lookup"><span data-stu-id="a386e-113">The UM web service does not have an explicit schema.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="a386e-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="a386e-114">In this section</span></span>
<span data-ttu-id="a386e-115"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="a386e-115"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="a386e-116">Exchange 的统一消息 web 服务操作</span><span class="sxs-lookup"><span data-stu-id="a386e-116">Unified Messaging web service operations for Exchange</span></span>](unified-messaging-web-service-operations-for-exchange.md)   
- [<span data-ttu-id="a386e-117">Exchange 的统一消息 web 服务 XML 元素</span><span class="sxs-lookup"><span data-stu-id="a386e-117">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="a386e-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a386e-118">See also</span></span>

- [<span data-ttu-id="a386e-119">Exchange 的自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="a386e-119">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="a386e-120">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="a386e-120">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="a386e-121">开始使用 Exchange 中的 Web 服务</span><span class="sxs-lookup"><span data-stu-id="a386e-121">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

