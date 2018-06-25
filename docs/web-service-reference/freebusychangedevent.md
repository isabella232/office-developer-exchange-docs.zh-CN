---
title: FreeBusyChangedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyChangedEvent
api_type:
- schema
ms.assetid: 63abbfc5-c29f-4110-a922-6b1247187f28
description: FreeBusyChangedEvent 元素表示项目的忙/闲时间已发生更改的事件。
ms.openlocfilehash: 7271d375526e7614d0150594c2b988666a59eb8d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754427"
---
# <a name="freebusychangedevent"></a><span data-ttu-id="0ab1d-103">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="0ab1d-103">FreeBusyChangedEvent</span></span>

<span data-ttu-id="0ab1d-104">**FreeBusyChangedEvent**元素表示项目的忙/闲时间已发生更改的事件。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-104">The **FreeBusyChangedEvent** element represents an event in which an item's free/busy time has changed.</span></span> 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

 <span data-ttu-id="0ab1d-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="0ab1d-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ab1d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0ab1d-106">Attributes and elements</span></span>

<span data-ttu-id="0ab1d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ab1d-108">属性</span><span class="sxs-lookup"><span data-stu-id="0ab1d-108">Attributes</span></span>

<span data-ttu-id="0ab1d-109">无。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ab1d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0ab1d-110">Child elements</span></span>

|<span data-ttu-id="0ab1d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0ab1d-111">**Element**</span></span>|<span data-ttu-id="0ab1d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0ab1d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ab1d-113">水印</span><span class="sxs-lookup"><span data-stu-id="0ab1d-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="0ab1d-114">代表邮箱事件表格中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="0ab1d-115">时间戳</span><span class="sxs-lookup"><span data-stu-id="0ab1d-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="0ab1d-116">表示忙/闲项目邮箱事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-116">Represents the timestamp of a free/busy item mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="0ab1d-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="0ab1d-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="0ab1d-118">代表忙/闲项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-118">Represents the identifier of the free/busy item.</span></span>  <br/> |
|[<span data-ttu-id="0ab1d-119">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="0ab1d-119">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="0ab1d-120">表示的忙/闲信息的项目的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-120">Represents the identifier of the parent folder of the free/busy item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ab1d-121">父元素</span><span class="sxs-lookup"><span data-stu-id="0ab1d-121">Parent elements</span></span>

|<span data-ttu-id="0ab1d-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="0ab1d-122">**Element**</span></span>|<span data-ttu-id="0ab1d-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="0ab1d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ab1d-124">通知</span><span class="sxs-lookup"><span data-stu-id="0ab1d-124">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0ab1d-125">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-125">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0ab1d-126">文本值</span><span class="sxs-lookup"><span data-stu-id="0ab1d-126">Text value</span></span>

<span data-ttu-id="0ab1d-127">无。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ab1d-128">备注</span><span class="sxs-lookup"><span data-stu-id="0ab1d-128">Remarks</span></span>

<span data-ttu-id="0ab1d-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0ab1d-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ab1d-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="0ab1d-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ab1d-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="0ab1d-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0ab1d-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="0ab1d-132">Schema name</span></span>  <br/> |<span data-ttu-id="0ab1d-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="0ab1d-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="0ab1d-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="0ab1d-134">Validation file</span></span>  <br/> |<span data-ttu-id="0ab1d-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0ab1d-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0ab1d-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="0ab1d-136">Can be empty</span></span>  <br/> |<span data-ttu-id="0ab1d-137">False</span><span class="sxs-lookup"><span data-stu-id="0ab1d-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ab1d-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0ab1d-138">See also</span></span>



[<span data-ttu-id="0ab1d-139">订阅操作</span><span class="sxs-lookup"><span data-stu-id="0ab1d-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="0ab1d-140">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="0ab1d-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="0ab1d-141">取消操作</span><span class="sxs-lookup"><span data-stu-id="0ab1d-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="0ab1d-142">使用请求订阅</span><span class="sxs-lookup"><span data-stu-id="0ab1d-142">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="0ab1d-143">EWS 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="0ab1d-143">Event notifications in EWS</span></span>](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)

