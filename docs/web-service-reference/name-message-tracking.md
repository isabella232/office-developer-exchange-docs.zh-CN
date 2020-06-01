---
title: 名称（邮件跟踪）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: a1669f6d-53f3-4849-9b30-56909aaeac82
description: Name 元素表示邮件跟踪报告的属性名称。
ms.openlocfilehash: 86f049c0a90dbeb55418a5eee58079adf17e5ded
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466897"
---
# <a name="name-message-tracking"></a><span data-ttu-id="3a674-103">名称（邮件跟踪）</span><span class="sxs-lookup"><span data-stu-id="3a674-103">Name (Message Tracking)</span></span>

<span data-ttu-id="3a674-104">**Name**元素表示邮件跟踪报告的属性名称。</span><span class="sxs-lookup"><span data-stu-id="3a674-104">The **Name** element represents the property name for a message tracking report.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="3a674-105">**String**</span><span class="sxs-lookup"><span data-stu-id="3a674-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3a674-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3a674-106">Attributes and elements</span></span>

<span data-ttu-id="3a674-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3a674-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a674-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3a674-108">Attributes</span></span>

<span data-ttu-id="3a674-109">无。</span><span class="sxs-lookup"><span data-stu-id="3a674-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a674-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3a674-110">Child elements</span></span>

<span data-ttu-id="3a674-111">无。</span><span class="sxs-lookup"><span data-stu-id="3a674-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3a674-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3a674-112">Parent elements</span></span>

|<span data-ttu-id="3a674-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3a674-113">**Element**</span></span>|<span data-ttu-id="3a674-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3a674-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a674-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="3a674-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="3a674-116">表示用于创建邮件跟踪报告的属性的字符串的名称和值对。</span><span class="sxs-lookup"><span data-stu-id="3a674-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a674-117">文本值</span><span class="sxs-lookup"><span data-stu-id="3a674-117">Text value</span></span>

<span data-ttu-id="3a674-118">如果使用此元素，则需要一个 text 值。</span><span class="sxs-lookup"><span data-stu-id="3a674-118">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a674-119">备注</span><span class="sxs-lookup"><span data-stu-id="3a674-119">Remarks</span></span>

<span data-ttu-id="3a674-120">此元素最多可在[TrackingPropertyType](trackingpropertytype.md)元素中出现一次。</span><span class="sxs-lookup"><span data-stu-id="3a674-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="3a674-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3a674-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a674-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="3a674-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a674-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="3a674-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a674-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="3a674-124">Schema Name</span></span>  <br/> |<span data-ttu-id="3a674-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="3a674-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="3a674-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="3a674-126">Validation File</span></span>  <br/> |<span data-ttu-id="3a674-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3a674-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a674-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="3a674-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a674-129">False</span><span class="sxs-lookup"><span data-stu-id="3a674-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a674-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a674-130">See also</span></span>

- [<span data-ttu-id="3a674-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3a674-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

