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
description: 通知元素包含有关订阅的信息的数组以及上次通知之后发生的事件。
ms.openlocfilehash: 88fc56ba6e672e3dea7a1d31f7cc1fda018b9a15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462617"
---
# <a name="notifications"></a><span data-ttu-id="f2a13-103">通知</span><span class="sxs-lookup"><span data-stu-id="f2a13-103">Notifications</span></span>

<span data-ttu-id="f2a13-104">**通知**元素包含有关订阅的信息的数组以及上次通知之后发生的事件。</span><span class="sxs-lookup"><span data-stu-id="f2a13-104">The **Notifications** element contains an array of information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 <span data-ttu-id="f2a13-105">**NonEmptyArrayOfNotificationsType**</span><span class="sxs-lookup"><span data-stu-id="f2a13-105">**NonEmptyArrayOfNotificationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2a13-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f2a13-106">Attributes and elements</span></span>

<span data-ttu-id="f2a13-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f2a13-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2a13-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f2a13-108">Attributes</span></span>

<span data-ttu-id="f2a13-109">无。</span><span class="sxs-lookup"><span data-stu-id="f2a13-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2a13-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f2a13-110">Child elements</span></span>

|<span data-ttu-id="f2a13-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2a13-111">**Element**</span></span>|<span data-ttu-id="f2a13-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2a13-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2a13-113">通知</span><span class="sxs-lookup"><span data-stu-id="f2a13-113">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f2a13-114">包含有关订阅以及上次通知之后发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="f2a13-114">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2a13-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f2a13-115">Parent elements</span></span>

|<span data-ttu-id="f2a13-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2a13-116">**Element**</span></span>|<span data-ttu-id="f2a13-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2a13-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2a13-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f2a13-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="f2a13-119">包含单个[GetStreamingEvents 操作](getstreamingevents-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="f2a13-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f2a13-120">文本值</span><span class="sxs-lookup"><span data-stu-id="f2a13-120">Text value</span></span>

<span data-ttu-id="f2a13-121">无。</span><span class="sxs-lookup"><span data-stu-id="f2a13-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f2a13-122">说明</span><span class="sxs-lookup"><span data-stu-id="f2a13-122">Remarks</span></span>

<span data-ttu-id="f2a13-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f2a13-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2a13-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="f2a13-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2a13-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="f2a13-125">Namespace</span></span>  <br/> |<span data-ttu-id="f2a13-126">https://schemas.microsoft.com/exchange/services/2006/messages 和 https://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="f2a13-126">https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="f2a13-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="f2a13-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f2a13-128">邮件架构;类型架构</span><span class="sxs-lookup"><span data-stu-id="f2a13-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="f2a13-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="f2a13-129">Validation File</span></span>  <br/> |<span data-ttu-id="f2a13-130">消息 .xsd;类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="f2a13-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2a13-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="f2a13-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2a13-132">False</span><span class="sxs-lookup"><span data-stu-id="f2a13-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2a13-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2a13-133">See also</span></span>



[<span data-ttu-id="f2a13-134">GetFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f2a13-134">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="f2a13-135">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f2a13-135">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="f2a13-136">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f2a13-136">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="f2a13-137">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f2a13-137">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="f2a13-138">订阅操作</span><span class="sxs-lookup"><span data-stu-id="f2a13-138">Subscribe operation</span></span>](subscribe-operation.md)

