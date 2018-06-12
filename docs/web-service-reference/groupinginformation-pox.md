---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: GroupingInformation 元素包含一个值，用于组跨多个邮箱订阅通知时保持关联的用户的邮箱。
ms.openlocfilehash: bcde002c794ac79d9515befc0755c1f954ee8706
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825781"
---
# <a name="groupinginformation-pox"></a><span data-ttu-id="0fdee-103">GroupingInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="0fdee-103">GroupingInformation (POX)</span></span>

<span data-ttu-id="0fdee-104">**GroupingInformation**元素包含一个值，用于跨多个邮箱订阅通知时组[维护关联](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)的用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="0fdee-104">The **GroupingInformation** element contains a value that is used to group the user's mailbox to [maintain affinity](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) when subscribing to notifications across multiple mailboxes.</span></span> 
  
[<span data-ttu-id="0fdee-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="0fdee-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="0fdee-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="0fdee-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="0fdee-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="0fdee-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="0fdee-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="0fdee-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="0fdee-109">GroupingInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="0fdee-109">GroupingInformation (POX)</span></span>](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0fdee-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0fdee-110">Attributes and elements</span></span>

<span data-ttu-id="0fdee-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0fdee-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fdee-112">属性</span><span class="sxs-lookup"><span data-stu-id="0fdee-112">Attributes</span></span>

<span data-ttu-id="0fdee-113">无。</span><span class="sxs-lookup"><span data-stu-id="0fdee-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0fdee-114">子元素</span><span class="sxs-lookup"><span data-stu-id="0fdee-114">Child elements</span></span>

<span data-ttu-id="0fdee-115">无。</span><span class="sxs-lookup"><span data-stu-id="0fdee-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0fdee-116">父元素</span><span class="sxs-lookup"><span data-stu-id="0fdee-116">Parent elements</span></span>

|<span data-ttu-id="0fdee-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="0fdee-117">**Element**</span></span>|<span data-ttu-id="0fdee-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="0fdee-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fdee-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="0fdee-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="0fdee-120">包含客户端连接到 Exchange 服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="0fdee-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0fdee-121">文本值</span><span class="sxs-lookup"><span data-stu-id="0fdee-121">Text value</span></span>

<span data-ttu-id="0fdee-122">其他邮箱的**GroupingInformation**元素的值进行比较的文本值。</span><span class="sxs-lookup"><span data-stu-id="0fdee-122">The text value is compared to the value of the **GroupingInformation** element for other mailboxes.</span></span> <span data-ttu-id="0fdee-123">具有相同的值，并使用相同的 Exchange Web Services (EWS) 终点的邮箱的组合可以在一起，以维护关联。</span><span class="sxs-lookup"><span data-stu-id="0fdee-123">Mailboxes that have the same value and use the same Exchange Web Services (EWS) endpoint can be grouped together to maintain affinity.</span></span> <span data-ttu-id="0fdee-124">有关详细信息，请参阅[在 Exchange 维护一组订阅和邮箱服务器之间的关联](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0fdee-124">For more details, see [Maintain affinity between a group of subscriptions and the Mailbox server in Exchange](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0fdee-125">备注</span><span class="sxs-lookup"><span data-stu-id="0fdee-125">Remarks</span></span>

<span data-ttu-id="0fdee-126">**GroupingInformation**元素仅适用于具有[类型 (POX)](type-pox.md)子元素的值为"EXPR"的**协议**元素。</span><span class="sxs-lookup"><span data-stu-id="0fdee-126">The **GroupingInformation** element is only applicable to **Protocol** elements that have a [Type (POX)](type-pox.md) child element with a value of "EXPR".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0fdee-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0fdee-127">See also</span></span>

- [<span data-ttu-id="0fdee-128">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="0fdee-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
- [<span data-ttu-id="0fdee-129">在 Exchange 维护一组订阅和邮箱服务器之间的关联</span><span class="sxs-lookup"><span data-stu-id="0fdee-129">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

