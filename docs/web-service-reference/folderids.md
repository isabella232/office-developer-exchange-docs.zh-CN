---
title: FolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: FolderIds 元素包含一个由文件夹标识符组成的数组，用于标识要复制、移动、获取、删除或监视事件通知的文件夹。
ms.openlocfilehash: ff0476f72c7da088bd2b39f58ab560dcc82197e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530991"
---
# <a name="folderids"></a><span data-ttu-id="2858f-103">FolderIds</span><span class="sxs-lookup"><span data-stu-id="2858f-103">FolderIds</span></span>

<span data-ttu-id="2858f-104">**FolderIds**元素包含一个由文件夹标识符组成的数组，用于标识要复制、移动、获取、删除或监视事件通知的文件夹。</span><span class="sxs-lookup"><span data-stu-id="2858f-104">The **FolderIds** element contains an array of folder identifiers that are used to identify folders to copy, move, get, delete, or monitor for event notifications.</span></span> 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 <span data-ttu-id="2858f-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="2858f-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2858f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2858f-106">Attributes and elements</span></span>

<span data-ttu-id="2858f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2858f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2858f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2858f-108">Attributes</span></span>

<span data-ttu-id="2858f-109">无。</span><span class="sxs-lookup"><span data-stu-id="2858f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2858f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2858f-110">Child elements</span></span>

|<span data-ttu-id="2858f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2858f-111">**Element**</span></span>|<span data-ttu-id="2858f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2858f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2858f-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="2858f-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="2858f-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="2858f-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="2858f-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="2858f-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="2858f-116">标识可通过名称引用的 Microsoft Exchange Server 文件夹。</span><span class="sxs-lookup"><span data-stu-id="2858f-116">Identifies Microsoft Exchange Server folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2858f-117">父元素</span><span class="sxs-lookup"><span data-stu-id="2858f-117">Parent elements</span></span>

|<span data-ttu-id="2858f-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="2858f-118">**Element**</span></span>|<span data-ttu-id="2858f-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="2858f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2858f-120">GetFolder</span><span class="sxs-lookup"><span data-stu-id="2858f-120">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="2858f-121">定义从 Exchange 存储中获取文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="2858f-121">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="2858f-122">下面是此元素的 XPath 表达式:  `/GetFolder`</span><span class="sxs-lookup"><span data-stu-id="2858f-122">The following is the XPath expression to this element:  `/GetFolder`</span></span> <br/> |
|[<span data-ttu-id="2858f-123">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="2858f-123">DeleteFolder</span></span>](deletefolder.md) <br/> |<span data-ttu-id="2858f-124">定义从 Exchange 存储中删除文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="2858f-124">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="2858f-125">下面是此元素的 XPath 表达式:  `/DeleteFolder`</span><span class="sxs-lookup"><span data-stu-id="2858f-125">The following is the XPath expression to this element:  `/DeleteFolder`</span></span> <br/> |
|[<span data-ttu-id="2858f-126">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="2858f-126">EmptyFolder</span></span>](emptyfolder.md) <br/> |<span data-ttu-id="2858f-127">定义从 Exchange 存储中删除文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="2858f-127">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="2858f-128">下面是此元素的 XPath 表达式:  `/EmptyFolder`</span><span class="sxs-lookup"><span data-stu-id="2858f-128">The following is the XPath expression to this element:  `/EmptyFolder`</span></span> <br/> |
|[<span data-ttu-id="2858f-129">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="2858f-129">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="2858f-130">定义在 Exchange 存储中移动文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="2858f-130">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="2858f-131">下面是此元素的 XPath 表达式:  `/MoveFolder`</span><span class="sxs-lookup"><span data-stu-id="2858f-131">The following is the XPath expression to this element:  `/MoveFolder`</span></span> <br/> |
|[<span data-ttu-id="2858f-132">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="2858f-132">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="2858f-133">定义在 Exchange 存储中复制文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="2858f-133">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="2858f-134">下面是此元素的 XPath 表达式:  `/CopyFolder`</span><span class="sxs-lookup"><span data-stu-id="2858f-134">The following is the XPath expression to this element:  `/CopyFolder`</span></span> <br/> |
|[<span data-ttu-id="2858f-135">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="2858f-135">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="2858f-136">表示对基于推送的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="2858f-136">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="2858f-137">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="2858f-137">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="2858f-138">表示对基于请求的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="2858f-138">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2858f-139">备注</span><span class="sxs-lookup"><span data-stu-id="2858f-139">Remarks</span></span>

<span data-ttu-id="2858f-140">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2858f-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2858f-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="2858f-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2858f-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="2858f-142">Namespace</span></span>  <br/> |<span data-ttu-id="2858f-143">https://schemas.microsoft.com/exchange/services/2006/messages 和 https://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="2858f-143">https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="2858f-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="2858f-144">Schema Name</span></span>  <br/> |<span data-ttu-id="2858f-145">邮件架构;类型架构</span><span class="sxs-lookup"><span data-stu-id="2858f-145">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="2858f-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="2858f-146">Validation File</span></span>  <br/> |<span data-ttu-id="2858f-147">消息 .xsd;类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="2858f-147">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2858f-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="2858f-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="2858f-149">False</span><span class="sxs-lookup"><span data-stu-id="2858f-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2858f-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2858f-150">See also</span></span>



[<span data-ttu-id="2858f-151">GetFolder 操作</span><span class="sxs-lookup"><span data-stu-id="2858f-151">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="2858f-152">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="2858f-152">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="2858f-153">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="2858f-153">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="2858f-154">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="2858f-154">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="2858f-155">订阅操作</span><span class="sxs-lookup"><span data-stu-id="2858f-155">Subscribe operation</span></span>](subscribe-operation.md)

