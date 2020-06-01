---
title: FieldOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldOrder
api_type:
- schema
ms.assetid: b9364842-bbe2-4221-afef-bf5022bc89ec
description: FieldOrder 元素表示对结果进行排序所依据的单个字段，并指示排序的方向。
ms.openlocfilehash: 19dee7175d541dd99b53e004ea8ccd785b619184
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461259"
---
# <a name="fieldorder"></a><span data-ttu-id="a87c2-103">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="a87c2-103">FieldOrder</span></span>

<span data-ttu-id="a87c2-104">**FieldOrder**元素表示对结果进行排序所依据的单个字段，并指示排序的方向。</span><span class="sxs-lookup"><span data-stu-id="a87c2-104">The **FieldOrder** element represents a single field by which to sort results and indicates the direction for the sort.</span></span> 
  
```xml
<FieldOrder Order="">
   <FieldURI/>
</FieldOrder>
```

```xml
<FieldOrder Order="">
   <ExtendedFieldURI/> 
</FieldOrder>
```

```xml
<FieldOrder Order="">
   <IndexedFieldURI/>
</FieldOrder>
```

<span data-ttu-id="a87c2-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="a87c2-105">**FieldOrderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a87c2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a87c2-106">Attributes and elements</span></span>

<span data-ttu-id="a87c2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a87c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a87c2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a87c2-108">Attributes</span></span>

|<span data-ttu-id="a87c2-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="a87c2-109">**Attribute**</span></span>|<span data-ttu-id="a87c2-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="a87c2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a87c2-111">**Order**</span><span class="sxs-lookup"><span data-stu-id="a87c2-111">**Order**</span></span> <br/> | <span data-ttu-id="a87c2-112">描述排序次序的方向。</span><span class="sxs-lookup"><span data-stu-id="a87c2-112">Describes the sort order direction.</span></span><br/><br/> <span data-ttu-id="a87c2-113">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="a87c2-113">The following are the possible values:</span></span> <br/> <br/><span data-ttu-id="a87c2-114">-升序</span><span class="sxs-lookup"><span data-stu-id="a87c2-114">-  Ascending</span></span>  <br/><span data-ttu-id="a87c2-115">-降序</span><span class="sxs-lookup"><span data-stu-id="a87c2-115">-  Descending</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a87c2-116">子元素</span><span class="sxs-lookup"><span data-stu-id="a87c2-116">Child elements</span></span>

|<span data-ttu-id="a87c2-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="a87c2-117">**Element**</span></span>|<span data-ttu-id="a87c2-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="a87c2-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a87c2-119">FieldURI</span><span class="sxs-lookup"><span data-stu-id="a87c2-119">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="a87c2-120">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="a87c2-120">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="a87c2-121">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="a87c2-121">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="a87c2-122">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="a87c2-122">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="a87c2-123">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="a87c2-123">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="a87c2-124">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="a87c2-124">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a87c2-125">父元素</span><span class="sxs-lookup"><span data-stu-id="a87c2-125">Parent elements</span></span>

|<span data-ttu-id="a87c2-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="a87c2-126">**Element**</span></span>|<span data-ttu-id="a87c2-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="a87c2-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a87c2-128">SortOrder</span><span class="sxs-lookup"><span data-stu-id="a87c2-128">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="a87c2-129">定义如何在 FindItem 请求中对项目进行排序。</span><span class="sxs-lookup"><span data-stu-id="a87c2-129">Defines how items are sorted in a FindItem request.</span></span>  <br/> <span data-ttu-id="a87c2-130">下面是此元素的 XPath 表达式:  `/FindItem/SortOrder`</span><span class="sxs-lookup"><span data-stu-id="a87c2-130">The following is the XPath expression to this element:  `/FindItem/SortOrder`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a87c2-131">说明</span><span class="sxs-lookup"><span data-stu-id="a87c2-131">Remarks</span></span>

<span data-ttu-id="a87c2-132">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a87c2-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a87c2-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="a87c2-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a87c2-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="a87c2-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a87c2-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="a87c2-135">Schema Name</span></span>  <br/> |<span data-ttu-id="a87c2-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="a87c2-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="a87c2-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="a87c2-137">Validation File</span></span>  <br/> |<span data-ttu-id="a87c2-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a87c2-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a87c2-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="a87c2-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="a87c2-140">False</span><span class="sxs-lookup"><span data-stu-id="a87c2-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a87c2-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a87c2-141">See also</span></span>

- [<span data-ttu-id="a87c2-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a87c2-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

