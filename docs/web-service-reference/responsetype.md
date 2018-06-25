---
title: ResponseType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseType
api_type:
- schema
ms.assetid: cdc09dda-ce20-4504-880d-9da6025ca812
description: ResponseType 元素均表示接收会议的收件人响应的类型。
ms.openlocfilehash: fcfd47cb988ee00303b2c4205cb3d058cb6599b2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827200"
---
# <a name="responsetype"></a><span data-ttu-id="ece50-103">ResponseType</span><span class="sxs-lookup"><span data-stu-id="ece50-103">ResponseType</span></span>

<span data-ttu-id="ece50-104">**ResponseType**元素均表示接收会议的收件人响应的类型。</span><span class="sxs-lookup"><span data-stu-id="ece50-104">The **ResponseType** element represents the type of recipient response that is received for a meeting.</span></span> 
  
```xml
<ResponseType/>
```

 <span data-ttu-id="ece50-105">**ResponseTypeType**</span><span class="sxs-lookup"><span data-stu-id="ece50-105">**ResponseTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ece50-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ece50-106">Attributes and elements</span></span>

<span data-ttu-id="ece50-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ece50-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ece50-108">属性</span><span class="sxs-lookup"><span data-stu-id="ece50-108">Attributes</span></span>

<span data-ttu-id="ece50-109">无。</span><span class="sxs-lookup"><span data-stu-id="ece50-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ece50-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ece50-110">Child elements</span></span>

<span data-ttu-id="ece50-111">无。</span><span class="sxs-lookup"><span data-stu-id="ece50-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ece50-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ece50-112">Parent elements</span></span>

|<span data-ttu-id="ece50-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ece50-113">**Element**</span></span>|<span data-ttu-id="ece50-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ece50-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ece50-115">参与者</span><span class="sxs-lookup"><span data-stu-id="ece50-115">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="ece50-116">代表与会者和会议的资源。</span><span class="sxs-lookup"><span data-stu-id="ece50-116">Represents attendees and resources for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="ece50-117">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="ece50-117">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="ece50-118">代表 Exchange 存储中的取消会议</span><span class="sxs-lookup"><span data-stu-id="ece50-118">Represents a meeting cancellation in the Exchange store</span></span>  <br/> |
|[<span data-ttu-id="ece50-119">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="ece50-119">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="ece50-120">代表 Exchange 存储中的会议消息。</span><span class="sxs-lookup"><span data-stu-id="ece50-120">Represents a meeting message in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ece50-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ece50-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ece50-122">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="ece50-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ece50-123">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="ece50-123">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="ece50-124">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="ece50-124">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ece50-125">文本值</span><span class="sxs-lookup"><span data-stu-id="ece50-125">Text value</span></span>

<span data-ttu-id="ece50-126">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="ece50-126">A text value is required.</span></span> <span data-ttu-id="ece50-127">此元素的可能的文本值如下：</span><span class="sxs-lookup"><span data-stu-id="ece50-127">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="ece50-128">Unknown</span><span class="sxs-lookup"><span data-stu-id="ece50-128">Unknown</span></span>
    
- <span data-ttu-id="ece50-129">组织者</span><span class="sxs-lookup"><span data-stu-id="ece50-129">Organizer</span></span>
    
- <span data-ttu-id="ece50-130">暂定</span><span class="sxs-lookup"><span data-stu-id="ece50-130">Tentative</span></span>
    
- <span data-ttu-id="ece50-131">Accept</span><span class="sxs-lookup"><span data-stu-id="ece50-131">Accept</span></span>
    
- <span data-ttu-id="ece50-132">拒绝</span><span class="sxs-lookup"><span data-stu-id="ece50-132">Decline</span></span>
    
- <span data-ttu-id="ece50-133">NoResponseReceived</span><span class="sxs-lookup"><span data-stu-id="ece50-133">NoResponseReceived</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ece50-134">备注</span><span class="sxs-lookup"><span data-stu-id="ece50-134">Remarks</span></span>

<span data-ttu-id="ece50-135">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ece50-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ece50-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="ece50-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ece50-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="ece50-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ece50-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="ece50-138">Schema Name</span></span>  <br/> |<span data-ttu-id="ece50-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="ece50-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="ece50-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="ece50-140">Validation File</span></span>  <br/> |<span data-ttu-id="ece50-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ece50-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ece50-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="ece50-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="ece50-143">False</span><span class="sxs-lookup"><span data-stu-id="ece50-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ece50-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ece50-144">See also</span></span>



- [<span data-ttu-id="ece50-145">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ece50-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

