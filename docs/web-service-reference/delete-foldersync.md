---
title: 删除 (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- schema
ms.assetid: c4397d91-43ef-40a9-a80e-d31501a33caa
description: 删除元素标识为在本地客户端库删除单个文件夹。
ms.openlocfilehash: 5cad36c6fcff782195fdb285e2d3c4f3c5ec0f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2018
ms.locfileid: "19753783"
---
# <a name="delete-foldersync"></a><span data-ttu-id="e7f9c-103">删除 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="e7f9c-103">Delete (FolderSync)</span></span>

<span data-ttu-id="e7f9c-104">**删除**元素标识为在本地客户端库删除单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="e7f9c-104">The **Delete** element identifies a single folder to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="e7f9c-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="e7f9c-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)  
- [<span data-ttu-id="e7f9c-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e7f9c-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="e7f9c-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e7f9c-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="e7f9c-108">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="e7f9c-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)  
- [<span data-ttu-id="e7f9c-109">删除 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="e7f9c-109">Delete (FolderSync)</span></span>](delete-foldersync.md)
  
```xml
<Delete>
   <FolderId/>
</Delete>
```

<span data-ttu-id="e7f9c-110">**SyncFolderHierarchyDeleteType**</span><span class="sxs-lookup"><span data-stu-id="e7f9c-110">**SyncFolderHierarchyDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e7f9c-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e7f9c-111">Attributes and elements</span></span>

<span data-ttu-id="e7f9c-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e7f9c-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7f9c-113">属性</span><span class="sxs-lookup"><span data-stu-id="e7f9c-113">Attributes</span></span>

<span data-ttu-id="e7f9c-114">无。</span><span class="sxs-lookup"><span data-stu-id="e7f9c-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7f9c-115">子元素</span><span class="sxs-lookup"><span data-stu-id="e7f9c-115">Child elements</span></span>

|<span data-ttu-id="e7f9c-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="e7f9c-116">**Element**</span></span>|<span data-ttu-id="e7f9c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="e7f9c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7f9c-118">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="e7f9c-118">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="e7f9c-119">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="e7f9c-119">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e7f9c-120">父元素</span><span class="sxs-lookup"><span data-stu-id="e7f9c-120">Parent elements</span></span>

|<span data-ttu-id="e7f9c-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="e7f9c-121">**Element**</span></span>|<span data-ttu-id="e7f9c-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="e7f9c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7f9c-123">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="e7f9c-123">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="e7f9c-124">包含表示的客户端上的文件夹和运行 Microsoft Exchange Server 2007 的计算机上的文件夹之间的差异的类型的更改类型排序的数组。</span><span class="sxs-lookup"><span data-stu-id="e7f9c-124">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7f9c-125">注解</span><span class="sxs-lookup"><span data-stu-id="e7f9c-125">Remarks</span></span>

<span data-ttu-id="e7f9c-126">描述此元素的架构位于安装了客户端访问服务器角色的 Exchange 2007 计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e7f9c-126">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7f9c-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="e7f9c-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7f9c-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="e7f9c-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7f9c-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="e7f9c-129">Schema name</span></span>  <br/> |<span data-ttu-id="e7f9c-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="e7f9c-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="e7f9c-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="e7f9c-131">Validation file</span></span>  <br/> |<span data-ttu-id="e7f9c-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e7f9c-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7f9c-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="e7f9c-133">Can be empty</span></span>  <br/> |<span data-ttu-id="e7f9c-134">False</span><span class="sxs-lookup"><span data-stu-id="e7f9c-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7f9c-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7f9c-135">See also</span></span>

- [<span data-ttu-id="e7f9c-136">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="e7f9c-136">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="e7f9c-137">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="e7f9c-137">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="e7f9c-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e7f9c-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

