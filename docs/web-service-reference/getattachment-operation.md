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
description: GetAttachment 操作用于检索 Exchange 存储中项目的现有附件。
ms.openlocfilehash: ac7eafd61c62b077a8d20e5fd8d004924bf06cf1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461287"
---
# <a name="getattachment-operation"></a><span data-ttu-id="a6a0b-103">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="a6a0b-103">GetAttachment operation</span></span>

<span data-ttu-id="a6a0b-104">GetAttachment 操作用于检索 Exchange 存储中项目的现有附件。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-104">The GetAttachment operation is used to retrieve existing attachments on items in the Exchange store.</span></span>
  
## <a name="getattachment-request-example"></a><span data-ttu-id="a6a0b-105">GetAttachment 请求示例</span><span class="sxs-lookup"><span data-stu-id="a6a0b-105">GetAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="a6a0b-106">Description</span><span class="sxs-lookup"><span data-stu-id="a6a0b-106">Description</span></span>

<span data-ttu-id="a6a0b-107">下面的 GetAttachment 请求示例演示如何获取附件。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-107">The following example of GetAttachment request shows how to get an attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="a6a0b-108">代码</span><span class="sxs-lookup"><span data-stu-id="a6a0b-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="a6a0b-109">备注</span><span class="sxs-lookup"><span data-stu-id="a6a0b-109">Comments</span></span>

<span data-ttu-id="a6a0b-110">[AttachmentShape](attachmentshape.md)元素允许您指定应返回的附件信息。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-110">The [AttachmentShape](attachmentshape.md) element allows you to specify which attachment information should be returned.</span></span> <span data-ttu-id="a6a0b-111">空的[AttachmentShape](attachmentshape.md)元素有效，并将呈现不包含任何其他属性的项目附件的 MIME 内容的附件。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-111">An empty [AttachmentShape](attachmentshape.md) element is valid and will render your attachments without MIME content for item attachments, with a text body type, and without any additional properties.</span></span> 
  
<span data-ttu-id="a6a0b-112">[会话](attachmentids.md)集合允许您指定一个或多个要返回的附件标识符。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-112">The [AttachmentIds](attachmentids.md) collection allows you to specify one or more attachment identifiers to return.</span></span> <span data-ttu-id="a6a0b-113">请注意，这些类型的类型为 RequestAttachmentIdType，因此从**CreateAttachment**收到的任何会话在将其传递到**RootItemChangeKey**之前，必须删除**RootItemId**和**GetAttachment**属性。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-113">Note that these are of type RequestAttachmentIdType, so any AttachmentIds that you receive from **CreateAttachment** must have the **RootItemId** and **RootItemChangeKey** attributes removed before passing them to **GetAttachment**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a6a0b-114">附件标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-114">The attachment identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="a6a0b-115">Request 元素</span><span class="sxs-lookup"><span data-stu-id="a6a0b-115">Request elements</span></span>

<span data-ttu-id="a6a0b-116">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a6a0b-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a6a0b-117">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="a6a0b-117">GetAttachment</span></span>](getattachment.md)
    
- [<span data-ttu-id="a6a0b-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="a6a0b-118">AttachmentShape</span></span>](attachmentshape.md)
    
- [<span data-ttu-id="a6a0b-119">会话</span><span class="sxs-lookup"><span data-stu-id="a6a0b-119">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="a6a0b-120">AttachmentId （GetAttachment 和 DeleteAttachment）</span><span class="sxs-lookup"><span data-stu-id="a6a0b-120">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a><span data-ttu-id="a6a0b-121">GetAttachment 响应示例</span><span class="sxs-lookup"><span data-stu-id="a6a0b-121">GetAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="a6a0b-122">Description</span><span class="sxs-lookup"><span data-stu-id="a6a0b-122">Description</span></span>

<span data-ttu-id="a6a0b-123">下面的示例演示对 GetAttachment 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-123">The following example shows a successful response to a GetAttachment request.</span></span> <span data-ttu-id="a6a0b-124">本示例返回一个文件附件。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-124">This example returns a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="a6a0b-125">代码</span><span class="sxs-lookup"><span data-stu-id="a6a0b-125">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="a6a0b-126">备注</span><span class="sxs-lookup"><span data-stu-id="a6a0b-126">Comments</span></span>

<span data-ttu-id="a6a0b-127">GetAttachment 的响应邮件始终包含完整的附件;也就是说，将始终包含所有属性。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-127">The response messages for GetAttachment will always contain the full attachment; that is, all properties will always be included.</span></span> <span data-ttu-id="a6a0b-128">对于文件附件，这些属性是[名称（AttachmentType）](name-attachmenttype.md)、 [ContentType](contenttype.md)、 [ContentId](contentid.md)、 [ContentLocation](contentlocation.md)和[Content](content.md)。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-128">For file attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md), and [Content](content.md).</span></span> <span data-ttu-id="a6a0b-129">对于项目附件，这些属性是[名称（AttachmentType）](name-attachmenttype.md)、 [ContentType](contenttype.md)、 [ContentId](contentid.md)、 [ContentLocation](contentlocation.md)和项目的所有属性，就像**AllProperties**形状已在 GetItem 调用中使用一样。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-129">For item attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) and all of the item's properties, as if the **AllProperties** shape had been used in a GetItem call.</span></span> <span data-ttu-id="a6a0b-130">[AttachmentShape](attachmentshape.md)元素（如果存在）将允许使用者应用程序请求项目附件的其他扩展属性。</span><span class="sxs-lookup"><span data-stu-id="a6a0b-130">The [AttachmentShape](attachmentshape.md) element, if present, will allow a consumer application to request additional extended properties for item attachments.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="a6a0b-131">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="a6a0b-131">Successful response elements</span></span>

<span data-ttu-id="a6a0b-132">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a6a0b-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a6a0b-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a6a0b-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a6a0b-134">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="a6a0b-134">GetAttachmentResponse</span></span>](getattachmentresponse.md)
    
- [<span data-ttu-id="a6a0b-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a6a0b-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a6a0b-136">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a6a0b-136">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
    
- [<span data-ttu-id="a6a0b-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a6a0b-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a6a0b-138">附件</span><span class="sxs-lookup"><span data-stu-id="a6a0b-138">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a6a0b-139">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="a6a0b-139">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="a6a0b-140">AttachmentId （GetAttachment 和 DeleteAttachment）</span><span class="sxs-lookup"><span data-stu-id="a6a0b-140">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
- [<span data-ttu-id="a6a0b-141">名称（AttachmentType）</span><span class="sxs-lookup"><span data-stu-id="a6a0b-141">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="a6a0b-142">Content</span><span class="sxs-lookup"><span data-stu-id="a6a0b-142">Content</span></span>](content.md)
    
## <a name="see-also"></a><span data-ttu-id="a6a0b-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6a0b-143">See also</span></span>



[<span data-ttu-id="a6a0b-144">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="a6a0b-144">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="a6a0b-145">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="a6a0b-145">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

