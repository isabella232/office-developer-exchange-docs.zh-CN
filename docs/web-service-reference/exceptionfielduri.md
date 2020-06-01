---
title: ExceptionFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: ExceptionFieldURI 元素标识请求中的特定错误。 此元素仅用作 MessageXml 节点中的错误响应的一部分。
ms.openlocfilehash: a47d44098f85d8bacb1e7a2c48a33e478e56c7ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454342"
---
# <a name="exceptionfielduri"></a><span data-ttu-id="22f86-104">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="22f86-104">ExceptionFieldURI</span></span>

<span data-ttu-id="22f86-105">**ExceptionFieldURI**元素标识请求中的特定错误。</span><span class="sxs-lookup"><span data-stu-id="22f86-105">The **ExceptionFieldURI** element identifies particular errors in a request.</span></span> <span data-ttu-id="22f86-106">此元素仅用作[MessageXml](messagexml.md)节点中的错误响应的一部分。</span><span class="sxs-lookup"><span data-stu-id="22f86-106">This element is only used as part of an error response in the [MessageXml](messagexml.md) node.</span></span> 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 <span data-ttu-id="22f86-107">**ExceptionPropertyURIType**</span><span class="sxs-lookup"><span data-stu-id="22f86-107">**ExceptionPropertyURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22f86-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22f86-108">Attributes and elements</span></span>

<span data-ttu-id="22f86-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22f86-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22f86-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="22f86-110">Attributes</span></span>

|<span data-ttu-id="22f86-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="22f86-111">**Attribute**</span></span>|<span data-ttu-id="22f86-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="22f86-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22f86-113">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="22f86-113">**FieldURI**</span></span> <br/> |<span data-ttu-id="22f86-114">标识定期项目的事件的属性。</span><span class="sxs-lookup"><span data-stu-id="22f86-114">Identifies a property of an occurrence of a recurring item.</span></span> <span data-ttu-id="22f86-115">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="22f86-115">This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="22f86-116">FieldURI 属性</span><span class="sxs-lookup"><span data-stu-id="22f86-116">FieldURI Attribute</span></span>

|<span data-ttu-id="22f86-117">**值**</span><span class="sxs-lookup"><span data-stu-id="22f86-117">**Value**</span></span>|<span data-ttu-id="22f86-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="22f86-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22f86-119">附件：名称</span><span class="sxs-lookup"><span data-stu-id="22f86-119">attachment:Name</span></span>  <br/> |<span data-ttu-id="22f86-120">将附件名称标识为包含错误。</span><span class="sxs-lookup"><span data-stu-id="22f86-120">Identifies the attachment name as containing an error.</span></span>  <br/> |
|<span data-ttu-id="22f86-121">附件： ContentType</span><span class="sxs-lookup"><span data-stu-id="22f86-121">attachment:ContentType</span></span>  <br/> |<span data-ttu-id="22f86-122">将内容类型标识为包含一个错误。</span><span class="sxs-lookup"><span data-stu-id="22f86-122">Identifies the content type as containing an error.</span></span>  <br/> |
|<span data-ttu-id="22f86-123">附件：内容</span><span class="sxs-lookup"><span data-stu-id="22f86-123">attachment:Content</span></span>  <br/> |<span data-ttu-id="22f86-124">将内容标识为包含错误。</span><span class="sxs-lookup"><span data-stu-id="22f86-124">Identifies the content as containing an error.</span></span>  <br/> |
|<span data-ttu-id="22f86-125">重复周期：月</span><span class="sxs-lookup"><span data-stu-id="22f86-125">recurrence:Month</span></span>  <br/> |<span data-ttu-id="22f86-126">将 "月份" 字段标识为包含错误。</span><span class="sxs-lookup"><span data-stu-id="22f86-126">Identifies the month field as containing an error.</span></span>  <br/> |
|<span data-ttu-id="22f86-127">重复周期： DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="22f86-127">recurrence:DayOfWeekIndex</span></span>  <br/> |<span data-ttu-id="22f86-128">将星期索引的日期标识为包含错误。</span><span class="sxs-lookup"><span data-stu-id="22f86-128">Identifies the day of week index as containing an error.</span></span>  <br/> |
|<span data-ttu-id="22f86-129">重复周期： DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="22f86-129">recurrence:DaysOfWeek</span></span>  <br/> |<span data-ttu-id="22f86-130">将 DaysOfWeek 属性标识为包含一个错误。</span><span class="sxs-lookup"><span data-stu-id="22f86-130">Identifies the DaysOfWeek property as containing an error.</span></span>  <br/> |
|<span data-ttu-id="22f86-131">重复周期： DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="22f86-131">recurrence:DayOfMonth</span></span>  <br/> |<span data-ttu-id="22f86-132">将 DayOfMonth 标识为包含错误。</span><span class="sxs-lookup"><span data-stu-id="22f86-132">Identifies the DayOfMonth as containing an error.</span></span>  <br/> |
|<span data-ttu-id="22f86-133">重复周期：间隔</span><span class="sxs-lookup"><span data-stu-id="22f86-133">recurrence:Interval</span></span>  <br/> |<span data-ttu-id="22f86-134">标识包含错误的间隔。</span><span class="sxs-lookup"><span data-stu-id="22f86-134">Identifies the interval as containing an error.</span></span>  <br/> |
|<span data-ttu-id="22f86-135">重复周期： NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="22f86-135">recurrence:NumberOfOccurrences</span></span>  <br/> |<span data-ttu-id="22f86-136">将发生次数标识为包含错误。</span><span class="sxs-lookup"><span data-stu-id="22f86-136">Identifies the number of occurrences as containing an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="22f86-137">子元素</span><span class="sxs-lookup"><span data-stu-id="22f86-137">Child elements</span></span>

<span data-ttu-id="22f86-138">无。</span><span class="sxs-lookup"><span data-stu-id="22f86-138">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="22f86-139">父元素</span><span class="sxs-lookup"><span data-stu-id="22f86-139">Parent elements</span></span>

|<span data-ttu-id="22f86-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="22f86-140">**Element**</span></span>|<span data-ttu-id="22f86-141">**描述**</span><span class="sxs-lookup"><span data-stu-id="22f86-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22f86-142">MessageXml</span><span class="sxs-lookup"><span data-stu-id="22f86-142">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="22f86-143">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="22f86-143">Provides additional error response information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22f86-144">说明</span><span class="sxs-lookup"><span data-stu-id="22f86-144">Remarks</span></span>

<span data-ttu-id="22f86-145">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22f86-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22f86-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="22f86-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22f86-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="22f86-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22f86-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="22f86-148">Schema Name</span></span>  <br/> |<span data-ttu-id="22f86-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="22f86-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="22f86-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="22f86-150">Validation File</span></span>  <br/> |<span data-ttu-id="22f86-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="22f86-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="22f86-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="22f86-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="22f86-153">False</span><span class="sxs-lookup"><span data-stu-id="22f86-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22f86-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="22f86-154">See also</span></span>



- [<span data-ttu-id="22f86-155">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="22f86-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

