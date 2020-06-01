---
title: SyncState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncState
api_type:
- schema
ms.assetid: e5ebaae3-0f07-481d-ac67-d9687a3c7ac3
description: SyncState 元素包含一个 base64 编码的格式的同步数据，该格式是在每个成功的请求之后更新的。 这用于标识同步状态。
ms.openlocfilehash: 8e2d9a633cdad0a124b87e4e794399c06d3b5445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458962"
---
# <a name="syncstate"></a><span data-ttu-id="e7ea4-104">SyncState</span><span class="sxs-lookup"><span data-stu-id="e7ea4-104">SyncState</span></span>

<span data-ttu-id="e7ea4-105">**SyncState**元素包含一个 base64 编码的格式的同步数据，该格式是在每个成功的请求之后更新的。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-105">The **SyncState** element contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="e7ea4-106">这用于标识同步状态。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-106">This is used to identify the synchronization state.</span></span> 
  
```xml
<SyncState/>
```

 <span data-ttu-id="e7ea4-107">**String**</span><span class="sxs-lookup"><span data-stu-id="e7ea4-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7ea4-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e7ea4-108">Attributes and elements</span></span>

<span data-ttu-id="e7ea4-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7ea4-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="e7ea4-110">Attributes</span></span>

<span data-ttu-id="e7ea4-111">无。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7ea4-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e7ea4-112">Child elements</span></span>

<span data-ttu-id="e7ea4-113">无。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e7ea4-114">父元素</span><span class="sxs-lookup"><span data-stu-id="e7ea4-114">Parent elements</span></span>

|<span data-ttu-id="e7ea4-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="e7ea4-115">**Element**</span></span>|<span data-ttu-id="e7ea4-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="e7ea4-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7ea4-117">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="e7ea4-117">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="e7ea4-118">定义在客户端上同步文件夹层次结构的请求。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-118">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> |
|[<span data-ttu-id="e7ea4-119">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e7ea4-119">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="e7ea4-120">包含 SyncFolderHierarchy 请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-120">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
|[<span data-ttu-id="e7ea4-121">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e7ea4-121">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="e7ea4-122">定义对 Exchange 存储文件夹中的项目进行同步的请求。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-122">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
|[<span data-ttu-id="e7ea4-123">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e7ea4-123">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="e7ea4-124">包含 SyncFolderItems 请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-124">Contains the status and result of a SyncFolderItems request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e7ea4-125">文本值</span><span class="sxs-lookup"><span data-stu-id="e7ea4-125">Text value</span></span>

<span data-ttu-id="e7ea4-126">使用此元素时，必须提供文本值。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-126">A text value is required when this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7ea4-127">说明</span><span class="sxs-lookup"><span data-stu-id="e7ea4-127">Remarks</span></span>

<span data-ttu-id="e7ea4-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e7ea4-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7ea4-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="e7ea4-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7ea4-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="e7ea4-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e7ea4-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="e7ea4-131">Schema name</span></span>  <br/> |<span data-ttu-id="e7ea4-132">消息架构</span><span class="sxs-lookup"><span data-stu-id="e7ea4-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e7ea4-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="e7ea4-133">Validation file</span></span>  <br/> |<span data-ttu-id="e7ea4-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e7ea4-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e7ea4-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="e7ea4-135">Can be empty</span></span>  <br/> |<span data-ttu-id="e7ea4-136">False</span><span class="sxs-lookup"><span data-stu-id="e7ea4-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7ea4-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7ea4-137">See also</span></span>



[<span data-ttu-id="e7ea4-138">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="e7ea4-138">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
  
[<span data-ttu-id="e7ea4-139">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="e7ea4-139">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="e7ea4-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e7ea4-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

