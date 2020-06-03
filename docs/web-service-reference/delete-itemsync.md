---
title: Delete （ItemSync）
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
description: Delete 元素标识要在本地客户端存储中删除的单个项。
ms.openlocfilehash: 6e30ddc7f7248fe7ff7136e19ba58c7d5d8a800f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454678"
---
# <a name="delete-itemsync"></a><span data-ttu-id="91cfd-103">Delete （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="91cfd-103">Delete (ItemSync)</span></span>

<span data-ttu-id="91cfd-104">**Delete**元素标识要在本地客户端存储中删除的单个项。</span><span class="sxs-lookup"><span data-stu-id="91cfd-104">The **Delete** element identifies a single item to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="91cfd-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="91cfd-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)  
- [<span data-ttu-id="91cfd-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="91cfd-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="91cfd-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="91cfd-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)  
- [<span data-ttu-id="91cfd-108">更改（项目）</span><span class="sxs-lookup"><span data-stu-id="91cfd-108">Changes (Items)</span></span>](changes-items.md)  
- [<span data-ttu-id="91cfd-109">Delete （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="91cfd-109">Delete (ItemSync)</span></span>](delete-itemsync.md)
  
```xml
<Delete>
   <ItemId/>
</Delete>
```

<span data-ttu-id="91cfd-110">**SyncFolderItemsDeleteType**</span><span class="sxs-lookup"><span data-stu-id="91cfd-110">**SyncFolderItemsDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="91cfd-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="91cfd-111">Attributes and elements</span></span>

<span data-ttu-id="91cfd-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="91cfd-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91cfd-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="91cfd-113">Attributes</span></span>

<span data-ttu-id="91cfd-114">无。</span><span class="sxs-lookup"><span data-stu-id="91cfd-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91cfd-115">子元素</span><span class="sxs-lookup"><span data-stu-id="91cfd-115">Child elements</span></span>

|<span data-ttu-id="91cfd-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="91cfd-116">**Element**</span></span>|<span data-ttu-id="91cfd-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="91cfd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91cfd-118">ItemId</span><span class="sxs-lookup"><span data-stu-id="91cfd-118">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="91cfd-119">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="91cfd-119">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="91cfd-120">父元素</span><span class="sxs-lookup"><span data-stu-id="91cfd-120">Parent elements</span></span>

|<span data-ttu-id="91cfd-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="91cfd-121">**Element**</span></span>|<span data-ttu-id="91cfd-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="91cfd-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91cfd-123">更改（项目）</span><span class="sxs-lookup"><span data-stu-id="91cfd-123">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="91cfd-124">包含更改类型的序列数组，这些类型表示客户端上的项与 Exchange 服务器上的项之间的差异类型。</span><span class="sxs-lookup"><span data-stu-id="91cfd-124">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91cfd-125">说明</span><span class="sxs-lookup"><span data-stu-id="91cfd-125">Remarks</span></span>

<span data-ttu-id="91cfd-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="91cfd-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91cfd-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="91cfd-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91cfd-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="91cfd-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="91cfd-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="91cfd-129">Schema name</span></span>  <br/> |<span data-ttu-id="91cfd-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="91cfd-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="91cfd-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="91cfd-131">Validation file</span></span>  <br/> |<span data-ttu-id="91cfd-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="91cfd-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="91cfd-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="91cfd-133">Can be empty</span></span>  <br/> |<span data-ttu-id="91cfd-134">False</span><span class="sxs-lookup"><span data-stu-id="91cfd-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91cfd-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="91cfd-135">See also</span></span>

- [<span data-ttu-id="91cfd-136">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="91cfd-136">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="91cfd-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="91cfd-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

