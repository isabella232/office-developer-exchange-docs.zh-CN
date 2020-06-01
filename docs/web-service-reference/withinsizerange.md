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
description: WithinSizeRange 元素指定传入邮件必须满足的最小和最大大小，以便条件或例外情况适用。
ms.openlocfilehash: 31da5815b70e20c47594da89b0b7ccab87eaf8f3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459740"
---
# <a name="withinsizerange"></a><span data-ttu-id="7c396-103">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="7c396-103">WithinSizeRange</span></span>

<span data-ttu-id="7c396-104">**WithinSizeRange**元素指定传入邮件必须满足的最小和最大大小，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="7c396-104">The **WithinSizeRange** element specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinSizeRange>
     <MinimumSize/>
     <MaximumSize/>
</WithinSizeRange>
```

 <span data-ttu-id="7c396-105">**RulePredicateSizeRangeType**</span><span class="sxs-lookup"><span data-stu-id="7c396-105">**RulePredicateSizeRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7c396-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7c396-106">Attributes and elements</span></span>

<span data-ttu-id="7c396-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7c396-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c396-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7c396-108">Attributes</span></span>

<span data-ttu-id="7c396-109">无。</span><span class="sxs-lookup"><span data-stu-id="7c396-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c396-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7c396-110">Child elements</span></span>

|<span data-ttu-id="7c396-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7c396-111">**Element**</span></span>|<span data-ttu-id="7c396-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7c396-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c396-113">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="7c396-113">MinimumSize</span></span>](minimumsize.md) <br/> |<span data-ttu-id="7c396-114">指定当条件或例外情况适用时，邮件必须满足的最小大小。</span><span class="sxs-lookup"><span data-stu-id="7c396-114">Specifies the minimum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="7c396-115">MaximumSize</span><span class="sxs-lookup"><span data-stu-id="7c396-115">MaximumSize</span></span>](maximumsize.md) <br/> |<span data-ttu-id="7c396-116">指定要应用的条件或例外的邮件必须满足的最大大小。</span><span class="sxs-lookup"><span data-stu-id="7c396-116">Specifies the maximum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7c396-117">父元素</span><span class="sxs-lookup"><span data-stu-id="7c396-117">Parent elements</span></span>

|<span data-ttu-id="7c396-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="7c396-118">**Element**</span></span>|<span data-ttu-id="7c396-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="7c396-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c396-120">条件</span><span class="sxs-lookup"><span data-stu-id="7c396-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="7c396-121">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="7c396-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="7c396-122">异常</span><span class="sxs-lookup"><span data-stu-id="7c396-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="7c396-123">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="7c396-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7c396-124">文本值</span><span class="sxs-lookup"><span data-stu-id="7c396-124">Text value</span></span>

<span data-ttu-id="7c396-125">无。</span><span class="sxs-lookup"><span data-stu-id="7c396-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c396-126">说明</span><span class="sxs-lookup"><span data-stu-id="7c396-126">Remarks</span></span>

<span data-ttu-id="7c396-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7c396-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c396-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="7c396-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c396-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="7c396-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7c396-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="7c396-130">Schema Name</span></span>  <br/> |<span data-ttu-id="7c396-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="7c396-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7c396-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="7c396-132">Validation File</span></span>  <br/> |<span data-ttu-id="7c396-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7c396-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7c396-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="7c396-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="7c396-135">True</span><span class="sxs-lookup"><span data-stu-id="7c396-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c396-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7c396-136">See also</span></span>



- [<span data-ttu-id="7c396-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7c396-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

