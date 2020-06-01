---
title: ConversationId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationId
api_type:
- schema
ms.assetid: d5f1ddb3-9af3-4677-a6ba-111b304a951e
description: ConversationId 元素包含项或对话的标识符。
ms.openlocfilehash: 4f12d70ae6b72773760a731f5778cf6743ce699f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461469"
---
# <a name="conversationid"></a><span data-ttu-id="4e800-103">ConversationId</span><span class="sxs-lookup"><span data-stu-id="4e800-103">ConversationId</span></span>

<span data-ttu-id="4e800-104">**ConversationId**元素包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="4e800-104">The **ConversationId** element contains the identifier of an item or conversation.</span></span> 
  
```XML
<ConversationId Id="" ChangeKey="" />
```

 <span data-ttu-id="4e800-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="4e800-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e800-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4e800-106">Attributes and elements</span></span>

<span data-ttu-id="4e800-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4e800-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e800-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4e800-108">Attributes</span></span>

|<span data-ttu-id="4e800-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="4e800-109">**Attribute**</span></span>|<span data-ttu-id="4e800-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e800-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e800-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="4e800-111">**Id**</span></span> <br/> |<span data-ttu-id="4e800-112">标识 Exchange 存储中的特定项目。</span><span class="sxs-lookup"><span data-stu-id="4e800-112">Identifies a specific item in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="4e800-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="4e800-113">**ChangeKey**</span></span> <br/> | <span data-ttu-id="4e800-114">标识项目的特定版本。</span><span class="sxs-lookup"><span data-stu-id="4e800-114">Identifies a specific version of an item.</span></span> <span data-ttu-id="4e800-115">在以下情况下， **ChangeKey**是必需的：</span><span class="sxs-lookup"><span data-stu-id="4e800-115">A **ChangeKey** is required for the following scenarios:</span></span>  <br/><br/><span data-ttu-id="4e800-116">-如果**ConflictResolution**属性设置为 "自动解析"，则[UpdateItem](updateitem.md)元素需要**ChangeKey** 。</span><span class="sxs-lookup"><span data-stu-id="4e800-116">- The [UpdateItem](updateitem.md) element requires a **ChangeKey** if the **ConflictResolution** attribute is set to AutoResolve.</span></span> <span data-ttu-id="4e800-117">"自动解析" 是默认值。</span><span class="sxs-lookup"><span data-stu-id="4e800-117">AutoResolve is a default value.</span></span> <span data-ttu-id="4e800-118">如果不包含**ChangeKey**属性，则响应将返回一个等于**ErrorChangeKeyRequired**的[ResponseCode](responsecode.md)值。</span><span class="sxs-lookup"><span data-stu-id="4e800-118">If the **ChangeKey** attribute is not included, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorChangeKeyRequired**.</span></span><br/><br/><span data-ttu-id="4e800-119">- [SendItem](senditem.md)、 [DeleteItem](deleteitem.md)和[DeleteFolder](deletefolder.md)元素需要一个**ChangeKey**来测试所尝试的操作是否将对项目的最新版本进行操作。</span><span class="sxs-lookup"><span data-stu-id="4e800-119">- [SendItem](senditem.md), [DeleteItem](deleteitem.md), and [DeleteFolder](deletefolder.md) elements require a **ChangeKey** to test whether the attempted operation will act upon the most recent version of an item.</span></span> <span data-ttu-id="4e800-120">如果**ChangeKey**属性未包含在**ItemId**中，或者如果**ChangeKey**为空，响应将返回一个等于**ErrorStaleObject**的[ResponseCode](responsecode.md)值。</span><span class="sxs-lookup"><span data-stu-id="4e800-120">If the **ChangeKey** attribute is not included in the **ItemId** or if the **ChangeKey** is empty, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorStaleObject**.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4e800-121">子元素</span><span class="sxs-lookup"><span data-stu-id="4e800-121">Child elements</span></span>

<span data-ttu-id="4e800-122">无。</span><span class="sxs-lookup"><span data-stu-id="4e800-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4e800-123">父元素</span><span class="sxs-lookup"><span data-stu-id="4e800-123">Parent elements</span></span>

|<span data-ttu-id="4e800-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e800-124">**Element**</span></span>|<span data-ttu-id="4e800-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e800-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e800-126">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4e800-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4e800-127">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="4e800-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="4e800-128">Contact</span><span class="sxs-lookup"><span data-stu-id="4e800-128">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="4e800-129">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="4e800-129">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="4e800-130">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="4e800-130">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="4e800-131">代表要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="4e800-131">Represents a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="4e800-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="4e800-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="4e800-133">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="4e800-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="4e800-134">项目</span><span class="sxs-lookup"><span data-stu-id="4e800-134">Item</span></span>](item.md) <br/> |<span data-ttu-id="4e800-135">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="4e800-135">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e800-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="4e800-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="4e800-137">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="4e800-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e800-138">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="4e800-138">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="4e800-139">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="4e800-139">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e800-140">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4e800-140">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4e800-141">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="4e800-141">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e800-142">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="4e800-142">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="4e800-143">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="4e800-143">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e800-144">Message</span><span class="sxs-lookup"><span data-stu-id="4e800-144">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4e800-145">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4e800-145">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="4e800-146">PostItem</span><span class="sxs-lookup"><span data-stu-id="4e800-146">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="4e800-147">表示 Exchange 存储中的公告项。</span><span class="sxs-lookup"><span data-stu-id="4e800-147">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e800-148">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="4e800-148">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="4e800-149">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="4e800-149">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e800-150">任务</span><span class="sxs-lookup"><span data-stu-id="4e800-150">Task</span></span>](task.md) <br/> |<span data-ttu-id="4e800-151">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="4e800-151">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e800-152">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="4e800-152">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="4e800-153">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="4e800-153">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4e800-154">文本值</span><span class="sxs-lookup"><span data-stu-id="4e800-154">Text value</span></span>

<span data-ttu-id="4e800-155">无。</span><span class="sxs-lookup"><span data-stu-id="4e800-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e800-156">说明</span><span class="sxs-lookup"><span data-stu-id="4e800-156">Remarks</span></span>

<span data-ttu-id="4e800-157">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4e800-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e800-158">元素信息</span><span class="sxs-lookup"><span data-stu-id="4e800-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e800-159">命名空间</span><span class="sxs-lookup"><span data-stu-id="4e800-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e800-160">架构名称</span><span class="sxs-lookup"><span data-stu-id="4e800-160">Schema Name</span></span>  <br/> |<span data-ttu-id="4e800-161">类型架构</span><span class="sxs-lookup"><span data-stu-id="4e800-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e800-162">验证文件</span><span class="sxs-lookup"><span data-stu-id="4e800-162">Validation File</span></span>  <br/> |<span data-ttu-id="4e800-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e800-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e800-164">可以为空</span><span class="sxs-lookup"><span data-stu-id="4e800-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e800-165">False</span><span class="sxs-lookup"><span data-stu-id="4e800-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e800-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4e800-166">See also</span></span>

- [<span data-ttu-id="4e800-167">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="4e800-167">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="4e800-168">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4e800-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

