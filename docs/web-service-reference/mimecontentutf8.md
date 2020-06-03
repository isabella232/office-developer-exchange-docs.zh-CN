---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: MimeContentUTF8 元素包含以 base64Binary 格式表示的对象的 UTF-8 MIME 流，并支持电子邮件地址国际化和 [RFC6530]。
ms.openlocfilehash: a9214bda876c1aadac5b026b3adf38faea8ef17a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530427"
---
# <a name="mimecontentutf8"></a><span data-ttu-id="f9b28-103">MimeContentUTF8</span><span class="sxs-lookup"><span data-stu-id="f9b28-103">MimeContentUTF8</span></span>

<span data-ttu-id="f9b28-104">**MimeContentUTF8**元素包含以 base64Binary 格式表示的对象的 utf-8 MIME 流，并支持电子邮件地址国际化和[[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt)。</span><span class="sxs-lookup"><span data-stu-id="f9b28-104">The **MimeContentUTF8** element contains the UTF-8 MIME stream of an object that is represented in base64Binary format and supports email address internationalization and [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span></span>
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 <span data-ttu-id="f9b28-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="f9b28-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9b28-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f9b28-106">Attributes and elements</span></span>

<span data-ttu-id="f9b28-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f9b28-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9b28-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f9b28-108">Attributes</span></span>

|<span data-ttu-id="f9b28-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f9b28-109">**Attribute**</span></span>|<span data-ttu-id="f9b28-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f9b28-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f9b28-111">**CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="f9b28-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="f9b28-112">如果设置，则服务器将忽略此属性的值。</span><span class="sxs-lookup"><span data-stu-id="f9b28-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f9b28-113">子元素</span><span class="sxs-lookup"><span data-stu-id="f9b28-113">Child elements</span></span>

<span data-ttu-id="f9b28-114">无。</span><span class="sxs-lookup"><span data-stu-id="f9b28-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f9b28-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f9b28-115">Parent elements</span></span>

<span data-ttu-id="f9b28-116">[CalendarItem](calendaritem.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)  | [项](item.md)  | [MeetingCancellation](meetingcancellation.md)  | [MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [邮件](message-ex15websvcsotherref.md)  | [RemoveItem](removeitem.md)  | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="f9b28-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f9b28-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f9b28-117">Text value</span></span>

<span data-ttu-id="f9b28-118">如果使用此元素，则表示 base64binary MIME 流的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="f9b28-118">A text value that represents a base64binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9b28-119">备注</span><span class="sxs-lookup"><span data-stu-id="f9b28-119">Remarks</span></span>

<span data-ttu-id="f9b28-120">邮件内容在存储在**MimeContentUTF8**值之前，会经历以下三种编码级别：</span><span class="sxs-lookup"><span data-stu-id="f9b28-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContentUTF8** value:</span></span> 
  
1. <span data-ttu-id="f9b28-121">邮件文本—这是正文编码，例如，日语字符的 iso-2022-jp。</span><span class="sxs-lookup"><span data-stu-id="f9b28-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="f9b28-122">MIME 流—这是**MimeContentUTF8**元素的邮件文本的 UTF8 编码，或[MimeContent](mimecontent.md)元素的邮件文本的 ASCII 编码。</span><span class="sxs-lookup"><span data-stu-id="f9b28-122">MIME stream — This is the UTF8 encoding of the message text for the **MimeContentUTF8** element, or the ASCII encoding of the message text for the [MimeContent](mimecontent.md) element.</span></span> 
    
3. <span data-ttu-id="f9b28-123">XML 文档—这始终是 MIME 流的 base64 编码的 ASCII 流，其中的字符（如 ""）在 XML 分析程序中是隐藏的，这些字符（如 ' \< '）对 xml 是有意义的。</span><span class="sxs-lookup"><span data-stu-id="f9b28-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="f9b28-124">每个级别都独立于它之前的级别。</span><span class="sxs-lookup"><span data-stu-id="f9b28-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="f9b28-125">**MimeContentUTF8**元素可能包含与项目一起返回的其他属性所包含的数据。</span><span class="sxs-lookup"><span data-stu-id="f9b28-125">The **MimeContentUTF8** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="f9b28-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f9b28-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="f9b28-127">版本差异</span><span class="sxs-lookup"><span data-stu-id="f9b28-127">Version differences</span></span>

<span data-ttu-id="f9b28-128">此元素在从生成15.00.0986.00 开始的 Exchange 版本中可用。</span><span class="sxs-lookup"><span data-stu-id="f9b28-128">This element is available in versions of Exchange starting with build 15.00.0986.00.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9b28-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="f9b28-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9b28-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="f9b28-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f9b28-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="f9b28-131">Schema Name</span></span>  <br/> |<span data-ttu-id="f9b28-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="f9b28-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="f9b28-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="f9b28-133">Validation File</span></span>  <br/> |<span data-ttu-id="f9b28-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f9b28-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f9b28-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="f9b28-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="f9b28-136">False</span><span class="sxs-lookup"><span data-stu-id="f9b28-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9b28-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f9b28-137">See also</span></span>



- [<span data-ttu-id="f9b28-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f9b28-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

