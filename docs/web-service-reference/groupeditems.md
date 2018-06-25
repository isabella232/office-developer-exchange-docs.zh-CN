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
description: GroupedItems 元素均表示项目组合的 FindItem 操作调用的结果的集合。
ms.openlocfilehash: f8aed9b78fc54307f44b96a45e5c31a4cc76ab50
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825756"
---
# <a name="groupeditems"></a><span data-ttu-id="a7559-103">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="a7559-103">GroupedItems</span></span>

<span data-ttu-id="a7559-104">**GroupedItems**元素表示集合的分组[FindItem 操作](finditem-operation.md)的结果项目呼叫。</span><span class="sxs-lookup"><span data-stu-id="a7559-104">The **GroupedItems** element represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="a7559-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="a7559-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="a7559-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a7559-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="a7559-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a7559-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="a7559-108">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="a7559-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="a7559-109">组</span><span class="sxs-lookup"><span data-stu-id="a7559-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="a7559-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="a7559-110">GroupedItems</span></span>](groupeditems.md)
  
```xml
<GroupedItems>
   <GroupIndex/>
   <Items/>
</GroupedItems>
```

 <span data-ttu-id="a7559-111">**GroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="a7559-111">**GroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7559-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a7559-112">Attributes and elements</span></span>

<span data-ttu-id="a7559-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a7559-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7559-114">属性</span><span class="sxs-lookup"><span data-stu-id="a7559-114">Attributes</span></span>

<span data-ttu-id="a7559-115">无。</span><span class="sxs-lookup"><span data-stu-id="a7559-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7559-116">子元素</span><span class="sxs-lookup"><span data-stu-id="a7559-116">Child elements</span></span>

|<span data-ttu-id="a7559-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7559-117">**Element**</span></span>|<span data-ttu-id="a7559-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7559-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7559-119">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="a7559-119">GroupIndex</span></span>](groupindex.md) <br/> |<span data-ttu-id="a7559-120">代表组合[FindItem 操作](finditem-operation.md)中的项目进行分组的属性值用于呼叫。</span><span class="sxs-lookup"><span data-stu-id="a7559-120">Represents the property value that is used to group items in a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="a7559-121">Items</span><span class="sxs-lookup"><span data-stu-id="a7559-121">Items</span></span>](items.md) <br/> |<span data-ttu-id="a7559-122">包含数组的分组项目。</span><span class="sxs-lookup"><span data-stu-id="a7559-122">Contains an array of grouped items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7559-123">父元素</span><span class="sxs-lookup"><span data-stu-id="a7559-123">Parent elements</span></span>

|<span data-ttu-id="a7559-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7559-124">**Element**</span></span>|<span data-ttu-id="a7559-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7559-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7559-126">组</span><span class="sxs-lookup"><span data-stu-id="a7559-126">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="a7559-127">包含标识[FindItem 操作](finditem-operation.md)请求中使用的搜索和聚合条件找到的组的集合。</span><span class="sxs-lookup"><span data-stu-id="a7559-127">Contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7559-128">注解</span><span class="sxs-lookup"><span data-stu-id="a7559-128">Remarks</span></span>

<span data-ttu-id="a7559-129">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a7559-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7559-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="a7559-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7559-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="a7559-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7559-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="a7559-132">Schema name</span></span>  <br/> |<span data-ttu-id="a7559-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="a7559-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7559-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="a7559-134">Validation file</span></span>  <br/> |<span data-ttu-id="a7559-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a7559-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7559-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="a7559-136">Can be empty</span></span>  <br/> |<span data-ttu-id="a7559-137">False</span><span class="sxs-lookup"><span data-stu-id="a7559-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7559-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a7559-138">See also</span></span>



[<span data-ttu-id="a7559-139">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="a7559-139">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="a7559-140">查找项目</span><span class="sxs-lookup"><span data-stu-id="a7559-140">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

