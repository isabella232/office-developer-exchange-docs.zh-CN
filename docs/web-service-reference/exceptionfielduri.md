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
ms.openlocfilehash: 79909405179cec0d0b86ad12bf52031e1daeb790
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754176"
---
# <a name="exceptionfielduri"></a><span data-ttu-id="175ca-104">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="175ca-104">ExceptionFieldURI</span></span>

<span data-ttu-id="175ca-105">**ExceptionFieldURI**元素标识请求中的特定错误。</span><span class="sxs-lookup"><span data-stu-id="175ca-105">The **ExceptionFieldURI** element identifies particular errors in a request.</span></span> <span data-ttu-id="175ca-106">此元素仅用作[MessageXml](messagexml.md)节点中的错误响应的一部分。</span><span class="sxs-lookup"><span data-stu-id="175ca-106">This element is only used as part of an error response in the [MessageXml](messagexml.md) node.</span></span> 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 <span data-ttu-id="175ca-107">**ExceptionPropertyURIType**</span><span class="sxs-lookup"><span data-stu-id="175ca-107">**ExceptionPropertyURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="175ca-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="175ca-108">Attributes and elements</span></span>

<span data-ttu-id="175ca-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="175ca-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="175ca-110">属性</span><span class="sxs-lookup"><span data-stu-id="175ca-110">Attributes</span></span>

|<span data-ttu-id="175ca-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="175ca-111">**Attribute**</span></span>|<span data-ttu-id="175ca-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="175ca-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="175ca-113">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="175ca-113">**FieldURI**</span></span> <br/> |<span data-ttu-id="175ca-114">标识定期项匹配项的属性。</span><span class="sxs-lookup"><span data-stu-id="175ca-114">Identifies a property of an occurrence of a recurring item.</span></span> <span data-ttu-id="175ca-115">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="175ca-115">This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="175ca-116">FieldURI 属性</span><span class="sxs-lookup"><span data-stu-id="175ca-116">FieldURI Attribute</span></span>

|<span data-ttu-id="175ca-117">**值**</span><span class="sxs-lookup"><span data-stu-id="175ca-117">**Value**</span></span>|<span data-ttu-id="175ca-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="175ca-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="175ca-119">附件： 名称</span><span class="sxs-lookup"><span data-stu-id="175ca-119">attachment:Name</span></span>  <br/> |<span data-ttu-id="175ca-120">标识为包含出错附件名称。</span><span class="sxs-lookup"><span data-stu-id="175ca-120">Identifies the attachment name as containing an error.</span></span>  <br/> |
|<span data-ttu-id="175ca-121">附件： ContentType</span><span class="sxs-lookup"><span data-stu-id="175ca-121">attachment:ContentType</span></span>  <br/> |<span data-ttu-id="175ca-122">标识为包含错误的内容类型。</span><span class="sxs-lookup"><span data-stu-id="175ca-122">Identifies the content type as containing an error.</span></span>  <br/> |
|<span data-ttu-id="175ca-123">附件： 内容</span><span class="sxs-lookup"><span data-stu-id="175ca-123">attachment:Content</span></span>  <br/> |<span data-ttu-id="175ca-124">标识为包含错误的内容。</span><span class="sxs-lookup"><span data-stu-id="175ca-124">Identifies the content as containing an error.</span></span>  <br/> |
|<span data-ttu-id="175ca-125">重复月：</span><span class="sxs-lookup"><span data-stu-id="175ca-125">recurrence:Month</span></span>  <br/> |<span data-ttu-id="175ca-126">标识为包含错误 month 字段。</span><span class="sxs-lookup"><span data-stu-id="175ca-126">Identifies the month field as containing an error.</span></span>  <br/> |
|<span data-ttu-id="175ca-127">定期： DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="175ca-127">recurrence:DayOfWeekIndex</span></span>  <br/> |<span data-ttu-id="175ca-128">标识为包含错误的周索引的天。</span><span class="sxs-lookup"><span data-stu-id="175ca-128">Identifies the day of week index as containing an error.</span></span>  <br/> |
|<span data-ttu-id="175ca-129">定期： DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="175ca-129">recurrence:DaysOfWeek</span></span>  <br/> |<span data-ttu-id="175ca-130">标识为包含错误的 DaysOfWeek 属性。</span><span class="sxs-lookup"><span data-stu-id="175ca-130">Identifies the DaysOfWeek property as containing an error.</span></span>  <br/> |
|<span data-ttu-id="175ca-131">定期： DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="175ca-131">recurrence:DayOfMonth</span></span>  <br/> |<span data-ttu-id="175ca-132">标识为包含错误 DayOfMonth。</span><span class="sxs-lookup"><span data-stu-id="175ca-132">Identifies the DayOfMonth as containing an error.</span></span>  <br/> |
|<span data-ttu-id="175ca-133">定期： 间隔</span><span class="sxs-lookup"><span data-stu-id="175ca-133">recurrence:Interval</span></span>  <br/> |<span data-ttu-id="175ca-134">标识为包含错误的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="175ca-134">Identifies the interval as containing an error.</span></span>  <br/> |
|<span data-ttu-id="175ca-135">定期： NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="175ca-135">recurrence:NumberOfOccurrences</span></span>  <br/> |<span data-ttu-id="175ca-136">标识为包含错误的次数。</span><span class="sxs-lookup"><span data-stu-id="175ca-136">Identifies the number of occurrences as containing an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="175ca-137">子元素</span><span class="sxs-lookup"><span data-stu-id="175ca-137">Child elements</span></span>

<span data-ttu-id="175ca-138">无。</span><span class="sxs-lookup"><span data-stu-id="175ca-138">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="175ca-139">父元素</span><span class="sxs-lookup"><span data-stu-id="175ca-139">Parent elements</span></span>

|<span data-ttu-id="175ca-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="175ca-140">**Element**</span></span>|<span data-ttu-id="175ca-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="175ca-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="175ca-142">MessageXml</span><span class="sxs-lookup"><span data-stu-id="175ca-142">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="175ca-143">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="175ca-143">Provides additional error response information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="175ca-144">备注</span><span class="sxs-lookup"><span data-stu-id="175ca-144">Remarks</span></span>

<span data-ttu-id="175ca-145">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="175ca-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="175ca-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="175ca-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="175ca-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="175ca-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="175ca-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="175ca-148">Schema Name</span></span>  <br/> |<span data-ttu-id="175ca-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="175ca-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="175ca-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="175ca-150">Validation File</span></span>  <br/> |<span data-ttu-id="175ca-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="175ca-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="175ca-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="175ca-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="175ca-153">False</span><span class="sxs-lookup"><span data-stu-id="175ca-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="175ca-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="175ca-154">See also</span></span>



- [<span data-ttu-id="175ca-155">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="175ca-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

