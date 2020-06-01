---
title: SyncFolderItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 463ed78c-bf82-4cd8-971a-d18425e9e7be
description: SyncFolderItems 元素定义对 Exchange 存储文件夹中的项目进行同步的请求。
ms.openlocfilehash: 0fa5b1544d5627d1423287369e72f97662c28d12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465147"
---
# <a name="syncfolderitems"></a><span data-ttu-id="d30a5-103">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="d30a5-103">SyncFolderItems</span></span>

<span data-ttu-id="d30a5-104">**SyncFolderItems**元素定义对 Exchange 存储文件夹中的项目进行同步的请求。</span><span class="sxs-lookup"><span data-stu-id="d30a5-104">The **SyncFolderItems** element defines a request to synchronize items in an Exchange store folder.</span></span> 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>   <SyncScope/>
</SyncFolderItems>
```

 <span data-ttu-id="d30a5-105">**SyncFolderItemsType**</span><span class="sxs-lookup"><span data-stu-id="d30a5-105">**SyncFolderItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d30a5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d30a5-106">Attributes and elements</span></span>

<span data-ttu-id="d30a5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d30a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d30a5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d30a5-108">Attributes</span></span>

<span data-ttu-id="d30a5-109">无。</span><span class="sxs-lookup"><span data-stu-id="d30a5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d30a5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d30a5-110">Child elements</span></span>

|<span data-ttu-id="d30a5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d30a5-111">**Element**</span></span>|<span data-ttu-id="d30a5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d30a5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d30a5-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="d30a5-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="d30a5-114">标识要包含在 SyncFolderItems 响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="d30a5-114">Identifies the item properties and content to include in a SyncFolderItems response.</span></span> <span data-ttu-id="d30a5-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="d30a5-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d30a5-116">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="d30a5-116">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="d30a5-117">表示包含要同步的项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="d30a5-117">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="d30a5-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="d30a5-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d30a5-119">SyncState</span><span class="sxs-lookup"><span data-stu-id="d30a5-119">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d30a5-120">包含在每次成功请求后更新的、base64 编码的格式的同步数据。</span><span class="sxs-lookup"><span data-stu-id="d30a5-120">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="d30a5-121">这用于标识同步状态。</span><span class="sxs-lookup"><span data-stu-id="d30a5-121">This is used to identify the synchronization state.</span></span> <span data-ttu-id="d30a5-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="d30a5-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d30a5-123">忽略</span><span class="sxs-lookup"><span data-stu-id="d30a5-123">Ignore</span></span>](ignore.md) <br/> |<span data-ttu-id="d30a5-124">确定在同步过程中要跳过的项。</span><span class="sxs-lookup"><span data-stu-id="d30a5-124">Identifies items to skip during synchronization.</span></span> <span data-ttu-id="d30a5-125">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="d30a5-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d30a5-126">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="d30a5-126">MaxChangesReturned</span></span>](maxchangesreturned.md) <br/> |<span data-ttu-id="d30a5-127">描述同步响应中可返回的最大更改数。</span><span class="sxs-lookup"><span data-stu-id="d30a5-127">Describes the maximum number of changes that can be returned in a synchronization response.</span></span> <span data-ttu-id="d30a5-128">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="d30a5-128">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d30a5-129">SyncScope</span><span class="sxs-lookup"><span data-stu-id="d30a5-129">SyncScope</span></span>](syncscope.md) <br/> |<span data-ttu-id="d30a5-130">指定是否在同步响应中仅返回项目或项目和文件夹相关信息。</span><span class="sxs-lookup"><span data-stu-id="d30a5-130">Specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> <span data-ttu-id="d30a5-131">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="d30a5-131">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d30a5-132">父元素</span><span class="sxs-lookup"><span data-stu-id="d30a5-132">Parent elements</span></span>

<span data-ttu-id="d30a5-133">无。</span><span class="sxs-lookup"><span data-stu-id="d30a5-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d30a5-134">说明</span><span class="sxs-lookup"><span data-stu-id="d30a5-134">Remarks</span></span>

<span data-ttu-id="d30a5-135">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d30a5-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d30a5-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="d30a5-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d30a5-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="d30a5-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d30a5-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="d30a5-138">Schema name</span></span>  <br/> |<span data-ttu-id="d30a5-139">邮件架构</span><span class="sxs-lookup"><span data-stu-id="d30a5-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="d30a5-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="d30a5-140">Validation file</span></span>  <br/> |<span data-ttu-id="d30a5-141">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="d30a5-141">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d30a5-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="d30a5-142">Can be empty</span></span>  <br/> |<span data-ttu-id="d30a5-143">False</span><span class="sxs-lookup"><span data-stu-id="d30a5-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d30a5-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d30a5-144">See also</span></span>



[<span data-ttu-id="d30a5-145">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="d30a5-145">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="d30a5-146">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d30a5-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

