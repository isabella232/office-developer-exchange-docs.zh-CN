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
description: LastDeliveryTime 元素包含上次当前文件夹中的此对话中收到的邮件的传递时间。
ms.openlocfilehash: 240f6acaf3e5249686ab26501a26ee3e0f337b0f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826198"
---
# <a name="lastdeliverytime"></a><span data-ttu-id="50919-103">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="50919-103">LastDeliveryTime</span></span>

<span data-ttu-id="50919-104">**LastDeliveryTime**元素包含上次当前文件夹中的此对话中收到的邮件的传递时间。</span><span class="sxs-lookup"><span data-stu-id="50919-104">The **LastDeliveryTime** element contains the delivery time of the message that was last received in this conversation in the current folder.</span></span> 
  
[<span data-ttu-id="50919-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="50919-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="50919-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="50919-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="50919-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="50919-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="50919-108">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="50919-108">LastDeliveryTime</span></span>](lastdeliverytime.md)
  
```XML
<LastDeliveryTime/>
```

 <span data-ttu-id="50919-109">**xs:dateTime**</span><span class="sxs-lookup"><span data-stu-id="50919-109">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50919-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="50919-110">Attributes and elements</span></span>

<span data-ttu-id="50919-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="50919-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50919-112">属性</span><span class="sxs-lookup"><span data-stu-id="50919-112">Attributes</span></span>

<span data-ttu-id="50919-113">无。</span><span class="sxs-lookup"><span data-stu-id="50919-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50919-114">子元素</span><span class="sxs-lookup"><span data-stu-id="50919-114">Child elements</span></span>

<span data-ttu-id="50919-115">无。</span><span class="sxs-lookup"><span data-stu-id="50919-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="50919-116">父元素</span><span class="sxs-lookup"><span data-stu-id="50919-116">Parent elements</span></span>

|<span data-ttu-id="50919-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="50919-117">**Element**</span></span>|<span data-ttu-id="50919-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="50919-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50919-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="50919-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="50919-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="50919-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="50919-121">文本值</span><span class="sxs-lookup"><span data-stu-id="50919-121">Text value</span></span>

<span data-ttu-id="50919-122">**LastDeliveryTime**元素的文本值的日期和时间上次当前文件夹中的此对话中收到的邮件。</span><span class="sxs-lookup"><span data-stu-id="50919-122">The text value of the **LastDeliveryTime** element is the date and time of the message that was last received in this conversation in the current folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="50919-123">备注</span><span class="sxs-lookup"><span data-stu-id="50919-123">Remarks</span></span>

<span data-ttu-id="50919-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="50919-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50919-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="50919-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50919-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="50919-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50919-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="50919-127">Schema name</span></span>  <br/> |<span data-ttu-id="50919-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="50919-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="50919-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="50919-129">Validation file</span></span>  <br/> |<span data-ttu-id="50919-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="50919-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="50919-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="50919-131">Can be empty</span></span>  <br/> |<span data-ttu-id="50919-132">False</span><span class="sxs-lookup"><span data-stu-id="50919-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50919-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="50919-133">See also</span></span>



[<span data-ttu-id="50919-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="50919-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="50919-135">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="50919-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="50919-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="50919-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="50919-137">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="50919-137">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)
