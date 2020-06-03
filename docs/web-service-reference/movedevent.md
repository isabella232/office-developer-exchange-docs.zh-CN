---
title: MovedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MovedEvent
api_type:
- schema
ms.assetid: 572f8b40-dfa8-47bc-b0c1-e1a7138506fd
description: MovedEvent 元素表示一个事件，其中的项或文件夹将从一个父文件夹移动到另一个父文件夹。
ms.openlocfilehash: 1f8fb57dba7edb769fe0dd658d89c032dccf8c5f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530406"
---
# <a name="movedevent"></a><span data-ttu-id="831da-103">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="831da-103">MovedEvent</span></span>

<span data-ttu-id="831da-104">**MovedEvent**元素表示一个事件，其中的项或文件夹将从一个父文件夹移动到另一个父文件夹。</span><span class="sxs-lookup"><span data-stu-id="831da-104">The **MovedEvent** element represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span> 
  
```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldItemId/>
   <OldParentFolderId/>
</MovedEvent>
```

```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</MovedEvent>
```


<span data-ttu-id="831da-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="831da-105">**MovedCopiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="831da-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="831da-106">Attributes and elements</span></span>

<span data-ttu-id="831da-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="831da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="831da-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="831da-108">Attributes</span></span>

<span data-ttu-id="831da-109">无。</span><span class="sxs-lookup"><span data-stu-id="831da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="831da-110">子元素</span><span class="sxs-lookup"><span data-stu-id="831da-110">Child elements</span></span>

|<span data-ttu-id="831da-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="831da-111">**Element**</span></span>|<span data-ttu-id="831da-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="831da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="831da-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="831da-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="831da-114">代表 "邮箱事件" 表中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="831da-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="831da-115">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="831da-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="831da-116">表示移动项目/文件夹邮箱事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="831da-116">Represents the timestamp of a move item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="831da-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="831da-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="831da-118">表示已移动文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="831da-118">Represents the identifier of the moved folder.</span></span>  <br/> |
|[<span data-ttu-id="831da-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="831da-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="831da-120">表示已移动项的标识符。</span><span class="sxs-lookup"><span data-stu-id="831da-120">Represents the identifier of the moved item.</span></span>  <br/> |
|[<span data-ttu-id="831da-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="831da-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="831da-122">表示包含已移动的项或文件夹的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="831da-122">Represents the identifier of the folder that contains the moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="831da-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="831da-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="831da-124">包含原始文件夹在移动或复制之前的文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="831da-124">Contains the folder identifier of the original folder before it was moved or copied.</span></span>  <br/> |
|[<span data-ttu-id="831da-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="831da-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="831da-126">包含原始项目在移动前的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="831da-126">Contains the unique identifier of the original item before it was moved.</span></span>  <br/> |
|[<span data-ttu-id="831da-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="831da-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="831da-128">包含移动的项或文件夹的原始父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="831da-128">Contains the identifier of the original parent folder of an item or folder that was moved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="831da-129">父元素</span><span class="sxs-lookup"><span data-stu-id="831da-129">Parent elements</span></span>

|<span data-ttu-id="831da-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="831da-130">**Element**</span></span>|<span data-ttu-id="831da-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="831da-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="831da-132">通知</span><span class="sxs-lookup"><span data-stu-id="831da-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="831da-133">包含有关订阅以及上次通知之后发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="831da-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="831da-134">说明</span><span class="sxs-lookup"><span data-stu-id="831da-134">Remarks</span></span>

<span data-ttu-id="831da-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="831da-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="831da-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="831da-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="831da-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="831da-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="831da-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="831da-138">Schema name</span></span>  <br/> |<span data-ttu-id="831da-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="831da-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="831da-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="831da-140">Validation file</span></span>  <br/> |<span data-ttu-id="831da-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="831da-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="831da-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="831da-142">Can be empty</span></span>  <br/> |<span data-ttu-id="831da-143">False</span><span class="sxs-lookup"><span data-stu-id="831da-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="831da-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="831da-144">See also</span></span>

- [<span data-ttu-id="831da-145">订阅操作</span><span class="sxs-lookup"><span data-stu-id="831da-145">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="831da-146">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="831da-146">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="831da-147">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="831da-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)

