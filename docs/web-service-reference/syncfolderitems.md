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
description: SyncFolderItems 元素定义同步 Exchange 存储区文件夹中的项目的请求。
ms.openlocfilehash: 368e19babfccaeab40380103495c63d30647905c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838174"
---
# <a name="syncfolderitems"></a><span data-ttu-id="d0029-103">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="d0029-103">SyncFolderItems</span></span>

<span data-ttu-id="d0029-104">**SyncFolderItems**元素定义同步 Exchange 存储区文件夹中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="d0029-104">The **SyncFolderItems** element defines a request to synchronize items in an Exchange store folder.</span></span> 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>   <SyncScope/>
</SyncFolderItems>
```

 <span data-ttu-id="d0029-105">**SyncFolderItemsType**</span><span class="sxs-lookup"><span data-stu-id="d0029-105">**SyncFolderItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0029-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d0029-106">Attributes and elements</span></span>

<span data-ttu-id="d0029-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d0029-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0029-108">属性</span><span class="sxs-lookup"><span data-stu-id="d0029-108">Attributes</span></span>

<span data-ttu-id="d0029-109">无。</span><span class="sxs-lookup"><span data-stu-id="d0029-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0029-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d0029-110">Child elements</span></span>

|<span data-ttu-id="d0029-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d0029-111">**Element**</span></span>|<span data-ttu-id="d0029-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d0029-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0029-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="d0029-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="d0029-114">标识项目属性和 SyncFolderItems 响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="d0029-114">Identifies the item properties and content to include in a SyncFolderItems response.</span></span> <span data-ttu-id="d0029-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="d0029-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d0029-116">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="d0029-116">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="d0029-117">代表包含要同步的项的文件夹。</span><span class="sxs-lookup"><span data-stu-id="d0029-117">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="d0029-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="d0029-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d0029-119">SyncState</span><span class="sxs-lookup"><span data-stu-id="d0029-119">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d0029-120">包含 base64 编码的同步数据的每个请求成功后都会更新窗体。</span><span class="sxs-lookup"><span data-stu-id="d0029-120">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="d0029-121">这用于标识的同步状态。</span><span class="sxs-lookup"><span data-stu-id="d0029-121">This is used to identify the synchronization state.</span></span> <span data-ttu-id="d0029-122">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d0029-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d0029-123">忽略</span><span class="sxs-lookup"><span data-stu-id="d0029-123">Ignore</span></span>](ignore.md) <br/> |<span data-ttu-id="d0029-124">标识同步过程中跳过的项目。</span><span class="sxs-lookup"><span data-stu-id="d0029-124">Identifies items to skip during synchronization.</span></span> <span data-ttu-id="d0029-125">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d0029-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d0029-126">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="d0029-126">MaxChangesReturned</span></span>](maxchangesreturned.md) <br/> |<span data-ttu-id="d0029-127">介绍可以同步响应中返回的更改的最大数量。</span><span class="sxs-lookup"><span data-stu-id="d0029-127">Describes the maximum number of changes that can be returned in a synchronization response.</span></span> <span data-ttu-id="d0029-128">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="d0029-128">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d0029-129">SyncScope</span><span class="sxs-lookup"><span data-stu-id="d0029-129">SyncScope</span></span>](syncscope.md) <br/> |<span data-ttu-id="d0029-130">指定是否同步响应中返回项目或项目和文件夹的相关信息。</span><span class="sxs-lookup"><span data-stu-id="d0029-130">Specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> <span data-ttu-id="d0029-131">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d0029-131">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0029-132">父元素</span><span class="sxs-lookup"><span data-stu-id="d0029-132">Parent elements</span></span>

<span data-ttu-id="d0029-133">无。</span><span class="sxs-lookup"><span data-stu-id="d0029-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0029-134">备注</span><span class="sxs-lookup"><span data-stu-id="d0029-134">Remarks</span></span>

<span data-ttu-id="d0029-135">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d0029-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0029-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="d0029-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0029-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="d0029-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d0029-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="d0029-138">Schema name</span></span>  <br/> |<span data-ttu-id="d0029-139">邮件架构</span><span class="sxs-lookup"><span data-stu-id="d0029-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="d0029-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="d0029-140">Validation file</span></span>  <br/> |<span data-ttu-id="d0029-141">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d0029-141">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0029-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="d0029-142">Can be empty</span></span>  <br/> |<span data-ttu-id="d0029-143">False</span><span class="sxs-lookup"><span data-stu-id="d0029-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0029-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0029-144">See also</span></span>



[<span data-ttu-id="d0029-145">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="d0029-145">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="d0029-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d0029-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

