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
description: SyncState 元素包含 base64 编码的同步数据的每个请求成功后都会更新窗体。 这用于标识的同步状态。
ms.openlocfilehash: 3c600dde09fd813dcfb1f6e74671ebe9004701a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838179"
---
# <a name="syncstate"></a><span data-ttu-id="90983-104">SyncState</span><span class="sxs-lookup"><span data-stu-id="90983-104">SyncState</span></span>

<span data-ttu-id="90983-105">**SyncState**元素包含 base64 编码的同步数据的每个请求成功后都会更新窗体。</span><span class="sxs-lookup"><span data-stu-id="90983-105">The **SyncState** element contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="90983-106">这用于标识的同步状态。</span><span class="sxs-lookup"><span data-stu-id="90983-106">This is used to identify the synchronization state.</span></span> 
  
```xml
<SyncState/>
```

 <span data-ttu-id="90983-107">**字符串**</span><span class="sxs-lookup"><span data-stu-id="90983-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90983-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="90983-108">Attributes and elements</span></span>

<span data-ttu-id="90983-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="90983-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90983-110">属性</span><span class="sxs-lookup"><span data-stu-id="90983-110">Attributes</span></span>

<span data-ttu-id="90983-111">无。</span><span class="sxs-lookup"><span data-stu-id="90983-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90983-112">子元素</span><span class="sxs-lookup"><span data-stu-id="90983-112">Child elements</span></span>

<span data-ttu-id="90983-113">无。</span><span class="sxs-lookup"><span data-stu-id="90983-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="90983-114">父元素</span><span class="sxs-lookup"><span data-stu-id="90983-114">Parent elements</span></span>

|<span data-ttu-id="90983-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="90983-115">**Element**</span></span>|<span data-ttu-id="90983-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="90983-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90983-117">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="90983-117">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="90983-118">定义同步客户端上的文件夹层次结构的请求。</span><span class="sxs-lookup"><span data-stu-id="90983-118">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> |
|[<span data-ttu-id="90983-119">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="90983-119">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="90983-120">包含状态和 SyncFolderHierarchy 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="90983-120">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
|[<span data-ttu-id="90983-121">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="90983-121">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="90983-122">定义同步 Exchange 存储区文件夹中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="90983-122">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
|[<span data-ttu-id="90983-123">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="90983-123">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="90983-124">包含状态和 SyncFolderItems 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="90983-124">Contains the status and result of a SyncFolderItems request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="90983-125">文本值</span><span class="sxs-lookup"><span data-stu-id="90983-125">Text value</span></span>

<span data-ttu-id="90983-126">使用此元素时所需的文本值。</span><span class="sxs-lookup"><span data-stu-id="90983-126">A text value is required when this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90983-127">备注</span><span class="sxs-lookup"><span data-stu-id="90983-127">Remarks</span></span>

<span data-ttu-id="90983-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="90983-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90983-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="90983-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90983-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="90983-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="90983-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="90983-131">Schema name</span></span>  <br/> |<span data-ttu-id="90983-132">消息架构</span><span class="sxs-lookup"><span data-stu-id="90983-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="90983-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="90983-133">Validation file</span></span>  <br/> |<span data-ttu-id="90983-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="90983-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="90983-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="90983-135">Can be empty</span></span>  <br/> |<span data-ttu-id="90983-136">False</span><span class="sxs-lookup"><span data-stu-id="90983-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90983-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="90983-137">See also</span></span>



[<span data-ttu-id="90983-138">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="90983-138">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
  
[<span data-ttu-id="90983-139">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="90983-139">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="90983-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="90983-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

