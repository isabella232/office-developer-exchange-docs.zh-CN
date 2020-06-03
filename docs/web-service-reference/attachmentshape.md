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
description: AttachmentShape 元素标识要在 GetAttachment 请求的响应中返回的其他属性。
ms.openlocfilehash: e70fbaad0f649c5afdc151b777efef0f8927ba1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529663"
---
# <a name="attachmentshape"></a><span data-ttu-id="a8c1d-103">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="a8c1d-103">AttachmentShape</span></span>

<span data-ttu-id="a8c1d-104">**AttachmentShape**元素标识要在[GetAttachment](getattachment.md)请求的响应中返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-104">The **AttachmentShape** element identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> 
  
- [<span data-ttu-id="a8c1d-105">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="a8c1d-105">GetAttachment</span></span>](getattachment.md)
  
- [<span data-ttu-id="a8c1d-106">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="a8c1d-106">AttachmentShape</span></span>](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 <span data-ttu-id="a8c1d-107">**AttachmentResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="a8c1d-107">**AttachmentResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8c1d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a8c1d-108">Attributes and elements</span></span>

<span data-ttu-id="a8c1d-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8c1d-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="a8c1d-110">Attributes</span></span>

<span data-ttu-id="a8c1d-111">无。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8c1d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="a8c1d-112">Child elements</span></span>

|<span data-ttu-id="a8c1d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a8c1d-113">**Element**</span></span>|<span data-ttu-id="a8c1d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a8c1d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8c1d-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="a8c1d-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="a8c1d-116">指定响应中是否返回项目或附件的多用途 Internet 邮件扩展（MIME）内容。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> <span data-ttu-id="a8c1d-117">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a8c1d-118">BodyType</span><span class="sxs-lookup"><span data-stu-id="a8c1d-118">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="a8c1d-119">标识正文文本在响应中的格式。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-119">Identifies how the body text is formatted in the response.</span></span> <span data-ttu-id="a8c1d-120">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a8c1d-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="a8c1d-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="a8c1d-122">指定是否从附件中筛选出可能不安全的 HTML 内容。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-122">Specifies whether potentially unsafe HTML content is filtered from an attachment.</span></span> <span data-ttu-id="a8c1d-123">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-123">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a8c1d-124">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="a8c1d-124">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="a8c1d-125">标识要在响应中返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-125">Identifies additional properties to return in a response.</span></span> <span data-ttu-id="a8c1d-126">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-126">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a8c1d-127">父元素</span><span class="sxs-lookup"><span data-stu-id="a8c1d-127">Parent elements</span></span>

|<span data-ttu-id="a8c1d-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="a8c1d-128">**Element**</span></span>|<span data-ttu-id="a8c1d-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="a8c1d-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8c1d-130">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="a8c1d-130">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="a8c1d-131">定义从 Exchange 存储中的邮箱获取附件的请求的元素。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-131">The element that defines a request to get an attachment from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="a8c1d-132">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="a8c1d-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a8c1d-133">文本值</span><span class="sxs-lookup"><span data-stu-id="a8c1d-133">Text value</span></span>

<span data-ttu-id="a8c1d-134">无。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8c1d-135">说明</span><span class="sxs-lookup"><span data-stu-id="a8c1d-135">Remarks</span></span>

<span data-ttu-id="a8c1d-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a8c1d-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8c1d-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="a8c1d-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8c1d-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="a8c1d-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a8c1d-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="a8c1d-139">Schema Name</span></span>  <br/> |<span data-ttu-id="a8c1d-140">消息架构</span><span class="sxs-lookup"><span data-stu-id="a8c1d-140">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a8c1d-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="a8c1d-141">Validation File</span></span>  <br/> |<span data-ttu-id="a8c1d-142">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a8c1d-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a8c1d-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="a8c1d-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="a8c1d-144">False</span><span class="sxs-lookup"><span data-stu-id="a8c1d-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8c1d-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a8c1d-145">See also</span></span>

- [<span data-ttu-id="a8c1d-146">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="a8c1d-146">GetAttachment operation</span></span>](getattachment-operation.md)
- [<span data-ttu-id="a8c1d-147">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a8c1d-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

