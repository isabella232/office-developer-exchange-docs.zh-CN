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
description: ModifiedEvent 元素均表示修改项目或文件夹的事件。
ms.openlocfilehash: fb464fb0a270d8ca7d33d40e5425e260970b2f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826482"
---
# <a name="modifiedevent"></a><span data-ttu-id="7c807-103">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="7c807-103">ModifiedEvent</span></span>

<span data-ttu-id="7c807-104">**ModifiedEvent**元素均表示修改项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="7c807-104">The **ModifiedEvent** element represents an event in which an item or folder is modified.</span></span> 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

 <span data-ttu-id="7c807-105">**ModifiedEventType**</span><span class="sxs-lookup"><span data-stu-id="7c807-105">**ModifiedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7c807-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7c807-106">Attributes and elements</span></span>

<span data-ttu-id="7c807-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7c807-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c807-108">属性</span><span class="sxs-lookup"><span data-stu-id="7c807-108">Attributes</span></span>

<span data-ttu-id="7c807-109">无。</span><span class="sxs-lookup"><span data-stu-id="7c807-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c807-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7c807-110">Child elements</span></span>

|<span data-ttu-id="7c807-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7c807-111">**Element**</span></span>|<span data-ttu-id="7c807-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7c807-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c807-113">水印</span><span class="sxs-lookup"><span data-stu-id="7c807-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="7c807-114">代表邮箱事件表格中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="7c807-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="7c807-115">时间戳</span><span class="sxs-lookup"><span data-stu-id="7c807-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="7c807-116">代表一个已修改的项或文件夹邮箱事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="7c807-116">Represents the timestamp of a modified item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="7c807-117">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="7c807-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="7c807-118">表示修改文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="7c807-118">Represents the identifier of the modified folder.</span></span>  <br/> |
|[<span data-ttu-id="7c807-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="7c807-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="7c807-120">代表已修改的项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="7c807-120">Represents the identifier of the modified item.</span></span>  <br/> |
|[<span data-ttu-id="7c807-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="7c807-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="7c807-122">表示已修改的项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="7c807-122">Represents the identifier of the parent folder of the modified item or folder.</span></span>  <br/> |
|[<span data-ttu-id="7c807-123">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="7c807-123">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="7c807-124">表示给定文件夹中未读项目的计数。</span><span class="sxs-lookup"><span data-stu-id="7c807-124">Represents the count of unread items within a given folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7c807-125">父元素</span><span class="sxs-lookup"><span data-stu-id="7c807-125">Parent elements</span></span>

|<span data-ttu-id="7c807-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="7c807-126">**Element**</span></span>|<span data-ttu-id="7c807-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="7c807-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c807-128">通知</span><span class="sxs-lookup"><span data-stu-id="7c807-128">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7c807-129">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="7c807-129">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c807-130">备注</span><span class="sxs-lookup"><span data-stu-id="7c807-130">Remarks</span></span>

<span data-ttu-id="7c807-131">为文件夹中的项目的每次修改生成两个已修改的事件。</span><span class="sxs-lookup"><span data-stu-id="7c807-131">Two modified events are generated for each modification of an item in a folder.</span></span> <span data-ttu-id="7c807-132">一个事件是与更改的项相关的。</span><span class="sxs-lookup"><span data-stu-id="7c807-132">One event is relevant to the item that changed.</span></span> <span data-ttu-id="7c807-133">与项目的父文件夹相关其他事件。</span><span class="sxs-lookup"><span data-stu-id="7c807-133">The other event is relevant to the parent folder of the item.</span></span> <span data-ttu-id="7c807-134">这是针对创建订阅的同一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="7c807-134">This is the same folder that the subscription was created against.</span></span> <span data-ttu-id="7c807-135">与文件夹关联的事件用于通信的潜在更改到的文件夹的[UnreadCount](unreadcount.md)属性。</span><span class="sxs-lookup"><span data-stu-id="7c807-135">The event that is associated with the folder is used to communicate a potential change to the [UnreadCount](unreadcount.md) property on the folder.</span></span> 
  
<span data-ttu-id="7c807-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7c807-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c807-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="7c807-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c807-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="7c807-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7c807-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="7c807-139">Schema name</span></span>  <br/> |<span data-ttu-id="7c807-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="7c807-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="7c807-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="7c807-141">Validation file</span></span>  <br/> |<span data-ttu-id="7c807-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7c807-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7c807-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="7c807-143">Can be empty</span></span>  <br/> |<span data-ttu-id="7c807-144">False</span><span class="sxs-lookup"><span data-stu-id="7c807-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c807-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7c807-145">See also</span></span>



[<span data-ttu-id="7c807-146">订阅操作</span><span class="sxs-lookup"><span data-stu-id="7c807-146">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="7c807-147">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="7c807-147">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="7c807-148">取消操作</span><span class="sxs-lookup"><span data-stu-id="7c807-148">Unsubscribe operation</span></span>](unsubscribe-operation.md)

