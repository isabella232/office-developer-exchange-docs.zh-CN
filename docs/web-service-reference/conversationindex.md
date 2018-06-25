---
title: ConversationIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationIndex
api_type:
- schema
ms.assetid: fdf47e22-8d93-4ae4-883b-0c9f07f48724
description: ConversationIndex 元素包含表示此消息所属的主题的二进制 ID。
ms.openlocfilehash: 3f4f72224269717325d2fbf56f0a25fab20352a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753581"
---
# <a name="conversationindex"></a><span data-ttu-id="9e31c-103">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="9e31c-103">ConversationIndex</span></span>

<span data-ttu-id="9e31c-104">**ConversationIndex**元素包含表示此消息所属的主题的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="9e31c-104">The **ConversationIndex** element contains a binary ID that represents the thread to which this message belongs.</span></span> 
  
```xml
<ConversationIndex/>
```

 <span data-ttu-id="9e31c-105">**Base64Binary**</span><span class="sxs-lookup"><span data-stu-id="9e31c-105">**Base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e31c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9e31c-106">Attributes and elements</span></span>

<span data-ttu-id="9e31c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9e31c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e31c-108">属性</span><span class="sxs-lookup"><span data-stu-id="9e31c-108">Attributes</span></span>

<span data-ttu-id="9e31c-109">无。</span><span class="sxs-lookup"><span data-stu-id="9e31c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9e31c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9e31c-110">Child elements</span></span>

<span data-ttu-id="9e31c-111">无。</span><span class="sxs-lookup"><span data-stu-id="9e31c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9e31c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9e31c-112">Parent elements</span></span>

|<span data-ttu-id="9e31c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9e31c-113">**Element**</span></span>|<span data-ttu-id="9e31c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9e31c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e31c-115">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="9e31c-115">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="9e31c-116">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="9e31c-116">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-117">Message</span><span class="sxs-lookup"><span data-stu-id="9e31c-117">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9e31c-118">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="9e31c-118">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-119">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="9e31c-119">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="9e31c-120">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="9e31c-120">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="9e31c-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="9e31c-122">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="9e31c-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-123">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="9e31c-123">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="9e31c-124">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="9e31c-124">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-125">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="9e31c-125">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="9e31c-126">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="9e31c-126">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-127">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="9e31c-127">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="9e31c-128">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="9e31c-128">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-129">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="9e31c-129">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="9e31c-130">表示暂时接受的会议请求答复。</span><span class="sxs-lookup"><span data-stu-id="9e31c-130">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-131">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="9e31c-131">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="9e31c-132">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="9e31c-132">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-133">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="9e31c-133">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="9e31c-134">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="9e31c-134">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-135">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="9e31c-135">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="9e31c-136">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="9e31c-136">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-137">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="9e31c-137">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="9e31c-138">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="9e31c-138">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-139">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="9e31c-139">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="9e31c-140">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="9e31c-140">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="9e31c-141">PostItem</span><span class="sxs-lookup"><span data-stu-id="9e31c-141">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="9e31c-142">代表一个 Exchange 存储中的公告项目。</span><span class="sxs-lookup"><span data-stu-id="9e31c-142">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="9e31c-143">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9e31c-143">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9e31c-144">文本值</span><span class="sxs-lookup"><span data-stu-id="9e31c-144">Text value</span></span>

<span data-ttu-id="9e31c-145">文本值表示的二进制格式**Base64Binary**标识符。</span><span class="sxs-lookup"><span data-stu-id="9e31c-145">The text value represents a binary identifier in **Base64Binary** format.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9e31c-146">注解</span><span class="sxs-lookup"><span data-stu-id="9e31c-146">Remarks</span></span>

<span data-ttu-id="9e31c-147">描述此元素的架构位于 Exchange 服务器已安装了客户端访问服务器角色的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9e31c-147">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e31c-148">元素信息</span><span class="sxs-lookup"><span data-stu-id="9e31c-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e31c-149">命名空间</span><span class="sxs-lookup"><span data-stu-id="9e31c-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9e31c-150">架构名称</span><span class="sxs-lookup"><span data-stu-id="9e31c-150">Schema Name</span></span>  <br/> |<span data-ttu-id="9e31c-151">类型架构</span><span class="sxs-lookup"><span data-stu-id="9e31c-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="9e31c-152">验证文件</span><span class="sxs-lookup"><span data-stu-id="9e31c-152">Validation File</span></span>  <br/> |<span data-ttu-id="9e31c-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9e31c-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9e31c-154">可以为空</span><span class="sxs-lookup"><span data-stu-id="9e31c-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="9e31c-155">False</span><span class="sxs-lookup"><span data-stu-id="9e31c-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e31c-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9e31c-156">See also</span></span>



- [<span data-ttu-id="9e31c-157">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9e31c-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

