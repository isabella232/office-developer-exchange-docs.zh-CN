---
title: ProcessRightAway
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ProcessRightAway
api_type:
- schema
ms.assetid: f6bba68b-ae4f-41c1-b3e7-c8a31cdb1b0c
description: ProcessRightAway 元素指示是否在操作在服务器上开始处理时立即发送响应，或者在操作完成后是否发送响应。 必须存在此元素，才能将异步向请求的操作发送异步响应。
ms.openlocfilehash: 58d2b926c48db5e7395df64e1f8ee9d6a8f0e73c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44434069"
---
# <a name="processrightaway"></a><span data-ttu-id="500f3-104">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="500f3-104">ProcessRightAway</span></span>

<span data-ttu-id="500f3-105">**ProcessRightAway**元素指示是否在操作在服务器上开始处理时立即发送响应，或者在操作完成后是否发送响应。</span><span class="sxs-lookup"><span data-stu-id="500f3-105">The **ProcessRightAway** element indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="500f3-106">必须存在此元素，才能将异步向请求的操作发送异步响应。</span><span class="sxs-lookup"><span data-stu-id="500f3-106">This element must be present for the response to be sent asynchronous to the requested action.</span></span> 
  
[<span data-ttu-id="500f3-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="500f3-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="500f3-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="500f3-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="500f3-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="500f3-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="500f3-110">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="500f3-110">ProcessRightAway</span></span>](processrightaway.md)
  
```XML
<ProcessRightAway/>
```

 <span data-ttu-id="500f3-111">**xs： boolean**</span><span class="sxs-lookup"><span data-stu-id="500f3-111">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="500f3-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="500f3-112">Attributes and elements</span></span>

<span data-ttu-id="500f3-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="500f3-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="500f3-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="500f3-114">Attributes</span></span>

<span data-ttu-id="500f3-115">无。</span><span class="sxs-lookup"><span data-stu-id="500f3-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="500f3-116">子元素</span><span class="sxs-lookup"><span data-stu-id="500f3-116">Child elements</span></span>

<span data-ttu-id="500f3-117">无。</span><span class="sxs-lookup"><span data-stu-id="500f3-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="500f3-118">父元素</span><span class="sxs-lookup"><span data-stu-id="500f3-118">Parent elements</span></span>

|<span data-ttu-id="500f3-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="500f3-119">**Element**</span></span>|<span data-ttu-id="500f3-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="500f3-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="500f3-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="500f3-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="500f3-122">包含要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="500f3-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="500f3-123">文本值</span><span class="sxs-lookup"><span data-stu-id="500f3-123">Text value</span></span>

<span data-ttu-id="500f3-124">如果文本值为**true** ，则表示在该操作在服务器上开始处理时立即发送响应。</span><span class="sxs-lookup"><span data-stu-id="500f3-124">A text value of **true** indicates that the response is sent as soon as the action starts processing on the server.</span></span> <span data-ttu-id="500f3-125">如果文本值为**false** ，则表示响应是在操作完成后发送的。</span><span class="sxs-lookup"><span data-stu-id="500f3-125">A text value of **false** indicates that the response is sent after the action has completed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="500f3-126">备注</span><span class="sxs-lookup"><span data-stu-id="500f3-126">Remarks</span></span>

<span data-ttu-id="500f3-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="500f3-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="500f3-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="500f3-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="500f3-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="500f3-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="500f3-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="500f3-130">Schema Name</span></span>  <br/> |<span data-ttu-id="500f3-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="500f3-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="500f3-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="500f3-132">Validation File</span></span>  <br/> |<span data-ttu-id="500f3-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="500f3-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="500f3-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="500f3-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="500f3-135">False</span><span class="sxs-lookup"><span data-stu-id="500f3-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="500f3-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="500f3-136">See also</span></span>



[<span data-ttu-id="500f3-137">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="500f3-137">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="500f3-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="500f3-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

