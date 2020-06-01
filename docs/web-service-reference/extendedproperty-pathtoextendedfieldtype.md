---
title: ExtendedProperty （PathToExtendedFieldType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: ExtendedProperty 元素指定统一联系人存储区的扩展属性。
ms.openlocfilehash: f6c283d5cce3bc927662ad0d9c796c0589e7054c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460139"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a><span data-ttu-id="148de-103">ExtendedProperty （PathToExtendedFieldType）</span><span class="sxs-lookup"><span data-stu-id="148de-103">ExtendedProperty (PathToExtendedFieldType)</span></span>

<span data-ttu-id="148de-104">**ExtendedProperty**元素指定统一联系人存储区的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="148de-104">The **ExtendedProperty** element specifies an extended property for the Unified Contact Store.</span></span> 
  
```xml
<ExtendedProperty DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" FieldURI="">
</ExtendedProperty>
```

<span data-ttu-id="148de-105">**PathToExtendedFieldType**</span><span class="sxs-lookup"><span data-stu-id="148de-105">**PathToExtendedFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="148de-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="148de-106">Attributes and elements</span></span>

<span data-ttu-id="148de-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="148de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="148de-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="148de-108">Attributes</span></span>

|<span data-ttu-id="148de-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="148de-109">**Attribute**</span></span>|<span data-ttu-id="148de-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="148de-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="148de-111">DistinguishedPropertySetId</span><span class="sxs-lookup"><span data-stu-id="148de-111">DistinguishedPropertySetId</span></span>  <br/> |<span data-ttu-id="148de-112">指示可分辨属性集标识符。</span><span class="sxs-lookup"><span data-stu-id="148de-112">Indicates the distinguished property set identifier.</span></span> <span data-ttu-id="148de-113">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="148de-113">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="148de-114">PropertySetId</span><span class="sxs-lookup"><span data-stu-id="148de-114">PropertySetId</span></span>  <br/> |<span data-ttu-id="148de-115">指示 GUID 属性集标识符。</span><span class="sxs-lookup"><span data-stu-id="148de-115">Indicates the GUID property set identifier.</span></span> <span data-ttu-id="148de-116">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="148de-116">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="148de-117">PropertyTag</span><span class="sxs-lookup"><span data-stu-id="148de-117">PropertyTag</span></span>  <br/> | <span data-ttu-id="148de-118">表示属性标记减去类型部分。</span><span class="sxs-lookup"><span data-stu-id="148de-118">Represents the property tag minus the type part.</span></span><br/><br/><span data-ttu-id="148de-119">有两种方法可供选择：</span><span class="sxs-lookup"><span data-stu-id="148de-119">There are two options for representation:</span></span>  <br/><br/><span data-ttu-id="148de-120">-十六进制：0x3fa4</span><span class="sxs-lookup"><span data-stu-id="148de-120">-  Hexadecimal: 0x3fa4</span></span>  <br/><span data-ttu-id="148de-121">-十进制：0-65535</span><span class="sxs-lookup"><span data-stu-id="148de-121">-  Decimal: 0-65535</span></span><br/><br/>  <span data-ttu-id="148de-122">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="148de-122">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="148de-123">PropertyName</span><span class="sxs-lookup"><span data-stu-id="148de-123">PropertyName</span></span>  <br/> |<span data-ttu-id="148de-124">指示属性名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="148de-124">String that indicates the property name.</span></span> <span data-ttu-id="148de-125">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="148de-125">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="148de-126">PropertyId</span><span class="sxs-lookup"><span data-stu-id="148de-126">PropertyId</span></span>  <br/> |<span data-ttu-id="148de-127">指示属性标识符的整数。</span><span class="sxs-lookup"><span data-stu-id="148de-127">Integer that indicates the property identifier.</span></span> <span data-ttu-id="148de-128">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="148de-128">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="148de-129">Recordtype</span><span class="sxs-lookup"><span data-stu-id="148de-129">PropertyType</span></span>  <br/> |<span data-ttu-id="148de-130">指示属性类型。</span><span class="sxs-lookup"><span data-stu-id="148de-130">Indicates the property type.</span></span> <span data-ttu-id="148de-131">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="148de-131">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="148de-132">FieldURI</span><span class="sxs-lookup"><span data-stu-id="148de-132">FieldURI</span></span>  <br/> |<span data-ttu-id="148de-133">指示字段统一资源标识符（URI）。</span><span class="sxs-lookup"><span data-stu-id="148de-133">Indicates the field Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="148de-134">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="148de-134">This attribute is required.</span></span> <span data-ttu-id="148de-135">有关可能的值，请参阅[FieldURI](fielduri.md)元素。</span><span class="sxs-lookup"><span data-stu-id="148de-135">For possible values, see the [FieldURI](fielduri.md) element.</span></span>  <br/> |
   
#### <a name="distinguishedpropertysetid"></a><span data-ttu-id="148de-136">DistinguishedPropertySetId</span><span class="sxs-lookup"><span data-stu-id="148de-136">DistinguishedPropertySetId</span></span>

|<span data-ttu-id="148de-137">**值**</span><span class="sxs-lookup"><span data-stu-id="148de-137">**Value**</span></span>|<span data-ttu-id="148de-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="148de-138">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="148de-139">要求</span><span class="sxs-lookup"><span data-stu-id="148de-139">Meeting</span></span>  <br/> |<span data-ttu-id="148de-140">表示会议。</span><span class="sxs-lookup"><span data-stu-id="148de-140">Indicates a meeting.</span></span>  <br/> |
|<span data-ttu-id="148de-141">Appointment</span><span class="sxs-lookup"><span data-stu-id="148de-141">Appointment</span></span>  <br/> |<span data-ttu-id="148de-142">指示约会。</span><span class="sxs-lookup"><span data-stu-id="148de-142">Indicates an appointment.</span></span>  <br/> |
|<span data-ttu-id="148de-143">常见</span><span class="sxs-lookup"><span data-stu-id="148de-143">Common</span></span>  <br/> |<span data-ttu-id="148de-144">指示通用属性集。</span><span class="sxs-lookup"><span data-stu-id="148de-144">Indicates the common property set.</span></span>  <br/> |
|<span data-ttu-id="148de-145">PublicStrings</span><span class="sxs-lookup"><span data-stu-id="148de-145">PublicStrings</span></span>  <br/> |<span data-ttu-id="148de-146">指示公共字符串。</span><span class="sxs-lookup"><span data-stu-id="148de-146">Indicates public strings.</span></span>  <br/> |
|<span data-ttu-id="148de-147">地址</span><span class="sxs-lookup"><span data-stu-id="148de-147">Address</span></span>  <br/> |<span data-ttu-id="148de-148">指示地址。</span><span class="sxs-lookup"><span data-stu-id="148de-148">Indicates an address.</span></span>  <br/> |
|<span data-ttu-id="148de-149">InternetHeaders</span><span class="sxs-lookup"><span data-stu-id="148de-149">InternetHeaders</span></span>  <br/> |<span data-ttu-id="148de-150">指示 Internet 标头。</span><span class="sxs-lookup"><span data-stu-id="148de-150">Indicates Internet headers.</span></span>  <br/> |
|<span data-ttu-id="148de-151">CalendarAssistant</span><span class="sxs-lookup"><span data-stu-id="148de-151">CalendarAssistant</span></span>  <br/> |<span data-ttu-id="148de-152">指示日历助理。</span><span class="sxs-lookup"><span data-stu-id="148de-152">Indicates the Calendar Assistant.</span></span>  <br/> |
|<span data-ttu-id="148de-153">UnifiedMessaging</span><span class="sxs-lookup"><span data-stu-id="148de-153">UnifiedMessaging</span></span>  <br/> |<span data-ttu-id="148de-154">指示统一消息。</span><span class="sxs-lookup"><span data-stu-id="148de-154">Indicates Unified Messaging.</span></span>  <br/> |
|<span data-ttu-id="148de-155">任务</span><span class="sxs-lookup"><span data-stu-id="148de-155">Task</span></span>  <br/> |<span data-ttu-id="148de-156">指示任务。</span><span class="sxs-lookup"><span data-stu-id="148de-156">Indicates a task.</span></span>  <br/> |
   
#### <a name="propertytype"></a><span data-ttu-id="148de-157">Recordtype</span><span class="sxs-lookup"><span data-stu-id="148de-157">PropertyType</span></span>

|<span data-ttu-id="148de-158">**值**</span><span class="sxs-lookup"><span data-stu-id="148de-158">**Value**</span></span>|<span data-ttu-id="148de-159">**说明**</span><span class="sxs-lookup"><span data-stu-id="148de-159">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="148de-160">ApplicationTime</span><span class="sxs-lookup"><span data-stu-id="148de-160">ApplicationTime</span></span>  <br/> |<span data-ttu-id="148de-161">指示应用程序的时间。</span><span class="sxs-lookup"><span data-stu-id="148de-161">Indicates the application time.</span></span>  <br/> |
|<span data-ttu-id="148de-162">ApplicationTimeArray</span><span class="sxs-lookup"><span data-stu-id="148de-162">ApplicationTimeArray</span></span>  <br/> |<span data-ttu-id="148de-163">指示应用程序的时间数组。</span><span class="sxs-lookup"><span data-stu-id="148de-163">Indicates an array of application times.</span></span>  <br/> |
|<span data-ttu-id="148de-164">Binary</span><span class="sxs-lookup"><span data-stu-id="148de-164">Binary</span></span>  <br/> |<span data-ttu-id="148de-165">指示二进制值。</span><span class="sxs-lookup"><span data-stu-id="148de-165">Indicates a binary value.</span></span>  <br/> |
|<span data-ttu-id="148de-166">BinaryArray</span><span class="sxs-lookup"><span data-stu-id="148de-166">BinaryArray</span></span>  <br/> |<span data-ttu-id="148de-167">指示二进制值数组。</span><span class="sxs-lookup"><span data-stu-id="148de-167">Indicates an array of binary values.</span></span>  <br/> |
|<span data-ttu-id="148de-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="148de-168">Boolean</span></span>  <br/> |<span data-ttu-id="148de-169">指示布尔值。</span><span class="sxs-lookup"><span data-stu-id="148de-169">Indicates a Boolean value.</span></span>  <br/> |
|<span data-ttu-id="148de-170">CLSID</span><span class="sxs-lookup"><span data-stu-id="148de-170">CLSID</span></span>  <br/> |<span data-ttu-id="148de-171">指示 CLSID。</span><span class="sxs-lookup"><span data-stu-id="148de-171">Indicates a CLSID.</span></span>  <br/> |
|<span data-ttu-id="148de-172">CLSIDArray</span><span class="sxs-lookup"><span data-stu-id="148de-172">CLSIDArray</span></span>  <br/> |<span data-ttu-id="148de-173">指示一个 Clsid 数组。</span><span class="sxs-lookup"><span data-stu-id="148de-173">Indicates an array of CLSIDs.</span></span>  <br/> |
|<span data-ttu-id="148de-174">货币</span><span class="sxs-lookup"><span data-stu-id="148de-174">Currency</span></span>  <br/> |<span data-ttu-id="148de-175">指示货币值。</span><span class="sxs-lookup"><span data-stu-id="148de-175">Indicates a currency value.</span></span>  <br/> |
|<span data-ttu-id="148de-176">CurrencyArray</span><span class="sxs-lookup"><span data-stu-id="148de-176">CurrencyArray</span></span>  <br/> |<span data-ttu-id="148de-177">指示货币值的数组。</span><span class="sxs-lookup"><span data-stu-id="148de-177">Indicates an array of currency values.</span></span>  <br/> |
|<span data-ttu-id="148de-178">双精度</span><span class="sxs-lookup"><span data-stu-id="148de-178">Double</span></span>  <br/> |<span data-ttu-id="148de-179">指示**双精度型**。</span><span class="sxs-lookup"><span data-stu-id="148de-179">Indicates a **double**.</span></span>  <br/> |
|<span data-ttu-id="148de-180">DoubleArray</span><span class="sxs-lookup"><span data-stu-id="148de-180">DoubleArray</span></span>  <br/> |<span data-ttu-id="148de-181">指示**双精度**值的数组。</span><span class="sxs-lookup"><span data-stu-id="148de-181">Indicates an array of **double** values.</span></span>  <br/> |
|<span data-ttu-id="148de-182">错误</span><span class="sxs-lookup"><span data-stu-id="148de-182">Error</span></span>  <br/> |<span data-ttu-id="148de-183">指示错误。</span><span class="sxs-lookup"><span data-stu-id="148de-183">Indicates an error.</span></span> <span data-ttu-id="148de-184">这是出于错误报告目的。</span><span class="sxs-lookup"><span data-stu-id="148de-184">This is for error-reporting purposes.</span></span> <span data-ttu-id="148de-185">它不能在限制中使用，也不能用于获取或设置值。</span><span class="sxs-lookup"><span data-stu-id="148de-185">It cannot be used in restrictions or for getting or setting values.</span></span>  <br/> |
|<span data-ttu-id="148de-186">浮点</span><span class="sxs-lookup"><span data-stu-id="148de-186">Float</span></span>  <br/> |<span data-ttu-id="148de-187">指示**float**。</span><span class="sxs-lookup"><span data-stu-id="148de-187">Indicates a **float**.</span></span>  <br/> |
|<span data-ttu-id="148de-188">FloatArray</span><span class="sxs-lookup"><span data-stu-id="148de-188">FloatArray</span></span>  <br/> |<span data-ttu-id="148de-189">指示**float**值数组。</span><span class="sxs-lookup"><span data-stu-id="148de-189">Indicates an array of **float** values.</span></span>  <br/> |
|<span data-ttu-id="148de-190">Integer</span><span class="sxs-lookup"><span data-stu-id="148de-190">Integer</span></span>  <br/> |<span data-ttu-id="148de-191">指示一个整数。</span><span class="sxs-lookup"><span data-stu-id="148de-191">Indicates an integer.</span></span>  <br/> |
|<span data-ttu-id="148de-192">IntegerArray</span><span class="sxs-lookup"><span data-stu-id="148de-192">IntegerArray</span></span>  <br/> |<span data-ttu-id="148de-193">指示一个整数数组。</span><span class="sxs-lookup"><span data-stu-id="148de-193">Indicates an array of integers.</span></span>  <br/> |
|<span data-ttu-id="148de-194">长型</span><span class="sxs-lookup"><span data-stu-id="148de-194">Long</span></span>  <br/> |<span data-ttu-id="148de-195">指示**长**。</span><span class="sxs-lookup"><span data-stu-id="148de-195">Indicates a **long**.</span></span>  <br/> |
|<span data-ttu-id="148de-196">LongArray</span><span class="sxs-lookup"><span data-stu-id="148de-196">LongArray</span></span>  <br/> |<span data-ttu-id="148de-197">指示**long**值的数组。</span><span class="sxs-lookup"><span data-stu-id="148de-197">Indicates an array of **long** values.</span></span>  <br/> |
|<span data-ttu-id="148de-198">NULL</span><span class="sxs-lookup"><span data-stu-id="148de-198">Null</span></span>  <br/> |<span data-ttu-id="148de-199">指示 null 值。</span><span class="sxs-lookup"><span data-stu-id="148de-199">Indicates a null value.</span></span> <span data-ttu-id="148de-200">这是出于错误报告目的。</span><span class="sxs-lookup"><span data-stu-id="148de-200">This is for error-reporting purposes.</span></span> <span data-ttu-id="148de-201">它不能在限制中使用，也不能用于获取或设置值。</span><span class="sxs-lookup"><span data-stu-id="148de-201">It cannot be used in restrictions or for getting or setting values.</span></span>  <br/> |
|<span data-ttu-id="148de-202">对象</span><span class="sxs-lookup"><span data-stu-id="148de-202">Object</span></span>  <br/> |<span data-ttu-id="148de-203">指示对象。</span><span class="sxs-lookup"><span data-stu-id="148de-203">Indicates an object.</span></span> <span data-ttu-id="148de-204">这是出于错误报告目的。</span><span class="sxs-lookup"><span data-stu-id="148de-204">This is for error-reporting purposes.</span></span> <span data-ttu-id="148de-205">它不能在限制中使用，也不能用于获取或设置值。</span><span class="sxs-lookup"><span data-stu-id="148de-205">It cannot be used in restrictions or for getting or setting values.</span></span>  <br/> |
|<span data-ttu-id="148de-206">ObjectArray</span><span class="sxs-lookup"><span data-stu-id="148de-206">ObjectArray</span></span>  <br/> |<span data-ttu-id="148de-207">指示对象的数组。</span><span class="sxs-lookup"><span data-stu-id="148de-207">Indicates an array of objects.</span></span> <span data-ttu-id="148de-208">这是出于错误报告目的。</span><span class="sxs-lookup"><span data-stu-id="148de-208">This is for error-reporting purposes.</span></span> <span data-ttu-id="148de-209">它不能在限制中使用，也不能用于获取或设置值。</span><span class="sxs-lookup"><span data-stu-id="148de-209">It cannot be used in restrictions or for getting or setting values.</span></span>  <br/> |
|<span data-ttu-id="148de-210">短</span><span class="sxs-lookup"><span data-stu-id="148de-210">Short</span></span>  <br/> |<span data-ttu-id="148de-211">指示**短整型**。</span><span class="sxs-lookup"><span data-stu-id="148de-211">Indicates a **short**.</span></span>  <br/> |
|<span data-ttu-id="148de-212">ShortArray</span><span class="sxs-lookup"><span data-stu-id="148de-212">ShortArray</span></span>  <br/> |<span data-ttu-id="148de-213">指示一个**短**值数组。</span><span class="sxs-lookup"><span data-stu-id="148de-213">Indicates an array of **short** values.</span></span>  <br/> |
|<span data-ttu-id="148de-214">SystemTime</span><span class="sxs-lookup"><span data-stu-id="148de-214">SystemTime</span></span>  <br/> |<span data-ttu-id="148de-215">指示系统时间值。</span><span class="sxs-lookup"><span data-stu-id="148de-215">Indicates a system time value.</span></span>  <br/> |
|<span data-ttu-id="148de-216">SystemTimeArray</span><span class="sxs-lookup"><span data-stu-id="148de-216">SystemTimeArray</span></span>  <br/> |<span data-ttu-id="148de-217">指示系统时间值的数组。</span><span class="sxs-lookup"><span data-stu-id="148de-217">Indicates an array of system time values.</span></span>  <br/> |
|<span data-ttu-id="148de-218">String</span><span class="sxs-lookup"><span data-stu-id="148de-218">String</span></span>  <br/> |<span data-ttu-id="148de-219">指示字符串。</span><span class="sxs-lookup"><span data-stu-id="148de-219">Indicates a string.</span></span>  <br/> |
|<span data-ttu-id="148de-220">StringArray</span><span class="sxs-lookup"><span data-stu-id="148de-220">StringArray</span></span>  <br/> |<span data-ttu-id="148de-221">指示一个字符串数组。</span><span class="sxs-lookup"><span data-stu-id="148de-221">Indicates an array of strings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="148de-222">子元素</span><span class="sxs-lookup"><span data-stu-id="148de-222">Child elements</span></span>

<span data-ttu-id="148de-223">无。</span><span class="sxs-lookup"><span data-stu-id="148de-223">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="148de-224">父元素</span><span class="sxs-lookup"><span data-stu-id="148de-224">Parent elements</span></span>

|<span data-ttu-id="148de-225">**元素**</span><span class="sxs-lookup"><span data-stu-id="148de-225">**Element**</span></span>|<span data-ttu-id="148de-226">**说明**</span><span class="sxs-lookup"><span data-stu-id="148de-226">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="148de-227">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="148de-227">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="148de-228">标识扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="148de-228">Identifies an extended MAPI property.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="148de-229">备注</span><span class="sxs-lookup"><span data-stu-id="148de-229">Remarks</span></span>

<span data-ttu-id="148de-230">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="148de-230">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="148de-231">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="148de-231">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="148de-232">元素信息</span><span class="sxs-lookup"><span data-stu-id="148de-232">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="148de-233">命名空间</span><span class="sxs-lookup"><span data-stu-id="148de-233">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="148de-234">架构名称</span><span class="sxs-lookup"><span data-stu-id="148de-234">Schema Name</span></span>  <br/> |<span data-ttu-id="148de-235">类型架构</span><span class="sxs-lookup"><span data-stu-id="148de-235">Type schema</span></span>  <br/> |
|<span data-ttu-id="148de-236">验证文件</span><span class="sxs-lookup"><span data-stu-id="148de-236">Validation File</span></span>  <br/> |<span data-ttu-id="148de-237">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="148de-237">types.xsd</span></span>  <br/> |
|<span data-ttu-id="148de-238">可以为空</span><span class="sxs-lookup"><span data-stu-id="148de-238">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="148de-239">另请参阅</span><span class="sxs-lookup"><span data-stu-id="148de-239">See also</span></span>

- [<span data-ttu-id="148de-240">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="148de-240">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

