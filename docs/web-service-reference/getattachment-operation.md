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
# <a name="getattachment-operation"></a>GetAttachment 操作

GetAttachment 操作用于检索 Exchange 存储中项目的现有附件。
  
## <a name="getattachment-request-example"></a>GetAttachment 请求示例

### <a name="description"></a>Description

下面的 GetAttachment 请求示例演示如何获取附件。
  
### <a name="code"></a>代码

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

### <a name="comments"></a>备注

[AttachmentShape](attachmentshape.md)元素允许您指定应返回的附件信息。 空的[AttachmentShape](attachmentshape.md)元素有效，并将呈现不包含任何其他属性的项目附件的 MIME 内容的附件。 
  
[会话](attachmentids.md)集合允许您指定一个或多个要返回的附件标识符。 请注意，这些类型的类型为 RequestAttachmentIdType，因此从**CreateAttachment**收到的任何会话在将其传递到**RootItemChangeKey**之前，必须删除**RootItemId**和**GetAttachment**属性。
  
> [!NOTE]
> 附件标识符和更改密钥已缩短，以保持可读性。 
  
### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [GetAttachment](getattachment.md)
    
- [AttachmentShape](attachmentshape.md)
    
- [会话](attachmentids.md)
    
- [AttachmentId （GetAttachment 和 DeleteAttachment）](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a>GetAttachment 响应示例

### <a name="description"></a>Description

下面的示例演示对 GetAttachment 请求的成功响应。 本示例返回一个文件附件。
  
### <a name="code"></a>代码

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

### <a name="comments"></a>备注

GetAttachment 的响应邮件始终包含完整的附件;也就是说，将始终包含所有属性。 对于文件附件，这些属性是[名称（AttachmentType）](name-attachmenttype.md)、 [ContentType](contenttype.md)、 [ContentId](contentid.md)、 [ContentLocation](contentlocation.md)和[Content](content.md)。 对于项目附件，这些属性是[名称（AttachmentType）](name-attachmenttype.md)、 [ContentType](contenttype.md)、 [ContentId](contentid.md)、 [ContentLocation](contentlocation.md)和项目的所有属性，就像**AllProperties**形状已在 GetItem 调用中使用一样。 [AttachmentShape](attachmentshape.md)元素（如果存在）将允许使用者应用程序请求项目附件的其他扩展属性。 
  
### <a name="successful-response-elements"></a>成功的响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetAttachmentResponse](getattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetAttachmentResponseMessage](getattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [附件](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [AttachmentId （GetAttachment 和 DeleteAttachment）](attachmentid-getattachment-and-deleteattachment.md)
    
- [名称（AttachmentType）](name-attachmenttype.md)
    
- [Content](content.md)
    
## <a name="see-also"></a>另请参阅



[CreateAttachment 操作](createattachment-operation.md)
  
[DeleteAttachment 操作](deleteattachment-operation.md)

