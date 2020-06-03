---
title: IndexedPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: IndexedPageFolderView 元素介绍如何在 FindFolder 响应中返回分页项目信息。
ms.openlocfilehash: 6e9e2796c0bdcd9a15487f0e1bc7cbdf09d0a492
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457198"
---
# <a name="indexedpagefolderview"></a><span data-ttu-id="26e58-103">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="26e58-103">IndexedPageFolderView</span></span>

<span data-ttu-id="26e58-104">**IndexedPageFolderView**元素介绍如何在[FindFolder](findfolder.md)响应中返回分页项目信息。</span><span class="sxs-lookup"><span data-stu-id="26e58-104">The **IndexedPageFolderView** element describes how paged item information is returned in a [FindFolder](findfolder.md) response.</span></span> 
  
[<span data-ttu-id="26e58-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="26e58-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="26e58-106">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="26e58-106">IndexedPageFolderView</span></span>](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 <span data-ttu-id="26e58-107">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="26e58-107">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26e58-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="26e58-108">Attributes and elements</span></span>

<span data-ttu-id="26e58-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="26e58-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26e58-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="26e58-110">Attributes</span></span>

|<span data-ttu-id="26e58-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="26e58-111">**Attribute**</span></span>|<span data-ttu-id="26e58-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="26e58-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26e58-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="26e58-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="26e58-114">描述要在响应中返回的最大文件夹数。</span><span class="sxs-lookup"><span data-stu-id="26e58-114">Describes the maximum number of folders to return in the response.</span></span> <span data-ttu-id="26e58-115">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="26e58-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="26e58-116">**Offset**</span><span class="sxs-lookup"><span data-stu-id="26e58-116">**Offset**</span></span> <br/> |<span data-ttu-id="26e58-117">描述**BasePoint**中的偏移量。</span><span class="sxs-lookup"><span data-stu-id="26e58-117">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="26e58-118">偏移量必须大于或等于零。</span><span class="sxs-lookup"><span data-stu-id="26e58-118">Offset must be greater than or equal to zero.</span></span> <span data-ttu-id="26e58-119">如果**BasePoint**等于开头，则偏移量为正值。</span><span class="sxs-lookup"><span data-stu-id="26e58-119">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="26e58-120">如果**BasePoint**等于 End，则处理的是负的偏移量。</span><span class="sxs-lookup"><span data-stu-id="26e58-120">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span>  <br/> <span data-ttu-id="26e58-121">这将标识哪个文件夹将是在响应中传递的第一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="26e58-121">This identifies which folder will be the first folder delivered in the response.</span></span> <span data-ttu-id="26e58-122">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="26e58-122">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="26e58-123">**BasePoint**</span><span class="sxs-lookup"><span data-stu-id="26e58-123">**BasePoint**</span></span> <br/> |<span data-ttu-id="26e58-124">描述文件夹页面是否将从使用搜索条件找到的文件夹集的开头或结尾开始。</span><span class="sxs-lookup"><span data-stu-id="26e58-124">Describes whether the page of folders will start from the start or the end of the set of folders that are found with the search criteria.</span></span> <span data-ttu-id="26e58-125">从末尾进行的查找始终向后搜索。</span><span class="sxs-lookup"><span data-stu-id="26e58-125">Seeking from the end always searches backward.</span></span> <span data-ttu-id="26e58-126">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="26e58-126">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="26e58-127">BasePoint 属性</span><span class="sxs-lookup"><span data-stu-id="26e58-127">BasePoint Attribute</span></span>

|<span data-ttu-id="26e58-128">**值**</span><span class="sxs-lookup"><span data-stu-id="26e58-128">**Value**</span></span>|<span data-ttu-id="26e58-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="26e58-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26e58-130">始</span><span class="sxs-lookup"><span data-stu-id="26e58-130">Beginning</span></span>  <br/> |<span data-ttu-id="26e58-131">分页视图从找到的文件夹集的开头开始。</span><span class="sxs-lookup"><span data-stu-id="26e58-131">The paged view starts at the beginning of the found folder set.</span></span>  <br/> |
|<span data-ttu-id="26e58-132">End</span><span class="sxs-lookup"><span data-stu-id="26e58-132">End</span></span>  <br/> |<span data-ttu-id="26e58-133">分页视图从找到的文件夹集的末尾开始。</span><span class="sxs-lookup"><span data-stu-id="26e58-133">The paged view starts at the end of the found folder set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="26e58-134">子元素</span><span class="sxs-lookup"><span data-stu-id="26e58-134">Child elements</span></span>

<span data-ttu-id="26e58-135">无。</span><span class="sxs-lookup"><span data-stu-id="26e58-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26e58-136">父元素</span><span class="sxs-lookup"><span data-stu-id="26e58-136">Parent elements</span></span>

|<span data-ttu-id="26e58-137">**元素**</span><span class="sxs-lookup"><span data-stu-id="26e58-137">**Element**</span></span>|<span data-ttu-id="26e58-138">**描述**</span><span class="sxs-lookup"><span data-stu-id="26e58-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26e58-139">FindFolder</span><span class="sxs-lookup"><span data-stu-id="26e58-139">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="26e58-140">定义在邮箱中查找文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="26e58-140">Defines a request to find folders in a mailbox.</span></span>  <br/> <span data-ttu-id="26e58-141">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="26e58-141">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26e58-142">备注</span><span class="sxs-lookup"><span data-stu-id="26e58-142">Remarks</span></span>

<span data-ttu-id="26e58-143">从 end 中查找包括移到由偏移量标识的源。</span><span class="sxs-lookup"><span data-stu-id="26e58-143">Seeking from end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="26e58-144">此外，还会按请求的记录数向后移动指针。</span><span class="sxs-lookup"><span data-stu-id="26e58-144">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="26e58-145">例如，如果有100条记录，偏移量是从末尾到25，则搜索从75开始。</span><span class="sxs-lookup"><span data-stu-id="26e58-145">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="26e58-146">如果返回10个记录，指针将向后移动10条记录到65，并返回记录65至75。</span><span class="sxs-lookup"><span data-stu-id="26e58-146">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="26e58-147">下一个索引为64。</span><span class="sxs-lookup"><span data-stu-id="26e58-147">The next index is 64.</span></span> <span data-ttu-id="26e58-148">距页面末尾的下一个偏移量是100减去64，等于36。</span><span class="sxs-lookup"><span data-stu-id="26e58-148">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="26e58-149">用于获取下一个索引页的终点的下一个偏移值为36。</span><span class="sxs-lookup"><span data-stu-id="26e58-149">The value for the next offset from the end to get the next indexed page is 36.</span></span>
  
<span data-ttu-id="26e58-150">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="26e58-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26e58-151">元素信息</span><span class="sxs-lookup"><span data-stu-id="26e58-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26e58-152">命名空间</span><span class="sxs-lookup"><span data-stu-id="26e58-152">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="26e58-153">架构名称</span><span class="sxs-lookup"><span data-stu-id="26e58-153">Schema Name</span></span>  <br/> |<span data-ttu-id="26e58-154">消息架构</span><span class="sxs-lookup"><span data-stu-id="26e58-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="26e58-155">验证文件</span><span class="sxs-lookup"><span data-stu-id="26e58-155">Validation File</span></span>  <br/> |<span data-ttu-id="26e58-156">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="26e58-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="26e58-157">可以为空</span><span class="sxs-lookup"><span data-stu-id="26e58-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="26e58-158">False</span><span class="sxs-lookup"><span data-stu-id="26e58-158">False</span></span>  <br/> |
   

