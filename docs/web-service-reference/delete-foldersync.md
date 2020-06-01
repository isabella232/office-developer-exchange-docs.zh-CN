---
title: Delete （FolderSync）
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
description: Delete 元素标识要在本地客户端存储中删除的单个文件夹。
ms.openlocfilehash: 68f8687b8cf0723d7fd63a3d55da8ef7c2f98f8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454979"
---
# <a name="delete-foldersync"></a><span data-ttu-id="0cbd0-103">Delete （FolderSync）</span><span class="sxs-lookup"><span data-stu-id="0cbd0-103">Delete (FolderSync)</span></span>

<span data-ttu-id="0cbd0-104">**Delete**元素标识要在本地客户端存储中删除的单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="0cbd0-104">The **Delete** element identifies a single folder to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="0cbd0-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="0cbd0-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)  
- [<span data-ttu-id="0cbd0-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0cbd0-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="0cbd0-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0cbd0-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="0cbd0-108">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="0cbd0-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)  
- [<span data-ttu-id="0cbd0-109">Delete （FolderSync）</span><span class="sxs-lookup"><span data-stu-id="0cbd0-109">Delete (FolderSync)</span></span>](delete-foldersync.md)
  
```xml
<Delete>
   <FolderId/>
</Delete>
```

<span data-ttu-id="0cbd0-110">**SyncFolderHierarchyDeleteType**</span><span class="sxs-lookup"><span data-stu-id="0cbd0-110">**SyncFolderHierarchyDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0cbd0-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0cbd0-111">Attributes and elements</span></span>

<span data-ttu-id="0cbd0-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0cbd0-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0cbd0-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="0cbd0-113">Attributes</span></span>

<span data-ttu-id="0cbd0-114">无。</span><span class="sxs-lookup"><span data-stu-id="0cbd0-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0cbd0-115">子元素</span><span class="sxs-lookup"><span data-stu-id="0cbd0-115">Child elements</span></span>

|<span data-ttu-id="0cbd0-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="0cbd0-116">**Element**</span></span>|<span data-ttu-id="0cbd0-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cbd0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cbd0-118">FolderId</span><span class="sxs-lookup"><span data-stu-id="0cbd0-118">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="0cbd0-119">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="0cbd0-119">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0cbd0-120">父元素</span><span class="sxs-lookup"><span data-stu-id="0cbd0-120">Parent elements</span></span>

|<span data-ttu-id="0cbd0-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="0cbd0-121">**Element**</span></span>|<span data-ttu-id="0cbd0-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cbd0-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cbd0-123">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="0cbd0-123">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="0cbd0-124">包含更改类型的序列化数组，这些类型代表客户端上的文件夹与运行 Microsoft Exchange Server 2007 的计算机上的文件夹之间的差异类型。</span><span class="sxs-lookup"><span data-stu-id="0cbd0-124">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cbd0-125">备注</span><span class="sxs-lookup"><span data-stu-id="0cbd0-125">Remarks</span></span>

<span data-ttu-id="0cbd0-126">描述此元素的架构位于安装了客户端访问服务器角色的 Exchange 2007 计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0cbd0-126">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0cbd0-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="0cbd0-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cbd0-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="0cbd0-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0cbd0-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="0cbd0-129">Schema name</span></span>  <br/> |<span data-ttu-id="0cbd0-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="0cbd0-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="0cbd0-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="0cbd0-131">Validation file</span></span>  <br/> |<span data-ttu-id="0cbd0-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0cbd0-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0cbd0-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="0cbd0-133">Can be empty</span></span>  <br/> |<span data-ttu-id="0cbd0-134">False</span><span class="sxs-lookup"><span data-stu-id="0cbd0-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0cbd0-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0cbd0-135">See also</span></span>

- [<span data-ttu-id="0cbd0-136">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="0cbd0-136">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="0cbd0-137">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="0cbd0-137">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="0cbd0-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0cbd0-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

