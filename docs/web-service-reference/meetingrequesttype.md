---
title: MeetingRequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: MeetingRequestType 元素描述会议请求的类型。
ms.openlocfilehash: 7269587e2fa72aeb9070a7b53ee9215829729329
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826432"
---
# <a name="meetingrequesttype"></a><span data-ttu-id="49fa0-103">MeetingRequestType</span><span class="sxs-lookup"><span data-stu-id="49fa0-103">MeetingRequestType</span></span>

<span data-ttu-id="49fa0-104">**MeetingRequestType**元素描述会议请求的类型。</span><span class="sxs-lookup"><span data-stu-id="49fa0-104">The **MeetingRequestType** element describes the type of the meeting request.</span></span> 
  
```xml
<MeetingRequestType/>
```

 <span data-ttu-id="49fa0-105">**MeetingRequestTypeType**</span><span class="sxs-lookup"><span data-stu-id="49fa0-105">**MeetingRequestTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49fa0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="49fa0-106">Attributes and elements</span></span>

<span data-ttu-id="49fa0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="49fa0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49fa0-108">属性</span><span class="sxs-lookup"><span data-stu-id="49fa0-108">Attributes</span></span>

<span data-ttu-id="49fa0-109">无。</span><span class="sxs-lookup"><span data-stu-id="49fa0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49fa0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="49fa0-110">Child elements</span></span>

<span data-ttu-id="49fa0-111">无。</span><span class="sxs-lookup"><span data-stu-id="49fa0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="49fa0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="49fa0-112">Parent elements</span></span>

|<span data-ttu-id="49fa0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="49fa0-113">**Element**</span></span>|<span data-ttu-id="49fa0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="49fa0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49fa0-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="49fa0-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="49fa0-116">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="49fa0-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="49fa0-117">文本值</span><span class="sxs-lookup"><span data-stu-id="49fa0-117">Text value</span></span>

<span data-ttu-id="49fa0-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="49fa0-118">A text value is required.</span></span> <span data-ttu-id="49fa0-119">下表列出了此元素的可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="49fa0-119">The following table lists the possible text values for this element.</span></span>
  
|<span data-ttu-id="49fa0-120">**值**</span><span class="sxs-lookup"><span data-stu-id="49fa0-120">**Value**</span></span>|<span data-ttu-id="49fa0-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="49fa0-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="49fa0-122">FullUpdate</span><span class="sxs-lookup"><span data-stu-id="49fa0-122">FullUpdate</span></span>  <br/> |<span data-ttu-id="49fa0-123">标识为完全更新现有请求的会议请求。</span><span class="sxs-lookup"><span data-stu-id="49fa0-123">Identifies the meeting request as a full update to an existing request.</span></span> <span data-ttu-id="49fa0-124">完全更新具有更新时间和信息性内容。</span><span class="sxs-lookup"><span data-stu-id="49fa0-124">A full update has updated time and informational content.</span></span>  <br/> |
|<span data-ttu-id="49fa0-125">InformationalUpdate</span><span class="sxs-lookup"><span data-stu-id="49fa0-125">InformationalUpdate</span></span>  <br/> |<span data-ttu-id="49fa0-126">标识会议请求，如仅包含更新的信息性内容。</span><span class="sxs-lookup"><span data-stu-id="49fa0-126">Identifies the meeting request as only containing updated informational content.</span></span>  <br/> |
|<span data-ttu-id="49fa0-127">NewMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="49fa0-127">NewMeetingRequest</span></span>  <br/> |<span data-ttu-id="49fa0-128">标识为新的会议请求的会议请求。</span><span class="sxs-lookup"><span data-stu-id="49fa0-128">Identifies the meeting request as a new meeting request.</span></span>  <br/> |
|<span data-ttu-id="49fa0-129">无</span><span class="sxs-lookup"><span data-stu-id="49fa0-129">None</span></span>  <br/> |<span data-ttu-id="49fa0-130">指示会议请求类型未定义。</span><span class="sxs-lookup"><span data-stu-id="49fa0-130">Indicates that the meeting request type is not defined.</span></span>  <br/> |
|<span data-ttu-id="49fa0-131">过时</span><span class="sxs-lookup"><span data-stu-id="49fa0-131">Outdated</span></span>  <br/> |<span data-ttu-id="49fa0-132">标识为过时的会议请求。</span><span class="sxs-lookup"><span data-stu-id="49fa0-132">Identifies the meeting request as outdated.</span></span>  <br/> |
|<span data-ttu-id="49fa0-133">PrincipalWantsCopy</span><span class="sxs-lookup"><span data-stu-id="49fa0-133">PrincipalWantsCopy</span></span>  <br/> |<span data-ttu-id="49fa0-134">指示会议请求所属的主体用户已将会议邮件转发给代理人，并且包含标记，信息性其副本。</span><span class="sxs-lookup"><span data-stu-id="49fa0-134">Indicates that the meeting request belongs to a principal who has forwarded meeting messages to a delegate and has his copies marked as informational.</span></span>  <br/> |
|<span data-ttu-id="49fa0-135">SilentUpdate</span><span class="sxs-lookup"><span data-stu-id="49fa0-135">SilentUpdate</span></span>  <br/> |<span data-ttu-id="49fa0-136">标识为向现有会议的无提示更新会议请求。</span><span class="sxs-lookup"><span data-stu-id="49fa0-136">Identifies the meeting request as a silent update to an existing meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49fa0-137">注解</span><span class="sxs-lookup"><span data-stu-id="49fa0-137">Remarks</span></span>

<span data-ttu-id="49fa0-138">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="49fa0-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49fa0-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="49fa0-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49fa0-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="49fa0-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49fa0-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="49fa0-141">Schema Name</span></span>  <br/> |<span data-ttu-id="49fa0-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="49fa0-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="49fa0-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="49fa0-143">Validation File</span></span>  <br/> |<span data-ttu-id="49fa0-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="49fa0-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49fa0-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="49fa0-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="49fa0-146">False</span><span class="sxs-lookup"><span data-stu-id="49fa0-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49fa0-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="49fa0-147">See also</span></span>



- [<span data-ttu-id="49fa0-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="49fa0-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

