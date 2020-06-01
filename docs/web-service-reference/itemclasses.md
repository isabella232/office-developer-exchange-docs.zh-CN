---
title: ItemClasses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemClasses
api_type:
- schema
ms.assetid: f95430cc-2860-47c1-af2d-8c4156c9b281
description: ItemClasses 元素表示必须在传入的邮件上标记的项目类，以便条件或例外情况适用。
ms.openlocfilehash: 56b99cad2abef0a9953e1793e5b633acca83a9eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460111"
---
# <a name="itemclasses"></a><span data-ttu-id="7ac64-103">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="7ac64-103">ItemClasses</span></span>

<span data-ttu-id="7ac64-104">**ItemClasses**元素表示必须在传入的邮件上标记的项目类，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="7ac64-104">The **ItemClasses** element represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 <span data-ttu-id="7ac64-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="7ac64-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ac64-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7ac64-106">Attributes and elements</span></span>

<span data-ttu-id="7ac64-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7ac64-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ac64-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7ac64-108">Attributes</span></span>

<span data-ttu-id="7ac64-109">无。</span><span class="sxs-lookup"><span data-stu-id="7ac64-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ac64-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7ac64-110">Child elements</span></span>

|<span data-ttu-id="7ac64-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ac64-111">**Element**</span></span>|<span data-ttu-id="7ac64-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ac64-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ac64-113">字符串</span><span class="sxs-lookup"><span data-stu-id="7ac64-113">String</span></span>](string.md) <br/> |<span data-ttu-id="7ac64-114">表示单个项目类。</span><span class="sxs-lookup"><span data-stu-id="7ac64-114">Represents a single item class.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7ac64-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7ac64-115">Parent elements</span></span>

|<span data-ttu-id="7ac64-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ac64-116">**Element**</span></span>|<span data-ttu-id="7ac64-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ac64-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ac64-118">条件</span><span class="sxs-lookup"><span data-stu-id="7ac64-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="7ac64-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="7ac64-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="7ac64-120">异常</span><span class="sxs-lookup"><span data-stu-id="7ac64-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="7ac64-121">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="7ac64-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7ac64-122">文本值</span><span class="sxs-lookup"><span data-stu-id="7ac64-122">Text value</span></span>

<span data-ttu-id="7ac64-123">无。</span><span class="sxs-lookup"><span data-stu-id="7ac64-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ac64-124">说明</span><span class="sxs-lookup"><span data-stu-id="7ac64-124">Remarks</span></span>

<span data-ttu-id="7ac64-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7ac64-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ac64-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="7ac64-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ac64-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="7ac64-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ac64-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="7ac64-128">Schema name</span></span>  <br/> |<span data-ttu-id="7ac64-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="7ac64-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="7ac64-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="7ac64-130">Validation file</span></span>  <br/> |<span data-ttu-id="7ac64-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7ac64-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ac64-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="7ac64-132">Can be empty</span></span>  <br/> |<span data-ttu-id="7ac64-133">False</span><span class="sxs-lookup"><span data-stu-id="7ac64-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ac64-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ac64-134">See also</span></span>



- [<span data-ttu-id="7ac64-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7ac64-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

