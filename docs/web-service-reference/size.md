---
title: 大小
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Size
api_type:
- schema
ms.assetid: 966f4daf-c20e-49f8-aeb6-965f3e2da7c3
description: 大小元素表示以字节为单位的项目或当前文件夹中的某个对话中的所有项目的大小。 此属性是只读的。
ms.openlocfilehash: 15ee0bce6bc5fa2065cef4ecee40d7a6d65e3249
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827509"
---
# <a name="size"></a><span data-ttu-id="31088-104">大小</span><span class="sxs-lookup"><span data-stu-id="31088-104">Size</span></span>

<span data-ttu-id="31088-105">**大小**元素表示以字节为单位的项目或当前文件夹中的某个对话中的所有项目的大小。</span><span class="sxs-lookup"><span data-stu-id="31088-105">The **Size** element represents the size in bytes of an item or all the items in a conversation in the current folder.</span></span> <span data-ttu-id="31088-106">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="31088-106">This property is read-only.</span></span> 
  
```XML
<Size/>
```

 <span data-ttu-id="31088-107">**int**</span><span class="sxs-lookup"><span data-stu-id="31088-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31088-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="31088-108">Attributes and elements</span></span>

<span data-ttu-id="31088-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="31088-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31088-110">属性</span><span class="sxs-lookup"><span data-stu-id="31088-110">Attributes</span></span>

<span data-ttu-id="31088-111">无。</span><span class="sxs-lookup"><span data-stu-id="31088-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31088-112">子元素</span><span class="sxs-lookup"><span data-stu-id="31088-112">Child elements</span></span>

<span data-ttu-id="31088-113">无。</span><span class="sxs-lookup"><span data-stu-id="31088-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31088-114">父元素</span><span class="sxs-lookup"><span data-stu-id="31088-114">Parent elements</span></span>

|<span data-ttu-id="31088-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="31088-115">**Element**</span></span>|<span data-ttu-id="31088-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="31088-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31088-117">日历项目</span><span class="sxs-lookup"><span data-stu-id="31088-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="31088-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="31088-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="31088-119">联系人</span><span class="sxs-lookup"><span data-stu-id="31088-119">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="31088-120">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="31088-120">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="31088-121">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="31088-121">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="31088-122">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="31088-122">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="31088-123">DistributionList</span><span class="sxs-lookup"><span data-stu-id="31088-123">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="31088-124">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="31088-124">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="31088-125">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="31088-125">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="31088-126">代表附加到 Exchange 存储中的项的文件。</span><span class="sxs-lookup"><span data-stu-id="31088-126">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31088-127">项目</span><span class="sxs-lookup"><span data-stu-id="31088-127">Item</span></span>](item.md) <br/> |<span data-ttu-id="31088-128">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="31088-128">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31088-129">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="31088-129">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="31088-130">代表附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="31088-130">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="31088-131">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="31088-131">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="31088-132">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="31088-132">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31088-133">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="31088-133">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="31088-134">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="31088-134">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31088-135">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="31088-135">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="31088-136">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="31088-136">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31088-137">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="31088-137">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="31088-138">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="31088-138">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31088-139">Message</span><span class="sxs-lookup"><span data-stu-id="31088-139">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="31088-140">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="31088-140">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="31088-141">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="31088-141">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="31088-142">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="31088-142">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31088-143">任务</span><span class="sxs-lookup"><span data-stu-id="31088-143">Task</span></span>](task.md) <br/> |<span data-ttu-id="31088-144">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="31088-144">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31088-145">文本值</span><span class="sxs-lookup"><span data-stu-id="31088-145">Text value</span></span>

<span data-ttu-id="31088-146">文本值是项的一个整数值，标识以字节为单位的大小。</span><span class="sxs-lookup"><span data-stu-id="31088-146">The text value is an integer value that identifies the size of the item in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31088-147">备注</span><span class="sxs-lookup"><span data-stu-id="31088-147">Remarks</span></span>

<span data-ttu-id="31088-148">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="31088-148">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31088-149">元素信息</span><span class="sxs-lookup"><span data-stu-id="31088-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31088-150">命名空间</span><span class="sxs-lookup"><span data-stu-id="31088-150">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31088-151">架构名称</span><span class="sxs-lookup"><span data-stu-id="31088-151">Schema Name</span></span>  <br/> |<span data-ttu-id="31088-152">类型架构</span><span class="sxs-lookup"><span data-stu-id="31088-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="31088-153">验证文件</span><span class="sxs-lookup"><span data-stu-id="31088-153">Validation File</span></span>  <br/> |<span data-ttu-id="31088-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="31088-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31088-155">可以为空</span><span class="sxs-lookup"><span data-stu-id="31088-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="31088-156">False</span><span class="sxs-lookup"><span data-stu-id="31088-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31088-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="31088-157">See also</span></span>



- [<span data-ttu-id="31088-158">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="31088-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

