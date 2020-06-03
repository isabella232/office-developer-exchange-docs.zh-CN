---
title: LastDeliveryTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LastDeliveryTime
api_type:
- schema
ms.assetid: 23d02ceb-f28e-40f2-8f63-673723a50e2a
description: LastDeliveryTime 元素包含上次在此对话中的当前文件夹中收到的邮件的传递时间。
ms.openlocfilehash: 77147693a9394e983575afa6fcfda242f8f76ae3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458108"
---
# <a name="lastdeliverytime"></a><span data-ttu-id="85b1f-103">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="85b1f-103">LastDeliveryTime</span></span>

<span data-ttu-id="85b1f-104">**LastDeliveryTime**元素包含上次在此对话中的当前文件夹中收到的邮件的传递时间。</span><span class="sxs-lookup"><span data-stu-id="85b1f-104">The **LastDeliveryTime** element contains the delivery time of the message that was last received in this conversation in the current folder.</span></span> 
  
[<span data-ttu-id="85b1f-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="85b1f-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="85b1f-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="85b1f-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="85b1f-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="85b1f-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="85b1f-108">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="85b1f-108">LastDeliveryTime</span></span>](lastdeliverytime.md)
  
```XML
<LastDeliveryTime/>
```

 <span data-ttu-id="85b1f-109">**xs： dateTime**</span><span class="sxs-lookup"><span data-stu-id="85b1f-109">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85b1f-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="85b1f-110">Attributes and elements</span></span>

<span data-ttu-id="85b1f-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="85b1f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85b1f-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="85b1f-112">Attributes</span></span>

<span data-ttu-id="85b1f-113">无。</span><span class="sxs-lookup"><span data-stu-id="85b1f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85b1f-114">子元素</span><span class="sxs-lookup"><span data-stu-id="85b1f-114">Child elements</span></span>

<span data-ttu-id="85b1f-115">无。</span><span class="sxs-lookup"><span data-stu-id="85b1f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85b1f-116">父元素</span><span class="sxs-lookup"><span data-stu-id="85b1f-116">Parent elements</span></span>

|<span data-ttu-id="85b1f-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="85b1f-117">**Element**</span></span>|<span data-ttu-id="85b1f-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="85b1f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85b1f-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="85b1f-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="85b1f-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="85b1f-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="85b1f-121">文本值</span><span class="sxs-lookup"><span data-stu-id="85b1f-121">Text value</span></span>

<span data-ttu-id="85b1f-122">**LastDeliveryTime**元素的文本值是当前文件夹中此对话中上次收到的邮件的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="85b1f-122">The text value of the **LastDeliveryTime** element is the date and time of the message that was last received in this conversation in the current folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85b1f-123">备注</span><span class="sxs-lookup"><span data-stu-id="85b1f-123">Remarks</span></span>

<span data-ttu-id="85b1f-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="85b1f-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85b1f-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="85b1f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85b1f-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="85b1f-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85b1f-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="85b1f-127">Schema name</span></span>  <br/> |<span data-ttu-id="85b1f-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="85b1f-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="85b1f-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="85b1f-129">Validation file</span></span>  <br/> |<span data-ttu-id="85b1f-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85b1f-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85b1f-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="85b1f-131">Can be empty</span></span>  <br/> |<span data-ttu-id="85b1f-132">False</span><span class="sxs-lookup"><span data-stu-id="85b1f-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85b1f-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="85b1f-133">See also</span></span>



[<span data-ttu-id="85b1f-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="85b1f-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="85b1f-135">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="85b1f-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="85b1f-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="85b1f-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="85b1f-137">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="85b1f-137">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

