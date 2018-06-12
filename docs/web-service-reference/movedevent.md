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
description: MovedEvent 元素表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。
ms.openlocfilehash: a375f421ca9159103e47b515729316b21149c68a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826479"
---
# <a name="movedevent"></a><span data-ttu-id="f2821-103">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="f2821-103">MovedEvent</span></span>

<span data-ttu-id="f2821-104">**MovedEvent**元素表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="f2821-104">The **MovedEvent** element represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span> 
  
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

 <span data-ttu-id="f2821-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="f2821-105">**MovedCopiedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2821-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f2821-106">Attributes and elements</span></span>

<span data-ttu-id="f2821-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f2821-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2821-108">属性</span><span class="sxs-lookup"><span data-stu-id="f2821-108">Attributes</span></span>

<span data-ttu-id="f2821-109">无。</span><span class="sxs-lookup"><span data-stu-id="f2821-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2821-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f2821-110">Child elements</span></span>

|<span data-ttu-id="f2821-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2821-111">**Element**</span></span>|<span data-ttu-id="f2821-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2821-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2821-113">水印</span><span class="sxs-lookup"><span data-stu-id="f2821-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="f2821-114">代表邮箱事件表格中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="f2821-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="f2821-115">时间戳</span><span class="sxs-lookup"><span data-stu-id="f2821-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="f2821-116">代表移动项目/文件夹邮箱事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="f2821-116">Represents the timestamp of a move item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="f2821-117">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="f2821-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="f2821-118">代表移动文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="f2821-118">Represents the identifier of the moved folder.</span></span>  <br/> |
|[<span data-ttu-id="f2821-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="f2821-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f2821-120">代表移动项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="f2821-120">Represents the identifier of the moved item.</span></span>  <br/> |
|[<span data-ttu-id="f2821-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="f2821-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="f2821-122">表示包含移动的项目或文件夹的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="f2821-122">Represents the identifier of the folder that contains the moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="f2821-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="f2821-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="f2821-124">它已移动或复制之前，请包含原始文件夹的文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="f2821-124">Contains the folder identifier of the original folder before it was moved or copied.</span></span>  <br/> |
|[<span data-ttu-id="f2821-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="f2821-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="f2821-126">包含原始项目的唯一标识符，它移动之前。</span><span class="sxs-lookup"><span data-stu-id="f2821-126">Contains the unique identifier of the original item before it was moved.</span></span>  <br/> |
|[<span data-ttu-id="f2821-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="f2821-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="f2821-128">包含项或已移动的文件夹的原始父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="f2821-128">Contains the identifier of the original parent folder of an item or folder that was moved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2821-129">父元素</span><span class="sxs-lookup"><span data-stu-id="f2821-129">Parent elements</span></span>

|<span data-ttu-id="f2821-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2821-130">**Element**</span></span>|<span data-ttu-id="f2821-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2821-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2821-132">通知</span><span class="sxs-lookup"><span data-stu-id="f2821-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f2821-133">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="f2821-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2821-134">备注</span><span class="sxs-lookup"><span data-stu-id="f2821-134">Remarks</span></span>

<span data-ttu-id="f2821-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f2821-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2821-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="f2821-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2821-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="f2821-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f2821-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="f2821-138">Schema name</span></span>  <br/> |<span data-ttu-id="f2821-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="f2821-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="f2821-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="f2821-140">Validation file</span></span>  <br/> |<span data-ttu-id="f2821-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f2821-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2821-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="f2821-142">Can be empty</span></span>  <br/> |<span data-ttu-id="f2821-143">False</span><span class="sxs-lookup"><span data-stu-id="f2821-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2821-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2821-144">See also</span></span>



[<span data-ttu-id="f2821-145">订阅操作</span><span class="sxs-lookup"><span data-stu-id="f2821-145">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="f2821-146">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="f2821-146">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="f2821-147">取消操作</span><span class="sxs-lookup"><span data-stu-id="f2821-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)

