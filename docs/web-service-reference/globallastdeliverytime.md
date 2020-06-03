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
description: GlobalLastDeliveryTime 元素包含在此对话中的邮件在邮箱中的所有文件夹中最后一次接收的传递时间。
ms.openlocfilehash: b6d4d7c1d51c206e44973a717d25df4066845ada
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459410"
---
# <a name="globallastdeliverytime"></a><span data-ttu-id="a69c8-103">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="a69c8-103">GlobalLastDeliveryTime</span></span>

<span data-ttu-id="a69c8-104">**GlobalLastDeliveryTime**元素包含在此对话中的邮件在邮箱中的所有文件夹中最后一次接收的传递时间。</span><span class="sxs-lookup"><span data-stu-id="a69c8-104">The **GlobalLastDeliveryTime** element contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
[<span data-ttu-id="a69c8-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="a69c8-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="a69c8-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="a69c8-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="a69c8-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a69c8-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="a69c8-108">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="a69c8-108">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md)
  
```XML
<GlobalLastDeliveryTime/>
```

 <span data-ttu-id="a69c8-109">**xs： dateTime**</span><span class="sxs-lookup"><span data-stu-id="a69c8-109">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a69c8-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a69c8-110">Attributes and elements</span></span>

<span data-ttu-id="a69c8-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a69c8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a69c8-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="a69c8-112">Attributes</span></span>

<span data-ttu-id="a69c8-113">无。</span><span class="sxs-lookup"><span data-stu-id="a69c8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a69c8-114">子元素</span><span class="sxs-lookup"><span data-stu-id="a69c8-114">Child elements</span></span>

<span data-ttu-id="a69c8-115">无。</span><span class="sxs-lookup"><span data-stu-id="a69c8-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a69c8-116">父元素</span><span class="sxs-lookup"><span data-stu-id="a69c8-116">Parent elements</span></span>

|<span data-ttu-id="a69c8-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="a69c8-117">**Element**</span></span>|<span data-ttu-id="a69c8-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="a69c8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a69c8-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a69c8-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="a69c8-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="a69c8-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a69c8-121">文本值</span><span class="sxs-lookup"><span data-stu-id="a69c8-121">Text value</span></span>

<span data-ttu-id="a69c8-122">**GlobalLastDeliveryTime**元素的文本值是邮箱中的所有文件夹的最近在此对话中收到的邮件的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a69c8-122">The text value of the **GlobalLastDeliveryTime** element is the date and time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a69c8-123">备注</span><span class="sxs-lookup"><span data-stu-id="a69c8-123">Remarks</span></span>

<span data-ttu-id="a69c8-124">此元素是在 Exchange Server 2010 Service Pack 1 （SP1）中引入的。描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a69c8-124">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a69c8-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="a69c8-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a69c8-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="a69c8-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a69c8-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="a69c8-127">Schema name</span></span>  <br/> |<span data-ttu-id="a69c8-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="a69c8-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="a69c8-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="a69c8-129">Validation file</span></span>  <br/> |<span data-ttu-id="a69c8-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a69c8-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a69c8-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="a69c8-131">Can be empty</span></span>  <br/> |<span data-ttu-id="a69c8-132">False</span><span class="sxs-lookup"><span data-stu-id="a69c8-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a69c8-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a69c8-133">See also</span></span>



[<span data-ttu-id="a69c8-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="a69c8-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="a69c8-135">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="a69c8-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="a69c8-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="a69c8-136">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

