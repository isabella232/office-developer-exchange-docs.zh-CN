---
title: 更改（项目）
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
description: Change 元素包含更改类型的序列数组，这些类型表示客户端上的项与 Exchange 服务器上的项之间的差异类型。
ms.openlocfilehash: 6fda7b5602f172bae84ad7b211db2811def4f883
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463263"
---
# <a name="changes-items"></a><span data-ttu-id="50e1c-103">更改（项目）</span><span class="sxs-lookup"><span data-stu-id="50e1c-103">Changes (Items)</span></span>

<span data-ttu-id="50e1c-104">Change**元素包含更改类型**的序列数组，这些类型表示客户端上的项与 Exchange 服务器上的项之间的差异类型。</span><span class="sxs-lookup"><span data-stu-id="50e1c-104">The **Changes** element contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span> 
  
[<span data-ttu-id="50e1c-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="50e1c-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="50e1c-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="50e1c-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="50e1c-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="50e1c-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="50e1c-108">更改（项目）</span><span class="sxs-lookup"><span data-stu-id="50e1c-108">Changes (Items)</span></span>](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="50e1c-109">**SyncFolderItemsChangesType**</span><span class="sxs-lookup"><span data-stu-id="50e1c-109">**SyncFolderItemsChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50e1c-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="50e1c-110">Attributes and elements</span></span>

<span data-ttu-id="50e1c-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="50e1c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50e1c-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="50e1c-112">Attributes</span></span>

<span data-ttu-id="50e1c-113">无。</span><span class="sxs-lookup"><span data-stu-id="50e1c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50e1c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="50e1c-114">Child elements</span></span>

|<span data-ttu-id="50e1c-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="50e1c-115">**Element**</span></span>|<span data-ttu-id="50e1c-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="50e1c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50e1c-117">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="50e1c-117">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="50e1c-118">标识要在本地客户端存储中创建的单个项目。</span><span class="sxs-lookup"><span data-stu-id="50e1c-118">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="50e1c-119">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="50e1c-119">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="50e1c-120">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="50e1c-120">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="50e1c-121">Delete （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="50e1c-121">Delete (ItemSync)</span></span>](delete-itemsync.md) <br/> |<span data-ttu-id="50e1c-122">标识要在本地客户端存储中删除的单个项。</span><span class="sxs-lookup"><span data-stu-id="50e1c-122">Identifies a single item to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="50e1c-123">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="50e1c-123">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="50e1c-124">在已读取项目时，在[SyncFolderItems 操作](syncfolderitems-operation.md)响应中返回。</span><span class="sxs-lookup"><span data-stu-id="50e1c-124">Returned in [SyncFolderItems operation](syncfolderitems-operation.md) responses when an item has been read.</span></span> <span data-ttu-id="50e1c-125">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="50e1c-125">This property is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="50e1c-126">父元素</span><span class="sxs-lookup"><span data-stu-id="50e1c-126">Parent elements</span></span>

|<span data-ttu-id="50e1c-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="50e1c-127">**Element**</span></span>|<span data-ttu-id="50e1c-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="50e1c-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50e1c-129">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="50e1c-129">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="50e1c-130">包含[SyncFolderItems 操作](syncfolderitems-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="50e1c-130">Contains the status and result of a [SyncFolderItems operation](syncfolderitems-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50e1c-131">备注</span><span class="sxs-lookup"><span data-stu-id="50e1c-131">Remarks</span></span>

<span data-ttu-id="50e1c-132">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="50e1c-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50e1c-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="50e1c-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50e1c-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="50e1c-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="50e1c-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="50e1c-135">Schema name</span></span>  <br/> |<span data-ttu-id="50e1c-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="50e1c-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="50e1c-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="50e1c-137">Validation file</span></span>  <br/> |<span data-ttu-id="50e1c-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="50e1c-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="50e1c-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="50e1c-139">Can be empty</span></span>  <br/> |<span data-ttu-id="50e1c-140">False</span><span class="sxs-lookup"><span data-stu-id="50e1c-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50e1c-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="50e1c-141">See also</span></span>



[<span data-ttu-id="50e1c-142">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="50e1c-142">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="50e1c-143">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="50e1c-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

