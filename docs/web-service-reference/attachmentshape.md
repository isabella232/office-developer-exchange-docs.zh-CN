---
title: AttachmentShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: AttachmentShape 元素标识要 GetAttachment 请求的响应中返回的其他属性。
ms.openlocfilehash: dc6769faa5fd28ce31b796f86c507aec54abff7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753281"
---
# <a name="attachmentshape"></a><span data-ttu-id="d29a3-103">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="d29a3-103">AttachmentShape</span></span>

<span data-ttu-id="d29a3-104">**AttachmentShape**元素标识要[GetAttachment](getattachment.md)请求的响应中返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="d29a3-104">The **AttachmentShape** element identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> 
  
- [<span data-ttu-id="d29a3-105">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="d29a3-105">GetAttachment</span></span>](getattachment.md)
  
- [<span data-ttu-id="d29a3-106">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="d29a3-106">AttachmentShape</span></span>](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 <span data-ttu-id="d29a3-107">**AttachmentResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="d29a3-107">**AttachmentResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d29a3-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d29a3-108">Attributes and elements</span></span>

<span data-ttu-id="d29a3-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d29a3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d29a3-110">属性</span><span class="sxs-lookup"><span data-stu-id="d29a3-110">Attributes</span></span>

<span data-ttu-id="d29a3-111">无。</span><span class="sxs-lookup"><span data-stu-id="d29a3-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d29a3-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d29a3-112">Child elements</span></span>

|<span data-ttu-id="d29a3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d29a3-113">**Element**</span></span>|<span data-ttu-id="d29a3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d29a3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d29a3-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="d29a3-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="d29a3-116">指定是否在响应中返回的项目或附件多用途 Internet 邮件扩展 (MIME) 内容。</span><span class="sxs-lookup"><span data-stu-id="d29a3-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> <span data-ttu-id="d29a3-117">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d29a3-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d29a3-118">BodyType</span><span class="sxs-lookup"><span data-stu-id="d29a3-118">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="d29a3-119">介绍如何在响应中设置的正文文本的格式。</span><span class="sxs-lookup"><span data-stu-id="d29a3-119">Identifies how the body text is formatted in the response.</span></span> <span data-ttu-id="d29a3-120">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d29a3-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d29a3-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="d29a3-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="d29a3-122">指定是否从附件筛选存在安全隐患的 HTML 内容。</span><span class="sxs-lookup"><span data-stu-id="d29a3-122">Specifies whether potentially unsafe HTML content is filtered from an attachment.</span></span> <span data-ttu-id="d29a3-123">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d29a3-123">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d29a3-124">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="d29a3-124">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="d29a3-125">标识要返回的响应中的其他属性。</span><span class="sxs-lookup"><span data-stu-id="d29a3-125">Identifies additional properties to return in a response.</span></span> <span data-ttu-id="d29a3-126">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d29a3-126">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d29a3-127">父元素</span><span class="sxs-lookup"><span data-stu-id="d29a3-127">Parent elements</span></span>

|<span data-ttu-id="d29a3-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="d29a3-128">**Element**</span></span>|<span data-ttu-id="d29a3-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="d29a3-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d29a3-130">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="d29a3-130">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="d29a3-131">定义一个请求以获取从 Exchange 存储中的邮箱的附件的元素。</span><span class="sxs-lookup"><span data-stu-id="d29a3-131">The element that defines a request to get an attachment from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="d29a3-132">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="d29a3-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d29a3-133">文本值</span><span class="sxs-lookup"><span data-stu-id="d29a3-133">Text value</span></span>

<span data-ttu-id="d29a3-134">无。</span><span class="sxs-lookup"><span data-stu-id="d29a3-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d29a3-135">备注</span><span class="sxs-lookup"><span data-stu-id="d29a3-135">Remarks</span></span>

<span data-ttu-id="d29a3-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d29a3-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d29a3-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="d29a3-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d29a3-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="d29a3-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d29a3-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="d29a3-139">Schema Name</span></span>  <br/> |<span data-ttu-id="d29a3-140">消息架构</span><span class="sxs-lookup"><span data-stu-id="d29a3-140">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d29a3-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="d29a3-141">Validation File</span></span>  <br/> |<span data-ttu-id="d29a3-142">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d29a3-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d29a3-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="d29a3-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="d29a3-144">False</span><span class="sxs-lookup"><span data-stu-id="d29a3-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d29a3-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d29a3-145">See also</span></span>

- [<span data-ttu-id="d29a3-146">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="d29a3-146">GetAttachment operation</span></span>](getattachment-operation.md)
- [<span data-ttu-id="d29a3-147">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d29a3-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

