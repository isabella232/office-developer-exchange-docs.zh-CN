---
title: Exchange 统一的消息 web 服务引用
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
description: 在 Exchange 统一消息 (UM) web 服务中查找参考内容。
ms.openlocfilehash: 12ee91c5a8b7e1ba23b937f142a9ae2835697fef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838316"
---
# <a name="unified-messaging-web-service-reference-for-exchange"></a><span data-ttu-id="7f466-103">Exchange 统一的消息 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="7f466-103">Unified Messaging web service reference for Exchange</span></span>

<span data-ttu-id="7f466-104">在 Exchange 统一消息 (UM) web 服务中查找参考内容。</span><span class="sxs-lookup"><span data-stu-id="7f466-104">Find reference content for the Unified Messaging (UM) web service in Exchange.</span></span>
  
<span data-ttu-id="7f466-105">统一消息 (UM) web 服务提供一个扩展点，使客户端来读取和更改 UM 属性的信息以及请求邮箱存储项目进行分析和电话设备上指明。</span><span class="sxs-lookup"><span data-stu-id="7f466-105">The Unified Messaging (UM) web service provides an extensibility point that enables clients to read and change information about UM properties and request that mailbox store items be parsed and dictated over a telephony device.</span></span> <span data-ttu-id="7f466-106">本节包含有关操作和 UM web 服务的 XML 消息构成元素的信息。</span><span class="sxs-lookup"><span data-stu-id="7f466-106">This section contains information about the operations and elements that make up the XML messages for the UM web service.</span></span> <span data-ttu-id="7f466-107">此内容适用于的服务终结点 URL 类似于 https://\<yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx。</span><span class="sxs-lookup"><span data-stu-id="7f466-107">This content applies to the service endpoint URL that is similar to https://\<yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span></span> 
  
<span data-ttu-id="7f466-108">您可以使用自动发现服务获取 UM web 服务终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="7f466-108">You can use the Autodiscover service to get the URL to the UM web service endpoint.</span></span> <span data-ttu-id="7f466-109">有关自动发现的详细信息，请参阅[exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7f466-109">For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="7f466-110">启动与 Exchange 2010 的 Exchange 版本，我们建议您使用统一消息操作所提供的[Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx)而不是 UM web 服务，原因如下： > 基于 EWS 的 UM 功能具有EWS 托管 API 中的第一类支持。</span><span class="sxs-lookup"><span data-stu-id="7f466-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the UM web service, for the following reasons: >  The EWS-based UM features have first-class support in the EWS Managed API.</span></span> <span data-ttu-id="7f466-111">> 在版本的 Exchange 与 Exchange 2010 开始，到 EWS 但不是到统一消息 web 服务添加新 UM 功能。</span><span class="sxs-lookup"><span data-stu-id="7f466-111">>  In versions of Exchange starting with Exchange 2010, new UM features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
<span data-ttu-id="7f466-112">UM web 服务没有显式架构。</span><span class="sxs-lookup"><span data-stu-id="7f466-112">The UM web service does not have an explicit schema.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="7f466-113">本节内容</span><span class="sxs-lookup"><span data-stu-id="7f466-113">In this section</span></span>
<span data-ttu-id="7f466-114"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="7f466-114"></span></span>

- [<span data-ttu-id="7f466-115">Exchange 统一的消息 web 服务操作</span><span class="sxs-lookup"><span data-stu-id="7f466-115">Unified Messaging web service operations for Exchange</span></span>](unified-messaging-web-service-operations-for-exchange.md)
    
- [<span data-ttu-id="7f466-116">Exchange 的统一的消息 web 服务 XML 元素</span><span class="sxs-lookup"><span data-stu-id="7f466-116">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="7f466-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7f466-117">See also</span></span>

- [<span data-ttu-id="7f466-118">Exchange 的自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="7f466-118">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="7f466-119">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="7f466-119">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="7f466-120">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="7f466-120">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

