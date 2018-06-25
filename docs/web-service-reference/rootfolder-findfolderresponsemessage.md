---
title: RootFolder (FindFolderResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 5089c815-663f-46be-bc59-aed9ee20f94a
description: RootFolder 元素包含 FindFolder 操作过程中的单个根文件夹的搜索结果。
ms.openlocfilehash: 1cd79d5fa34318e7fe29606df84cbf0ef0520b93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827253"
---
# <a name="rootfolder-findfolderresponsemessage"></a><span data-ttu-id="c63b4-103">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="c63b4-103">RootFolder (FindFolderResponseMessage)</span></span>

<span data-ttu-id="c63b4-104">**RootFolder**元素包含[FindFolder 操作](findfolder-operation.md)期间的单个根文件夹的搜索结果。</span><span class="sxs-lookup"><span data-stu-id="c63b4-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 <span data-ttu-id="c63b4-105">**FindFolderParentType**</span><span class="sxs-lookup"><span data-stu-id="c63b4-105">**FindFolderParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c63b4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c63b4-106">Attributes and elements</span></span>

<span data-ttu-id="c63b4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c63b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c63b4-108">属性</span><span class="sxs-lookup"><span data-stu-id="c63b4-108">Attributes</span></span>

|<span data-ttu-id="c63b4-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c63b4-109">**Attribute**</span></span>|<span data-ttu-id="c63b4-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c63b4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c63b4-111">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="c63b4-111">IndexedPagingOffset</span></span>  <br/> |<span data-ttu-id="c63b4-112">表示使用索引的分页视图时，则在下一个请求时应使用的下一个索引。</span><span class="sxs-lookup"><span data-stu-id="c63b4-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="c63b4-113">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="c63b4-113">NumeratorOffset</span></span>  <br/> |<span data-ttu-id="c63b4-114">代表要用于下一个请求时使用分数页面视图的新分子值。</span><span class="sxs-lookup"><span data-stu-id="c63b4-114">Represents the new numerator value to use for the next request when using fractional page views.</span></span>  <br/> |
|<span data-ttu-id="c63b4-115">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="c63b4-115">AbsoluteDenominator</span></span>  <br/> |<span data-ttu-id="c63b4-116">代表下一步分母执行分数分页时用于下一个请求。</span><span class="sxs-lookup"><span data-stu-id="c63b4-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="c63b4-117">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="c63b4-117">IncludesLastItemInRange</span></span>  <br/> |<span data-ttu-id="c63b4-118">指示当前结果是否包含在查询中的最后一个文件夹，因此不需要进一步分页。</span><span class="sxs-lookup"><span data-stu-id="c63b4-118">Indicates whether the current results contain the last folder in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="c63b4-119">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="c63b4-119">TotalItemsInView</span></span>  <br/> |<span data-ttu-id="c63b4-120">代表文件夹超出限制的总数。</span><span class="sxs-lookup"><span data-stu-id="c63b4-120">Represents the total number of folders that pass the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c63b4-121">子元素</span><span class="sxs-lookup"><span data-stu-id="c63b4-121">Child elements</span></span>

|<span data-ttu-id="c63b4-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="c63b4-122">**Element**</span></span>|<span data-ttu-id="c63b4-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="c63b4-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c63b4-124">Folders</span><span class="sxs-lookup"><span data-stu-id="c63b4-124">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c63b4-125">包含使用[FindFolder 操作](findfolder-operation.md)找到的文件夹的数组。</span><span class="sxs-lookup"><span data-stu-id="c63b4-125">Contains an array of folders found by using the [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c63b4-126">父元素</span><span class="sxs-lookup"><span data-stu-id="c63b4-126">Parent elements</span></span>

|<span data-ttu-id="c63b4-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="c63b4-127">**Element**</span></span>|<span data-ttu-id="c63b4-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="c63b4-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c63b4-129">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c63b4-129">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md) <br/> |<span data-ttu-id="c63b4-130">包含状态和[FindFolder 操作](findfolder-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="c63b4-130">Contains the status and result of a [FindFolder operation](findfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c63b4-131">注解</span><span class="sxs-lookup"><span data-stu-id="c63b4-131">Remarks</span></span>

<span data-ttu-id="c63b4-132">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c63b4-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c63b4-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="c63b4-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c63b4-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="c63b4-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c63b4-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="c63b4-135">Schema name</span></span>  <br/> |<span data-ttu-id="c63b4-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="c63b4-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c63b4-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="c63b4-137">Validation file</span></span>  <br/> |<span data-ttu-id="c63b4-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c63b4-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c63b4-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="c63b4-139">Can be empty</span></span>  <br/> |<span data-ttu-id="c63b4-140">False</span><span class="sxs-lookup"><span data-stu-id="c63b4-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c63b4-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c63b4-141">See also</span></span>



[<span data-ttu-id="c63b4-142">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c63b4-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="c63b4-143">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="c63b4-143">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

