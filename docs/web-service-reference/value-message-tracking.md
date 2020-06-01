---
title: 值（邮件跟踪）
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
ms.openlocfilehash: 4f6b5cb9d82a35bbe010b36e409cdc9f3a70173d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465006"
---
# <a name="value-message-tracking"></a><span data-ttu-id="ff075-103">值（邮件跟踪）</span><span class="sxs-lookup"><span data-stu-id="ff075-103">Value (Message Tracking)</span></span>

<span data-ttu-id="ff075-104">**Value**元素表示邮件跟踪报告的属性值。</span><span class="sxs-lookup"><span data-stu-id="ff075-104">The **Value** element represents the property value for a message tracking report.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="ff075-105">**String**</span><span class="sxs-lookup"><span data-stu-id="ff075-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ff075-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ff075-106">Attributes and elements</span></span>

<span data-ttu-id="ff075-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ff075-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff075-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ff075-108">Attributes</span></span>

<span data-ttu-id="ff075-109">无。</span><span class="sxs-lookup"><span data-stu-id="ff075-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff075-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ff075-110">Child elements</span></span>

<span data-ttu-id="ff075-111">无。</span><span class="sxs-lookup"><span data-stu-id="ff075-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ff075-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ff075-112">Parent elements</span></span>

|<span data-ttu-id="ff075-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ff075-113">**Element**</span></span>|<span data-ttu-id="ff075-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ff075-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff075-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="ff075-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="ff075-116">表示用于创建邮件跟踪报告的属性的字符串的名称和值对。</span><span class="sxs-lookup"><span data-stu-id="ff075-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ff075-117">文本值</span><span class="sxs-lookup"><span data-stu-id="ff075-117">Text value</span></span>

<span data-ttu-id="ff075-118">文本值是可选的。</span><span class="sxs-lookup"><span data-stu-id="ff075-118">The text value is optional.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff075-119">备注</span><span class="sxs-lookup"><span data-stu-id="ff075-119">Remarks</span></span>

<span data-ttu-id="ff075-120">此元素最多可在[TrackingPropertyType](trackingpropertytype.md)元素中出现一次。</span><span class="sxs-lookup"><span data-stu-id="ff075-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="ff075-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ff075-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff075-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="ff075-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff075-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="ff075-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ff075-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="ff075-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ff075-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="ff075-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ff075-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="ff075-126">Validation File</span></span>  <br/> |<span data-ttu-id="ff075-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ff075-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ff075-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="ff075-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff075-129">False</span><span class="sxs-lookup"><span data-stu-id="ff075-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff075-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ff075-130">See also</span></span>

- [<span data-ttu-id="ff075-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ff075-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

