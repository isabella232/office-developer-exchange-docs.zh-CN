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
description: FlaggedForAction 元素中的条件或例外应用的顺序的传入邮件上指定必须在出现的操作值的标志。
ms.openlocfilehash: 5b6e714512edcf12ded2c04f414d047b8622d305
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754381"
---
# <a name="flaggedforaction"></a><span data-ttu-id="2f47b-103">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="2f47b-103">FlaggedForAction</span></span>

<span data-ttu-id="2f47b-104">**FlaggedForAction**元素中的条件或例外应用的顺序的传入邮件上指定必须在出现的操作值的标志。</span><span class="sxs-lookup"><span data-stu-id="2f47b-104">The **FlaggedForAction** element specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<FlaggedForAction/>
```

 <span data-ttu-id="2f47b-105">**FlaggedForActionType**</span><span class="sxs-lookup"><span data-stu-id="2f47b-105">**FlaggedForActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f47b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2f47b-106">Attributes and elements</span></span>

<span data-ttu-id="2f47b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f47b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f47b-108">属性</span><span class="sxs-lookup"><span data-stu-id="2f47b-108">Attributes</span></span>

<span data-ttu-id="2f47b-109">无。</span><span class="sxs-lookup"><span data-stu-id="2f47b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f47b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2f47b-110">Child elements</span></span>

<span data-ttu-id="2f47b-111">无。</span><span class="sxs-lookup"><span data-stu-id="2f47b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f47b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2f47b-112">Parent elements</span></span>

|<span data-ttu-id="2f47b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f47b-113">**Element**</span></span>|<span data-ttu-id="2f47b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f47b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f47b-115">条件</span><span class="sxs-lookup"><span data-stu-id="2f47b-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="2f47b-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="2f47b-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="2f47b-117">异常</span><span class="sxs-lookup"><span data-stu-id="2f47b-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="2f47b-118">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="2f47b-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2f47b-119">文本值</span><span class="sxs-lookup"><span data-stu-id="2f47b-119">Text value</span></span>

<span data-ttu-id="2f47b-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="2f47b-120">A text value is required.</span></span> <span data-ttu-id="2f47b-121">此元素的可能的文本值如下：</span><span class="sxs-lookup"><span data-stu-id="2f47b-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="2f47b-122">任意</span><span class="sxs-lookup"><span data-stu-id="2f47b-122">Any</span></span>
    
- <span data-ttu-id="2f47b-123">调用</span><span class="sxs-lookup"><span data-stu-id="2f47b-123">Call</span></span>
    
- <span data-ttu-id="2f47b-124">DoNotForward</span><span class="sxs-lookup"><span data-stu-id="2f47b-124">DoNotForward</span></span>
    
- <span data-ttu-id="2f47b-125">后续</span><span class="sxs-lookup"><span data-stu-id="2f47b-125">FollowUp</span></span>
    
- <span data-ttu-id="2f47b-126">注意</span><span class="sxs-lookup"><span data-stu-id="2f47b-126">FYI</span></span>
    
- <span data-ttu-id="2f47b-127">Forward</span><span class="sxs-lookup"><span data-stu-id="2f47b-127">Forward</span></span>
    
- <span data-ttu-id="2f47b-128">NoResponseNecessary</span><span class="sxs-lookup"><span data-stu-id="2f47b-128">NoResponseNecessary</span></span>
    
- <span data-ttu-id="2f47b-129">已阅读</span><span class="sxs-lookup"><span data-stu-id="2f47b-129">Read</span></span>
    
- <span data-ttu-id="2f47b-130">答复</span><span class="sxs-lookup"><span data-stu-id="2f47b-130">Reply</span></span>
    
- <span data-ttu-id="2f47b-131">ReplyToAll</span><span class="sxs-lookup"><span data-stu-id="2f47b-131">ReplyToAll</span></span>
    
- <span data-ttu-id="2f47b-132">审阅</span><span class="sxs-lookup"><span data-stu-id="2f47b-132">Review</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f47b-133">备注</span><span class="sxs-lookup"><span data-stu-id="2f47b-133">Remarks</span></span>

<span data-ttu-id="2f47b-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2f47b-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f47b-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="2f47b-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f47b-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="2f47b-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2f47b-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="2f47b-137">Schema Name</span></span>  <br/> |<span data-ttu-id="2f47b-138">消息架构</span><span class="sxs-lookup"><span data-stu-id="2f47b-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2f47b-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="2f47b-139">Validation File</span></span>  <br/> |<span data-ttu-id="2f47b-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2f47b-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f47b-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="2f47b-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f47b-142">True</span><span class="sxs-lookup"><span data-stu-id="2f47b-142">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f47b-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f47b-143">See also</span></span>



- [<span data-ttu-id="2f47b-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2f47b-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

