---
title: GroupedItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupedItems
api_type:
- schema
ms.assetid: 53170df4-4272-4b37-b23f-cd8e2d4a7396
description: GroupedItems 元素表示作为分组 FindItem 操作调用的结果的项的集合。
ms.openlocfilehash: 0ee1ca3c6d0cf98e2daefa60a1cb1fd096cda478
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530809"
---
# <a name="groupeditems"></a><span data-ttu-id="57c38-103">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="57c38-103">GroupedItems</span></span>

<span data-ttu-id="57c38-104">**GroupedItems**元素表示作为分组[FindItem 操作](finditem-operation.md)调用的结果的项的集合。</span><span class="sxs-lookup"><span data-stu-id="57c38-104">The **GroupedItems** element represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="57c38-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="57c38-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="57c38-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="57c38-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="57c38-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="57c38-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="57c38-108">RootFolder （FindItemResponseMessage）</span><span class="sxs-lookup"><span data-stu-id="57c38-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="57c38-109">组</span><span class="sxs-lookup"><span data-stu-id="57c38-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="57c38-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="57c38-110">GroupedItems</span></span>](groupeditems.md)
  
```xml
<GroupedItems>
   <GroupIndex/>
   <Items/>
</GroupedItems>
```

 <span data-ttu-id="57c38-111">**GroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="57c38-111">**GroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="57c38-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="57c38-112">Attributes and elements</span></span>

<span data-ttu-id="57c38-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="57c38-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57c38-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="57c38-114">Attributes</span></span>

<span data-ttu-id="57c38-115">无。</span><span class="sxs-lookup"><span data-stu-id="57c38-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57c38-116">子元素</span><span class="sxs-lookup"><span data-stu-id="57c38-116">Child elements</span></span>

|<span data-ttu-id="57c38-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="57c38-117">**Element**</span></span>|<span data-ttu-id="57c38-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="57c38-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57c38-119">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="57c38-119">GroupIndex</span></span>](groupindex.md) <br/> |<span data-ttu-id="57c38-120">表示用于对分组的[FindItem 操作](finditem-operation.md)调用中的项进行分组的属性值。</span><span class="sxs-lookup"><span data-stu-id="57c38-120">Represents the property value that is used to group items in a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="57c38-121">Items</span><span class="sxs-lookup"><span data-stu-id="57c38-121">Items</span></span>](items.md) <br/> |<span data-ttu-id="57c38-122">包含分组项的数组。</span><span class="sxs-lookup"><span data-stu-id="57c38-122">Contains an array of grouped items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="57c38-123">父元素</span><span class="sxs-lookup"><span data-stu-id="57c38-123">Parent elements</span></span>

|<span data-ttu-id="57c38-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="57c38-124">**Element**</span></span>|<span data-ttu-id="57c38-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="57c38-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57c38-126">组</span><span class="sxs-lookup"><span data-stu-id="57c38-126">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="57c38-127">包含使用[FindItem 操作](finditem-operation.md)请求中标识的搜索和聚合条件找到的组的集合。</span><span class="sxs-lookup"><span data-stu-id="57c38-127">Contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57c38-128">备注</span><span class="sxs-lookup"><span data-stu-id="57c38-128">Remarks</span></span>

<span data-ttu-id="57c38-129">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="57c38-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57c38-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="57c38-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57c38-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="57c38-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="57c38-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="57c38-132">Schema name</span></span>  <br/> |<span data-ttu-id="57c38-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="57c38-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="57c38-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="57c38-134">Validation file</span></span>  <br/> |<span data-ttu-id="57c38-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="57c38-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="57c38-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="57c38-136">Can be empty</span></span>  <br/> |<span data-ttu-id="57c38-137">False</span><span class="sxs-lookup"><span data-stu-id="57c38-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57c38-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="57c38-138">See also</span></span>



[<span data-ttu-id="57c38-139">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="57c38-139">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="57c38-140">查找项目</span><span class="sxs-lookup"><span data-stu-id="57c38-140">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

