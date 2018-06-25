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
description: ItemAttachment 元素均表示一个 Exchange 项目附加到另一个 Exchange 项目。
ms.openlocfilehash: 87e0331664f1fdf8857afc78500014d138f05401
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826137"
---
# <a name="itemattachment"></a><span data-ttu-id="baa3b-103">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="baa3b-103">ItemAttachment</span></span>

<span data-ttu-id="baa3b-104">**ItemAttachment**元素均表示一个 Exchange 项目附加到另一个 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="baa3b-104">The **ItemAttachment** element represents an Exchange item that is attached to another Exchange item.</span></span> 
  
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

 <span data-ttu-id="baa3b-105">**ItemAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="baa3b-105">**ItemAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="baa3b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="baa3b-106">Attributes and elements</span></span>

<span data-ttu-id="baa3b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="baa3b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="baa3b-108">属性</span><span class="sxs-lookup"><span data-stu-id="baa3b-108">Attributes</span></span>

<span data-ttu-id="baa3b-109">无。</span><span class="sxs-lookup"><span data-stu-id="baa3b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="baa3b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="baa3b-110">Child elements</span></span>

|<span data-ttu-id="baa3b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="baa3b-111">**Element**</span></span>|<span data-ttu-id="baa3b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="baa3b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baa3b-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="baa3b-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="baa3b-114">标识附件。</span><span class="sxs-lookup"><span data-stu-id="baa3b-114">Identifies the attachment.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-115">名称 (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="baa3b-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="baa3b-116">表示附件的名称。</span><span class="sxs-lookup"><span data-stu-id="baa3b-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="baa3b-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="baa3b-118">描述附件内容多用途 Internet 邮件扩展 (MIME) 类型。</span><span class="sxs-lookup"><span data-stu-id="baa3b-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="baa3b-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="baa3b-120">表示附件的内容的标识符。</span><span class="sxs-lookup"><span data-stu-id="baa3b-120">Represents an identifier to the contents of the attachment.</span></span> <span data-ttu-id="baa3b-121">[ContentId](contentid.md)可以设置为任何字符串值。</span><span class="sxs-lookup"><span data-stu-id="baa3b-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="baa3b-122">应用程序可以使用[ContentId](contentid.md)来实现自己标识机制。</span><span class="sxs-lookup"><span data-stu-id="baa3b-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="baa3b-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="baa3b-124">包含附件的内容的位置所对应的统一资源标识符 (URI)。</span><span class="sxs-lookup"><span data-stu-id="baa3b-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-125">Size</span><span class="sxs-lookup"><span data-stu-id="baa3b-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="baa3b-126">表示以字节为单位的附件文件的大小。</span><span class="sxs-lookup"><span data-stu-id="baa3b-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="baa3b-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="baa3b-128">表示上次修改附件时。</span><span class="sxs-lookup"><span data-stu-id="baa3b-128">Represents when the attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="baa3b-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="baa3b-130">表示是否附件显示为内嵌项目中。</span><span class="sxs-lookup"><span data-stu-id="baa3b-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-131">Item</span><span class="sxs-lookup"><span data-stu-id="baa3b-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="baa3b-132">代表一个通用的 Exchange 项目附件。</span><span class="sxs-lookup"><span data-stu-id="baa3b-132">Represents a generic Exchange item attachment.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-133">Message</span><span class="sxs-lookup"><span data-stu-id="baa3b-133">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="baa3b-134">代表 Exchange 电子邮件附件。</span><span class="sxs-lookup"><span data-stu-id="baa3b-134">Represents an Exchange e-mail message attachment.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-135">日历项目</span><span class="sxs-lookup"><span data-stu-id="baa3b-135">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="baa3b-136">代表 Exchange 日历项目附件。</span><span class="sxs-lookup"><span data-stu-id="baa3b-136">Represents an Exchange calendar item attachment.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-137">Contact</span><span class="sxs-lookup"><span data-stu-id="baa3b-137">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="baa3b-138">代表 Exchange 联系人项目附件。</span><span class="sxs-lookup"><span data-stu-id="baa3b-138">Represents an Exchange contact item attachment.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-139">任务</span><span class="sxs-lookup"><span data-stu-id="baa3b-139">Task</span></span>](task.md) <br/> |<span data-ttu-id="baa3b-140">代表 Exchange 任务附件。</span><span class="sxs-lookup"><span data-stu-id="baa3b-140">Represents an Exchange task attachment.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-141">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="baa3b-141">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="baa3b-142">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="baa3b-142">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-143">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="baa3b-143">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="baa3b-144">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="baa3b-144">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-145">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="baa3b-145">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="baa3b-146">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="baa3b-146">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="baa3b-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="baa3b-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="baa3b-148">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="baa3b-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="baa3b-149">父元素</span><span class="sxs-lookup"><span data-stu-id="baa3b-149">Parent elements</span></span>

|<span data-ttu-id="baa3b-150">**元素**</span><span class="sxs-lookup"><span data-stu-id="baa3b-150">**Element**</span></span>|<span data-ttu-id="baa3b-151">**说明**</span><span class="sxs-lookup"><span data-stu-id="baa3b-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baa3b-152">附件</span><span class="sxs-lookup"><span data-stu-id="baa3b-152">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="baa3b-153">包含项目和/或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="baa3b-153">Contains the items and/or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="baa3b-154">文本值</span><span class="sxs-lookup"><span data-stu-id="baa3b-154">Text value</span></span>

<span data-ttu-id="baa3b-155">无。</span><span class="sxs-lookup"><span data-stu-id="baa3b-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="baa3b-156">备注</span><span class="sxs-lookup"><span data-stu-id="baa3b-156">Remarks</span></span>

<span data-ttu-id="baa3b-157">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="baa3b-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="baa3b-158">元素信息</span><span class="sxs-lookup"><span data-stu-id="baa3b-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="baa3b-159">命名空间</span><span class="sxs-lookup"><span data-stu-id="baa3b-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="baa3b-160">架构名称</span><span class="sxs-lookup"><span data-stu-id="baa3b-160">Schema Name</span></span>  <br/> |<span data-ttu-id="baa3b-161">类型架构</span><span class="sxs-lookup"><span data-stu-id="baa3b-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="baa3b-162">验证文件</span><span class="sxs-lookup"><span data-stu-id="baa3b-162">Validation File</span></span>  <br/> |<span data-ttu-id="baa3b-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="baa3b-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="baa3b-164">可以为空</span><span class="sxs-lookup"><span data-stu-id="baa3b-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="baa3b-165">False</span><span class="sxs-lookup"><span data-stu-id="baa3b-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="baa3b-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="baa3b-166">See also</span></span>



- [<span data-ttu-id="baa3b-167">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="baa3b-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

