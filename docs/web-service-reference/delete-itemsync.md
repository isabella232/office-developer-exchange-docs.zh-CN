---
title: 删除 (ItemSync)
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
ms.assetid: 4f372d57-2e39-46af-9d83-6c8c55108587
description: 删除元素标识要删除在本地客户端库中的单个项。
ms.openlocfilehash: 18b7ae2f97db2de64896680c3aa76f2590c03177
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753791"
---
# <a name="delete-itemsync"></a><span data-ttu-id="01ea5-103">删除 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="01ea5-103">Delete (ItemSync)</span></span>

<span data-ttu-id="01ea5-104">**删除**元素标识要删除在本地客户端库中的单个项。</span><span class="sxs-lookup"><span data-stu-id="01ea5-104">The **Delete** element identifies a single item to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="01ea5-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="01ea5-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)  
- [<span data-ttu-id="01ea5-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="01ea5-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="01ea5-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="01ea5-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)  
- [<span data-ttu-id="01ea5-108">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="01ea5-108">Changes (Items)</span></span>](changes-items.md)  
- [<span data-ttu-id="01ea5-109">删除 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="01ea5-109">Delete (ItemSync)</span></span>](delete-itemsync.md)
  
```xml
<Delete>
   <ItemId/>
</Delete>
```

<span data-ttu-id="01ea5-110">**SyncFolderItemsDeleteType**</span><span class="sxs-lookup"><span data-stu-id="01ea5-110">**SyncFolderItemsDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="01ea5-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="01ea5-111">Attributes and elements</span></span>

<span data-ttu-id="01ea5-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="01ea5-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01ea5-113">属性</span><span class="sxs-lookup"><span data-stu-id="01ea5-113">Attributes</span></span>

<span data-ttu-id="01ea5-114">无。</span><span class="sxs-lookup"><span data-stu-id="01ea5-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01ea5-115">子元素</span><span class="sxs-lookup"><span data-stu-id="01ea5-115">Child elements</span></span>

|<span data-ttu-id="01ea5-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="01ea5-116">**Element**</span></span>|<span data-ttu-id="01ea5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="01ea5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01ea5-118">ItemId</span><span class="sxs-lookup"><span data-stu-id="01ea5-118">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="01ea5-119">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="01ea5-119">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="01ea5-120">父元素</span><span class="sxs-lookup"><span data-stu-id="01ea5-120">Parent elements</span></span>

|<span data-ttu-id="01ea5-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="01ea5-121">**Element**</span></span>|<span data-ttu-id="01ea5-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="01ea5-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01ea5-123">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="01ea5-123">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="01ea5-124">包含表示的客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。</span><span class="sxs-lookup"><span data-stu-id="01ea5-124">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01ea5-125">备注</span><span class="sxs-lookup"><span data-stu-id="01ea5-125">Remarks</span></span>

<span data-ttu-id="01ea5-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="01ea5-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01ea5-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="01ea5-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01ea5-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="01ea5-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01ea5-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="01ea5-129">Schema name</span></span>  <br/> |<span data-ttu-id="01ea5-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="01ea5-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="01ea5-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="01ea5-131">Validation file</span></span>  <br/> |<span data-ttu-id="01ea5-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="01ea5-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01ea5-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="01ea5-133">Can be empty</span></span>  <br/> |<span data-ttu-id="01ea5-134">False</span><span class="sxs-lookup"><span data-stu-id="01ea5-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01ea5-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01ea5-135">See also</span></span>

- [<span data-ttu-id="01ea5-136">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="01ea5-136">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="01ea5-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="01ea5-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

