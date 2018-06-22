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
description: CreateAttachment 操作创建的项目或文件附件，并将其附加到指定的项。
ms.openlocfilehash: fed60275a007f2796c60d936def7a937e4982f29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753623"
---
# <a name="createattachment-operation"></a><span data-ttu-id="b735c-103">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="b735c-103">CreateAttachment operation</span></span>

<span data-ttu-id="b735c-104">CreateAttachment 操作创建的项目或文件附件，并将其附加到指定的项。</span><span class="sxs-lookup"><span data-stu-id="b735c-104">The CreateAttachment operation creates either an item or file attachment and attaches it to the specified item.</span></span>
  
## <a name="file-createattachment-request-example"></a><span data-ttu-id="b735c-105">文件 CreateAttachment 请求示例</span><span class="sxs-lookup"><span data-stu-id="b735c-105">File CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="b735c-106">说明</span><span class="sxs-lookup"><span data-stu-id="b735c-106">Description</span></span>

<span data-ttu-id="b735c-107">CreateAttachment 请求的下面的示例演示如何创建的文件附件。</span><span class="sxs-lookup"><span data-stu-id="b735c-107">The following example of a CreateAttachment request shows how to create a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="b735c-108">代码</span><span class="sxs-lookup"><span data-stu-id="b735c-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
<soap:Body>
  <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comment"></a><span data-ttu-id="b735c-109">Comment</span><span class="sxs-lookup"><span data-stu-id="b735c-109">Comment</span></span>

<span data-ttu-id="b735c-110">必须提供附件的名称。</span><span class="sxs-lookup"><span data-stu-id="b735c-110">A name for the attachment must be provided.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b735c-111">已缩短的父项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="b735c-111">The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="b735c-112">请求元素</span><span class="sxs-lookup"><span data-stu-id="b735c-112">Request elements</span></span>

<span data-ttu-id="b735c-113">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b735c-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b735c-114">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="b735c-114">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="b735c-115">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="b735c-115">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="b735c-116">附件</span><span class="sxs-lookup"><span data-stu-id="b735c-116">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b735c-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="b735c-117">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="b735c-118">名称 (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="b735c-118">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="b735c-119">内容</span><span class="sxs-lookup"><span data-stu-id="b735c-119">Content</span></span>](content.md)
    
## <a name="successful-file-createattachment-response-example"></a><span data-ttu-id="b735c-120">成功文件 CreateAttachment 响应示例</span><span class="sxs-lookup"><span data-stu-id="b735c-120">Successful File CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="b735c-121">说明</span><span class="sxs-lookup"><span data-stu-id="b735c-121">Description</span></span>

<span data-ttu-id="b735c-122">下面的示例演示对 CreateAttachment 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="b735c-122">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="b735c-123">代码</span><span class="sxs-lookup"><span data-stu-id="b735c-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comment"></a><span data-ttu-id="b735c-124">Comment</span><span class="sxs-lookup"><span data-stu-id="b735c-124">Comment</span></span>

<span data-ttu-id="b735c-125">则响应中包含附加文件的标识符。</span><span class="sxs-lookup"><span data-stu-id="b735c-125">The response contains the identifier of the attached file.</span></span> <span data-ttu-id="b735c-126">它还包含根项目的标识符和更改项。</span><span class="sxs-lookup"><span data-stu-id="b735c-126">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="b735c-127">已缩短的项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="b735c-127">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="b735c-128">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="b735c-128">Successful response elements</span></span>

<span data-ttu-id="b735c-129">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b735c-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="b735c-130">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b735c-130">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b735c-131">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="b735c-131">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="b735c-132">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b735c-132">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b735c-133">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b735c-133">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="b735c-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b735c-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b735c-135">附件</span><span class="sxs-lookup"><span data-stu-id="b735c-135">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b735c-136">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="b735c-136">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="b735c-137">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="b735c-137">AttachmentId</span></span>](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a><span data-ttu-id="b735c-138">项目 CreateAttachment 请求示例</span><span class="sxs-lookup"><span data-stu-id="b735c-138">Item CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="b735c-139">说明</span><span class="sxs-lookup"><span data-stu-id="b735c-139">Description</span></span>

<span data-ttu-id="b735c-140">CreateAttachment 请求的下面的示例演示如何创建项目附件。</span><span class="sxs-lookup"><span data-stu-id="b735c-140">The following example of a CreateAttachment request shows how to create an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="b735c-141">代码</span><span class="sxs-lookup"><span data-stu-id="b735c-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comment"></a><span data-ttu-id="b735c-142">Comment</span><span class="sxs-lookup"><span data-stu-id="b735c-142">Comment</span></span>

<span data-ttu-id="b735c-143">必须提供附件的名称。</span><span class="sxs-lookup"><span data-stu-id="b735c-143">A name for the attachment must be provided.</span></span>
  
 <span data-ttu-id="b735c-144">**注释**已缩短的父项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="b735c-144">**Note** The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="b735c-145">请求元素</span><span class="sxs-lookup"><span data-stu-id="b735c-145">Request elements</span></span>

<span data-ttu-id="b735c-146">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b735c-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b735c-147">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="b735c-147">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="b735c-148">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="b735c-148">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="b735c-149">附件</span><span class="sxs-lookup"><span data-stu-id="b735c-149">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b735c-150">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="b735c-150">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="b735c-151">名称 (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="b735c-151">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="b735c-152">Message</span><span class="sxs-lookup"><span data-stu-id="b735c-152">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b735c-153">Subject</span><span class="sxs-lookup"><span data-stu-id="b735c-153">Subject</span></span>](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a><span data-ttu-id="b735c-154">成功的项 CreateAttachment 响应示例</span><span class="sxs-lookup"><span data-stu-id="b735c-154">Successful Item CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="b735c-155">说明</span><span class="sxs-lookup"><span data-stu-id="b735c-155">Description</span></span>

<span data-ttu-id="b735c-156">下面的示例演示对 CreateAttachment 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="b735c-156">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="b735c-157">代码</span><span class="sxs-lookup"><span data-stu-id="b735c-157">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comment"></a><span data-ttu-id="b735c-158">Comment</span><span class="sxs-lookup"><span data-stu-id="b735c-158">Comment</span></span>

<span data-ttu-id="b735c-159">则响应中包含新附件的标识符。</span><span class="sxs-lookup"><span data-stu-id="b735c-159">The response contains the identifier of the new attachment.</span></span> <span data-ttu-id="b735c-160">它还包含根项目的标识符和更改项。</span><span class="sxs-lookup"><span data-stu-id="b735c-160">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="b735c-161">根项目包含附件的项目。</span><span class="sxs-lookup"><span data-stu-id="b735c-161">The root item is the item that contains the attachment.</span></span> <span data-ttu-id="b735c-162">已缩短的项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="b735c-162">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="b735c-163">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="b735c-163">Successful response elements</span></span>

<span data-ttu-id="b735c-164">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b735c-164">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="b735c-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b735c-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b735c-166">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="b735c-166">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="b735c-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b735c-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b735c-168">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b735c-168">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="b735c-169">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b735c-169">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b735c-170">附件</span><span class="sxs-lookup"><span data-stu-id="b735c-170">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b735c-171">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="b735c-171">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="b735c-172">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="b735c-172">AttachmentId</span></span>](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a><span data-ttu-id="b735c-173">CreateAttachment 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="b735c-173">CreateAttachment Error response example</span></span>

### <a name="description"></a><span data-ttu-id="b735c-174">说明</span><span class="sxs-lookup"><span data-stu-id="b735c-174">Description</span></span>

<span data-ttu-id="b735c-175">下面的示例演示对 CreateAttachment 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="b735c-175">The following example shows an error response to the CreateAttachment request.</span></span> <span data-ttu-id="b735c-176">错误是由于，未指定附件的名称。</span><span class="sxs-lookup"><span data-stu-id="b735c-176">The error is due to the fact that the name of the attachment was not specified.</span></span>
  
### <a name="code"></a><span data-ttu-id="b735c-177">代码</span><span class="sxs-lookup"><span data-stu-id="b735c-177">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="b735c-178">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="b735c-178">Error response elements</span></span>

<span data-ttu-id="b735c-179">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b735c-179">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="b735c-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b735c-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b735c-181">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="b735c-181">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="b735c-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b735c-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b735c-183">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b735c-183">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="b735c-184">MessageText</span><span class="sxs-lookup"><span data-stu-id="b735c-184">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="b735c-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b735c-185">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b735c-186">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b735c-186">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="b735c-187">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b735c-187">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="b735c-188">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="b735c-188">ExceptionFieldURI</span></span>](exceptionfielduri.md)
    
- [<span data-ttu-id="b735c-189">附件</span><span class="sxs-lookup"><span data-stu-id="b735c-189">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a><span data-ttu-id="b735c-190">备注</span><span class="sxs-lookup"><span data-stu-id="b735c-190">Remarks</span></span>

<span data-ttu-id="b735c-191">如果多个附件附加到单个往返中的项目，最后一个响应消息中的 RootItemChangeKey 是项的表示具有附件的新更改键。</span><span class="sxs-lookup"><span data-stu-id="b735c-191">If multiple attachments are attached to an item in a single round trip, the RootItemChangeKey in the last response message is the one that represents the new change key of the item that has the attachments.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b735c-192">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b735c-192">See also</span></span>



[<span data-ttu-id="b735c-193">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="b735c-193">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="b735c-194">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="b735c-194">GetAttachment operation</span></span>](getattachment-operation.md)

