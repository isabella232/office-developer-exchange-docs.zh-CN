---
title: GetAttachment 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 24d10a15-b942-415e-9024-a6375708f326
description: GetAttachment 操作用于检索邮件存储中项目Exchange附件。
ms.openlocfilehash: 44a9e1988deb513039f7700e11c645c366641519
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509935"
---
# <a name="getattachment-operation"></a>GetAttachment 操作

GetAttachment 操作用于检索邮件存储中项目Exchange附件。
  
## <a name="getattachment-request-example"></a>GetAttachment 请求示例

### <a name="description"></a>Description

GetAttachment 请求的以下示例显示如何获取附件。
  
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

[AttachmentShape](attachmentshape.md)元素允许您指定应返回的附件信息。 空 [的 AttachmentShape](attachmentshape.md) 元素有效，它将呈现附件，而项目附件没有 MIME 内容，具有文本正文类型，且没有任何其他属性。 
  
[AttachmentIds](attachmentids.md)集合允许您指定要返回的一个或多个附件标识符。 请注意，这些类型为 RequestAttachmentIdType，因此从 **CreateAttachment** 接收的任何 AttachmentId 都必须在将 **RootItemId** 和 **RootItemChangeKey** 属性传递到 **GetAttachment** 之前删除。
  
> [!NOTE]
> 附件标识符和更改键已缩短，以保持可读性。 
  
### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [GetAttachment](getattachment.md)
    
- [AttachmentShape](attachmentshape.md)
    
- [AttachmentIds](attachmentids.md)
    
- [AttachmentId (GetAttachment and DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a>GetAttachment 响应示例

### <a name="description"></a>Description

以下示例显示 GetAttachment 请求的成功响应。 本示例返回文件附件。
  
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

GetAttachment 的响应邮件将始终包含完整附件;即，将始终包含所有属性。 对于文件附件，这些属性是[Name (AttachmentType) 、ContentType、ContentId、ContentLocation](name-attachmenttype.md)和[Content](content.md)。 [](contenttype.md) [](contentid.md) [](contentlocation.md) 对于项目附件，这些属性是 [Name (AttachmentType](name-attachmenttype.md)) 、ContentType、ContentId、ContentLocation [](contentlocation.md)以及项目的所有属性，就像 [](contenttype.md)**AllProperties** 形状已在 GetItem 调用中使用的一样。 [](contentid.md) [AttachmentShape](attachmentshape.md)元素（如果存在）将允许使用者应用程序请求项目附件的其他扩展属性。 
  
### <a name="successful-response-elements"></a>成功的响应元素

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetAttachmentResponse](getattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetAttachmentResponseMessage](getattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [附件](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [AttachmentId (GetAttachment and DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md)
    
- [Name (AttachmentType)](name-attachmenttype.md)
    
- [Content](content.md)
    
## <a name="see-also"></a>另请参阅



[CreateAttachment 操作](createattachment-operation.md)
  
[DeleteAttachment 操作](deleteattachment-operation.md)

