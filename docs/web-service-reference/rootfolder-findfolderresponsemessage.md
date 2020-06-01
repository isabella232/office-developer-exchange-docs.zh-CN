---
title: RootFolder （FindFolderResponseMessage）
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
description: RootFolder 元素包含在 FindFolder 操作过程中搜索单个根文件夹的结果。
ms.openlocfilehash: b5601d6abec67196c9991908e272a2122a201d69
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457135"
---
# <a name="rootfolder-findfolderresponsemessage"></a><span data-ttu-id="1915b-103">RootFolder （FindFolderResponseMessage）</span><span class="sxs-lookup"><span data-stu-id="1915b-103">RootFolder (FindFolderResponseMessage)</span></span>

<span data-ttu-id="1915b-104">**RootFolder**元素包含在[FindFolder 操作](findfolder-operation.md)过程中搜索单个根文件夹的结果。</span><span class="sxs-lookup"><span data-stu-id="1915b-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 <span data-ttu-id="1915b-105">**FindFolderParentType**</span><span class="sxs-lookup"><span data-stu-id="1915b-105">**FindFolderParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1915b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1915b-106">Attributes and elements</span></span>

<span data-ttu-id="1915b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1915b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1915b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1915b-108">Attributes</span></span>

|<span data-ttu-id="1915b-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="1915b-109">**Attribute**</span></span>|<span data-ttu-id="1915b-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="1915b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1915b-111">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="1915b-111">IndexedPagingOffset</span></span>  <br/> |<span data-ttu-id="1915b-112">表示在使用索引分页视图时应用于下一个请求的下一个索引。</span><span class="sxs-lookup"><span data-stu-id="1915b-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="1915b-113">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="1915b-113">NumeratorOffset</span></span>  <br/> |<span data-ttu-id="1915b-114">表示在使用分数页面视图时用于下一个请求的新的分子值。</span><span class="sxs-lookup"><span data-stu-id="1915b-114">Represents the new numerator value to use for the next request when using fractional page views.</span></span>  <br/> |
|<span data-ttu-id="1915b-115">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="1915b-115">AbsoluteDenominator</span></span>  <br/> |<span data-ttu-id="1915b-116">表示执行分数分页时用于下一个请求的下一个分母。</span><span class="sxs-lookup"><span data-stu-id="1915b-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="1915b-117">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="1915b-117">IncludesLastItemInRange</span></span>  <br/> |<span data-ttu-id="1915b-118">指示当前结果是否包含查询中的最后一个文件夹，以便不需要进一步分页。</span><span class="sxs-lookup"><span data-stu-id="1915b-118">Indicates whether the current results contain the last folder in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="1915b-119">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="1915b-119">TotalItemsInView</span></span>  <br/> |<span data-ttu-id="1915b-120">表示传递限制的文件夹总数。</span><span class="sxs-lookup"><span data-stu-id="1915b-120">Represents the total number of folders that pass the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1915b-121">子元素</span><span class="sxs-lookup"><span data-stu-id="1915b-121">Child elements</span></span>

|<span data-ttu-id="1915b-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="1915b-122">**Element**</span></span>|<span data-ttu-id="1915b-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="1915b-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1915b-124">Folders</span><span class="sxs-lookup"><span data-stu-id="1915b-124">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1915b-125">包含通过使用[FindFolder 操作](findfolder-operation.md)找到的文件夹数组。</span><span class="sxs-lookup"><span data-stu-id="1915b-125">Contains an array of folders found by using the [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1915b-126">父元素</span><span class="sxs-lookup"><span data-stu-id="1915b-126">Parent elements</span></span>

|<span data-ttu-id="1915b-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="1915b-127">**Element**</span></span>|<span data-ttu-id="1915b-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="1915b-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1915b-129">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1915b-129">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md) <br/> |<span data-ttu-id="1915b-130">包含[FindFolder 操作](findfolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="1915b-130">Contains the status and result of a [FindFolder operation](findfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1915b-131">备注</span><span class="sxs-lookup"><span data-stu-id="1915b-131">Remarks</span></span>

<span data-ttu-id="1915b-132">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1915b-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1915b-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="1915b-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1915b-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="1915b-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1915b-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="1915b-135">Schema name</span></span>  <br/> |<span data-ttu-id="1915b-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="1915b-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1915b-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="1915b-137">Validation file</span></span>  <br/> |<span data-ttu-id="1915b-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1915b-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1915b-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="1915b-139">Can be empty</span></span>  <br/> |<span data-ttu-id="1915b-140">False</span><span class="sxs-lookup"><span data-stu-id="1915b-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1915b-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1915b-141">See also</span></span>



[<span data-ttu-id="1915b-142">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="1915b-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="1915b-143">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="1915b-143">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

