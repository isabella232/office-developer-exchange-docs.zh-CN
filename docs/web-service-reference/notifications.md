---
title: 通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notifications
api_type:
- schema
ms.assetid: 153cc420-d2fe-42f1-afb2-9a31ee09a750
description: 通知元素包含一个数组订阅和自上次通知以来发生的事件有关的信息。
ms.openlocfilehash: f576bf579c91b77dcde8646a6af7fdc47145aef7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826550"
---
# <a name="notifications"></a><span data-ttu-id="33329-103">通知</span><span class="sxs-lookup"><span data-stu-id="33329-103">Notifications</span></span>

<span data-ttu-id="33329-104">**通知**元素包含一个数组订阅和自上次通知以来发生的事件有关的信息。</span><span class="sxs-lookup"><span data-stu-id="33329-104">The **Notifications** element contains an array of information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 <span data-ttu-id="33329-105">**NonEmptyArrayOfNotificationsType**</span><span class="sxs-lookup"><span data-stu-id="33329-105">**NonEmptyArrayOfNotificationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33329-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="33329-106">Attributes and elements</span></span>

<span data-ttu-id="33329-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="33329-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33329-108">属性</span><span class="sxs-lookup"><span data-stu-id="33329-108">Attributes</span></span>

<span data-ttu-id="33329-109">无。</span><span class="sxs-lookup"><span data-stu-id="33329-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="33329-110">子元素</span><span class="sxs-lookup"><span data-stu-id="33329-110">Child elements</span></span>

|<span data-ttu-id="33329-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="33329-111">**Element**</span></span>|<span data-ttu-id="33329-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="33329-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33329-113">通知</span><span class="sxs-lookup"><span data-stu-id="33329-113">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="33329-114">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="33329-114">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="33329-115">父元素</span><span class="sxs-lookup"><span data-stu-id="33329-115">Parent elements</span></span>

|<span data-ttu-id="33329-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="33329-116">**Element**</span></span>|<span data-ttu-id="33329-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="33329-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33329-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="33329-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="33329-119">包含状态和的单个结果[GetStreamingEvents 操作](getstreamingevents-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="33329-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="33329-120">文本值</span><span class="sxs-lookup"><span data-stu-id="33329-120">Text value</span></span>

<span data-ttu-id="33329-121">无。</span><span class="sxs-lookup"><span data-stu-id="33329-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="33329-122">备注</span><span class="sxs-lookup"><span data-stu-id="33329-122">Remarks</span></span>

<span data-ttu-id="33329-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="33329-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33329-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="33329-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33329-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="33329-125">Namespace</span></span>  <br/> |<span data-ttu-id="33329-126">http://schemas.microsoft.com/exchange/services/2006/messages 和 http://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="33329-126">http://schemas.microsoft.com/exchange/services/2006/messages and http://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="33329-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="33329-127">Schema Name</span></span>  <br/> |<span data-ttu-id="33329-128">邮件架构;类型架构</span><span class="sxs-lookup"><span data-stu-id="33329-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="33329-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="33329-129">Validation File</span></span>  <br/> |<span data-ttu-id="33329-130">Messages.xsd;Types.xsd</span><span class="sxs-lookup"><span data-stu-id="33329-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="33329-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="33329-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="33329-132">False</span><span class="sxs-lookup"><span data-stu-id="33329-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33329-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="33329-133">See also</span></span>



[<span data-ttu-id="33329-134">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="33329-134">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="33329-135">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="33329-135">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="33329-136">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="33329-136">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="33329-137">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="33329-137">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="33329-138">订阅操作</span><span class="sxs-lookup"><span data-stu-id="33329-138">Subscribe operation</span></span>](subscribe-operation.md)

