---
title: 更改 （层次结构）
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
description: 更改元素包含的更改类型表示的客户端上的文件夹和运行 Microsoft Exchange Server 2007 的计算机上的文件夹之间的区别类型排序的数组。
ms.openlocfilehash: 15e4f9f37c5e4a4083260dcf379a49beb2260030
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753449"
---
# <a name="changes-hierarchy"></a><span data-ttu-id="5dfbf-103">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="5dfbf-103">Changes (Hierarchy)</span></span>

<span data-ttu-id="5dfbf-104">**更改**元素包含的更改类型表示的客户端上的文件夹和运行 Microsoft Exchange Server 2007 的计算机上的文件夹之间的区别类型排序的数组。</span><span class="sxs-lookup"><span data-stu-id="5dfbf-104">The **Changes** element contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="5dfbf-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="5dfbf-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="5dfbf-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5dfbf-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="5dfbf-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5dfbf-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="5dfbf-108">更改 （层次结构）</span><span class="sxs-lookup"><span data-stu-id="5dfbf-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="5dfbf-109">**SyncFolderHierarchyChangesType**</span><span class="sxs-lookup"><span data-stu-id="5dfbf-109">**SyncFolderHierarchyChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5dfbf-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5dfbf-110">Attributes and elements</span></span>

<span data-ttu-id="5dfbf-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5dfbf-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5dfbf-112">属性</span><span class="sxs-lookup"><span data-stu-id="5dfbf-112">Attributes</span></span>

<span data-ttu-id="5dfbf-113">无。</span><span class="sxs-lookup"><span data-stu-id="5dfbf-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5dfbf-114">子元素</span><span class="sxs-lookup"><span data-stu-id="5dfbf-114">Child elements</span></span>

|<span data-ttu-id="5dfbf-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="5dfbf-115">**Element**</span></span>|<span data-ttu-id="5dfbf-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5dfbf-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5dfbf-117">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="5dfbf-117">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="5dfbf-118">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="5dfbf-118">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="5dfbf-119">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="5dfbf-119">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="5dfbf-120">标识要在本地客户端存储中更新单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="5dfbf-120">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="5dfbf-121">删除 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="5dfbf-121">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="5dfbf-122">标识为在本地客户端库删除单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="5dfbf-122">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5dfbf-123">父元素</span><span class="sxs-lookup"><span data-stu-id="5dfbf-123">Parent elements</span></span>

|<span data-ttu-id="5dfbf-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="5dfbf-124">**Element**</span></span>|<span data-ttu-id="5dfbf-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="5dfbf-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5dfbf-126">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5dfbf-126">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="5dfbf-127">包含状态和 SyncFolderHierarchy 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="5dfbf-127">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5dfbf-128">文本值</span><span class="sxs-lookup"><span data-stu-id="5dfbf-128">Text value</span></span>

<span data-ttu-id="5dfbf-129">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="5dfbf-129">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5dfbf-130">注解</span><span class="sxs-lookup"><span data-stu-id="5dfbf-130">Remarks</span></span>

<span data-ttu-id="5dfbf-131">描述此元素的架构位于安装了客户端访问服务器角色的 Exchange 2007 计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5dfbf-131">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5dfbf-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="5dfbf-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dfbf-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="5dfbf-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5dfbf-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="5dfbf-134">Schema name</span></span>  <br/> |<span data-ttu-id="5dfbf-135">消息架构</span><span class="sxs-lookup"><span data-stu-id="5dfbf-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5dfbf-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="5dfbf-136">Validation file</span></span>  <br/> |<span data-ttu-id="5dfbf-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5dfbf-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5dfbf-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="5dfbf-138">Can be empty</span></span>  <br/> |<span data-ttu-id="5dfbf-139">False</span><span class="sxs-lookup"><span data-stu-id="5dfbf-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5dfbf-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5dfbf-140">See also</span></span>



[<span data-ttu-id="5dfbf-141">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="5dfbf-141">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


[<span data-ttu-id="5dfbf-142">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="5dfbf-142">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="5dfbf-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5dfbf-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

