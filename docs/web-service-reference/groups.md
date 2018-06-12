---
title: 组
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Groups
api_type:
- schema
ms.assetid: 6b6b2d67-219d-4dfb-a4ed-d627b1cfb33f
description: Groups 元素包含与搜索和聚合条件找到的组的集合，这些 FindItem 操作请求中标识。
ms.openlocfilehash: 406a1974899e89243f52ba7a56afcc172c4f3df6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825786"
---
# <a name="groups"></a><span data-ttu-id="29d14-103">组</span><span class="sxs-lookup"><span data-stu-id="29d14-103">Groups</span></span>

<span data-ttu-id="29d14-104">**Groups**元素包含与搜索和聚合条件找到的组的集合，这些[FindItem 操作](finditem-operation.md)请求中标识。</span><span class="sxs-lookup"><span data-stu-id="29d14-104">The **Groups** element contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span> 
  
```xml
<Groups>
   <GroupedItems/>
</Groups>
```

 <span data-ttu-id="29d14-105">**ArrayOfGroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="29d14-105">**ArrayOfGroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="29d14-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="29d14-106">Attributes and elements</span></span>

<span data-ttu-id="29d14-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="29d14-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29d14-108">属性</span><span class="sxs-lookup"><span data-stu-id="29d14-108">Attributes</span></span>

<span data-ttu-id="29d14-109">无。</span><span class="sxs-lookup"><span data-stu-id="29d14-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="29d14-110">子元素</span><span class="sxs-lookup"><span data-stu-id="29d14-110">Child elements</span></span>

|<span data-ttu-id="29d14-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="29d14-111">**Element**</span></span>|<span data-ttu-id="29d14-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="29d14-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29d14-113">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="29d14-113">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="29d14-114">调用表示项的组合[FindItem 操作](finditem-operation.md)的结果的集合。</span><span class="sxs-lookup"><span data-stu-id="29d14-114">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="29d14-115">父元素</span><span class="sxs-lookup"><span data-stu-id="29d14-115">Parent elements</span></span>

|<span data-ttu-id="29d14-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="29d14-116">**Element**</span></span>|<span data-ttu-id="29d14-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="29d14-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29d14-118">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="29d14-118">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="29d14-119">包含[FindItem 操作](finditem-operation.md)操作过程中的单个根文件夹搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="29d14-119">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md) operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29d14-120">备注</span><span class="sxs-lookup"><span data-stu-id="29d14-120">Remarks</span></span>

<span data-ttu-id="29d14-121">一个[GroupedItems](groupeditems.md)实例中每个不同组结果，则会发生。</span><span class="sxs-lookup"><span data-stu-id="29d14-121">One [GroupedItems](groupeditems.md) instance will occur for each distinct group within the result.</span></span> 
  
<span data-ttu-id="29d14-122">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="29d14-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29d14-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="29d14-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29d14-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="29d14-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="29d14-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="29d14-125">Schema name</span></span>  <br/> |<span data-ttu-id="29d14-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="29d14-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="29d14-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="29d14-127">Validation file</span></span>  <br/> |<span data-ttu-id="29d14-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="29d14-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="29d14-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="29d14-129">Can be empty</span></span>  <br/> |<span data-ttu-id="29d14-130">False</span><span class="sxs-lookup"><span data-stu-id="29d14-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29d14-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="29d14-131">See also</span></span>



[<span data-ttu-id="29d14-132">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="29d14-132">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="29d14-133">查找项目</span><span class="sxs-lookup"><span data-stu-id="29d14-133">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

