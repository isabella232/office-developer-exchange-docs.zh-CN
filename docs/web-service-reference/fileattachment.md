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
description: FileAttachment 元素表示附加到 Exchange 存储中的项的文件。
ms.openlocfilehash: 5ce7aef753313aa9430f640bb3c26f652b8c1c43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754310"
---
# <a name="fileattachment"></a><span data-ttu-id="7b64b-103">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="7b64b-103">FileAttachment</span></span>

<span data-ttu-id="7b64b-104">**FileAttachment**元素表示附加到 Exchange 存储中的项的文件。</span><span class="sxs-lookup"><span data-stu-id="7b64b-104">The **FileAttachment** element represents a file that is attached to an item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="7b64b-105">**FileAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="7b64b-105">**FileAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b64b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7b64b-106">Attributes and elements</span></span>

<span data-ttu-id="7b64b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7b64b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b64b-108">属性</span><span class="sxs-lookup"><span data-stu-id="7b64b-108">Attributes</span></span>

<span data-ttu-id="7b64b-109">无。</span><span class="sxs-lookup"><span data-stu-id="7b64b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b64b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7b64b-110">Child elements</span></span>

|<span data-ttu-id="7b64b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b64b-111">**Element**</span></span>|<span data-ttu-id="7b64b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b64b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b64b-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="7b64b-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="7b64b-114">标识的文件附件。</span><span class="sxs-lookup"><span data-stu-id="7b64b-114">Identifies the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="7b64b-115">名称 (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="7b64b-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="7b64b-116">表示附件的名称。</span><span class="sxs-lookup"><span data-stu-id="7b64b-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="7b64b-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="7b64b-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="7b64b-118">描述附件内容多用途 Internet 邮件扩展 (MIME) 类型。</span><span class="sxs-lookup"><span data-stu-id="7b64b-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="7b64b-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="7b64b-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="7b64b-120">表示内容的附件的标识符。</span><span class="sxs-lookup"><span data-stu-id="7b64b-120">Represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="7b64b-121">[ContentId](contentid.md)可以设置为任何字符串值。</span><span class="sxs-lookup"><span data-stu-id="7b64b-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="7b64b-122">应用程序可以使用[ContentId](contentid.md)来实现自己标识机制。</span><span class="sxs-lookup"><span data-stu-id="7b64b-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="7b64b-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="7b64b-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="7b64b-124">包含附件的内容的位置所对应的统一资源标识符 (URI)。</span><span class="sxs-lookup"><span data-stu-id="7b64b-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="7b64b-125">Size</span><span class="sxs-lookup"><span data-stu-id="7b64b-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="7b64b-126">表示以字节为单位的附件文件的大小。</span><span class="sxs-lookup"><span data-stu-id="7b64b-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="7b64b-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="7b64b-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="7b64b-128">表示上次修改文件附件。</span><span class="sxs-lookup"><span data-stu-id="7b64b-128">Represents when the file attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="7b64b-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="7b64b-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="7b64b-130">表示是否附件显示为内嵌项目中。</span><span class="sxs-lookup"><span data-stu-id="7b64b-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="7b64b-131">IsContactPhoto</span><span class="sxs-lookup"><span data-stu-id="7b64b-131">IsContactPhoto</span></span>](iscontactphoto.md) <br/> |<span data-ttu-id="7b64b-132">指示附件是否是联系人的图片。</span><span class="sxs-lookup"><span data-stu-id="7b64b-132">Indicates whether the file attachment is a contact picture.</span></span>  <br/> |
|[<span data-ttu-id="7b64b-133">内容</span><span class="sxs-lookup"><span data-stu-id="7b64b-133">Content</span></span>](content.md) <br/> |<span data-ttu-id="7b64b-134">包含 Base64 编码的文件附件的内容。</span><span class="sxs-lookup"><span data-stu-id="7b64b-134">Contains the Base64-encoded contents of the file attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b64b-135">父元素</span><span class="sxs-lookup"><span data-stu-id="7b64b-135">Parent elements</span></span>

|<span data-ttu-id="7b64b-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b64b-136">**Element**</span></span>|<span data-ttu-id="7b64b-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b64b-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b64b-138">附件</span><span class="sxs-lookup"><span data-stu-id="7b64b-138">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7b64b-139">包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="7b64b-139">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7b64b-140">文本值</span><span class="sxs-lookup"><span data-stu-id="7b64b-140">Text value</span></span>

<span data-ttu-id="7b64b-141">无。</span><span class="sxs-lookup"><span data-stu-id="7b64b-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b64b-142">备注</span><span class="sxs-lookup"><span data-stu-id="7b64b-142">Remarks</span></span>

<span data-ttu-id="7b64b-143">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7b64b-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b64b-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="7b64b-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b64b-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="7b64b-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7b64b-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="7b64b-146">Schema name</span></span>  <br/> |<span data-ttu-id="7b64b-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="7b64b-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="7b64b-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="7b64b-148">Validation file</span></span>  <br/> |<span data-ttu-id="7b64b-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7b64b-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7b64b-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="7b64b-150">Can be empty</span></span>  <br/> |<span data-ttu-id="7b64b-151">False</span><span class="sxs-lookup"><span data-stu-id="7b64b-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b64b-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7b64b-152">See also</span></span>



- [<span data-ttu-id="7b64b-153">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7b64b-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

