---
title: 更改 （项）
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
ms.assetid: d3139fef-0455-4b89-babd-5d6783b50a58
description: 更改元素包含序列的数组的更改类型表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型。
ms.openlocfilehash: 8e38597276e3e3051a5c1494619d3220280e401f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753445"
---
# <a name="changes-items"></a><span data-ttu-id="0ef87-103">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="0ef87-103">Changes (Items)</span></span>

<span data-ttu-id="0ef87-104">**更改**元素包含序列的数组的更改类型表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型。</span><span class="sxs-lookup"><span data-stu-id="0ef87-104">The **Changes** element contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span> 
  
[<span data-ttu-id="0ef87-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="0ef87-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="0ef87-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0ef87-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="0ef87-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0ef87-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="0ef87-108">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="0ef87-108">Changes (Items)</span></span>](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="0ef87-109">**SyncFolderItemsChangesType**</span><span class="sxs-lookup"><span data-stu-id="0ef87-109">**SyncFolderItemsChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ef87-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0ef87-110">Attributes and elements</span></span>

<span data-ttu-id="0ef87-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0ef87-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ef87-112">属性</span><span class="sxs-lookup"><span data-stu-id="0ef87-112">Attributes</span></span>

<span data-ttu-id="0ef87-113">无。</span><span class="sxs-lookup"><span data-stu-id="0ef87-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ef87-114">子元素</span><span class="sxs-lookup"><span data-stu-id="0ef87-114">Child elements</span></span>

|<span data-ttu-id="0ef87-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="0ef87-115">**Element**</span></span>|<span data-ttu-id="0ef87-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="0ef87-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ef87-117">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="0ef87-117">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="0ef87-118">标识在本地客户端库中创建的单个项。</span><span class="sxs-lookup"><span data-stu-id="0ef87-118">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="0ef87-119">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="0ef87-119">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="0ef87-120">标识要更新本地客户端存储中的单个项。</span><span class="sxs-lookup"><span data-stu-id="0ef87-120">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="0ef87-121">删除 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="0ef87-121">Delete (ItemSync)</span></span>](delete-itemsync.md) <br/> |<span data-ttu-id="0ef87-122">标识要删除在本地客户端库中的单个项。</span><span class="sxs-lookup"><span data-stu-id="0ef87-122">Identifies a single item to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="0ef87-123">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="0ef87-123">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="0ef87-124">读取项目后，在[SyncFolderItems 操作](syncfolderitems-operation.md)响应中返回。</span><span class="sxs-lookup"><span data-stu-id="0ef87-124">Returned in [SyncFolderItems operation](syncfolderitems-operation.md) responses when an item has been read.</span></span> <span data-ttu-id="0ef87-125">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="0ef87-125">This property is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ef87-126">父元素</span><span class="sxs-lookup"><span data-stu-id="0ef87-126">Parent elements</span></span>

|<span data-ttu-id="0ef87-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="0ef87-127">**Element**</span></span>|<span data-ttu-id="0ef87-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="0ef87-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ef87-129">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0ef87-129">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="0ef87-130">包含状态和[SyncFolderItems 操作](syncfolderitems-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="0ef87-130">Contains the status and result of a [SyncFolderItems operation](syncfolderitems-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ef87-131">注解</span><span class="sxs-lookup"><span data-stu-id="0ef87-131">Remarks</span></span>

<span data-ttu-id="0ef87-132">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0ef87-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ef87-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="0ef87-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ef87-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="0ef87-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0ef87-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="0ef87-135">Schema name</span></span>  <br/> |<span data-ttu-id="0ef87-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="0ef87-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0ef87-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="0ef87-137">Validation file</span></span>  <br/> |<span data-ttu-id="0ef87-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0ef87-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0ef87-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="0ef87-139">Can be empty</span></span>  <br/> |<span data-ttu-id="0ef87-140">False</span><span class="sxs-lookup"><span data-stu-id="0ef87-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ef87-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0ef87-141">See also</span></span>



[<span data-ttu-id="0ef87-142">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="0ef87-142">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="0ef87-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0ef87-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

