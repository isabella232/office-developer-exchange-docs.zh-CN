---
title: 名称 （邮件跟踪）
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
ms.openlocfilehash: c905df03842de47b2bcbd62897aa9a8cf464cc6d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826501"
---
# <a name="name-message-tracking"></a><span data-ttu-id="cc992-103">名称 （邮件跟踪）</span><span class="sxs-lookup"><span data-stu-id="cc992-103">Name (Message Tracking)</span></span>

<span data-ttu-id="cc992-104">**Name**元素表示邮件跟踪报告的属性名称。</span><span class="sxs-lookup"><span data-stu-id="cc992-104">The **Name** element represents the property name for a message tracking report.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="cc992-105">**字符串**</span><span class="sxs-lookup"><span data-stu-id="cc992-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cc992-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cc992-106">Attributes and elements</span></span>

<span data-ttu-id="cc992-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cc992-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc992-108">属性</span><span class="sxs-lookup"><span data-stu-id="cc992-108">Attributes</span></span>

<span data-ttu-id="cc992-109">无。</span><span class="sxs-lookup"><span data-stu-id="cc992-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc992-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cc992-110">Child elements</span></span>

<span data-ttu-id="cc992-111">无。</span><span class="sxs-lookup"><span data-stu-id="cc992-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cc992-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cc992-112">Parent elements</span></span>

|<span data-ttu-id="cc992-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cc992-113">**Element**</span></span>|<span data-ttu-id="cc992-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cc992-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc992-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="cc992-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="cc992-116">表示字符串用于创建邮件跟踪报告的属性的名称 / 值的对。</span><span class="sxs-lookup"><span data-stu-id="cc992-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cc992-117">文本值</span><span class="sxs-lookup"><span data-stu-id="cc992-117">Text value</span></span>

<span data-ttu-id="cc992-118">如果使用此元素，则需要的文本值。</span><span class="sxs-lookup"><span data-stu-id="cc992-118">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc992-119">备注</span><span class="sxs-lookup"><span data-stu-id="cc992-119">Remarks</span></span>

<span data-ttu-id="cc992-120">此元素可以发生在[TrackingPropertyType](trackingpropertytype.md)元素中最一次。</span><span class="sxs-lookup"><span data-stu-id="cc992-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="cc992-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cc992-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc992-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="cc992-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc992-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="cc992-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cc992-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="cc992-124">Schema Name</span></span>  <br/> |<span data-ttu-id="cc992-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="cc992-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="cc992-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="cc992-126">Validation File</span></span>  <br/> |<span data-ttu-id="cc992-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cc992-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cc992-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="cc992-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="cc992-129">False</span><span class="sxs-lookup"><span data-stu-id="cc992-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc992-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cc992-130">See also</span></span>

- [<span data-ttu-id="cc992-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cc992-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

