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
description: FieldOrder 元素表示要用于对结果进行排序的单个字段，并指示用于排序的方向。
ms.openlocfilehash: 10e28f066f7fa6799bf6b03b694d98825f95626d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754297"
---
# <a name="fieldorder"></a><span data-ttu-id="5de3c-103">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="5de3c-103">FieldOrder</span></span>

<span data-ttu-id="5de3c-104">**FieldOrder**元素表示要用于对结果进行排序的单个字段，并指示用于排序的方向。</span><span class="sxs-lookup"><span data-stu-id="5de3c-104">The **FieldOrder** element represents a single field by which to sort results and indicates the direction for the sort.</span></span> 
  
```xml
<FieldOrder Order="">
   <FieldURI/>
</FieldOrder>
```

 <span data-ttu-id="5de3c-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="5de3c-105">**FieldOrderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5de3c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5de3c-106">Attributes and elements</span></span>

<span data-ttu-id="5de3c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5de3c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5de3c-108">属性</span><span class="sxs-lookup"><span data-stu-id="5de3c-108">Attributes</span></span>

|<span data-ttu-id="5de3c-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="5de3c-109">**Attribute**</span></span>|<span data-ttu-id="5de3c-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="5de3c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5de3c-111">**Order**</span><span class="sxs-lookup"><span data-stu-id="5de3c-111">**Order**</span></span> <br/> | <span data-ttu-id="5de3c-112">描述排序顺序的方向。</span><span class="sxs-lookup"><span data-stu-id="5de3c-112">Describes the sort order direction.</span></span><br/><br/> <span data-ttu-id="5de3c-113">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="5de3c-113">The following are the possible values:</span></span> <br/> <br/><span data-ttu-id="5de3c-114">-升序</span><span class="sxs-lookup"><span data-stu-id="5de3c-114">-  Ascending</span></span>  <br/><span data-ttu-id="5de3c-115">-降序</span><span class="sxs-lookup"><span data-stu-id="5de3c-115">-  Descending</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5de3c-116">子元素</span><span class="sxs-lookup"><span data-stu-id="5de3c-116">Child elements</span></span>

|<span data-ttu-id="5de3c-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="5de3c-117">**Element**</span></span>|<span data-ttu-id="5de3c-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="5de3c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5de3c-119">FieldURI</span><span class="sxs-lookup"><span data-stu-id="5de3c-119">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="5de3c-120">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="5de3c-120">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="5de3c-121">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="5de3c-121">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="5de3c-122">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="5de3c-122">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="5de3c-123">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="5de3c-123">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="5de3c-124">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="5de3c-124">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5de3c-125">父元素</span><span class="sxs-lookup"><span data-stu-id="5de3c-125">Parent elements</span></span>

|<span data-ttu-id="5de3c-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="5de3c-126">**Element**</span></span>|<span data-ttu-id="5de3c-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="5de3c-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5de3c-128">SortOrder</span><span class="sxs-lookup"><span data-stu-id="5de3c-128">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="5de3c-129">定义项 FindItem 请求中的排序方式。</span><span class="sxs-lookup"><span data-stu-id="5de3c-129">Defines how items are sorted in a FindItem request.</span></span>  <br/> <span data-ttu-id="5de3c-130">下面是此元素的 XPath 表达式:  `/FindItem/SortOrder`</span><span class="sxs-lookup"><span data-stu-id="5de3c-130">The following is the XPath expression to this element:  `/FindItem/SortOrder`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5de3c-131">备注</span><span class="sxs-lookup"><span data-stu-id="5de3c-131">Remarks</span></span>

<span data-ttu-id="5de3c-132">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5de3c-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5de3c-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="5de3c-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5de3c-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="5de3c-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5de3c-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="5de3c-135">Schema Name</span></span>  <br/> |<span data-ttu-id="5de3c-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="5de3c-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="5de3c-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="5de3c-137">Validation File</span></span>  <br/> |<span data-ttu-id="5de3c-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5de3c-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5de3c-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="5de3c-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="5de3c-140">False</span><span class="sxs-lookup"><span data-stu-id="5de3c-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5de3c-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5de3c-141">See also</span></span>

- [<span data-ttu-id="5de3c-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5de3c-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

