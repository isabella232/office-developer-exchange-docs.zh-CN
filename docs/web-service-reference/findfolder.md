---
title: FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: FindFolder元素定义的请求，以便查找邮箱中的文件夹。
ms.openlocfilehash: 69fbaebc5615ac7d19512770658cde83e4d352df
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353530"
---
# <a name="findfolder"></a><span data-ttu-id="fb3b3-103">FindFolder</span><span class="sxs-lookup"><span data-stu-id="fb3b3-103">FindFolder</span></span>

<span data-ttu-id="fb3b3-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **FindFolder**元素定义的请求，以便查找邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-104">The **FindFolder** element defines a request to find folders in a mailbox.</span></span> 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <FractionalPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

<span data-ttu-id="fb3b3-105">**FindFolderType**</span><span class="sxs-lookup"><span data-stu-id="fb3b3-105">**FindFolderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fb3b3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fb3b3-106">Attributes and elements</span></span>

<span data-ttu-id="fb3b3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb3b3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fb3b3-108">Attributes</span></span>

|<span data-ttu-id="fb3b3-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="fb3b3-109">**Attribute**</span></span>|<span data-ttu-id="fb3b3-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb3b3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb3b3-111">遍历</span><span class="sxs-lookup"><span data-stu-id="fb3b3-111">Traversal</span></span>  <br/> |<span data-ttu-id="fb3b3-p101">定义如何执行搜索。此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-p101">Defines how a search is performed. This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="fb3b3-114">遍历属性值</span><span class="sxs-lookup"><span data-stu-id="fb3b3-114">Traversal attribute values</span></span>

|<span data-ttu-id="fb3b3-115">**值**</span><span class="sxs-lookup"><span data-stu-id="fb3b3-115">**Value**</span></span>|<span data-ttu-id="fb3b3-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb3b3-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb3b3-117">浅</span><span class="sxs-lookup"><span data-stu-id="fb3b3-117">Shallow</span></span>  <br/> |<span data-ttu-id="fb3b3-p102">指示 FindFolder 操作来搜索仅标识的文件夹并返回只有文件夹 Id 尚未删除的项。这被称为浅层遍历。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-p102">Instructs the FindFolder operation to search only the identified folder and to return only the folder IDs for items that have not been deleted. This is called a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="fb3b3-120">深</span><span class="sxs-lookup"><span data-stu-id="fb3b3-120">Deep</span></span>  <br/> |<span data-ttu-id="fb3b3-p103">指示 FindFolder 操作来标识的父文件夹的所有子文件夹中搜索并返回只有文件夹 Id 尚未删除的项。这被称为 deep 遍历。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-p103">Instructs the FindFolder operation to search in all child folders of the identified parent folder and to return only the folder IDs for items that have not been deleted. This is called a deep traversal.</span></span>  <br/> |
|<span data-ttu-id="fb3b3-123">带有 SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="fb3b3-123">SoftDeleted</span></span>  <br/> |<span data-ttu-id="fb3b3-124">指示要执行浅跨度搜索已删除的项的 FindFolder 操作。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-124">Instructs the FindFolder operation to perform a shallow traversal search for deleted items.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fb3b3-125">子元素</span><span class="sxs-lookup"><span data-stu-id="fb3b3-125">Child elements</span></span>

|<span data-ttu-id="fb3b3-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="fb3b3-126">**Element**</span></span>|<span data-ttu-id="fb3b3-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb3b3-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb3b3-128">FolderShape</span><span class="sxs-lookup"><span data-stu-id="fb3b3-128">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="fb3b3-129">标识要在 FindFolder 响应中包含的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-129">Identifies the folder properties to include in a FindFolder response.</span></span>  <br/> |
|[<span data-ttu-id="fb3b3-130">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="fb3b3-130">IndexedPageFolderView</span></span>](indexedpagefolderview.md) <br/> |<span data-ttu-id="fb3b3-p104">描述如何分页的物料信息 FindFolder 响应中返回。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-p104">Describes how paged item information is returned in a FindFolder response. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="fb3b3-133">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="fb3b3-133">FractionalPageFolderView</span></span>](fractionalpagefolderview.md) <br/> |<span data-ttu-id="fb3b3-p105">介绍了分页的视图开始，并在 FindFolder 请求中返回的最大文件夹数。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-p105">Describes where the paged view starts and the maximum number of folders returned in a FindFolder request. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="fb3b3-136">限制</span><span class="sxs-lookup"><span data-stu-id="fb3b3-136">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="fb3b3-p106">定义用于筛选文件夹中的 FindFolder 操作的查询的限制。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-p106">Defines a restriction or query that is used to filter folders in a FindFolder operation. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="fb3b3-139">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="fb3b3-139">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="fb3b3-140">标识要搜索的 FindFolder 操作的文件夹。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-140">Identifies folders for the FindFolder operation to search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fb3b3-141">父元素</span><span class="sxs-lookup"><span data-stu-id="fb3b3-141">Parent elements</span></span>

<span data-ttu-id="fb3b3-142">无。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-142">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb3b3-143">说明</span><span class="sxs-lookup"><span data-stu-id="fb3b3-143">Remarks</span></span>

<span data-ttu-id="fb3b3-144">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="fb3b3-145">示例</span><span class="sxs-lookup"><span data-stu-id="fb3b3-145">Example</span></span>

<span data-ttu-id="fb3b3-146">FindFolder 请求的下面的示例演示如何在窗体中查找位于收件箱中的所有文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="fb3b3-146">The following example of a FindFolder request shows how to form a request to find all the folders located in an Inbox.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="fb3b3-147">元素信息</span><span class="sxs-lookup"><span data-stu-id="fb3b3-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb3b3-148">命名空间</span><span class="sxs-lookup"><span data-stu-id="fb3b3-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fb3b3-149">架构名称</span><span class="sxs-lookup"><span data-stu-id="fb3b3-149">Schema Name</span></span>  <br/> |<span data-ttu-id="fb3b3-150">消息架构</span><span class="sxs-lookup"><span data-stu-id="fb3b3-150">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fb3b3-151">验证文件</span><span class="sxs-lookup"><span data-stu-id="fb3b3-151">Validation File</span></span>  <br/> |<span data-ttu-id="fb3b3-152">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fb3b3-152">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fb3b3-153">可以为空</span><span class="sxs-lookup"><span data-stu-id="fb3b3-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="fb3b3-154">False</span><span class="sxs-lookup"><span data-stu-id="fb3b3-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb3b3-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fb3b3-155">See also</span></span>

- [<span data-ttu-id="fb3b3-156">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="fb3b3-156">FindFolder operation</span></span>](findfolder-operation.md)

