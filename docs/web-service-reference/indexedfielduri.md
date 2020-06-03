---
title: IndexedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: IndexedFieldURI 元素标识字典中的各个成员。
ms.openlocfilehash: f794d9970590417d916925f7258b28d4f0920d0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467016"
---
# <a name="indexedfielduri"></a><span data-ttu-id="659a0-103">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="659a0-103">IndexedFieldURI</span></span>

<span data-ttu-id="659a0-104">**IndexedFieldURI**元素标识字典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="659a0-104">The **IndexedFieldURI** element identifies individual members of a dictionary.</span></span> 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 <span data-ttu-id="659a0-105">**PathToIndexedFieldType**</span><span class="sxs-lookup"><span data-stu-id="659a0-105">**PathToIndexedFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="659a0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="659a0-106">Attributes and elements</span></span>

<span data-ttu-id="659a0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="659a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="659a0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="659a0-108">Attributes</span></span>

|<span data-ttu-id="659a0-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="659a0-109">**Attribute**</span></span>|<span data-ttu-id="659a0-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="659a0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="659a0-111">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="659a0-111">**FieldURI**</span></span> <br/> |<span data-ttu-id="659a0-112">标识包含要返回的成员的词典。</span><span class="sxs-lookup"><span data-stu-id="659a0-112">Identifies the dictionary that contains the member to return.</span></span> <span data-ttu-id="659a0-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="659a0-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="659a0-114">**FieldIndex**</span><span class="sxs-lookup"><span data-stu-id="659a0-114">**FieldIndex**</span></span> <br/> |<span data-ttu-id="659a0-115">标识要返回的字典的成员。</span><span class="sxs-lookup"><span data-stu-id="659a0-115">Identifies the member of the dictionary to return.</span></span> <span data-ttu-id="659a0-116">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="659a0-116">This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="659a0-117">FieldURI 属性</span><span class="sxs-lookup"><span data-stu-id="659a0-117">FieldURI Attribute</span></span>

|<span data-ttu-id="659a0-118">**值**</span><span class="sxs-lookup"><span data-stu-id="659a0-118">**Value**</span></span>|<span data-ttu-id="659a0-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="659a0-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="659a0-120">项： InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="659a0-120">item:InternetMessageHeader</span></span>  <br/> |<span data-ttu-id="659a0-121">表示项目的邮件头。</span><span class="sxs-lookup"><span data-stu-id="659a0-121">Represents the message header of an item.</span></span>  <br/> |
|<span data-ttu-id="659a0-122">联系人： ImAddress</span><span class="sxs-lookup"><span data-stu-id="659a0-122">contacts:ImAddress</span></span>  <br/> |<span data-ttu-id="659a0-123">表示联系人的即时消息地址。</span><span class="sxs-lookup"><span data-stu-id="659a0-123">Represents the instant messaging address of a contact.</span></span>  <br/> |
|<span data-ttu-id="659a0-124">联系人： PhysicalAddress：街道</span><span class="sxs-lookup"><span data-stu-id="659a0-124">contacts:PhysicalAddress:Street</span></span>  <br/> |<span data-ttu-id="659a0-125">表示联系人的街道地址。</span><span class="sxs-lookup"><span data-stu-id="659a0-125">Represents the street address of a contact.</span></span>  <br/> |
|<span data-ttu-id="659a0-126">联系人： PhysicalAddress： City</span><span class="sxs-lookup"><span data-stu-id="659a0-126">contacts:PhysicalAddress:City</span></span>  <br/> |<span data-ttu-id="659a0-127">表示联系人所在的城市。</span><span class="sxs-lookup"><span data-stu-id="659a0-127">Represents the city of a contact.</span></span>  <br/> |
|<span data-ttu-id="659a0-128">联系人： PhysicalAddress： State</span><span class="sxs-lookup"><span data-stu-id="659a0-128">contacts:PhysicalAddress:State</span></span>  <br/> |<span data-ttu-id="659a0-129">表示联系人的状态。</span><span class="sxs-lookup"><span data-stu-id="659a0-129">Represents the state of a contact.</span></span>  <br/> |
|<span data-ttu-id="659a0-130">联系人： PhysicalAddress：国家/地区</span><span class="sxs-lookup"><span data-stu-id="659a0-130">contacts:PhysicalAddress:Country</span></span>  <br/> |<span data-ttu-id="659a0-131">表示联系人所在的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="659a0-131">Represents the country/region of a contact.</span></span>  <br/> |
|<span data-ttu-id="659a0-132">联系人： PhysicalAddress：邮政编码</span><span class="sxs-lookup"><span data-stu-id="659a0-132">contacts:PhysicalAddress:PostalCode</span></span>  <br/> |<span data-ttu-id="659a0-133">表示联系人的邮政编码。</span><span class="sxs-lookup"><span data-stu-id="659a0-133">Represents the postal code of a contact.</span></span>  <br/> |
|<span data-ttu-id="659a0-134">联系人： PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="659a0-134">contacts:PhoneNumber</span></span>  <br/> |<span data-ttu-id="659a0-135">表示联系人的电话号码。</span><span class="sxs-lookup"><span data-stu-id="659a0-135">Represents the phone number of a contact.</span></span>  <br/> |
|<span data-ttu-id="659a0-136">联系人： EmailAddress</span><span class="sxs-lookup"><span data-stu-id="659a0-136">contacts:EmailAddress</span></span>  <br/> |<span data-ttu-id="659a0-137">表示联系人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="659a0-137">Represents the e-mail address of a contact.</span></span>  <br/> |
|<span data-ttu-id="659a0-138">distributionlist： Members： Member</span><span class="sxs-lookup"><span data-stu-id="659a0-138">distributionlist:Members:Member</span></span>  <br/> |<span data-ttu-id="659a0-139">表示一个通讯组列表的成员。</span><span class="sxs-lookup"><span data-stu-id="659a0-139">Represents a member of a distribution list.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="659a0-140">子元素</span><span class="sxs-lookup"><span data-stu-id="659a0-140">Child elements</span></span>

<span data-ttu-id="659a0-141">无。</span><span class="sxs-lookup"><span data-stu-id="659a0-141">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="659a0-142">父元素</span><span class="sxs-lookup"><span data-stu-id="659a0-142">Parent elements</span></span>

|<span data-ttu-id="659a0-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="659a0-143">**Element**</span></span>|<span data-ttu-id="659a0-144">**描述**</span><span class="sxs-lookup"><span data-stu-id="659a0-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="659a0-145">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="659a0-145">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="659a0-146">标识要获取、设置或创建的其他属性。</span><span class="sxs-lookup"><span data-stu-id="659a0-146">Identifies additional properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="659a0-147">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="659a0-147">AggregateOn</span></span>](aggregateon.md) <br/> |<span data-ttu-id="659a0-148">表示一个属性，该属性用于确定分组的 FindItem 结果集的分组项的顺序。</span><span class="sxs-lookup"><span data-stu-id="659a0-148">Represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span>  <br/> |
|[<span data-ttu-id="659a0-149">GroupBy</span><span class="sxs-lookup"><span data-stu-id="659a0-149">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="659a0-150">指定 FindItem 查询的任意分组。</span><span class="sxs-lookup"><span data-stu-id="659a0-150">Specifies an arbitrary grouping for FindItem queries.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="659a0-151">说明</span><span class="sxs-lookup"><span data-stu-id="659a0-151">Remarks</span></span>

<span data-ttu-id="659a0-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="659a0-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="659a0-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="659a0-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="659a0-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="659a0-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="659a0-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="659a0-155">Schema Name</span></span>  <br/> |<span data-ttu-id="659a0-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="659a0-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="659a0-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="659a0-157">Validation File</span></span>  <br/> |<span data-ttu-id="659a0-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="659a0-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="659a0-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="659a0-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="659a0-160">False</span><span class="sxs-lookup"><span data-stu-id="659a0-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="659a0-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="659a0-161">See also</span></span>



- [<span data-ttu-id="659a0-162">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="659a0-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

