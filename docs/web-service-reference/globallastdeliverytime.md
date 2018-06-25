---
title: GlobalLastDeliveryTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalLastDeliveryTime
api_type:
- schema
ms.assetid: a88dada9-c527-43a7-b2d3-31aad330def9
description: GlobalLastDeliveryTime 元素包含在邮箱中的所有文件夹上次此对话中收到的邮件的传递时间。
ms.openlocfilehash: fded5cd1891a406f0979cf4bec7321779d70ab3a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825733"
---
# <a name="globallastdeliverytime"></a><span data-ttu-id="7b3d6-103">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="7b3d6-103">GlobalLastDeliveryTime</span></span>

<span data-ttu-id="7b3d6-104">**GlobalLastDeliveryTime**元素包含在邮箱中的所有文件夹上次此对话中收到的邮件的传递时间。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-104">The **GlobalLastDeliveryTime** element contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
[<span data-ttu-id="7b3d6-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="7b3d6-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="7b3d6-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="7b3d6-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="7b3d6-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="7b3d6-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="7b3d6-108">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="7b3d6-108">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md)
  
```XML
<GlobalLastDeliveryTime/>
```

 <span data-ttu-id="7b3d6-109">**xs:dateTime**</span><span class="sxs-lookup"><span data-stu-id="7b3d6-109">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b3d6-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7b3d6-110">Attributes and elements</span></span>

<span data-ttu-id="7b3d6-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b3d6-112">属性</span><span class="sxs-lookup"><span data-stu-id="7b3d6-112">Attributes</span></span>

<span data-ttu-id="7b3d6-113">无。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b3d6-114">子元素</span><span class="sxs-lookup"><span data-stu-id="7b3d6-114">Child elements</span></span>

<span data-ttu-id="7b3d6-115">无。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7b3d6-116">父元素</span><span class="sxs-lookup"><span data-stu-id="7b3d6-116">Parent elements</span></span>

|<span data-ttu-id="7b3d6-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b3d6-117">**Element**</span></span>|<span data-ttu-id="7b3d6-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b3d6-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b3d6-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="7b3d6-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="7b3d6-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7b3d6-121">文本值</span><span class="sxs-lookup"><span data-stu-id="7b3d6-121">Text value</span></span>

<span data-ttu-id="7b3d6-122">**GlobalLastDeliveryTime**元素的文本值的日期和时间的邮箱中的所有文件夹中最后一次此对话中收到的邮件。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-122">The text value of the **GlobalLastDeliveryTime** element is the date and time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7b3d6-123">注解</span><span class="sxs-lookup"><span data-stu-id="7b3d6-123">Remarks</span></span>

<span data-ttu-id="7b3d6-124">此元素是在 Exchange Server 2010 Service Pack 1 (SP1) 中引入的。描述此元素的架构位于承载 Exchange Web 服务的 IIS 虚拟目录。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-124">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b3d6-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="7b3d6-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b3d6-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="7b3d6-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7b3d6-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="7b3d6-127">Schema name</span></span>  <br/> |<span data-ttu-id="7b3d6-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="7b3d6-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="7b3d6-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="7b3d6-129">Validation file</span></span>  <br/> |<span data-ttu-id="7b3d6-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7b3d6-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7b3d6-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="7b3d6-131">Can be empty</span></span>  <br/> |<span data-ttu-id="7b3d6-132">False</span><span class="sxs-lookup"><span data-stu-id="7b3d6-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b3d6-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7b3d6-133">See also</span></span>



[<span data-ttu-id="7b3d6-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="7b3d6-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="7b3d6-135">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="7b3d6-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="7b3d6-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="7b3d6-136">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

