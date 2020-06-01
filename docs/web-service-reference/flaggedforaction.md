---
title: FlaggedForAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FlaggedForAction
api_type:
- schema
ms.assetid: 6a08c48a-7b32-4754-8940-adbda55e8133
description: FlaggedForAction 元素指定必须出现在传入邮件上的 action 值标志，以便条件或例外情况适用。
ms.openlocfilehash: f996dc4bcf30db32e1d73fb302ab137f0a6ad4d4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466239"
---
# <a name="flaggedforaction"></a><span data-ttu-id="b82ca-103">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="b82ca-103">FlaggedForAction</span></span>

<span data-ttu-id="b82ca-104">**FlaggedForAction**元素指定必须出现在传入邮件上的 action 值标志，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="b82ca-104">The **FlaggedForAction** element specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<FlaggedForAction/>
```

 <span data-ttu-id="b82ca-105">**FlaggedForActionType**</span><span class="sxs-lookup"><span data-stu-id="b82ca-105">**FlaggedForActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b82ca-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b82ca-106">Attributes and elements</span></span>

<span data-ttu-id="b82ca-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b82ca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b82ca-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b82ca-108">Attributes</span></span>

<span data-ttu-id="b82ca-109">无。</span><span class="sxs-lookup"><span data-stu-id="b82ca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b82ca-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b82ca-110">Child elements</span></span>

<span data-ttu-id="b82ca-111">无。</span><span class="sxs-lookup"><span data-stu-id="b82ca-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b82ca-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b82ca-112">Parent elements</span></span>

|<span data-ttu-id="b82ca-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b82ca-113">**Element**</span></span>|<span data-ttu-id="b82ca-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b82ca-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b82ca-115">条件</span><span class="sxs-lookup"><span data-stu-id="b82ca-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="b82ca-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="b82ca-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="b82ca-117">异常</span><span class="sxs-lookup"><span data-stu-id="b82ca-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="b82ca-118">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="b82ca-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b82ca-119">文本值</span><span class="sxs-lookup"><span data-stu-id="b82ca-119">Text value</span></span>

<span data-ttu-id="b82ca-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="b82ca-120">A text value is required.</span></span> <span data-ttu-id="b82ca-121">以下是此元素的可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="b82ca-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="b82ca-122">任意</span><span class="sxs-lookup"><span data-stu-id="b82ca-122">Any</span></span>
    
- <span data-ttu-id="b82ca-123">呼叫</span><span class="sxs-lookup"><span data-stu-id="b82ca-123">Call</span></span>
    
- <span data-ttu-id="b82ca-124">DoNotForward</span><span class="sxs-lookup"><span data-stu-id="b82ca-124">DoNotForward</span></span>
    
- <span data-ttu-id="b82ca-125">努力</span><span class="sxs-lookup"><span data-stu-id="b82ca-125">FollowUp</span></span>
    
- <span data-ttu-id="b82ca-126">仅供参考</span><span class="sxs-lookup"><span data-stu-id="b82ca-126">FYI</span></span>
    
- <span data-ttu-id="b82ca-127">转发</span><span class="sxs-lookup"><span data-stu-id="b82ca-127">Forward</span></span>
    
- <span data-ttu-id="b82ca-128">NoResponseNecessary</span><span class="sxs-lookup"><span data-stu-id="b82ca-128">NoResponseNecessary</span></span>
    
- <span data-ttu-id="b82ca-129">阅读</span><span class="sxs-lookup"><span data-stu-id="b82ca-129">Read</span></span>
    
- <span data-ttu-id="b82ca-130">答复</span><span class="sxs-lookup"><span data-stu-id="b82ca-130">Reply</span></span>
    
- <span data-ttu-id="b82ca-131">ReplyToAll</span><span class="sxs-lookup"><span data-stu-id="b82ca-131">ReplyToAll</span></span>
    
- <span data-ttu-id="b82ca-132">审阅</span><span class="sxs-lookup"><span data-stu-id="b82ca-132">Review</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b82ca-133">说明</span><span class="sxs-lookup"><span data-stu-id="b82ca-133">Remarks</span></span>

<span data-ttu-id="b82ca-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b82ca-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b82ca-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="b82ca-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b82ca-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="b82ca-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b82ca-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="b82ca-137">Schema Name</span></span>  <br/> |<span data-ttu-id="b82ca-138">消息架构</span><span class="sxs-lookup"><span data-stu-id="b82ca-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b82ca-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="b82ca-139">Validation File</span></span>  <br/> |<span data-ttu-id="b82ca-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b82ca-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b82ca-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="b82ca-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="b82ca-142">True</span><span class="sxs-lookup"><span data-stu-id="b82ca-142">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b82ca-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b82ca-143">See also</span></span>



- [<span data-ttu-id="b82ca-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b82ca-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

