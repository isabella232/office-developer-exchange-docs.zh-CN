---
title: NewMailEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NewMailEvent
api_type:
- schema
ms.assetid: 45057945-a3ec-4dac-92db-f0dc5fcfc34d
description: NewMailEvent 元素表示邮箱中的一个新的邮件项目时触发的事件。
ms.openlocfilehash: 8df3e4a218a8eaa9d129854e4816a3a43beddafa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826527"
---
# <a name="newmailevent"></a><span data-ttu-id="3dc5a-103">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="3dc5a-103">NewMailEvent</span></span>

<span data-ttu-id="3dc5a-104">**NewMailEvent**元素表示邮箱中的一个新的邮件项目时触发的事件。</span><span class="sxs-lookup"><span data-stu-id="3dc5a-104">The **NewMailEvent** element represents an event that is triggered by a new mail item in a mailbox.</span></span> 
  
```xml
<NewMailEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</NewMailEvent>
```

 <span data-ttu-id="3dc5a-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="3dc5a-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3dc5a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3dc5a-106">Attributes and elements</span></span>

<span data-ttu-id="3dc5a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3dc5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3dc5a-108">属性</span><span class="sxs-lookup"><span data-stu-id="3dc5a-108">Attributes</span></span>

<span data-ttu-id="3dc5a-109">无。</span><span class="sxs-lookup"><span data-stu-id="3dc5a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3dc5a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3dc5a-110">Child elements</span></span>

|<span data-ttu-id="3dc5a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3dc5a-111">**Element**</span></span>|<span data-ttu-id="3dc5a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3dc5a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dc5a-113">水印</span><span class="sxs-lookup"><span data-stu-id="3dc5a-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="3dc5a-114">代表邮箱事件表格中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="3dc5a-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="3dc5a-115">时间戳</span><span class="sxs-lookup"><span data-stu-id="3dc5a-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="3dc5a-116">表示邮箱中的一个新的邮件项目的到达时间的戳。</span><span class="sxs-lookup"><span data-stu-id="3dc5a-116">Represents the timestamp of the arrival of a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3dc5a-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="3dc5a-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3dc5a-118">表示新邮件项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="3dc5a-118">Represents the identifier of a new mail item.</span></span>  <br/> |
|[<span data-ttu-id="3dc5a-119">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="3dc5a-119">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="3dc5a-120">表示新邮件项目的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="3dc5a-120">Represents the identifier of the parent folder of the new mail item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3dc5a-121">父元素</span><span class="sxs-lookup"><span data-stu-id="3dc5a-121">Parent elements</span></span>

|<span data-ttu-id="3dc5a-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="3dc5a-122">**Element**</span></span>|<span data-ttu-id="3dc5a-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="3dc5a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dc5a-124">通知</span><span class="sxs-lookup"><span data-stu-id="3dc5a-124">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3dc5a-125">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="3dc5a-125">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3dc5a-126">备注</span><span class="sxs-lookup"><span data-stu-id="3dc5a-126">Remarks</span></span>

<span data-ttu-id="3dc5a-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3dc5a-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3dc5a-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="3dc5a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3dc5a-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="3dc5a-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3dc5a-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="3dc5a-130">Schema name</span></span>  <br/> |<span data-ttu-id="3dc5a-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="3dc5a-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="3dc5a-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="3dc5a-132">Validation file</span></span>  <br/> |<span data-ttu-id="3dc5a-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3dc5a-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3dc5a-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="3dc5a-134">Can be empty</span></span>  <br/> |<span data-ttu-id="3dc5a-135">False</span><span class="sxs-lookup"><span data-stu-id="3dc5a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3dc5a-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3dc5a-136">See also</span></span>



[<span data-ttu-id="3dc5a-137">订阅操作</span><span class="sxs-lookup"><span data-stu-id="3dc5a-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="3dc5a-138">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="3dc5a-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="3dc5a-139">取消操作</span><span class="sxs-lookup"><span data-stu-id="3dc5a-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)

