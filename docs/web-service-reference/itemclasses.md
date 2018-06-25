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
description: ItemClasses 元素均表示必须在应用的条件或例外顺序中的传入邮件标记的项类。
ms.openlocfilehash: 70a4823f9017ba8c6f894394d5907f1adeb80167
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826148"
---
# <a name="itemclasses"></a><span data-ttu-id="cf165-103">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="cf165-103">ItemClasses</span></span>

<span data-ttu-id="cf165-104">**ItemClasses**元素均表示必须在应用的条件或例外顺序中的传入邮件标记的项类。</span><span class="sxs-lookup"><span data-stu-id="cf165-104">The **ItemClasses** element represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 <span data-ttu-id="cf165-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="cf165-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf165-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cf165-106">Attributes and elements</span></span>

<span data-ttu-id="cf165-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cf165-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf165-108">属性</span><span class="sxs-lookup"><span data-stu-id="cf165-108">Attributes</span></span>

<span data-ttu-id="cf165-109">无。</span><span class="sxs-lookup"><span data-stu-id="cf165-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cf165-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cf165-110">Child elements</span></span>

|<span data-ttu-id="cf165-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cf165-111">**Element**</span></span>|<span data-ttu-id="cf165-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf165-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf165-113">字符串</span><span class="sxs-lookup"><span data-stu-id="cf165-113">String</span></span>](string.md) <br/> |<span data-ttu-id="cf165-114">表示单个项目类。</span><span class="sxs-lookup"><span data-stu-id="cf165-114">Represents a single item class.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf165-115">父元素</span><span class="sxs-lookup"><span data-stu-id="cf165-115">Parent elements</span></span>

|<span data-ttu-id="cf165-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="cf165-116">**Element**</span></span>|<span data-ttu-id="cf165-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf165-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf165-118">条件</span><span class="sxs-lookup"><span data-stu-id="cf165-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="cf165-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="cf165-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="cf165-120">异常</span><span class="sxs-lookup"><span data-stu-id="cf165-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="cf165-121">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="cf165-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cf165-122">文本值</span><span class="sxs-lookup"><span data-stu-id="cf165-122">Text value</span></span>

<span data-ttu-id="cf165-123">无。</span><span class="sxs-lookup"><span data-stu-id="cf165-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf165-124">备注</span><span class="sxs-lookup"><span data-stu-id="cf165-124">Remarks</span></span>

<span data-ttu-id="cf165-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cf165-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf165-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="cf165-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf165-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="cf165-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cf165-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="cf165-128">Schema name</span></span>  <br/> |<span data-ttu-id="cf165-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="cf165-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="cf165-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="cf165-130">Validation file</span></span>  <br/> |<span data-ttu-id="cf165-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cf165-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cf165-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="cf165-132">Can be empty</span></span>  <br/> |<span data-ttu-id="cf165-133">False</span><span class="sxs-lookup"><span data-stu-id="cf165-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf165-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cf165-134">See also</span></span>



- [<span data-ttu-id="cf165-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cf165-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

