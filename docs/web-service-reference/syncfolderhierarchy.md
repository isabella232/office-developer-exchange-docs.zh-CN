---
title: SyncFolderHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: 55df4d01-e48e-4263-a851-78a66ad1093a
description: SyncFolderHierarchy 元素定义一个请求，以在客户端上同步文件夹层次结构。
ms.openlocfilehash: 68b607dbf603e955f74dfaccadd3ce6c4c9fb6ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466645"
---
# <a name="syncfolderhierarchy"></a><span data-ttu-id="48ba3-103">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="48ba3-103">SyncFolderHierarchy</span></span>

<span data-ttu-id="48ba3-104">**SyncFolderHierarchy**元素定义一个请求，以在客户端上同步文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="48ba3-104">The **SyncFolderHierarchy** element defines a request to synchronize a folder hierarchy on a client.</span></span> 
  
```xml
<SyncFolderHierarchy>
   <FolderShape/>   <SyncFolderId/>
   <SyncState/>
</SyncFolderHierarchy>
```

 <span data-ttu-id="48ba3-105">**SyncFolderHierarchyType**</span><span class="sxs-lookup"><span data-stu-id="48ba3-105">**SyncFolderHierarchyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48ba3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="48ba3-106">Attributes and elements</span></span>

<span data-ttu-id="48ba3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="48ba3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48ba3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="48ba3-108">Attributes</span></span>

<span data-ttu-id="48ba3-109">无。</span><span class="sxs-lookup"><span data-stu-id="48ba3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48ba3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="48ba3-110">Child elements</span></span>

|<span data-ttu-id="48ba3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="48ba3-111">**Element**</span></span>|<span data-ttu-id="48ba3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="48ba3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48ba3-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="48ba3-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="48ba3-114">标识要包含在[SyncFolderHierarchy](syncfolderhierarchy.md)响应中的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="48ba3-114">Identifies the folder properties to include in a [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span>  <br/> |
|[<span data-ttu-id="48ba3-115">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="48ba3-115">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="48ba3-116">表示包含要同步的项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="48ba3-116">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="48ba3-117">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="48ba3-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="48ba3-118">SyncState</span><span class="sxs-lookup"><span data-stu-id="48ba3-118">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="48ba3-119">包含在每次成功请求后更新的、base64 编码的格式的同步数据。</span><span class="sxs-lookup"><span data-stu-id="48ba3-119">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="48ba3-120">这用于标识同步状态。</span><span class="sxs-lookup"><span data-stu-id="48ba3-120">This is used to identify the synchronization state.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="48ba3-121">父元素</span><span class="sxs-lookup"><span data-stu-id="48ba3-121">Parent elements</span></span>

<span data-ttu-id="48ba3-122">无。</span><span class="sxs-lookup"><span data-stu-id="48ba3-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48ba3-123">说明</span><span class="sxs-lookup"><span data-stu-id="48ba3-123">Remarks</span></span>

<span data-ttu-id="48ba3-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="48ba3-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48ba3-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="48ba3-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48ba3-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="48ba3-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="48ba3-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="48ba3-127">Schema name</span></span>  <br/> |<span data-ttu-id="48ba3-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="48ba3-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="48ba3-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="48ba3-129">Validation file</span></span>  <br/> |<span data-ttu-id="48ba3-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="48ba3-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="48ba3-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="48ba3-131">Can be empty</span></span>  <br/> |<span data-ttu-id="48ba3-132">False</span><span class="sxs-lookup"><span data-stu-id="48ba3-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48ba3-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="48ba3-133">See also</span></span>



[<span data-ttu-id="48ba3-134">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="48ba3-134">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="48ba3-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="48ba3-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

