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
description: MimeContent 元素包含以 base64Binary 格式表示并支持 [RFC2045] 的对象的 ASCII MIME 流。
ms.openlocfilehash: 039ef1245d48e4cf13141970921dd210f4bd7d06
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530434"
---
# <a name="mimecontent"></a><span data-ttu-id="410d0-103">MimeContent</span><span class="sxs-lookup"><span data-stu-id="410d0-103">MimeContent</span></span>

<span data-ttu-id="410d0-104">**MimeContent**元素包含以 base64Binary 格式表示并支持[[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt)的对象的 ASCII MIME 流。</span><span class="sxs-lookup"><span data-stu-id="410d0-104">The **MimeContent** element contains the ASCII MIME stream of an object that is represented in base64Binary format and supports [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).</span></span>
  
```xml
<MimeContent CharacterSet="" />
```

 <span data-ttu-id="410d0-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="410d0-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="410d0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="410d0-106">Attributes and elements</span></span>

<span data-ttu-id="410d0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="410d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="410d0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="410d0-108">Attributes</span></span>

|<span data-ttu-id="410d0-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="410d0-109">**Attribute**</span></span>|<span data-ttu-id="410d0-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="410d0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="410d0-111">**CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="410d0-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="410d0-112">如果设置，则服务器将忽略此属性的值。</span><span class="sxs-lookup"><span data-stu-id="410d0-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="410d0-113">子元素</span><span class="sxs-lookup"><span data-stu-id="410d0-113">Child elements</span></span>

<span data-ttu-id="410d0-114">无。</span><span class="sxs-lookup"><span data-stu-id="410d0-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="410d0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="410d0-115">Parent elements</span></span>

<span data-ttu-id="410d0-116">[CalendarItem](calendaritem.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)  | [项](item.md)  | [MeetingCancellation](meetingcancellation.md)  | [MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [邮件](message-ex15websvcsotherref.md)  | [RemoveItem](removeitem.md)  | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="410d0-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="410d0-117">文本值</span><span class="sxs-lookup"><span data-stu-id="410d0-117">Text value</span></span>

<span data-ttu-id="410d0-118">如果使用此元素，则表示 base64Binary MIME 流的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="410d0-118">A text value that represents a base64Binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="410d0-119">备注</span><span class="sxs-lookup"><span data-stu-id="410d0-119">Remarks</span></span>

<span data-ttu-id="410d0-120">邮件内容在存储在**MimeContent**值之前，会经历以下三种编码级别：</span><span class="sxs-lookup"><span data-stu-id="410d0-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContent** value:</span></span> 
  
1. <span data-ttu-id="410d0-121">邮件文本—这是正文编码，例如，日语字符的 iso-2022-jp。</span><span class="sxs-lookup"><span data-stu-id="410d0-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="410d0-122">MIME 流—这是**MimeContent**元素的邮件文本的 ASCII 编码，或[MimeContentUTF8](mimecontentutf8.md)元素的邮件文本的 UTF8 编码。</span><span class="sxs-lookup"><span data-stu-id="410d0-122">MIME stream — This is the ASCII encoding of the message text for the **MimeContent** element, or the UTF8 encoding of the message text for the [MimeContentUTF8](mimecontentutf8.md) element.</span></span> 
    
3. <span data-ttu-id="410d0-123">XML 文档—这始终是 MIME 流的 base64 编码的 ASCII 流，其中的字符（如 ""）在 XML 分析程序中是隐藏的，这些字符（如 ' \< '）对 xml 是有意义的。</span><span class="sxs-lookup"><span data-stu-id="410d0-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="410d0-124">每个级别都独立于它之前的级别。</span><span class="sxs-lookup"><span data-stu-id="410d0-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="410d0-125">**MimeContent**元素可能包含与项目一起返回的其他属性所包含的数据。</span><span class="sxs-lookup"><span data-stu-id="410d0-125">The **MimeContent** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="410d0-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="410d0-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="410d0-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="410d0-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="410d0-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="410d0-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="410d0-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="410d0-129">Schema Name</span></span>  <br/> |<span data-ttu-id="410d0-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="410d0-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="410d0-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="410d0-131">Validation File</span></span>  <br/> |<span data-ttu-id="410d0-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="410d0-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="410d0-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="410d0-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="410d0-134">False</span><span class="sxs-lookup"><span data-stu-id="410d0-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="410d0-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="410d0-135">See also</span></span>



- [<span data-ttu-id="410d0-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="410d0-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

