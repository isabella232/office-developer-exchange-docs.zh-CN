---
title: FileAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: FileAttachment 元素表示附加到 Exchange 存储中的项目的文件。
ms.openlocfilehash: db9b541fb2527ae3c09cbdb33bedea7fb215bd30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461014"
---
# <a name="fileattachment"></a><span data-ttu-id="6229c-103">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="6229c-103">FileAttachment</span></span>

<span data-ttu-id="6229c-104">**FileAttachment**元素表示附加到 Exchange 存储中的项目的文件。</span><span class="sxs-lookup"><span data-stu-id="6229c-104">The **FileAttachment** element represents a file that is attached to an item in the Exchange store.</span></span> 
  
```XML
<FileAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <IsContactPhoto/>
   <Content/>
</FileAttachment>
```

 <span data-ttu-id="6229c-105">**FileAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="6229c-105">**FileAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6229c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6229c-106">Attributes and elements</span></span>

<span data-ttu-id="6229c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6229c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6229c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6229c-108">Attributes</span></span>

<span data-ttu-id="6229c-109">无。</span><span class="sxs-lookup"><span data-stu-id="6229c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6229c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6229c-110">Child elements</span></span>

|<span data-ttu-id="6229c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6229c-111">**Element**</span></span>|<span data-ttu-id="6229c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6229c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6229c-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="6229c-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="6229c-114">标识文件附件。</span><span class="sxs-lookup"><span data-stu-id="6229c-114">Identifies the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="6229c-115">名称（AttachmentType）</span><span class="sxs-lookup"><span data-stu-id="6229c-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="6229c-116">代表附件的名称。</span><span class="sxs-lookup"><span data-stu-id="6229c-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="6229c-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="6229c-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="6229c-118">描述附件内容的多用途 Internet 邮件扩展（MIME）类型。</span><span class="sxs-lookup"><span data-stu-id="6229c-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="6229c-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="6229c-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="6229c-120">表示附件内容的标识符。</span><span class="sxs-lookup"><span data-stu-id="6229c-120">Represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="6229c-121">[ContentId](contentid.md)可以设置为任何字符串值。</span><span class="sxs-lookup"><span data-stu-id="6229c-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="6229c-122">应用程序可以使用[ContentId](contentid.md)来实现自己的标识机制。</span><span class="sxs-lookup"><span data-stu-id="6229c-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="6229c-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="6229c-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="6229c-124">包含与附件内容的位置相对应的统一资源标识符（URI）。</span><span class="sxs-lookup"><span data-stu-id="6229c-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="6229c-125">大小</span><span class="sxs-lookup"><span data-stu-id="6229c-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="6229c-126">表示文件附件的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="6229c-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="6229c-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="6229c-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="6229c-128">表示上次修改文件附件的时间。</span><span class="sxs-lookup"><span data-stu-id="6229c-128">Represents when the file attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="6229c-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="6229c-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="6229c-130">表示附件是否内联显示在项目中。</span><span class="sxs-lookup"><span data-stu-id="6229c-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="6229c-131">IsContactPhoto</span><span class="sxs-lookup"><span data-stu-id="6229c-131">IsContactPhoto</span></span>](iscontactphoto.md) <br/> |<span data-ttu-id="6229c-132">指示文件附件是否为联系人图片。</span><span class="sxs-lookup"><span data-stu-id="6229c-132">Indicates whether the file attachment is a contact picture.</span></span>  <br/> |
|[<span data-ttu-id="6229c-133">Content</span><span class="sxs-lookup"><span data-stu-id="6229c-133">Content</span></span>](content.md) <br/> |<span data-ttu-id="6229c-134">包含文件附件的 Base64 编码的内容。</span><span class="sxs-lookup"><span data-stu-id="6229c-134">Contains the Base64-encoded contents of the file attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6229c-135">父元素</span><span class="sxs-lookup"><span data-stu-id="6229c-135">Parent elements</span></span>

|<span data-ttu-id="6229c-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="6229c-136">**Element**</span></span>|<span data-ttu-id="6229c-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="6229c-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6229c-138">附件</span><span class="sxs-lookup"><span data-stu-id="6229c-138">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6229c-139">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="6229c-139">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6229c-140">文本值</span><span class="sxs-lookup"><span data-stu-id="6229c-140">Text value</span></span>

<span data-ttu-id="6229c-141">无。</span><span class="sxs-lookup"><span data-stu-id="6229c-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6229c-142">说明</span><span class="sxs-lookup"><span data-stu-id="6229c-142">Remarks</span></span>

<span data-ttu-id="6229c-143">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6229c-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6229c-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="6229c-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6229c-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="6229c-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6229c-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="6229c-146">Schema name</span></span>  <br/> |<span data-ttu-id="6229c-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="6229c-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="6229c-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="6229c-148">Validation file</span></span>  <br/> |<span data-ttu-id="6229c-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6229c-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6229c-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="6229c-150">Can be empty</span></span>  <br/> |<span data-ttu-id="6229c-151">False</span><span class="sxs-lookup"><span data-stu-id="6229c-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6229c-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6229c-152">See also</span></span>



- [<span data-ttu-id="6229c-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6229c-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

