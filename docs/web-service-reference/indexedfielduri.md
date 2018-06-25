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
ms.openlocfilehash: 6a75e8855ecabf15ca31bb1e05d569c258a43b0b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825909"
---
# <a name="indexedfielduri"></a><span data-ttu-id="c42fb-103">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c42fb-103">IndexedFieldURI</span></span>

<span data-ttu-id="c42fb-104">**IndexedFieldURI**元素标识字典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="c42fb-104">The **IndexedFieldURI** element identifies individual members of a dictionary.</span></span> 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 <span data-ttu-id="c42fb-105">**PathToIndexedFieldType**</span><span class="sxs-lookup"><span data-stu-id="c42fb-105">**PathToIndexedFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c42fb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c42fb-106">Attributes and elements</span></span>

<span data-ttu-id="c42fb-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c42fb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c42fb-108">属性</span><span class="sxs-lookup"><span data-stu-id="c42fb-108">Attributes</span></span>

|<span data-ttu-id="c42fb-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c42fb-109">**Attribute**</span></span>|<span data-ttu-id="c42fb-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c42fb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c42fb-111">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="c42fb-111">**FieldURI**</span></span> <br/> |<span data-ttu-id="c42fb-112">标识字典，其中包含要返回的成员。</span><span class="sxs-lookup"><span data-stu-id="c42fb-112">Identifies the dictionary that contains the member to return.</span></span> <span data-ttu-id="c42fb-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="c42fb-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="c42fb-114">**FieldIndex**</span><span class="sxs-lookup"><span data-stu-id="c42fb-114">**FieldIndex**</span></span> <br/> |<span data-ttu-id="c42fb-115">标识要返回的词典的成员。</span><span class="sxs-lookup"><span data-stu-id="c42fb-115">Identifies the member of the dictionary to return.</span></span> <span data-ttu-id="c42fb-116">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="c42fb-116">This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="c42fb-117">FieldURI 属性</span><span class="sxs-lookup"><span data-stu-id="c42fb-117">FieldURI Attribute</span></span>

|<span data-ttu-id="c42fb-118">**值**</span><span class="sxs-lookup"><span data-stu-id="c42fb-118">**Value**</span></span>|<span data-ttu-id="c42fb-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="c42fb-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c42fb-120">项目： InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="c42fb-120">item:InternetMessageHeader</span></span>  <br/> |<span data-ttu-id="c42fb-121">表示项目的邮件头。</span><span class="sxs-lookup"><span data-stu-id="c42fb-121">Represents the message header of an item.</span></span>  <br/> |
|<span data-ttu-id="c42fb-122">联系人： ImAddress</span><span class="sxs-lookup"><span data-stu-id="c42fb-122">contacts:ImAddress</span></span>  <br/> |<span data-ttu-id="c42fb-123">代表即时消息联系人的地址。</span><span class="sxs-lookup"><span data-stu-id="c42fb-123">Represents the instant messaging address of a contact.</span></span>  <br/> |
|<span data-ttu-id="c42fb-124">联系人： PhysicalAddress:Street</span><span class="sxs-lookup"><span data-stu-id="c42fb-124">contacts:PhysicalAddress:Street</span></span>  <br/> |<span data-ttu-id="c42fb-125">表示联系人的街道地址。</span><span class="sxs-lookup"><span data-stu-id="c42fb-125">Represents the street address of a contact.</span></span>  <br/> |
|<span data-ttu-id="c42fb-126">联系人： PhysicalAddress:City</span><span class="sxs-lookup"><span data-stu-id="c42fb-126">contacts:PhysicalAddress:City</span></span>  <br/> |<span data-ttu-id="c42fb-127">代表联系人的城市。</span><span class="sxs-lookup"><span data-stu-id="c42fb-127">Represents the city of a contact.</span></span>  <br/> |
|<span data-ttu-id="c42fb-128">联系人： PhysicalAddress:State</span><span class="sxs-lookup"><span data-stu-id="c42fb-128">contacts:PhysicalAddress:State</span></span>  <br/> |<span data-ttu-id="c42fb-129">表示联系人的状态。</span><span class="sxs-lookup"><span data-stu-id="c42fb-129">Represents the state of a contact.</span></span>  <br/> |
|<span data-ttu-id="c42fb-130">联系人： PhysicalAddress:Country</span><span class="sxs-lookup"><span data-stu-id="c42fb-130">contacts:PhysicalAddress:Country</span></span>  <br/> |<span data-ttu-id="c42fb-131">代表国家/地区的联系人。</span><span class="sxs-lookup"><span data-stu-id="c42fb-131">Represents the country/region of a contact.</span></span>  <br/> |
|<span data-ttu-id="c42fb-132">联系人： PhysicalAddress:PostalCode</span><span class="sxs-lookup"><span data-stu-id="c42fb-132">contacts:PhysicalAddress:PostalCode</span></span>  <br/> |<span data-ttu-id="c42fb-133">代表联系人的邮政编码。</span><span class="sxs-lookup"><span data-stu-id="c42fb-133">Represents the postal code of a contact.</span></span>  <br/> |
|<span data-ttu-id="c42fb-134">联系人： PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="c42fb-134">contacts:PhoneNumber</span></span>  <br/> |<span data-ttu-id="c42fb-135">代表联系人的电话号码。</span><span class="sxs-lookup"><span data-stu-id="c42fb-135">Represents the phone number of a contact.</span></span>  <br/> |
|<span data-ttu-id="c42fb-136">联系人： 电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="c42fb-136">contacts:EmailAddress</span></span>  <br/> |<span data-ttu-id="c42fb-137">代表联系人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="c42fb-137">Represents the e-mail address of a contact.</span></span>  <br/> |
|<span data-ttu-id="c42fb-138">distributionlist:Members:Member</span><span class="sxs-lookup"><span data-stu-id="c42fb-138">distributionlist:Members:Member</span></span>  <br/> |<span data-ttu-id="c42fb-139">表示一个通讯组列表的成员。</span><span class="sxs-lookup"><span data-stu-id="c42fb-139">Represents a member of a distribution list.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c42fb-140">子元素</span><span class="sxs-lookup"><span data-stu-id="c42fb-140">Child elements</span></span>

<span data-ttu-id="c42fb-141">无。</span><span class="sxs-lookup"><span data-stu-id="c42fb-141">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c42fb-142">父元素</span><span class="sxs-lookup"><span data-stu-id="c42fb-142">Parent elements</span></span>

|<span data-ttu-id="c42fb-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="c42fb-143">**Element**</span></span>|<span data-ttu-id="c42fb-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="c42fb-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c42fb-145">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="c42fb-145">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="c42fb-146">标识要获取、 设置或创建的其他属性。</span><span class="sxs-lookup"><span data-stu-id="c42fb-146">Identifies additional properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="c42fb-147">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="c42fb-147">AggregateOn</span></span>](aggregateon.md) <br/> |<span data-ttu-id="c42fb-148">代表用于确定组合 FindItem 结果集的顺序分组的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="c42fb-148">Represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span>  <br/> |
|[<span data-ttu-id="c42fb-149">GroupBy</span><span class="sxs-lookup"><span data-stu-id="c42fb-149">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="c42fb-150">指定 FindItem 查询任意分组。</span><span class="sxs-lookup"><span data-stu-id="c42fb-150">Specifies an arbitrary grouping for FindItem queries.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c42fb-151">备注</span><span class="sxs-lookup"><span data-stu-id="c42fb-151">Remarks</span></span>

<span data-ttu-id="c42fb-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c42fb-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c42fb-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="c42fb-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c42fb-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="c42fb-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c42fb-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="c42fb-155">Schema Name</span></span>  <br/> |<span data-ttu-id="c42fb-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="c42fb-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="c42fb-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="c42fb-157">Validation File</span></span>  <br/> |<span data-ttu-id="c42fb-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c42fb-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c42fb-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="c42fb-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="c42fb-160">False</span><span class="sxs-lookup"><span data-stu-id="c42fb-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c42fb-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c42fb-161">See also</span></span>



- [<span data-ttu-id="c42fb-162">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c42fb-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

