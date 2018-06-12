---
title: 值 （邮件跟踪）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: cb2f228f-775a-4c7d-82e7-41c7c953c808
description: Value 元素表示邮件跟踪报告的属性值。
ms.openlocfilehash: 152e4fe61a4cff8013ae02900bd84bf244ae84a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838508"
---
# <a name="value-message-tracking"></a><span data-ttu-id="7639c-103">值 （邮件跟踪）</span><span class="sxs-lookup"><span data-stu-id="7639c-103">Value (Message Tracking)</span></span>

<span data-ttu-id="7639c-104">**Value**元素表示邮件跟踪报告的属性值。</span><span class="sxs-lookup"><span data-stu-id="7639c-104">The **Value** element represents the property value for a message tracking report.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="7639c-105">**字符串**</span><span class="sxs-lookup"><span data-stu-id="7639c-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7639c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7639c-106">Attributes and elements</span></span>

<span data-ttu-id="7639c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7639c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7639c-108">属性</span><span class="sxs-lookup"><span data-stu-id="7639c-108">Attributes</span></span>

<span data-ttu-id="7639c-109">无。</span><span class="sxs-lookup"><span data-stu-id="7639c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7639c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7639c-110">Child elements</span></span>

<span data-ttu-id="7639c-111">无。</span><span class="sxs-lookup"><span data-stu-id="7639c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7639c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7639c-112">Parent elements</span></span>

|<span data-ttu-id="7639c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7639c-113">**Element**</span></span>|<span data-ttu-id="7639c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7639c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7639c-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="7639c-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="7639c-116">表示字符串用于创建邮件跟踪报告的属性的名称 / 值的对。</span><span class="sxs-lookup"><span data-stu-id="7639c-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7639c-117">文本值</span><span class="sxs-lookup"><span data-stu-id="7639c-117">Text value</span></span>

<span data-ttu-id="7639c-118">文本值是可选的。</span><span class="sxs-lookup"><span data-stu-id="7639c-118">The text value is optional.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7639c-119">备注</span><span class="sxs-lookup"><span data-stu-id="7639c-119">Remarks</span></span>

<span data-ttu-id="7639c-120">此元素可以发生在[TrackingPropertyType](trackingpropertytype.md)元素中最一次。</span><span class="sxs-lookup"><span data-stu-id="7639c-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="7639c-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7639c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7639c-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="7639c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7639c-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="7639c-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7639c-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="7639c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7639c-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="7639c-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="7639c-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="7639c-126">Validation File</span></span>  <br/> |<span data-ttu-id="7639c-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7639c-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7639c-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="7639c-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="7639c-129">False</span><span class="sxs-lookup"><span data-stu-id="7639c-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7639c-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7639c-130">See also</span></span>

- [<span data-ttu-id="7639c-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7639c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

