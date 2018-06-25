---
title: HasAttachments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasAttachments
api_type:
- schema
ms.assetid: 538b7a85-11d7-4daa-8458-09b540760e8b
description: HasAttachments元素表示一个属性，如果某项有至少一个可见附件或者包含附件当会话包含至少一个项的设置为true 。此属性是只读的。
ms.openlocfilehash: e76e0ecbb357396540f0d1649cf5062edfb18660
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825801"
---
# <a name="hasattachments"></a><span data-ttu-id="235fb-104">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="235fb-104">HasAttachments</span></span>

<span data-ttu-id="235fb-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **HasAttachments**元素表示一个属性，如果某项有至少一个可见附件或者包含附件当会话包含至少一个项的设置为 **true** 。此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="235fb-p102">The **HasAttachments** element represents a property that is set to **true** if an item has at least one visible attachment or if a conversation contains at least one item that has an attachment. This property is read-only.</span></span> 
  
```XML
<HasAttachments/>
```

 <span data-ttu-id="235fb-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="235fb-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="235fb-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="235fb-108">Attributes and elements</span></span>

<span data-ttu-id="235fb-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="235fb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="235fb-110">属性</span><span class="sxs-lookup"><span data-stu-id="235fb-110">Attributes</span></span>

<span data-ttu-id="235fb-111">无。</span><span class="sxs-lookup"><span data-stu-id="235fb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="235fb-112">子元素</span><span class="sxs-lookup"><span data-stu-id="235fb-112">Child elements</span></span>

<span data-ttu-id="235fb-113">无。</span><span class="sxs-lookup"><span data-stu-id="235fb-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="235fb-114">父元素</span><span class="sxs-lookup"><span data-stu-id="235fb-114">Parent elements</span></span>

|<span data-ttu-id="235fb-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="235fb-115">**Element**</span></span>|<span data-ttu-id="235fb-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="235fb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="235fb-117">日历项目</span><span class="sxs-lookup"><span data-stu-id="235fb-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="235fb-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="235fb-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="235fb-119">条件</span><span class="sxs-lookup"><span data-stu-id="235fb-119">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="235fb-120">表示条件，履行时, 将触发该规则的规则操作。</span><span class="sxs-lookup"><span data-stu-id="235fb-120">Represents the conditions that, when fulfilled, will trigger the rule actions for that rule.</span></span>  <br/> |
|[<span data-ttu-id="235fb-121">联系人</span><span class="sxs-lookup"><span data-stu-id="235fb-121">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="235fb-122">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="235fb-122">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="235fb-123">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="235fb-123">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="235fb-124">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="235fb-124">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="235fb-125">DistributionList</span><span class="sxs-lookup"><span data-stu-id="235fb-125">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="235fb-126">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="235fb-126">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="235fb-127">异常</span><span class="sxs-lookup"><span data-stu-id="235fb-127">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="235fb-128">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="235fb-128">Represents all the available rule exception conditions for the Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="235fb-129">项目</span><span class="sxs-lookup"><span data-stu-id="235fb-129">Item</span></span>](item.md) <br/> |<span data-ttu-id="235fb-130">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="235fb-130">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="235fb-131">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="235fb-131">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="235fb-132">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="235fb-132">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="235fb-133">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="235fb-133">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="235fb-134">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="235fb-134">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="235fb-135">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="235fb-135">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="235fb-136">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="235fb-136">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="235fb-137">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="235fb-137">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="235fb-138">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="235fb-138">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="235fb-139">Message</span><span class="sxs-lookup"><span data-stu-id="235fb-139">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="235fb-140">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="235fb-140">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="235fb-141">任务</span><span class="sxs-lookup"><span data-stu-id="235fb-141">Task</span></span>](task.md) <br/> |<span data-ttu-id="235fb-142">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="235fb-142">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="235fb-143">文本值</span><span class="sxs-lookup"><span data-stu-id="235fb-143">Text value</span></span>

<span data-ttu-id="235fb-p103">表示一个布尔值的文本值是必需的。 **true**的值表示的项或对话中有至少一个可见附件。 **false**的值意味着，项目或对话既没有附件，或只包含隐藏的附件。</span><span class="sxs-lookup"><span data-stu-id="235fb-p103">A text value that represents a Boolean value is required. A value of **true** means that the item or conversation has at least one visible attachment. A value of **false** means that the item or conversation either has no attachments or has only hidden attachments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="235fb-147">备注</span><span class="sxs-lookup"><span data-stu-id="235fb-147">Remarks</span></span>

<span data-ttu-id="235fb-p104">**HasAttachments** 属性的布尔型 **AllAttachmentsHidden** MAPI 属性进行计算。如果一个项目没有附件，则 **AllAttachmentsHidden** 属性不存在。 **AllAttachmentsHidden** 属性是否在该项目上的所有附件都隐藏的是 **true**。 **AllAttachmentsHidden** 属性是 **false** ，如果有至少一个附件，并且附件中至少一个可见。 **AllAttachmentsHidden** 的 MAPI 属性用于搜索、 分组和排序的项目。</span><span class="sxs-lookup"><span data-stu-id="235fb-p104">The **HasAttachments** property is calculated from the Boolean **AllAttachmentsHidden** MAPI property. If an item does not have an attachment, the **AllAttachmentsHidden** property does not exist. If all the attachments on the item are hidden, the **AllAttachmentsHidden** property is **true**. The **AllAttachmentsHidden** property is **false** if it has at least one attachment and at least one of the attachments is visible. Use the **AllAttachmentsHidden** MAPI property for searching, grouping, and sorting items.</span></span> 
  
<span data-ttu-id="235fb-153">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="235fb-153">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="235fb-154">元素信息</span><span class="sxs-lookup"><span data-stu-id="235fb-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="235fb-155">命名空间</span><span class="sxs-lookup"><span data-stu-id="235fb-155">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="235fb-156">架构名称</span><span class="sxs-lookup"><span data-stu-id="235fb-156">Schema Name</span></span>  <br/> |<span data-ttu-id="235fb-157">类型架构</span><span class="sxs-lookup"><span data-stu-id="235fb-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="235fb-158">验证文件</span><span class="sxs-lookup"><span data-stu-id="235fb-158">Validation File</span></span>  <br/> |<span data-ttu-id="235fb-159">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="235fb-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="235fb-160">可以为空</span><span class="sxs-lookup"><span data-stu-id="235fb-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="235fb-161">False</span><span class="sxs-lookup"><span data-stu-id="235fb-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="235fb-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="235fb-162">See also</span></span>



- [<span data-ttu-id="235fb-163">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="235fb-163">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="235fb-164">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="235fb-164">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

