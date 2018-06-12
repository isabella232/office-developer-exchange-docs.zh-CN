---
title: EventData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventData
api_type:
- schema
ms.assetid: 74acdbad-d6ee-47e6-82fb-e45ecaaa0500
description: EventData 元素表示相关联的事件的处理步骤的数据。
ms.openlocfilehash: 2bf38cd4fd956580b31b6e455b947066f07f5593
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754163"
---
# <a name="eventdata"></a><span data-ttu-id="dadec-103">EventData</span><span class="sxs-lookup"><span data-stu-id="dadec-103">EventData</span></span>

<span data-ttu-id="dadec-104">**EventData**元素表示相关联的事件的处理步骤的数据。</span><span class="sxs-lookup"><span data-stu-id="dadec-104">The **EventData** element represents data that is associated with the processing step for the event.</span></span> 
  
```XML
<EventData>
   <String/>
</EventData>
```

 <span data-ttu-id="dadec-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="dadec-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dadec-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dadec-106">Attributes and elements</span></span>

<span data-ttu-id="dadec-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dadec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dadec-108">属性</span><span class="sxs-lookup"><span data-stu-id="dadec-108">Attributes</span></span>

<span data-ttu-id="dadec-109">无。</span><span class="sxs-lookup"><span data-stu-id="dadec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dadec-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dadec-110">Child elements</span></span>

|<span data-ttu-id="dadec-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="dadec-111">**Element**</span></span>|<span data-ttu-id="dadec-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="dadec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dadec-113">字符串</span><span class="sxs-lookup"><span data-stu-id="dadec-113">String</span></span>](string.md) <br/> |<span data-ttu-id="dadec-114">包含一个字符串，标识事件。</span><span class="sxs-lookup"><span data-stu-id="dadec-114">Contains a string that identifies an event.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dadec-115">父元素</span><span class="sxs-lookup"><span data-stu-id="dadec-115">Parent elements</span></span>

|<span data-ttu-id="dadec-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="dadec-116">**Element**</span></span>|<span data-ttu-id="dadec-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="dadec-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dadec-118">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="dadec-118">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="dadec-119">包含收件人为一个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="dadec-119">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dadec-120">文本值</span><span class="sxs-lookup"><span data-stu-id="dadec-120">Text value</span></span>

<span data-ttu-id="dadec-121">无。</span><span class="sxs-lookup"><span data-stu-id="dadec-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dadec-122">备注</span><span class="sxs-lookup"><span data-stu-id="dadec-122">Remarks</span></span>

<span data-ttu-id="dadec-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dadec-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dadec-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="dadec-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dadec-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="dadec-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dadec-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="dadec-126">Schema Name</span></span>  <br/> |<span data-ttu-id="dadec-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="dadec-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="dadec-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="dadec-128">Validation File</span></span>  <br/> |<span data-ttu-id="dadec-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dadec-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dadec-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="dadec-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="dadec-131">False</span><span class="sxs-lookup"><span data-stu-id="dadec-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dadec-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dadec-132">See also</span></span>



- [<span data-ttu-id="dadec-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dadec-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

