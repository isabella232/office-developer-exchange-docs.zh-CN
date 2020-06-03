---
title: CopiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopiedEvent
api_type:
- schema
ms.assetid: 82f2fcac-deaa-4ff8-801f-4fe28d8a19f5
description: CopiedEvent 元素表示在其中复制项目或文件夹的事件。
ms.openlocfilehash: 928910ddbe0bf1e48549d1665ab373f7382366d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529243"
---
# <a name="copiedevent"></a><span data-ttu-id="d2389-103">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="d2389-103">CopiedEvent</span></span>

<span data-ttu-id="d2389-104">**CopiedEvent**元素表示在其中复制项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="d2389-104">The **CopiedEvent** element represents an event in which an item or folder is copied.</span></span> 
  
```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

<span data-ttu-id="d2389-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="d2389-105">**MovedCopiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d2389-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d2389-106">Attributes and elements</span></span>

<span data-ttu-id="d2389-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d2389-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2389-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d2389-108">Attributes</span></span>

<span data-ttu-id="d2389-109">无。</span><span class="sxs-lookup"><span data-stu-id="d2389-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2389-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d2389-110">Child elements</span></span>

|<span data-ttu-id="d2389-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d2389-111">**Element**</span></span>|<span data-ttu-id="d2389-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d2389-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2389-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="d2389-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="d2389-114">代表 "邮箱事件" 表中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="d2389-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="d2389-115">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="d2389-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="d2389-116">代表复制项目/文件夹邮箱事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="d2389-116">Represents the timestamp of a copy item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="d2389-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="d2389-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="d2389-118">表示文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="d2389-118">Represents the identifier of the folder.</span></span>  <br/> |
|[<span data-ttu-id="d2389-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="d2389-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d2389-120">表示项的标识符。</span><span class="sxs-lookup"><span data-stu-id="d2389-120">Represents the identifier of the item.</span></span>  <br/> |
|[<span data-ttu-id="d2389-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="d2389-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="d2389-122">表示包含副本的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="d2389-122">Represents the identifier of the folder that contains the copy.</span></span>  <br/> |
|[<span data-ttu-id="d2389-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="d2389-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="d2389-124">代表复制前原始文件夹的文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="d2389-124">Represents the folder identifier of the original folder before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="d2389-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="d2389-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="d2389-126">包含原始项在复制前的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="d2389-126">Contains the unique identifier of the original item before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="d2389-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="d2389-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="d2389-128">包含已复制的项或文件夹的原始父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="d2389-128">Contains the identifier of the original parent folder of an item or folder that was copied.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d2389-129">父元素</span><span class="sxs-lookup"><span data-stu-id="d2389-129">Parent elements</span></span>

|<span data-ttu-id="d2389-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="d2389-130">**Element**</span></span>|<span data-ttu-id="d2389-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="d2389-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2389-132">通知</span><span class="sxs-lookup"><span data-stu-id="d2389-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d2389-133">包含有关订阅以及上次通知之后发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="d2389-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2389-134">说明</span><span class="sxs-lookup"><span data-stu-id="d2389-134">Remarks</span></span>

<span data-ttu-id="d2389-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d2389-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2389-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="d2389-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2389-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="d2389-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d2389-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="d2389-138">Schema name</span></span>  <br/> |<span data-ttu-id="d2389-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="d2389-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="d2389-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="d2389-140">Validation file</span></span>  <br/> |<span data-ttu-id="d2389-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d2389-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d2389-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="d2389-142">Can be empty</span></span>  <br/> |<span data-ttu-id="d2389-143">False</span><span class="sxs-lookup"><span data-stu-id="d2389-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2389-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2389-144">See also</span></span>

- [<span data-ttu-id="d2389-145">订阅操作</span><span class="sxs-lookup"><span data-stu-id="d2389-145">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="d2389-146">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="d2389-146">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="d2389-147">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="d2389-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="d2389-148">使用请求订阅</span><span class="sxs-lookup"><span data-stu-id="d2389-148">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [<span data-ttu-id="d2389-149">推送通知示例应用程序</span><span class="sxs-lookup"><span data-stu-id="d2389-149">Push Notification Sample Application</span></span>](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

