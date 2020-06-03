---
title: ItemAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemAttachment
api_type:
- schema
ms.assetid: 089ee599-f45e-46f5-a18a-5cfb3d2851ff
description: ItemAttachment 元素表示附加到另一个 Exchange 项目的 Exchange 项目。
ms.openlocfilehash: c3a07fa091c05654a03cbff58fb20204c26c9061
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526436"
---
# <a name="itemattachment"></a><span data-ttu-id="17192-103">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="17192-103">ItemAttachment</span></span>

<span data-ttu-id="17192-104">**ItemAttachment**元素表示附加到另一个 exchange 项目的 exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="17192-104">The **ItemAttachment** element represents an Exchange item that is attached to another Exchange item.</span></span> 
  
```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Item/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Message/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <CalendarItem/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Contact/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Task/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingMessage/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingRequest/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingResponse/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingCancellation/>
</ItemAttachment>
```

<span data-ttu-id="17192-105">**ItemAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="17192-105">**ItemAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="17192-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="17192-106">Attributes and elements</span></span>

<span data-ttu-id="17192-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="17192-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17192-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="17192-108">Attributes</span></span>

<span data-ttu-id="17192-109">无。</span><span class="sxs-lookup"><span data-stu-id="17192-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17192-110">子元素</span><span class="sxs-lookup"><span data-stu-id="17192-110">Child elements</span></span>

|<span data-ttu-id="17192-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="17192-111">**Element**</span></span>|<span data-ttu-id="17192-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="17192-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17192-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="17192-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="17192-114">标识附件。</span><span class="sxs-lookup"><span data-stu-id="17192-114">Identifies the attachment.</span></span>  <br/> |
|[<span data-ttu-id="17192-115">名称（AttachmentType）</span><span class="sxs-lookup"><span data-stu-id="17192-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="17192-116">代表附件的名称。</span><span class="sxs-lookup"><span data-stu-id="17192-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="17192-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="17192-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="17192-118">描述附件内容的多用途 Internet 邮件扩展（MIME）类型。</span><span class="sxs-lookup"><span data-stu-id="17192-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="17192-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="17192-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="17192-120">表示附件内容的标识符。</span><span class="sxs-lookup"><span data-stu-id="17192-120">Represents an identifier to the contents of the attachment.</span></span> <span data-ttu-id="17192-121">[ContentId](contentid.md)可以设置为任何字符串值。</span><span class="sxs-lookup"><span data-stu-id="17192-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="17192-122">应用程序可以使用[ContentId](contentid.md)来实现自己的标识机制。</span><span class="sxs-lookup"><span data-stu-id="17192-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="17192-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="17192-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="17192-124">包含与附件内容的位置相对应的统一资源标识符（URI）。</span><span class="sxs-lookup"><span data-stu-id="17192-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="17192-125">大小</span><span class="sxs-lookup"><span data-stu-id="17192-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="17192-126">表示文件附件的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="17192-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="17192-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="17192-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="17192-128">表示上次修改附件的时间。</span><span class="sxs-lookup"><span data-stu-id="17192-128">Represents when the attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="17192-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="17192-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="17192-130">表示附件是否内联显示在项目中。</span><span class="sxs-lookup"><span data-stu-id="17192-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="17192-131">项</span><span class="sxs-lookup"><span data-stu-id="17192-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="17192-132">表示通用 Exchange 项附件。</span><span class="sxs-lookup"><span data-stu-id="17192-132">Represents a generic Exchange item attachment.</span></span>  <br/> |
|[<span data-ttu-id="17192-133">消息</span><span class="sxs-lookup"><span data-stu-id="17192-133">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="17192-134">表示 Exchange 电子邮件附件。</span><span class="sxs-lookup"><span data-stu-id="17192-134">Represents an Exchange e-mail message attachment.</span></span>  <br/> |
|[<span data-ttu-id="17192-135">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="17192-135">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="17192-136">代表 Exchange 日历项附件。</span><span class="sxs-lookup"><span data-stu-id="17192-136">Represents an Exchange calendar item attachment.</span></span>  <br/> |
|[<span data-ttu-id="17192-137">联系人</span><span class="sxs-lookup"><span data-stu-id="17192-137">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="17192-138">表示 Exchange 联系人项目附件。</span><span class="sxs-lookup"><span data-stu-id="17192-138">Represents an Exchange contact item attachment.</span></span>  <br/> |
|[<span data-ttu-id="17192-139">任务</span><span class="sxs-lookup"><span data-stu-id="17192-139">Task</span></span>](task.md) <br/> |<span data-ttu-id="17192-140">代表 Exchange 任务附件。</span><span class="sxs-lookup"><span data-stu-id="17192-140">Represents an Exchange task attachment.</span></span>  <br/> |
|[<span data-ttu-id="17192-141">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="17192-141">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="17192-142">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="17192-142">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="17192-143">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="17192-143">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="17192-144">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="17192-144">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="17192-145">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="17192-145">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="17192-146">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="17192-146">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="17192-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="17192-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="17192-148">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="17192-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17192-149">父元素</span><span class="sxs-lookup"><span data-stu-id="17192-149">Parent elements</span></span>

|<span data-ttu-id="17192-150">**元素**</span><span class="sxs-lookup"><span data-stu-id="17192-150">**Element**</span></span>|<span data-ttu-id="17192-151">**说明**</span><span class="sxs-lookup"><span data-stu-id="17192-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17192-152">附件</span><span class="sxs-lookup"><span data-stu-id="17192-152">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="17192-153">包含附加到 Exchange 存储中的项目的项目和/或文件。</span><span class="sxs-lookup"><span data-stu-id="17192-153">Contains the items and/or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="17192-154">文本值</span><span class="sxs-lookup"><span data-stu-id="17192-154">Text value</span></span>

<span data-ttu-id="17192-155">无。</span><span class="sxs-lookup"><span data-stu-id="17192-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17192-156">说明</span><span class="sxs-lookup"><span data-stu-id="17192-156">Remarks</span></span>

<span data-ttu-id="17192-157">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="17192-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17192-158">元素信息</span><span class="sxs-lookup"><span data-stu-id="17192-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17192-159">命名空间</span><span class="sxs-lookup"><span data-stu-id="17192-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="17192-160">架构名称</span><span class="sxs-lookup"><span data-stu-id="17192-160">Schema Name</span></span>  <br/> |<span data-ttu-id="17192-161">类型架构</span><span class="sxs-lookup"><span data-stu-id="17192-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="17192-162">验证文件</span><span class="sxs-lookup"><span data-stu-id="17192-162">Validation File</span></span>  <br/> |<span data-ttu-id="17192-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="17192-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="17192-164">可以为空</span><span class="sxs-lookup"><span data-stu-id="17192-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="17192-165">False</span><span class="sxs-lookup"><span data-stu-id="17192-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17192-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="17192-166">See also</span></span>

- [<span data-ttu-id="17192-167">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="17192-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

