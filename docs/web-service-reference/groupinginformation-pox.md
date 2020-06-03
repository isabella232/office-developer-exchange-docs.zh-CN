---
title: GroupingInformation （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: GroupingInformation 元素包含一个值，用于对用户的邮箱进行分组，以便在通过多个邮箱订阅通知时保持相关性。
ms.openlocfilehash: 7cab5d68f7dd5ec1f6caded5b9da6cfee03f3a67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530076"
---
# <a name="groupinginformation-pox"></a><span data-ttu-id="19388-103">GroupingInformation （POX）</span><span class="sxs-lookup"><span data-stu-id="19388-103">GroupingInformation (POX)</span></span>

<span data-ttu-id="19388-104">**GroupingInformation**元素包含一个值，用于对用户的邮箱进行分组，以便在通过多个邮箱订阅通知时[保持相关性](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="19388-104">The **GroupingInformation** element contains a value that is used to group the user's mailbox to [maintain affinity](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) when subscribing to notifications across multiple mailboxes.</span></span> 
  
[<span data-ttu-id="19388-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="19388-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="19388-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="19388-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="19388-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="19388-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="19388-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="19388-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="19388-109">GroupingInformation （POX）</span><span class="sxs-lookup"><span data-stu-id="19388-109">GroupingInformation (POX)</span></span>](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="19388-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="19388-110">Attributes and elements</span></span>

<span data-ttu-id="19388-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="19388-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19388-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="19388-112">Attributes</span></span>

<span data-ttu-id="19388-113">无。</span><span class="sxs-lookup"><span data-stu-id="19388-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19388-114">子元素</span><span class="sxs-lookup"><span data-stu-id="19388-114">Child elements</span></span>

<span data-ttu-id="19388-115">无。</span><span class="sxs-lookup"><span data-stu-id="19388-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19388-116">父元素</span><span class="sxs-lookup"><span data-stu-id="19388-116">Parent elements</span></span>

|<span data-ttu-id="19388-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="19388-117">**Element**</span></span>|<span data-ttu-id="19388-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="19388-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19388-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="19388-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="19388-120">包含用于将客户端连接到 Exchange 服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="19388-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19388-121">文本值</span><span class="sxs-lookup"><span data-stu-id="19388-121">Text value</span></span>

<span data-ttu-id="19388-122">将文本值与其他邮箱的**GroupingInformation**元素的值进行比较。</span><span class="sxs-lookup"><span data-stu-id="19388-122">The text value is compared to the value of the **GroupingInformation** element for other mailboxes.</span></span> <span data-ttu-id="19388-123">具有相同值并使用相同的 Exchange Web 服务（EWS）终结点的邮箱可以组合在一起以保持相关性。</span><span class="sxs-lookup"><span data-stu-id="19388-123">Mailboxes that have the same value and use the same Exchange Web Services (EWS) endpoint can be grouped together to maintain affinity.</span></span> <span data-ttu-id="19388-124">有关更多详细信息，请参阅[维护 Exchange 中的一组订阅和邮箱服务器之间的相关性](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="19388-124">For more details, see [Maintain affinity between a group of subscriptions and the Mailbox server in Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19388-125">备注</span><span class="sxs-lookup"><span data-stu-id="19388-125">Remarks</span></span>

<span data-ttu-id="19388-126">**GroupingInformation**元素仅适用于具有值为 "EXPR" 的[类型（POX）](type-pox.md)子元素的**协议**元素。</span><span class="sxs-lookup"><span data-stu-id="19388-126">The **GroupingInformation** element is only applicable to **Protocol** elements that have a [Type (POX)](type-pox.md) child element with a value of "EXPR".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19388-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="19388-127">See also</span></span>

- [<span data-ttu-id="19388-128">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="19388-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
- [<span data-ttu-id="19388-129">维护 Exchange 中的一组订阅和邮箱服务器之间的相关性</span><span class="sxs-lookup"><span data-stu-id="19388-129">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

