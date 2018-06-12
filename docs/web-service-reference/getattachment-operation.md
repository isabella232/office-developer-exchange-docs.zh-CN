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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754469"
---
# <a name="getattachment-operation"></a>GetAttachment 操作

GetAttachment 操作用于检索现有 Exchange 存储中的项目的附件。
  
## <a name="getattachment-request-example"></a>GetAttachment 请求示例

### <a name="description"></a>说明

GetAttachment 请求的下面的示例演示如何获取附件。
  
### <a name="code"></a>代码

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

### <a name="comments"></a>注释

[AttachmentShape](attachmentshape.md)元素可以指定应返回哪些附件信息。 空[AttachmentShape](attachmentshape.md)元素有效，并且将呈现您没有文本正文类型，具有和没有任何其他属性的项目附件的 MIME 内容的附件。 
  
[AttachmentIds](attachmentids.md)集允许您指定要返回的一个或多个附件标识符。 请注意，这些属于 RequestAttachmentIdType，因此您收到来自**CreateAttachment**任何 AttachmentIds 必须具有的**RootItemId**和**RootItemChangeKey**属性将它们传递给**GetAttachment**之前删除的类型。
  
> [!NOTE]
> 已缩短的附件标识符和更改密钥，以保留可读性。 
  
### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [GetAttachment](getattachment.md)
    
- [AttachmentShape](attachmentshape.md)
    
- [AttachmentIds](attachmentids.md)
    
- [AttachmentId （GetAttachment 和 DeleteAttachment）](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a>GetAttachment 响应示例

### <a name="description"></a>说明

下面的示例演示对 GetAttachment 请求成功响应。 本示例返回的文件附件。
  
### <a name="code"></a>代码

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

### <a name="comments"></a>注释

GetAttachment 响应邮件将始终包含完整的附件;也就是说，所有属性将始终都为包含。 对于文件附件，这些属性的[名称 (AttachmentType)](name-attachmenttype.md)、 [ContentType](contenttype.md)、 [ContentId](contentid.md)、 [ContentLocation](contentlocation.md)，和[内容](content.md)。 对于项目的附件，这些属性的[名称 (AttachmentType)](name-attachmenttype.md)、 [ContentType](contenttype.md)、 [ContentId](contentid.md)、 [ContentLocation](contentlocation.md)和所有项目的属性， **AllProperties**形状象使用 GetItem 呼叫中。 [AttachmentShape](attachmentshape.md)元素中，如果存在此参数，将允许使用者应用程序请求的项目附件的其他扩展的属性。 
  
### <a name="successful-response-elements"></a>成功响应元素

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetAttachmentResponse](getattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetAttachmentResponseMessage](getattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [附件](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [AttachmentId （GetAttachment 和 DeleteAttachment）](attachmentid-getattachment-and-deleteattachment.md)
    
- [名称 (AttachmentType)](name-attachmenttype.md)
    
- [内容](content.md)
    
## <a name="see-also"></a>另请参阅



[CreateAttachment 操作](createattachment-operation.md)
  
[DeleteAttachment 操作](deleteattachment-operation.md)

