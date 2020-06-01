---
title: CreateAttachment 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e066db95-6963-4507-a8d0-8efad287f550
description: CreateAttachment 操作创建一个项目或文件附件，并将其附加到指定的项目。
ms.openlocfilehash: 8028c56aa306774b54b39e5ee1ac0382b9113fa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456568"
---
# <a name="createattachment-operation"></a><span data-ttu-id="8d35a-103">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="8d35a-103">CreateAttachment operation</span></span>

<span data-ttu-id="8d35a-104">CreateAttachment 操作创建一个项目或文件附件，并将其附加到指定的项目。</span><span class="sxs-lookup"><span data-stu-id="8d35a-104">The CreateAttachment operation creates either an item or file attachment and attaches it to the specified item.</span></span>
  
## <a name="file-createattachment-request-example"></a><span data-ttu-id="8d35a-105">File CreateAttachment 请求示例</span><span class="sxs-lookup"><span data-stu-id="8d35a-105">File CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="8d35a-106">说明</span><span class="sxs-lookup"><span data-stu-id="8d35a-106">Description</span></span>

<span data-ttu-id="8d35a-107">下面的 CreateAttachment 请求示例演示如何创建文件附件。</span><span class="sxs-lookup"><span data-stu-id="8d35a-107">The following example of a CreateAttachment request shows how to create a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="8d35a-108">代码</span><span class="sxs-lookup"><span data-stu-id="8d35a-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
<soap:Body>
  <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
    <ParentItemId Id="AAAtAE..." ChangeKey="CQAAABYA..."/>
    <Attachments>
      <t:FileAttachment>
        <t:Name>SomeFile</t:Name>
        <t:Content>AQIDBAU=</t:Content>
      </t:FileAttachment>
    </Attachments>
  </CreateAttachment>
</soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="8d35a-109">评论</span><span class="sxs-lookup"><span data-stu-id="8d35a-109">Comment</span></span>

<span data-ttu-id="8d35a-110">必须提供附件的名称。</span><span class="sxs-lookup"><span data-stu-id="8d35a-110">A name for the attachment must be provided.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d35a-111">已缩短父项目标识符和更改密钥以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="8d35a-111">The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="8d35a-112">Request 元素</span><span class="sxs-lookup"><span data-stu-id="8d35a-112">Request elements</span></span>

<span data-ttu-id="8d35a-113">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="8d35a-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="8d35a-114">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="8d35a-114">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="8d35a-115">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="8d35a-115">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="8d35a-116">附件</span><span class="sxs-lookup"><span data-stu-id="8d35a-116">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8d35a-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="8d35a-117">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="8d35a-118">名称（AttachmentType）</span><span class="sxs-lookup"><span data-stu-id="8d35a-118">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="8d35a-119">Content</span><span class="sxs-lookup"><span data-stu-id="8d35a-119">Content</span></span>](content.md)
    
## <a name="successful-file-createattachment-response-example"></a><span data-ttu-id="8d35a-120">成功的文件 CreateAttachment 响应示例</span><span class="sxs-lookup"><span data-stu-id="8d35a-120">Successful File CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="8d35a-121">说明</span><span class="sxs-lookup"><span data-stu-id="8d35a-121">Description</span></span>

<span data-ttu-id="8d35a-122">下面的示例演示对 CreateAttachment 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="8d35a-122">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="8d35a-123">代码</span><span class="sxs-lookup"><span data-stu-id="8d35a-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAE=" RootItemId="AAAtAEFk=" RootItemChangeKey="CQAAAB"/>
            </t:FileAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="8d35a-124">评论</span><span class="sxs-lookup"><span data-stu-id="8d35a-124">Comment</span></span>

<span data-ttu-id="8d35a-125">响应包含附加文件的标识符。</span><span class="sxs-lookup"><span data-stu-id="8d35a-125">The response contains the identifier of the attached file.</span></span> <span data-ttu-id="8d35a-126">它还包含根项的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="8d35a-126">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="8d35a-127">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="8d35a-127">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="8d35a-128">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="8d35a-128">Successful response elements</span></span>

<span data-ttu-id="8d35a-129">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="8d35a-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="8d35a-130">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8d35a-130">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8d35a-131">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="8d35a-131">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="8d35a-132">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8d35a-132">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8d35a-133">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8d35a-133">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="8d35a-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8d35a-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8d35a-135">附件</span><span class="sxs-lookup"><span data-stu-id="8d35a-135">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8d35a-136">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="8d35a-136">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="8d35a-137">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="8d35a-137">AttachmentId</span></span>](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a><span data-ttu-id="8d35a-138">Item CreateAttachment 请求示例</span><span class="sxs-lookup"><span data-stu-id="8d35a-138">Item CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="8d35a-139">说明</span><span class="sxs-lookup"><span data-stu-id="8d35a-139">Description</span></span>

<span data-ttu-id="8d35a-140">以下示例的 CreateAttachment 请求显示了如何创建项目附件。</span><span class="sxs-lookup"><span data-stu-id="8d35a-140">The following example of a CreateAttachment request shows how to create an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="8d35a-141">代码</span><span class="sxs-lookup"><span data-stu-id="8d35a-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="AAAtAE=" ChangeKey="CQAAABYA"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>An item attachment</t:Name>
          <t:Message>
            <t:Subject>A message to attach</t:Subject>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="8d35a-142">评论</span><span class="sxs-lookup"><span data-stu-id="8d35a-142">Comment</span></span>

<span data-ttu-id="8d35a-143">必须提供附件的名称。</span><span class="sxs-lookup"><span data-stu-id="8d35a-143">A name for the attachment must be provided.</span></span>
  
 <span data-ttu-id="8d35a-144">**注释**已缩短父项目标识符和更改密钥以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="8d35a-144">**Note** The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="8d35a-145">Request 元素</span><span class="sxs-lookup"><span data-stu-id="8d35a-145">Request elements</span></span>

<span data-ttu-id="8d35a-146">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="8d35a-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="8d35a-147">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="8d35a-147">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="8d35a-148">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="8d35a-148">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="8d35a-149">附件</span><span class="sxs-lookup"><span data-stu-id="8d35a-149">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8d35a-150">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="8d35a-150">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="8d35a-151">名称（AttachmentType）</span><span class="sxs-lookup"><span data-stu-id="8d35a-151">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="8d35a-152">邮件</span><span class="sxs-lookup"><span data-stu-id="8d35a-152">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8d35a-153">主题</span><span class="sxs-lookup"><span data-stu-id="8d35a-153">Subject</span></span>](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a><span data-ttu-id="8d35a-154">成功的项目 CreateAttachment 响应示例</span><span class="sxs-lookup"><span data-stu-id="8d35a-154">Successful Item CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="8d35a-155">说明</span><span class="sxs-lookup"><span data-stu-id="8d35a-155">Description</span></span>

<span data-ttu-id="8d35a-156">下面的示例演示对 CreateAttachment 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="8d35a-156">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="8d35a-157">代码</span><span class="sxs-lookup"><span data-stu-id="8d35a-157">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:ItemAttachment>
              <t:AttachmentId Id="AAAtAEFk=" RootItemId="AAAtAEFkb=" RootItemChangeKey="CQAAABYA"/>
            </t:ItemAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="8d35a-158">评论</span><span class="sxs-lookup"><span data-stu-id="8d35a-158">Comment</span></span>

<span data-ttu-id="8d35a-159">响应包含新附件的标识符。</span><span class="sxs-lookup"><span data-stu-id="8d35a-159">The response contains the identifier of the new attachment.</span></span> <span data-ttu-id="8d35a-160">它还包含根项的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="8d35a-160">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="8d35a-161">根项是包含附件的项。</span><span class="sxs-lookup"><span data-stu-id="8d35a-161">The root item is the item that contains the attachment.</span></span> <span data-ttu-id="8d35a-162">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="8d35a-162">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="8d35a-163">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="8d35a-163">Successful response elements</span></span>

<span data-ttu-id="8d35a-164">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="8d35a-164">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="8d35a-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8d35a-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8d35a-166">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="8d35a-166">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="8d35a-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8d35a-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8d35a-168">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8d35a-168">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="8d35a-169">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8d35a-169">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8d35a-170">附件</span><span class="sxs-lookup"><span data-stu-id="8d35a-170">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8d35a-171">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="8d35a-171">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="8d35a-172">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="8d35a-172">AttachmentId</span></span>](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a><span data-ttu-id="8d35a-173">CreateAttachment 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="8d35a-173">CreateAttachment Error response example</span></span>

### <a name="description"></a><span data-ttu-id="8d35a-174">说明</span><span class="sxs-lookup"><span data-stu-id="8d35a-174">Description</span></span>

<span data-ttu-id="8d35a-175">下面的示例演示对 CreateAttachment 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="8d35a-175">The following example shows an error response to the CreateAttachment request.</span></span> <span data-ttu-id="8d35a-176">错误是由于未指定附件的名称。</span><span class="sxs-lookup"><span data-stu-id="8d35a-176">The error is due to the fact that the name of the attachment was not specified.</span></span>
  
### <a name="code"></a><span data-ttu-id="8d35a-177">代码</span><span class="sxs-lookup"><span data-stu-id="8d35a-177">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Error">
          <m:MessageText>Required property is missing.</m:MessageText>
          <m:ResponseCode>ErrorRequiredPropertyMissing</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:ExceptionFieldURI FieldURI="attachment:Name"/>
          </m:MessageXml>
          <m:Attachments/>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="8d35a-178">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="8d35a-178">Error response elements</span></span>

<span data-ttu-id="8d35a-179">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="8d35a-179">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="8d35a-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8d35a-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8d35a-181">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="8d35a-181">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="8d35a-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8d35a-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8d35a-183">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8d35a-183">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="8d35a-184">MessageText</span><span class="sxs-lookup"><span data-stu-id="8d35a-184">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8d35a-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8d35a-185">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8d35a-186">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8d35a-186">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="8d35a-187">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8d35a-187">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="8d35a-188">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="8d35a-188">ExceptionFieldURI</span></span>](exceptionfielduri.md)
    
- [<span data-ttu-id="8d35a-189">附件</span><span class="sxs-lookup"><span data-stu-id="8d35a-189">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a><span data-ttu-id="8d35a-190">备注</span><span class="sxs-lookup"><span data-stu-id="8d35a-190">Remarks</span></span>

<span data-ttu-id="8d35a-191">如果在一次往返行程中，有多个附件附加到某个项目，则最后一条响应邮件中的 RootItemChangeKey 是代表包含附件的项目的新更改键的。</span><span class="sxs-lookup"><span data-stu-id="8d35a-191">If multiple attachments are attached to an item in a single round trip, the RootItemChangeKey in the last response message is the one that represents the new change key of the item that has the attachments.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d35a-192">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8d35a-192">See also</span></span>



[<span data-ttu-id="8d35a-193">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="8d35a-193">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="8d35a-194">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="8d35a-194">GetAttachment operation</span></span>](getattachment-operation.md)

