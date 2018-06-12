---
title: WithinSizeRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WithinSizeRange
api_type:
- schema
ms.assetid: 6f98650e-3399-4f87-9b7f-40bf20cdb821
description: WithinSizeRange 元素指定的条件或例外的顺序应用必须传入消息的最小和最大大小。
ms.openlocfilehash: 7711db9ca68f972f080c98197e30c7710620119a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838569"
---
# <a name="withinsizerange"></a><span data-ttu-id="fded2-103">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="fded2-103">WithinSizeRange</span></span>

<span data-ttu-id="fded2-104">**WithinSizeRange**元素指定的条件或例外的顺序应用必须传入消息的最小和最大大小。</span><span class="sxs-lookup"><span data-stu-id="fded2-104">The **WithinSizeRange** element specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinSizeRange>
     <MinimumSize/>
     <MaximumSize/>
</WithinSizeRange>
```

 <span data-ttu-id="fded2-105">**RulePredicateSizeRangeType**</span><span class="sxs-lookup"><span data-stu-id="fded2-105">**RulePredicateSizeRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fded2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fded2-106">Attributes and elements</span></span>

<span data-ttu-id="fded2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fded2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fded2-108">属性</span><span class="sxs-lookup"><span data-stu-id="fded2-108">Attributes</span></span>

<span data-ttu-id="fded2-109">无。</span><span class="sxs-lookup"><span data-stu-id="fded2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fded2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fded2-110">Child elements</span></span>

|<span data-ttu-id="fded2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fded2-111">**Element**</span></span>|<span data-ttu-id="fded2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fded2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fded2-113">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="fded2-113">MinimumSize</span></span>](minimumsize.md) <br/> |<span data-ttu-id="fded2-114">指定的条件或例外的顺序应用必须一条消息的最小大小。</span><span class="sxs-lookup"><span data-stu-id="fded2-114">Specifies the minimum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="fded2-115">大化</span><span class="sxs-lookup"><span data-stu-id="fded2-115">MaximumSize</span></span>](maximumsize.md) <br/> |<span data-ttu-id="fded2-116">指定的条件或例外的顺序应用必须一条消息的最大大小。</span><span class="sxs-lookup"><span data-stu-id="fded2-116">Specifies the maximum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fded2-117">父元素</span><span class="sxs-lookup"><span data-stu-id="fded2-117">Parent elements</span></span>

|<span data-ttu-id="fded2-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="fded2-118">**Element**</span></span>|<span data-ttu-id="fded2-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="fded2-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fded2-120">条件</span><span class="sxs-lookup"><span data-stu-id="fded2-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="fded2-121">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="fded2-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="fded2-122">异常</span><span class="sxs-lookup"><span data-stu-id="fded2-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="fded2-123">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="fded2-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fded2-124">文本值</span><span class="sxs-lookup"><span data-stu-id="fded2-124">Text value</span></span>

<span data-ttu-id="fded2-125">无。</span><span class="sxs-lookup"><span data-stu-id="fded2-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fded2-126">备注</span><span class="sxs-lookup"><span data-stu-id="fded2-126">Remarks</span></span>

<span data-ttu-id="fded2-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fded2-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fded2-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="fded2-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fded2-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="fded2-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fded2-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="fded2-130">Schema Name</span></span>  <br/> |<span data-ttu-id="fded2-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="fded2-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fded2-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="fded2-132">Validation File</span></span>  <br/> |<span data-ttu-id="fded2-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fded2-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fded2-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="fded2-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="fded2-135">True</span><span class="sxs-lookup"><span data-stu-id="fded2-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fded2-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fded2-136">See also</span></span>



- [<span data-ttu-id="fded2-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fded2-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

