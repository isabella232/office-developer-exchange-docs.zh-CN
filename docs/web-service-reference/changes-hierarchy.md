---
title: 更改（层次结构）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Changes
api_type:
- schema
ms.assetid: 918a0d1f-90a5-4eef-9592-07e15bef94e6
description: Change 元素包含一个序列化的更改类型的数组，这些类型代表客户端上的文件夹与运行 Microsoft Exchange Server 2007 的计算机上的文件夹之间的差异类型。
ms.openlocfilehash: a296d87f23e85d42b4c8c858e92eddfb586a8324
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463270"
---
# <a name="changes-hierarchy"></a><span data-ttu-id="c4851-103">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="c4851-103">Changes (Hierarchy)</span></span>

<span data-ttu-id="c4851-104">Change**元素包含**一个序列化的更改类型的数组，这些类型代表客户端上的文件夹与运行 Microsoft Exchange Server 2007 的计算机上的文件夹之间的差异类型。</span><span class="sxs-lookup"><span data-stu-id="c4851-104">The **Changes** element contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="c4851-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="c4851-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="c4851-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c4851-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="c4851-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c4851-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="c4851-108">更改（层次结构）</span><span class="sxs-lookup"><span data-stu-id="c4851-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="c4851-109">**SyncFolderHierarchyChangesType**</span><span class="sxs-lookup"><span data-stu-id="c4851-109">**SyncFolderHierarchyChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4851-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c4851-110">Attributes and elements</span></span>

<span data-ttu-id="c4851-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c4851-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4851-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="c4851-112">Attributes</span></span>

<span data-ttu-id="c4851-113">无。</span><span class="sxs-lookup"><span data-stu-id="c4851-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4851-114">子元素</span><span class="sxs-lookup"><span data-stu-id="c4851-114">Child elements</span></span>

|<span data-ttu-id="c4851-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="c4851-115">**Element**</span></span>|<span data-ttu-id="c4851-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4851-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4851-117">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c4851-117">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="c4851-118">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="c4851-118">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c4851-119">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c4851-119">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="c4851-120">标识要在本地客户端存储中更新单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="c4851-120">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c4851-121">Delete （FolderSync）</span><span class="sxs-lookup"><span data-stu-id="c4851-121">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="c4851-122">标识要在本地客户端存储中删除的单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="c4851-122">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4851-123">父元素</span><span class="sxs-lookup"><span data-stu-id="c4851-123">Parent elements</span></span>

|<span data-ttu-id="c4851-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="c4851-124">**Element**</span></span>|<span data-ttu-id="c4851-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4851-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4851-126">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c4851-126">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="c4851-127">包含 SyncFolderHierarchy 请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="c4851-127">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c4851-128">文本值</span><span class="sxs-lookup"><span data-stu-id="c4851-128">Text value</span></span>

<span data-ttu-id="c4851-129">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="c4851-129">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4851-130">备注</span><span class="sxs-lookup"><span data-stu-id="c4851-130">Remarks</span></span>

<span data-ttu-id="c4851-131">描述此元素的架构位于安装了客户端访问服务器角色的 Exchange 2007 计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c4851-131">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4851-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="c4851-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4851-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="c4851-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c4851-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="c4851-134">Schema name</span></span>  <br/> |<span data-ttu-id="c4851-135">消息架构</span><span class="sxs-lookup"><span data-stu-id="c4851-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c4851-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="c4851-136">Validation file</span></span>  <br/> |<span data-ttu-id="c4851-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c4851-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c4851-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="c4851-138">Can be empty</span></span>  <br/> |<span data-ttu-id="c4851-139">False</span><span class="sxs-lookup"><span data-stu-id="c4851-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4851-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4851-140">See also</span></span>



[<span data-ttu-id="c4851-141">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="c4851-141">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


[<span data-ttu-id="c4851-142">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="c4851-142">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="c4851-143">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c4851-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

