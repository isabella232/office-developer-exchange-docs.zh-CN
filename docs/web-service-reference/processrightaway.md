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
description: ProcessRightAway 元素指示是否将响应发送只要操作对服务器或是否将响应发送操作完成后启动处理。 此元素必须存在以响应发送异步到请求的操作。
ms.openlocfilehash: 940f8e8fa0a53801ce1c3a45c3aecf1bdb6f519d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826898"
---
# <a name="processrightaway"></a><span data-ttu-id="81ef5-104">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="81ef5-104">ProcessRightAway</span></span>

<span data-ttu-id="81ef5-105">**ProcessRightAway**元素指示是否将响应发送只要操作对服务器或是否将响应发送操作完成后启动处理。</span><span class="sxs-lookup"><span data-stu-id="81ef5-105">The **ProcessRightAway** element indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="81ef5-106">此元素必须存在以响应发送异步到请求的操作。</span><span class="sxs-lookup"><span data-stu-id="81ef5-106">This element must be present for the response to be sent asynchronous to the requested action.</span></span> 
  
[<span data-ttu-id="81ef5-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="81ef5-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="81ef5-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="81ef5-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="81ef5-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="81ef5-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="81ef5-110">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="81ef5-110">ProcessRightAway</span></span>](processrightaway.md)
  
```XML
<ProcessRightAway/>
```

 <span data-ttu-id="81ef5-111">**xs: boolean**</span><span class="sxs-lookup"><span data-stu-id="81ef5-111">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81ef5-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="81ef5-112">Attributes and elements</span></span>

<span data-ttu-id="81ef5-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="81ef5-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81ef5-114">属性</span><span class="sxs-lookup"><span data-stu-id="81ef5-114">Attributes</span></span>

<span data-ttu-id="81ef5-115">无。</span><span class="sxs-lookup"><span data-stu-id="81ef5-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81ef5-116">子元素</span><span class="sxs-lookup"><span data-stu-id="81ef5-116">Child elements</span></span>

<span data-ttu-id="81ef5-117">无。</span><span class="sxs-lookup"><span data-stu-id="81ef5-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="81ef5-118">父元素</span><span class="sxs-lookup"><span data-stu-id="81ef5-118">Parent elements</span></span>

|<span data-ttu-id="81ef5-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="81ef5-119">**Element**</span></span>|<span data-ttu-id="81ef5-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="81ef5-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81ef5-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="81ef5-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="81ef5-122">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="81ef5-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="81ef5-123">文本值</span><span class="sxs-lookup"><span data-stu-id="81ef5-123">Text value</span></span>

<span data-ttu-id="81ef5-124">文本值为**true**指示将响应发送只要操作启动服务器上的处理。</span><span class="sxs-lookup"><span data-stu-id="81ef5-124">A text value of **true** indicates that the response is sent as soon as the action starts processing on the server.</span></span> <span data-ttu-id="81ef5-125">文本值为**false**指示操作完成后，会发送响应。</span><span class="sxs-lookup"><span data-stu-id="81ef5-125">A text value of **false** indicates that the response is sent after the action has completed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="81ef5-126">备注</span><span class="sxs-lookup"><span data-stu-id="81ef5-126">Remarks</span></span>

<span data-ttu-id="81ef5-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="81ef5-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81ef5-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="81ef5-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81ef5-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="81ef5-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="81ef5-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="81ef5-130">Schema Name</span></span>  <br/> |<span data-ttu-id="81ef5-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="81ef5-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="81ef5-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="81ef5-132">Validation File</span></span>  <br/> |<span data-ttu-id="81ef5-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="81ef5-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="81ef5-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="81ef5-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="81ef5-135">False</span><span class="sxs-lookup"><span data-stu-id="81ef5-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81ef5-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="81ef5-136">See also</span></span>



[<span data-ttu-id="81ef5-137">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="81ef5-137">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="81ef5-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="81ef5-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

