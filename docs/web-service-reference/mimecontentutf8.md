---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: MimeContentUTF8 元素包含一个对象，表示 base64Binary 格式的 utf-8 MIME 流和支持电子邮件地址国际化和 [RFC6530]。
ms.openlocfilehash: 47599b6634738fd488e5b020f69e36d5fcf550a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826466"
---
# <a name="mimecontentutf8"></a><span data-ttu-id="2533d-103">MimeContentUTF8</span><span class="sxs-lookup"><span data-stu-id="2533d-103">MimeContentUTF8</span></span>

<span data-ttu-id="2533d-104">**MimeContentUTF8**元素包含一个对象，表示 base64Binary 格式并支持电子邮件地址国际化和[[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt)的 utf-8 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="2533d-104">The **MimeContentUTF8** element contains the UTF-8 MIME stream of an object that is represented in base64Binary format and supports email address internationalization and [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span></span>
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 <span data-ttu-id="2533d-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="2533d-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2533d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2533d-106">Attributes and elements</span></span>

<span data-ttu-id="2533d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2533d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2533d-108">属性</span><span class="sxs-lookup"><span data-stu-id="2533d-108">Attributes</span></span>

|<span data-ttu-id="2533d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="2533d-109">**Attribute**</span></span>|<span data-ttu-id="2533d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="2533d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2533d-111">**CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="2533d-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="2533d-112">如果设置，此属性的值将被忽略该服务器。</span><span class="sxs-lookup"><span data-stu-id="2533d-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2533d-113">子元素</span><span class="sxs-lookup"><span data-stu-id="2533d-113">Child elements</span></span>

<span data-ttu-id="2533d-114">无。</span><span class="sxs-lookup"><span data-stu-id="2533d-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2533d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2533d-115">Parent elements</span></span>

<span data-ttu-id="2533d-116">[日历项目](calendaritem.md) | [联系人](contact.md) | [DistributionList](distributionlist.md) | [项](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md) | [消息](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="2533d-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="2533d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="2533d-117">Text value</span></span>

<span data-ttu-id="2533d-118">如果使用此元素，则需要一个表示 base64binary MIME 流文本值。</span><span class="sxs-lookup"><span data-stu-id="2533d-118">A text value that represents a base64binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2533d-119">备注</span><span class="sxs-lookup"><span data-stu-id="2533d-119">Remarks</span></span>

<span data-ttu-id="2533d-120">消息内容经历的编码然后将其存储在**MimeContentUTF8**值的以下三个级别：</span><span class="sxs-lookup"><span data-stu-id="2533d-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContentUTF8** value:</span></span> 
  
1. <span data-ttu-id="2533d-121">消息正文 — 这是编码，如 iso-2022年-jp 日语字符的正文。</span><span class="sxs-lookup"><span data-stu-id="2533d-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="2533d-122">MIME 流 — 这是**MimeContentUTF8**元素中，消息文本的 UTF8 编码或[MimeContent](mimecontent.md)元素的消息文本的 ASCII 编码。</span><span class="sxs-lookup"><span data-stu-id="2533d-122">MIME stream — This is the UTF8 encoding of the message text for the **MimeContentUTF8** element, or the ASCII encoding of the message text for the [MimeContent](mimecontent.md) element.</span></span> 
    
3. <span data-ttu-id="2533d-123">XML 文档 — 这始终是 base64 编码 ASCII 流 MIME 流，其中等字符\<，其中有意义为 XML，从 XML 分析程序已被隐藏。</span><span class="sxs-lookup"><span data-stu-id="2533d-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="2533d-124">每个级别都独立于它之前的级别。</span><span class="sxs-lookup"><span data-stu-id="2533d-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="2533d-125">**MimeContentUTF8**元素可能包含其他与项目返回的属性包含相同的数据。</span><span class="sxs-lookup"><span data-stu-id="2533d-125">The **MimeContentUTF8** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="2533d-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2533d-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="2533d-127">版本差异</span><span class="sxs-lookup"><span data-stu-id="2533d-127">Version differences</span></span>

<span data-ttu-id="2533d-128">此元素是在生成 15.00.0986.00 开头的 Exchange 版本中可用。</span><span class="sxs-lookup"><span data-stu-id="2533d-128">This element is available in versions of Exchange starting with build 15.00.0986.00.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2533d-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="2533d-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2533d-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="2533d-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2533d-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="2533d-131">Schema Name</span></span>  <br/> |<span data-ttu-id="2533d-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="2533d-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="2533d-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="2533d-133">Validation File</span></span>  <br/> |<span data-ttu-id="2533d-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2533d-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2533d-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="2533d-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="2533d-136">False</span><span class="sxs-lookup"><span data-stu-id="2533d-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2533d-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2533d-137">See also</span></span>



- [<span data-ttu-id="2533d-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2533d-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

