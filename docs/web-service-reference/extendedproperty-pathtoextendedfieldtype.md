---
title: ExtendedProperty (PathToExtendedFieldType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: ExtendedProperty 元素指定的统一联系人存储库的扩展的属性。
ms.openlocfilehash: 7541fa6330ee96f7791febfabc672dbcf0e95b54
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754245"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a><span data-ttu-id="94360-103">ExtendedProperty (PathToExtendedFieldType)</span><span class="sxs-lookup"><span data-stu-id="94360-103">ExtendedProperty (PathToExtendedFieldType)</span></span>

<span data-ttu-id="94360-104">**ExtendedProperty**元素指定的统一联系人存储库的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="94360-104">The **ExtendedProperty** element specifies an extended property for the Unified Contact Store.</span></span> 
  
```xml
<ExtendedProperty DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" FieldURI="">
</ExtendedProperty>
```

<span data-ttu-id="94360-105">**PathToExtendedFieldType**</span><span class="sxs-lookup"><span data-stu-id="94360-105">**PathToExtendedFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="94360-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="94360-106">Attributes and elements</span></span>

<span data-ttu-id="94360-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="94360-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94360-108">属性</span><span class="sxs-lookup"><span data-stu-id="94360-108">Attributes</span></span>

|<span data-ttu-id="94360-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="94360-109">**Attribute**</span></span>|<span data-ttu-id="94360-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="94360-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94360-111">DistinguishedPropertySetId</span><span class="sxs-lookup"><span data-stu-id="94360-111">DistinguishedPropertySetId</span></span>  <br/> |<span data-ttu-id="94360-112">指示的可分辨的属性集标识符。</span><span class="sxs-lookup"><span data-stu-id="94360-112">Indicates the distinguished property set identifier.</span></span> <span data-ttu-id="94360-113">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="94360-113">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="94360-114">PropertySetId</span><span class="sxs-lookup"><span data-stu-id="94360-114">PropertySetId</span></span>  <br/> |<span data-ttu-id="94360-115">指示 GUID 属性集标识符。</span><span class="sxs-lookup"><span data-stu-id="94360-115">Indicates the GUID property set identifier.</span></span> <span data-ttu-id="94360-116">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="94360-116">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="94360-117">PropertyTag</span><span class="sxs-lookup"><span data-stu-id="94360-117">PropertyTag</span></span>  <br/> | <span data-ttu-id="94360-118">代表减去的类型部分的属性标记。</span><span class="sxs-lookup"><span data-stu-id="94360-118">Represents the property tag minus the type part.</span></span><br/><br/><span data-ttu-id="94360-119">有两个选项的表示形式：</span><span class="sxs-lookup"><span data-stu-id="94360-119">There are two options for representation:</span></span>  <br/><br/><span data-ttu-id="94360-120">-十六进制： 0x3fa4</span><span class="sxs-lookup"><span data-stu-id="94360-120">-  Hexadecimal: 0x3fa4</span></span>  <br/><span data-ttu-id="94360-121">-Decimal: 0-65535</span><span class="sxs-lookup"><span data-stu-id="94360-121">-  Decimal: 0-65535</span></span><br/><br/>  <span data-ttu-id="94360-122">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="94360-122">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="94360-123">PropertyName</span><span class="sxs-lookup"><span data-stu-id="94360-123">PropertyName</span></span>  <br/> |<span data-ttu-id="94360-124">指示在属性名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="94360-124">String that indicates the property name.</span></span> <span data-ttu-id="94360-125">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="94360-125">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="94360-126">PropertyId</span><span class="sxs-lookup"><span data-stu-id="94360-126">PropertyId</span></span>  <br/> |<span data-ttu-id="94360-127">指示属性标识符的整数。</span><span class="sxs-lookup"><span data-stu-id="94360-127">Integer that indicates the property identifier.</span></span> <span data-ttu-id="94360-128">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="94360-128">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="94360-129">PropertyType</span><span class="sxs-lookup"><span data-stu-id="94360-129">PropertyType</span></span>  <br/> |<span data-ttu-id="94360-130">指示属性类型。</span><span class="sxs-lookup"><span data-stu-id="94360-130">Indicates the property type.</span></span> <span data-ttu-id="94360-131">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="94360-131">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="94360-132">FieldURI</span><span class="sxs-lookup"><span data-stu-id="94360-132">FieldURI</span></span>  <br/> |<span data-ttu-id="94360-133">指示字段统一资源标识符 (URI)。</span><span class="sxs-lookup"><span data-stu-id="94360-133">Indicates the field Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="94360-134">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="94360-134">This attribute is required.</span></span> <span data-ttu-id="94360-135">可能的值，请参阅[FieldURI](fielduri.md)元素。</span><span class="sxs-lookup"><span data-stu-id="94360-135">For possible values, see the [FieldURI](fielduri.md) element.</span></span>  <br/> |
   
#### <a name="distinguishedpropertysetid"></a><span data-ttu-id="94360-136">DistinguishedPropertySetId</span><span class="sxs-lookup"><span data-stu-id="94360-136">DistinguishedPropertySetId</span></span>

|<span data-ttu-id="94360-137">**值**</span><span class="sxs-lookup"><span data-stu-id="94360-137">**Value**</span></span>|<span data-ttu-id="94360-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="94360-138">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94360-139">会议</span><span class="sxs-lookup"><span data-stu-id="94360-139">Meeting</span></span>  <br/> |<span data-ttu-id="94360-140">指示会议。</span><span class="sxs-lookup"><span data-stu-id="94360-140">Indicates a meeting.</span></span>  <br/> |
|<span data-ttu-id="94360-141">Appointment</span><span class="sxs-lookup"><span data-stu-id="94360-141">Appointment</span></span>  <br/> |<span data-ttu-id="94360-142">指示约会。</span><span class="sxs-lookup"><span data-stu-id="94360-142">Indicates an appointment.</span></span>  <br/> |
|<span data-ttu-id="94360-143">Common</span><span class="sxs-lookup"><span data-stu-id="94360-143">Common</span></span>  <br/> |<span data-ttu-id="94360-144">指示常见属性集。</span><span class="sxs-lookup"><span data-stu-id="94360-144">Indicates the common property set.</span></span>  <br/> |
|<span data-ttu-id="94360-145">PublicStrings</span><span class="sxs-lookup"><span data-stu-id="94360-145">PublicStrings</span></span>  <br/> |<span data-ttu-id="94360-146">指示公用的字符串。</span><span class="sxs-lookup"><span data-stu-id="94360-146">Indicates public strings.</span></span>  <br/> |
|<span data-ttu-id="94360-147">Address</span><span class="sxs-lookup"><span data-stu-id="94360-147">Address</span></span>  <br/> |<span data-ttu-id="94360-148">指示一个地址。</span><span class="sxs-lookup"><span data-stu-id="94360-148">Indicates an address.</span></span>  <br/> |
|<span data-ttu-id="94360-149">InternetHeaders</span><span class="sxs-lookup"><span data-stu-id="94360-149">InternetHeaders</span></span>  <br/> |<span data-ttu-id="94360-150">指示 Internet 邮件头。</span><span class="sxs-lookup"><span data-stu-id="94360-150">Indicates Internet headers.</span></span>  <br/> |
|<span data-ttu-id="94360-151">CalendarAssistant</span><span class="sxs-lookup"><span data-stu-id="94360-151">CalendarAssistant</span></span>  <br/> |<span data-ttu-id="94360-152">指示日历助理。</span><span class="sxs-lookup"><span data-stu-id="94360-152">Indicates the Calendar Assistant.</span></span>  <br/> |
|<span data-ttu-id="94360-153">UnifiedMessaging</span><span class="sxs-lookup"><span data-stu-id="94360-153">UnifiedMessaging</span></span>  <br/> |<span data-ttu-id="94360-154">指示统一消息。</span><span class="sxs-lookup"><span data-stu-id="94360-154">Indicates Unified Messaging.</span></span>  <br/> |
|<span data-ttu-id="94360-155">任务</span><span class="sxs-lookup"><span data-stu-id="94360-155">Task</span></span>  <br/> |<span data-ttu-id="94360-156">表示的任务。</span><span class="sxs-lookup"><span data-stu-id="94360-156">Indicates a task.</span></span>  <br/> |
   
#### <a name="propertytype"></a><span data-ttu-id="94360-157">PropertyType</span><span class="sxs-lookup"><span data-stu-id="94360-157">PropertyType</span></span>

|<span data-ttu-id="94360-158">**值**</span><span class="sxs-lookup"><span data-stu-id="94360-158">**Value**</span></span>|<span data-ttu-id="94360-159">**说明**</span><span class="sxs-lookup"><span data-stu-id="94360-159">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94360-160">ApplicationTime</span><span class="sxs-lookup"><span data-stu-id="94360-160">ApplicationTime</span></span>  <br/> |<span data-ttu-id="94360-161">指示应用程序的时间。</span><span class="sxs-lookup"><span data-stu-id="94360-161">Indicates the application time.</span></span>  <br/> |
|<span data-ttu-id="94360-162">ApplicationTimeArray</span><span class="sxs-lookup"><span data-stu-id="94360-162">ApplicationTimeArray</span></span>  <br/> |<span data-ttu-id="94360-163">指示应用程序的时间的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-163">Indicates an array of application times.</span></span>  <br/> |
|<span data-ttu-id="94360-164">二进制</span><span class="sxs-lookup"><span data-stu-id="94360-164">Binary</span></span>  <br/> |<span data-ttu-id="94360-165">指示二进制值。</span><span class="sxs-lookup"><span data-stu-id="94360-165">Indicates a binary value.</span></span>  <br/> |
|<span data-ttu-id="94360-166">BinaryArray</span><span class="sxs-lookup"><span data-stu-id="94360-166">BinaryArray</span></span>  <br/> |<span data-ttu-id="94360-167">指示二进制值的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-167">Indicates an array of binary values.</span></span>  <br/> |
|<span data-ttu-id="94360-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="94360-168">Boolean</span></span>  <br/> |<span data-ttu-id="94360-169">指示布尔值。</span><span class="sxs-lookup"><span data-stu-id="94360-169">Indicates a Boolean value.</span></span>  <br/> |
|<span data-ttu-id="94360-170">CLSID</span><span class="sxs-lookup"><span data-stu-id="94360-170">CLSID</span></span>  <br/> |<span data-ttu-id="94360-171">指示 CLSID。</span><span class="sxs-lookup"><span data-stu-id="94360-171">Indicates a CLSID.</span></span>  <br/> |
|<span data-ttu-id="94360-172">CLSIDArray</span><span class="sxs-lookup"><span data-stu-id="94360-172">CLSIDArray</span></span>  <br/> |<span data-ttu-id="94360-173">指示 Clsid 的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-173">Indicates an array of CLSIDs.</span></span>  <br/> |
|<span data-ttu-id="94360-174">货币</span><span class="sxs-lookup"><span data-stu-id="94360-174">Currency</span></span>  <br/> |<span data-ttu-id="94360-175">表示货币值。</span><span class="sxs-lookup"><span data-stu-id="94360-175">Indicates a currency value.</span></span>  <br/> |
|<span data-ttu-id="94360-176">CurrencyArray</span><span class="sxs-lookup"><span data-stu-id="94360-176">CurrencyArray</span></span>  <br/> |<span data-ttu-id="94360-177">指示的货币值的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-177">Indicates an array of currency values.</span></span>  <br/> |
|<span data-ttu-id="94360-178">双精度数</span><span class="sxs-lookup"><span data-stu-id="94360-178">Double</span></span>  <br/> |<span data-ttu-id="94360-179">指示**双**。</span><span class="sxs-lookup"><span data-stu-id="94360-179">Indicates a **double**.</span></span>  <br/> |
|<span data-ttu-id="94360-180">DoubleArray</span><span class="sxs-lookup"><span data-stu-id="94360-180">DoubleArray</span></span>  <br/> |<span data-ttu-id="94360-181">指示**双精度**值的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-181">Indicates an array of **double** values.</span></span>  <br/> |
|<span data-ttu-id="94360-182">Error</span><span class="sxs-lookup"><span data-stu-id="94360-182">Error</span></span>  <br/> |<span data-ttu-id="94360-183">指示错误。</span><span class="sxs-lookup"><span data-stu-id="94360-183">Indicates an error.</span></span> <span data-ttu-id="94360-184">这是错误报告的目的。</span><span class="sxs-lookup"><span data-stu-id="94360-184">This is for error-reporting purposes.</span></span> <span data-ttu-id="94360-185">限制或获取或设置值不能使用它。</span><span class="sxs-lookup"><span data-stu-id="94360-185">It cannot be used in restrictions or for getting or setting values.</span></span>  <br/> |
|<span data-ttu-id="94360-186">Float</span><span class="sxs-lookup"><span data-stu-id="94360-186">Float</span></span>  <br/> |<span data-ttu-id="94360-187">指示**float**。</span><span class="sxs-lookup"><span data-stu-id="94360-187">Indicates a **float**.</span></span>  <br/> |
|<span data-ttu-id="94360-188">FloatArray</span><span class="sxs-lookup"><span data-stu-id="94360-188">FloatArray</span></span>  <br/> |<span data-ttu-id="94360-189">指示的**浮点**值的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-189">Indicates an array of **float** values.</span></span>  <br/> |
|<span data-ttu-id="94360-190">整数</span><span class="sxs-lookup"><span data-stu-id="94360-190">Integer</span></span>  <br/> |<span data-ttu-id="94360-191">指示整数。</span><span class="sxs-lookup"><span data-stu-id="94360-191">Indicates an integer.</span></span>  <br/> |
|<span data-ttu-id="94360-192">IntegerArray</span><span class="sxs-lookup"><span data-stu-id="94360-192">IntegerArray</span></span>  <br/> |<span data-ttu-id="94360-193">指示包含整数的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-193">Indicates an array of integers.</span></span>  <br/> |
|<span data-ttu-id="94360-194">Long</span><span class="sxs-lookup"><span data-stu-id="94360-194">Long</span></span>  <br/> |<span data-ttu-id="94360-195">指示**长**。</span><span class="sxs-lookup"><span data-stu-id="94360-195">Indicates a **long**.</span></span>  <br/> |
|<span data-ttu-id="94360-196">LongArray</span><span class="sxs-lookup"><span data-stu-id="94360-196">LongArray</span></span>  <br/> |<span data-ttu-id="94360-197">指示**长整型**值的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-197">Indicates an array of **long** values.</span></span>  <br/> |
|<span data-ttu-id="94360-198">Null</span><span class="sxs-lookup"><span data-stu-id="94360-198">Null</span></span>  <br/> |<span data-ttu-id="94360-199">指示空值。</span><span class="sxs-lookup"><span data-stu-id="94360-199">Indicates a null value.</span></span> <span data-ttu-id="94360-200">这是错误报告的目的。</span><span class="sxs-lookup"><span data-stu-id="94360-200">This is for error-reporting purposes.</span></span> <span data-ttu-id="94360-201">限制或获取或设置值不能使用它。</span><span class="sxs-lookup"><span data-stu-id="94360-201">It cannot be used in restrictions or for getting or setting values.</span></span>  <br/> |
|<span data-ttu-id="94360-202">对象</span><span class="sxs-lookup"><span data-stu-id="94360-202">Object</span></span>  <br/> |<span data-ttu-id="94360-203">指示一个对象。</span><span class="sxs-lookup"><span data-stu-id="94360-203">Indicates an object.</span></span> <span data-ttu-id="94360-204">这是错误报告的目的。</span><span class="sxs-lookup"><span data-stu-id="94360-204">This is for error-reporting purposes.</span></span> <span data-ttu-id="94360-205">限制或获取或设置值不能使用它。</span><span class="sxs-lookup"><span data-stu-id="94360-205">It cannot be used in restrictions or for getting or setting values.</span></span>  <br/> |
|<span data-ttu-id="94360-206">ObjectArray</span><span class="sxs-lookup"><span data-stu-id="94360-206">ObjectArray</span></span>  <br/> |<span data-ttu-id="94360-207">指示对象的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-207">Indicates an array of objects.</span></span> <span data-ttu-id="94360-208">这是错误报告的目的。</span><span class="sxs-lookup"><span data-stu-id="94360-208">This is for error-reporting purposes.</span></span> <span data-ttu-id="94360-209">限制或获取或设置值不能使用它。</span><span class="sxs-lookup"><span data-stu-id="94360-209">It cannot be used in restrictions or for getting or setting values.</span></span>  <br/> |
|<span data-ttu-id="94360-210">短</span><span class="sxs-lookup"><span data-stu-id="94360-210">Short</span></span>  <br/> |<span data-ttu-id="94360-211">指示**短**。</span><span class="sxs-lookup"><span data-stu-id="94360-211">Indicates a **short**.</span></span>  <br/> |
|<span data-ttu-id="94360-212">ShortArray</span><span class="sxs-lookup"><span data-stu-id="94360-212">ShortArray</span></span>  <br/> |<span data-ttu-id="94360-213">指示的**简短**的值的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-213">Indicates an array of **short** values.</span></span>  <br/> |
|<span data-ttu-id="94360-214">SystemTime</span><span class="sxs-lookup"><span data-stu-id="94360-214">SystemTime</span></span>  <br/> |<span data-ttu-id="94360-215">指示系统时间值。</span><span class="sxs-lookup"><span data-stu-id="94360-215">Indicates a system time value.</span></span>  <br/> |
|<span data-ttu-id="94360-216">SystemTimeArray</span><span class="sxs-lookup"><span data-stu-id="94360-216">SystemTimeArray</span></span>  <br/> |<span data-ttu-id="94360-217">指示系统时间值的数组。</span><span class="sxs-lookup"><span data-stu-id="94360-217">Indicates an array of system time values.</span></span>  <br/> |
|<span data-ttu-id="94360-218">String</span><span class="sxs-lookup"><span data-stu-id="94360-218">String</span></span>  <br/> |<span data-ttu-id="94360-219">指示字符串。</span><span class="sxs-lookup"><span data-stu-id="94360-219">Indicates a string.</span></span>  <br/> |
|<span data-ttu-id="94360-220">StringArray</span><span class="sxs-lookup"><span data-stu-id="94360-220">StringArray</span></span>  <br/> |<span data-ttu-id="94360-221">指示一个字符串数组。</span><span class="sxs-lookup"><span data-stu-id="94360-221">Indicates an array of strings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="94360-222">子元素</span><span class="sxs-lookup"><span data-stu-id="94360-222">Child elements</span></span>

<span data-ttu-id="94360-223">无。</span><span class="sxs-lookup"><span data-stu-id="94360-223">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="94360-224">父元素</span><span class="sxs-lookup"><span data-stu-id="94360-224">Parent elements</span></span>

|<span data-ttu-id="94360-225">**元素**</span><span class="sxs-lookup"><span data-stu-id="94360-225">**Element**</span></span>|<span data-ttu-id="94360-226">**说明**</span><span class="sxs-lookup"><span data-stu-id="94360-226">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94360-227">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="94360-227">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="94360-228">标识扩展的 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="94360-228">Identifies an extended MAPI property.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94360-229">备注</span><span class="sxs-lookup"><span data-stu-id="94360-229">Remarks</span></span>

<span data-ttu-id="94360-230">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="94360-230">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="94360-231">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="94360-231">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94360-232">元素信息</span><span class="sxs-lookup"><span data-stu-id="94360-232">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94360-233">命名空间</span><span class="sxs-lookup"><span data-stu-id="94360-233">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="94360-234">架构名称</span><span class="sxs-lookup"><span data-stu-id="94360-234">Schema Name</span></span>  <br/> |<span data-ttu-id="94360-235">类型架构</span><span class="sxs-lookup"><span data-stu-id="94360-235">Type schema</span></span>  <br/> |
|<span data-ttu-id="94360-236">验证文件</span><span class="sxs-lookup"><span data-stu-id="94360-236">Validation File</span></span>  <br/> |<span data-ttu-id="94360-237">types.xsd</span><span class="sxs-lookup"><span data-stu-id="94360-237">types.xsd</span></span>  <br/> |
|<span data-ttu-id="94360-238">可以为空</span><span class="sxs-lookup"><span data-stu-id="94360-238">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="94360-239">另请参阅</span><span class="sxs-lookup"><span data-stu-id="94360-239">See also</span></span>

- [<span data-ttu-id="94360-240">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="94360-240">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

