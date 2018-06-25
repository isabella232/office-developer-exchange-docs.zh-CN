---
title: GetAttachment 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 24d10a15-b942-415e-9024-a6375708f326
description: GetAttachment 操作用于检索现有 Exchange 存储中的项目的附件。
ms.openlocfilehash: c260033208bf49c60463c09041d8ffcc52a8f5c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754469"
---
# <a name="getattachment-operation"></a><span data-ttu-id="86021-103">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="86021-103">GetAttachment operation</span></span>

<span data-ttu-id="86021-104">GetAttachment 操作用于检索现有 Exchange 存储中的项目的附件。</span><span class="sxs-lookup"><span data-stu-id="86021-104">The GetAttachment operation is used to retrieve existing attachments on items in the Exchange store.</span></span>
  
## <a name="getattachment-request-example"></a><span data-ttu-id="86021-105">GetAttachment 请求示例</span><span class="sxs-lookup"><span data-stu-id="86021-105">GetAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="86021-106">说明</span><span class="sxs-lookup"><span data-stu-id="86021-106">Description</span></span>

<span data-ttu-id="86021-107">GetAttachment 请求的下面的示例演示如何获取附件。</span><span class="sxs-lookup"><span data-stu-id="86021-107">The following example of GetAttachment request shows how to get an attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="86021-108">代码</span><span class="sxs-lookup"><span data-stu-id="86021-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="86021-109">注释</span><span class="sxs-lookup"><span data-stu-id="86021-109">Comments</span></span>

<span data-ttu-id="86021-110">[AttachmentShape](attachmentshape.md)元素可以指定应返回哪些附件信息。</span><span class="sxs-lookup"><span data-stu-id="86021-110">The [AttachmentShape](attachmentshape.md) element allows you to specify which attachment information should be returned.</span></span> <span data-ttu-id="86021-111">空[AttachmentShape](attachmentshape.md)元素有效，并且将呈现您没有文本正文类型，具有和没有任何其他属性的项目附件的 MIME 内容的附件。</span><span class="sxs-lookup"><span data-stu-id="86021-111">An empty [AttachmentShape](attachmentshape.md) element is valid and will render your attachments without MIME content for item attachments, with a text body type, and without any additional properties.</span></span> 
  
<span data-ttu-id="86021-112">[AttachmentIds](attachmentids.md)集允许您指定要返回的一个或多个附件标识符。</span><span class="sxs-lookup"><span data-stu-id="86021-112">The [AttachmentIds](attachmentids.md) collection allows you to specify one or more attachment identifiers to return.</span></span> <span data-ttu-id="86021-113">请注意，这些属于 RequestAttachmentIdType，因此您收到来自**CreateAttachment**任何 AttachmentIds 必须具有的**RootItemId**和**RootItemChangeKey**属性将它们传递给**GetAttachment**之前删除的类型。</span><span class="sxs-lookup"><span data-stu-id="86021-113">Note that these are of type RequestAttachmentIdType, so any AttachmentIds that you receive from **CreateAttachment** must have the **RootItemId** and **RootItemChangeKey** attributes removed before passing them to **GetAttachment**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="86021-114">已缩短的附件标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="86021-114">The attachment identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="86021-115">请求元素</span><span class="sxs-lookup"><span data-stu-id="86021-115">Request elements</span></span>

<span data-ttu-id="86021-116">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="86021-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="86021-117">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="86021-117">GetAttachment</span></span>](getattachment.md)
    
- [<span data-ttu-id="86021-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="86021-118">AttachmentShape</span></span>](attachmentshape.md)
    
- [<span data-ttu-id="86021-119">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="86021-119">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="86021-120">AttachmentId （GetAttachment 和 DeleteAttachment）</span><span class="sxs-lookup"><span data-stu-id="86021-120">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a><span data-ttu-id="86021-121">GetAttachment 响应示例</span><span class="sxs-lookup"><span data-stu-id="86021-121">GetAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="86021-122">说明</span><span class="sxs-lookup"><span data-stu-id="86021-122">Description</span></span>

<span data-ttu-id="86021-123">下面的示例演示对 GetAttachment 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="86021-123">The following example shows a successful response to a GetAttachment request.</span></span> <span data-ttu-id="86021-124">本示例返回的文件附件。</span><span class="sxs-lookup"><span data-stu-id="86021-124">This example returns a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="86021-125">代码</span><span class="sxs-lookup"><span data-stu-id="86021-125">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
              <t:Name>SomeFile</t:Name>
              <t:Content>AQIDBAU=</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </GetAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="86021-126">注释</span><span class="sxs-lookup"><span data-stu-id="86021-126">Comments</span></span>

<span data-ttu-id="86021-127">GetAttachment 响应邮件将始终包含完整的附件;也就是说，所有属性将始终都为包含。</span><span class="sxs-lookup"><span data-stu-id="86021-127">The response messages for GetAttachment will always contain the full attachment; that is, all properties will always be included.</span></span> <span data-ttu-id="86021-128">对于文件附件，这些属性的[名称 (AttachmentType)](name-attachmenttype.md)、 [ContentType](contenttype.md)、 [ContentId](contentid.md)、 [ContentLocation](contentlocation.md)，和[内容](content.md)。</span><span class="sxs-lookup"><span data-stu-id="86021-128">For file attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md), and [Content](content.md).</span></span> <span data-ttu-id="86021-129">对于项目的附件，这些属性的[名称 (AttachmentType)](name-attachmenttype.md)、 [ContentType](contenttype.md)、 [ContentId](contentid.md)、 [ContentLocation](contentlocation.md)和所有项目的属性， **AllProperties**形状象使用 GetItem 呼叫中。</span><span class="sxs-lookup"><span data-stu-id="86021-129">For item attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) and all of the item's properties, as if the **AllProperties** shape had been used in a GetItem call.</span></span> <span data-ttu-id="86021-130">[AttachmentShape](attachmentshape.md)元素中，如果存在此参数，将允许使用者应用程序请求的项目附件的其他扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="86021-130">The [AttachmentShape](attachmentshape.md) element, if present, will allow a consumer application to request additional extended properties for item attachments.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="86021-131">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="86021-131">Successful response elements</span></span>

<span data-ttu-id="86021-132">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="86021-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="86021-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="86021-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="86021-134">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="86021-134">GetAttachmentResponse</span></span>](getattachmentresponse.md)
    
- [<span data-ttu-id="86021-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="86021-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="86021-136">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="86021-136">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
    
- [<span data-ttu-id="86021-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="86021-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="86021-138">附件</span><span class="sxs-lookup"><span data-stu-id="86021-138">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="86021-139">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="86021-139">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="86021-140">AttachmentId （GetAttachment 和 DeleteAttachment）</span><span class="sxs-lookup"><span data-stu-id="86021-140">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
- [<span data-ttu-id="86021-141">名称 (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="86021-141">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="86021-142">内容</span><span class="sxs-lookup"><span data-stu-id="86021-142">Content</span></span>](content.md)
    
## <a name="see-also"></a><span data-ttu-id="86021-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="86021-143">See also</span></span>



[<span data-ttu-id="86021-144">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="86021-144">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="86021-145">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="86021-145">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

