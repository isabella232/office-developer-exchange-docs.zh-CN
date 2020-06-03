---
title: ModifiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedEvent
api_type:
- schema
ms.assetid: ca1309f4-2df7-4289-811c-75c3db0e7072
description: ModifiedEvent 元素表示在其中修改项或文件夹的事件。
ms.openlocfilehash: 1a798773601a0857b9064c7fa6a532a7a36517ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468549"
---
# <a name="modifiedevent"></a><span data-ttu-id="baebb-103">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="baebb-103">ModifiedEvent</span></span>

<span data-ttu-id="baebb-104">**ModifiedEvent**元素表示在其中修改项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="baebb-104">The **ModifiedEvent** element represents an event in which an item or folder is modified.</span></span> 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/> 
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

<span data-ttu-id="baebb-105">**ModifiedEventType**</span><span class="sxs-lookup"><span data-stu-id="baebb-105">**ModifiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="baebb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="baebb-106">Attributes and elements</span></span>

<span data-ttu-id="baebb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="baebb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="baebb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="baebb-108">Attributes</span></span>

<span data-ttu-id="baebb-109">无。</span><span class="sxs-lookup"><span data-stu-id="baebb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="baebb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="baebb-110">Child elements</span></span>

|<span data-ttu-id="baebb-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="baebb-111">**Element**</span></span>|<span data-ttu-id="baebb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="baebb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baebb-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="baebb-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="baebb-114">表示邮箱事件表中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="baebb-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="baebb-115">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="baebb-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="baebb-116">表示已修改的项目或文件夹邮箱事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="baebb-116">Represents the timestamp of a modified item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="baebb-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="baebb-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="baebb-118">表示已修改文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="baebb-118">Represents the identifier of the modified folder.</span></span>  <br/> |
|[<span data-ttu-id="baebb-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="baebb-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="baebb-120">表示已修改的项的标识符。</span><span class="sxs-lookup"><span data-stu-id="baebb-120">Represents the identifier of the modified item.</span></span>  <br/> |
|[<span data-ttu-id="baebb-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="baebb-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="baebb-122">表示已修改的项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="baebb-122">Represents the identifier of the parent folder of the modified item or folder.</span></span>  <br/> |
|[<span data-ttu-id="baebb-123">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="baebb-123">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="baebb-124">表示给定文件夹中未读项目的计数。</span><span class="sxs-lookup"><span data-stu-id="baebb-124">Represents the count of unread items within a given folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="baebb-125">父元素</span><span class="sxs-lookup"><span data-stu-id="baebb-125">Parent elements</span></span>

|<span data-ttu-id="baebb-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="baebb-126">**Element**</span></span>|<span data-ttu-id="baebb-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="baebb-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baebb-128">通知</span><span class="sxs-lookup"><span data-stu-id="baebb-128">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="baebb-129">包含有关订阅以及上次通知之后发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="baebb-129">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="baebb-130">备注</span><span class="sxs-lookup"><span data-stu-id="baebb-130">Remarks</span></span>

<span data-ttu-id="baebb-131">为文件夹中的项目的每个修改生成两个修改的事件。</span><span class="sxs-lookup"><span data-stu-id="baebb-131">Two modified events are generated for each modification of an item in a folder.</span></span> <span data-ttu-id="baebb-132">一个事件与已更改的项目相关。</span><span class="sxs-lookup"><span data-stu-id="baebb-132">One event is relevant to the item that changed.</span></span> <span data-ttu-id="baebb-133">另一个事件与项目的父文件夹相关。</span><span class="sxs-lookup"><span data-stu-id="baebb-133">The other event is relevant to the parent folder of the item.</span></span> <span data-ttu-id="baebb-134">此文件夹与创建订阅所用的文件夹相同。</span><span class="sxs-lookup"><span data-stu-id="baebb-134">This is the same folder that the subscription was created against.</span></span> <span data-ttu-id="baebb-135">与该文件夹相关联的事件用于将潜在更改传递给文件夹的[UnreadCount](unreadcount.md)属性。</span><span class="sxs-lookup"><span data-stu-id="baebb-135">The event that is associated with the folder is used to communicate a potential change to the [UnreadCount](unreadcount.md) property on the folder.</span></span> 
  
<span data-ttu-id="baebb-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="baebb-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="baebb-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="baebb-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="baebb-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="baebb-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="baebb-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="baebb-139">Schema name</span></span>  <br/> |<span data-ttu-id="baebb-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="baebb-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="baebb-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="baebb-141">Validation file</span></span>  <br/> |<span data-ttu-id="baebb-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="baebb-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="baebb-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="baebb-143">Can be empty</span></span>  <br/> |<span data-ttu-id="baebb-144">False</span><span class="sxs-lookup"><span data-stu-id="baebb-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="baebb-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="baebb-145">See also</span></span>

- [<span data-ttu-id="baebb-146">订阅操作</span><span class="sxs-lookup"><span data-stu-id="baebb-146">Subscribe operation</span></span>](subscribe-operation.md)  
- [<span data-ttu-id="baebb-147">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="baebb-147">GetEvents operation</span></span>](getevents-operation.md)  
- [<span data-ttu-id="baebb-148">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="baebb-148">Unsubscribe operation</span></span>](unsubscribe-operation.md)

