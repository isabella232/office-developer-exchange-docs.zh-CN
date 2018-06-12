---
title: CreatedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreatedEvent
api_type:
- schema
ms.assetid: f0e53a53-c352-42a5-8280-cd808b0e961b
description: CreatedEvent 元素表示在其中创建项目或文件夹的事件。
ms.openlocfilehash: f52516090d0789b4dd9fc1ced824786ce000e885
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753632"
---
# <a name="createdevent"></a><span data-ttu-id="1756c-103">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="1756c-103">CreatedEvent</span></span>

<span data-ttu-id="1756c-104">**CreatedEvent**元素表示在其中创建项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="1756c-104">The **CreatedEvent** element represents an event in which an item or folder is created.</span></span> 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

 <span data-ttu-id="1756c-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="1756c-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1756c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1756c-106">Attributes and elements</span></span>

<span data-ttu-id="1756c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1756c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1756c-108">属性</span><span class="sxs-lookup"><span data-stu-id="1756c-108">Attributes</span></span>

<span data-ttu-id="1756c-109">无。</span><span class="sxs-lookup"><span data-stu-id="1756c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1756c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1756c-110">Child elements</span></span>

|<span data-ttu-id="1756c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1756c-111">**Element**</span></span>|<span data-ttu-id="1756c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1756c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1756c-113">水印</span><span class="sxs-lookup"><span data-stu-id="1756c-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="1756c-114">代表邮箱事件表格中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="1756c-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="1756c-115">时间戳</span><span class="sxs-lookup"><span data-stu-id="1756c-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="1756c-116">代表一个创建的项目或文件夹邮箱事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="1756c-116">Represents the timestamp of a created item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="1756c-117">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="1756c-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="1756c-118">表示创建的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="1756c-118">Represents the identifier of the created folder.</span></span>  <br/> |
|[<span data-ttu-id="1756c-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="1756c-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="1756c-120">代表创建项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="1756c-120">Represents the identifier of the created item.</span></span>  <br/> |
|[<span data-ttu-id="1756c-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="1756c-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="1756c-122">表示创建的项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="1756c-122">Represents the identifier of the parent folder of the created item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1756c-123">父元素</span><span class="sxs-lookup"><span data-stu-id="1756c-123">Parent elements</span></span>

|<span data-ttu-id="1756c-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="1756c-124">**Element**</span></span>|<span data-ttu-id="1756c-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="1756c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1756c-126">通知</span><span class="sxs-lookup"><span data-stu-id="1756c-126">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1756c-127">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="1756c-127">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1756c-128">备注</span><span class="sxs-lookup"><span data-stu-id="1756c-128">Remarks</span></span>

<span data-ttu-id="1756c-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1756c-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1756c-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="1756c-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1756c-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="1756c-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1756c-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="1756c-132">Schema name</span></span>  <br/> |<span data-ttu-id="1756c-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="1756c-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="1756c-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="1756c-134">Validation file</span></span>  <br/> |<span data-ttu-id="1756c-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1756c-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1756c-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="1756c-136">Can be empty</span></span>  <br/> |<span data-ttu-id="1756c-137">False</span><span class="sxs-lookup"><span data-stu-id="1756c-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1756c-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1756c-138">See also</span></span>



[<span data-ttu-id="1756c-139">订阅操作</span><span class="sxs-lookup"><span data-stu-id="1756c-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="1756c-140">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="1756c-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="1756c-141">取消操作</span><span class="sxs-lookup"><span data-stu-id="1756c-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="1756c-142">使用请求订阅</span><span class="sxs-lookup"><span data-stu-id="1756c-142">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="1756c-143">EWS 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="1756c-143">Event notifications in EWS</span></span>](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)

