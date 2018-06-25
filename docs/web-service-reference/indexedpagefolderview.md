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
description: IndexedPageFolderView 元素描述如何分页的项目信息 FindFolder 响应中返回。
ms.openlocfilehash: f32f778daa6fa3fea93ab2bc1951f2407dcf7f80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825910"
---
# <a name="indexedpagefolderview"></a><span data-ttu-id="7af2c-103">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="7af2c-103">IndexedPageFolderView</span></span>

<span data-ttu-id="7af2c-104">**IndexedPageFolderView**元素描述如何分页的项目信息[FindFolder](findfolder.md)响应中返回。</span><span class="sxs-lookup"><span data-stu-id="7af2c-104">The **IndexedPageFolderView** element describes how paged item information is returned in a [FindFolder](findfolder.md) response.</span></span> 
  
[<span data-ttu-id="7af2c-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="7af2c-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="7af2c-106">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="7af2c-106">IndexedPageFolderView</span></span>](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 <span data-ttu-id="7af2c-107">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="7af2c-107">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7af2c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7af2c-108">Attributes and elements</span></span>

<span data-ttu-id="7af2c-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7af2c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7af2c-110">属性</span><span class="sxs-lookup"><span data-stu-id="7af2c-110">Attributes</span></span>

|<span data-ttu-id="7af2c-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="7af2c-111">**Attribute**</span></span>|<span data-ttu-id="7af2c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7af2c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7af2c-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="7af2c-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="7af2c-114">介绍在响应中返回的文件夹的最大数目。</span><span class="sxs-lookup"><span data-stu-id="7af2c-114">Describes the maximum number of folders to return in the response.</span></span> <span data-ttu-id="7af2c-115">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="7af2c-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="7af2c-116">**Offset**</span><span class="sxs-lookup"><span data-stu-id="7af2c-116">**Offset**</span></span> <br/> |<span data-ttu-id="7af2c-117">介绍从**基点**的偏移量。</span><span class="sxs-lookup"><span data-stu-id="7af2c-117">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="7af2c-118">偏移量必须大于或等于零。</span><span class="sxs-lookup"><span data-stu-id="7af2c-118">Offset must be greater than or equal to zero.</span></span> <span data-ttu-id="7af2c-119">如果**基点**等于开头，则偏移量为正数。</span><span class="sxs-lookup"><span data-stu-id="7af2c-119">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="7af2c-120">如果**基点**等于结束，则好像它是负数处理偏移量。</span><span class="sxs-lookup"><span data-stu-id="7af2c-120">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span>  <br/> <span data-ttu-id="7af2c-121">这标识了哪个文件夹将传递的响应中的第一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="7af2c-121">This identifies which folder will be the first folder delivered in the response.</span></span> <span data-ttu-id="7af2c-122">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="7af2c-122">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="7af2c-123">**基点**</span><span class="sxs-lookup"><span data-stu-id="7af2c-123">**BasePoint**</span></span> <br/> |<span data-ttu-id="7af2c-124">描述是否的文件夹页上将启动从开始或结束处的一组与搜索条件找到的文件夹。</span><span class="sxs-lookup"><span data-stu-id="7af2c-124">Describes whether the page of folders will start from the start or the end of the set of folders that are found with the search criteria.</span></span> <span data-ttu-id="7af2c-125">始终从末尾查找往回搜索。</span><span class="sxs-lookup"><span data-stu-id="7af2c-125">Seeking from the end always searches backward.</span></span> <span data-ttu-id="7af2c-126">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="7af2c-126">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="7af2c-127">基点属性</span><span class="sxs-lookup"><span data-stu-id="7af2c-127">BasePoint Attribute</span></span>

|<span data-ttu-id="7af2c-128">**值**</span><span class="sxs-lookup"><span data-stu-id="7af2c-128">**Value**</span></span>|<span data-ttu-id="7af2c-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="7af2c-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7af2c-130">开始</span><span class="sxs-lookup"><span data-stu-id="7af2c-130">Beginning</span></span>  <br/> |<span data-ttu-id="7af2c-131">找到的文件夹集的开头开始分页的视图。</span><span class="sxs-lookup"><span data-stu-id="7af2c-131">The paged view starts at the beginning of the found folder set.</span></span>  <br/> |
|<span data-ttu-id="7af2c-132">End</span><span class="sxs-lookup"><span data-stu-id="7af2c-132">End</span></span>  <br/> |<span data-ttu-id="7af2c-133">找到的文件夹集的末尾开始分页的视图。</span><span class="sxs-lookup"><span data-stu-id="7af2c-133">The paged view starts at the end of the found folder set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7af2c-134">子元素</span><span class="sxs-lookup"><span data-stu-id="7af2c-134">Child elements</span></span>

<span data-ttu-id="7af2c-135">无。</span><span class="sxs-lookup"><span data-stu-id="7af2c-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7af2c-136">父元素</span><span class="sxs-lookup"><span data-stu-id="7af2c-136">Parent elements</span></span>

|<span data-ttu-id="7af2c-137">**元素**</span><span class="sxs-lookup"><span data-stu-id="7af2c-137">**Element**</span></span>|<span data-ttu-id="7af2c-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="7af2c-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7af2c-139">FindFolder</span><span class="sxs-lookup"><span data-stu-id="7af2c-139">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="7af2c-140">定义查找邮箱中的文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="7af2c-140">Defines a request to find folders in a mailbox.</span></span>  <br/> <span data-ttu-id="7af2c-141">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="7af2c-141">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7af2c-142">注解</span><span class="sxs-lookup"><span data-stu-id="7af2c-142">Remarks</span></span>

<span data-ttu-id="7af2c-143">从最终查找涉及将移至原点标识的偏移量。</span><span class="sxs-lookup"><span data-stu-id="7af2c-143">Seeking from end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="7af2c-144">此外，将指针向后移动请求的记录数。</span><span class="sxs-lookup"><span data-stu-id="7af2c-144">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="7af2c-145">例如，如果有 100 条记录，偏移量为 25 从末尾，从 75 开始搜索。</span><span class="sxs-lookup"><span data-stu-id="7af2c-145">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="7af2c-146">如果返回了 10 条记录，10 个附加到 65 记录，并返回记录到 75 65 指针是向后移动。</span><span class="sxs-lookup"><span data-stu-id="7af2c-146">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="7af2c-147">下一个索引为 64。</span><span class="sxs-lookup"><span data-stu-id="7af2c-147">The next index is 64.</span></span> <span data-ttu-id="7af2c-148">从页面结尾的下一步偏移量为 100 减 64 其等于 36。</span><span class="sxs-lookup"><span data-stu-id="7af2c-148">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="7af2c-149">从结束后，若要获取的已编制索引的下一页的下一步偏移量值为 36。</span><span class="sxs-lookup"><span data-stu-id="7af2c-149">The value for the next offset from the end to get the next indexed page is 36.</span></span>
  
<span data-ttu-id="7af2c-150">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7af2c-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7af2c-151">元素信息</span><span class="sxs-lookup"><span data-stu-id="7af2c-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7af2c-152">命名空间</span><span class="sxs-lookup"><span data-stu-id="7af2c-152">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7af2c-153">架构名称</span><span class="sxs-lookup"><span data-stu-id="7af2c-153">Schema Name</span></span>  <br/> |<span data-ttu-id="7af2c-154">消息架构</span><span class="sxs-lookup"><span data-stu-id="7af2c-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7af2c-155">验证文件</span><span class="sxs-lookup"><span data-stu-id="7af2c-155">Validation File</span></span>  <br/> |<span data-ttu-id="7af2c-156">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7af2c-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7af2c-157">可以为空</span><span class="sxs-lookup"><span data-stu-id="7af2c-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="7af2c-158">False</span><span class="sxs-lookup"><span data-stu-id="7af2c-158">False</span></span>  <br/> |
   

