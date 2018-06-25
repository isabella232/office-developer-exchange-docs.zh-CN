---
title: MimeContent
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MimeContent
api_type:
- schema
ms.assetid: 4f472a08-5653-4c54-ba65-831dfe32f20f
description: MimeContent 元素包含一个对象，表示 base64Binary 格式并支持 [RFC2045] 的 ASCII MIME 流。
ms.openlocfilehash: 60f2d42f09347611559137c494d93036f1192829
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826465"
---
# <a name="mimecontent"></a><span data-ttu-id="7ab32-103">MimeContent</span><span class="sxs-lookup"><span data-stu-id="7ab32-103">MimeContent</span></span>

<span data-ttu-id="7ab32-104">**MimeContent**元素包含一个对象，表示 base64Binary 格式并支持[[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt)的 ASCII MIME 流。</span><span class="sxs-lookup"><span data-stu-id="7ab32-104">The **MimeContent** element contains the ASCII MIME stream of an object that is represented in base64Binary format and supports [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).</span></span>
  
```xml
<MimeContent CharacterSet="" />
```

 <span data-ttu-id="7ab32-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="7ab32-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ab32-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7ab32-106">Attributes and elements</span></span>

<span data-ttu-id="7ab32-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7ab32-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ab32-108">属性</span><span class="sxs-lookup"><span data-stu-id="7ab32-108">Attributes</span></span>

|<span data-ttu-id="7ab32-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="7ab32-109">**Attribute**</span></span>|<span data-ttu-id="7ab32-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ab32-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ab32-111">**CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="7ab32-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="7ab32-112">如果设置，此属性的值将被忽略该服务器。</span><span class="sxs-lookup"><span data-stu-id="7ab32-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7ab32-113">子元素</span><span class="sxs-lookup"><span data-stu-id="7ab32-113">Child elements</span></span>

<span data-ttu-id="7ab32-114">无。</span><span class="sxs-lookup"><span data-stu-id="7ab32-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7ab32-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7ab32-115">Parent elements</span></span>

<span data-ttu-id="7ab32-116">[日历项目](calendaritem.md) | [联系人](contact.md) | [DistributionList](distributionlist.md) | [项](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md) | [消息](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="7ab32-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7ab32-117">文本值</span><span class="sxs-lookup"><span data-stu-id="7ab32-117">Text value</span></span>

<span data-ttu-id="7ab32-118">如果使用此元素，则需要一个表示 base64Binary MIME 流文本值。</span><span class="sxs-lookup"><span data-stu-id="7ab32-118">A text value that represents a base64Binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ab32-119">注解</span><span class="sxs-lookup"><span data-stu-id="7ab32-119">Remarks</span></span>

<span data-ttu-id="7ab32-120">消息内容经历的编码然后将其存储在**MimeContent**值的以下三个级别：</span><span class="sxs-lookup"><span data-stu-id="7ab32-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContent** value:</span></span> 
  
1. <span data-ttu-id="7ab32-121">消息正文 — 这是编码，如 iso-2022年-jp 日语字符的正文。</span><span class="sxs-lookup"><span data-stu-id="7ab32-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="7ab32-122">MIME 流 — 这是**MimeContent**元素中，消息文本的 ASCII 编码或[MimeContentUTF8](mimecontentutf8.md)元素的消息文本的 UTF8 编码。</span><span class="sxs-lookup"><span data-stu-id="7ab32-122">MIME stream — This is the ASCII encoding of the message text for the **MimeContent** element, or the UTF8 encoding of the message text for the [MimeContentUTF8](mimecontentutf8.md) element.</span></span> 
    
3. <span data-ttu-id="7ab32-123">XML 文档 — 这始终是 base64 编码 ASCII 流 MIME 流，其中等字符\<，其中有意义为 XML，从 XML 分析程序已被隐藏。</span><span class="sxs-lookup"><span data-stu-id="7ab32-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="7ab32-124">每个级别都独立于它之前的级别。</span><span class="sxs-lookup"><span data-stu-id="7ab32-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="7ab32-125">**MimeContent**元素可能包含其他与项目返回的属性包含相同的数据。</span><span class="sxs-lookup"><span data-stu-id="7ab32-125">The **MimeContent** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="7ab32-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7ab32-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ab32-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="7ab32-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ab32-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="7ab32-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ab32-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="7ab32-129">Schema Name</span></span>  <br/> |<span data-ttu-id="7ab32-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="7ab32-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="7ab32-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="7ab32-131">Validation File</span></span>  <br/> |<span data-ttu-id="7ab32-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7ab32-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ab32-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="7ab32-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="7ab32-134">False</span><span class="sxs-lookup"><span data-stu-id="7ab32-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ab32-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ab32-135">See also</span></span>



- [<span data-ttu-id="7ab32-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7ab32-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

