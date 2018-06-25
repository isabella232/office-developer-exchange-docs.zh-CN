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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753623"
---
# <a name="createattachment-operation"></a>CreateAttachment 操作

CreateAttachment 操作创建的项目或文件附件，并将其附加到指定的项。
  
## <a name="file-createattachment-request-example"></a>文件 CreateAttachment 请求示例

### <a name="description"></a>说明

CreateAttachment 请求的下面的示例演示如何创建的文件附件。
  
### <a name="code"></a>代码

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

### <a name="comment"></a>Comment

必须提供附件的名称。
  
> [!NOTE]
> 已缩短的父项标识符和更改密钥，以保留可读性。 
  
### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [CreateAttachment](createattachment.md)
    
- [ParentItemId](parentitemid.md)
    
- [附件](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [名称 (AttachmentType)](name-attachmenttype.md)
    
- [内容](content.md)
    
## <a name="successful-file-createattachment-response-example"></a>成功文件 CreateAttachment 响应示例

### <a name="description"></a>说明

下面的示例演示对 CreateAttachment 请求成功响应。
  
### <a name="code"></a>代码

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

### <a name="comment"></a>Comment

则响应中包含附加文件的标识符。 它还包含根项目的标识符和更改项。 已缩短的项标识符和更改密钥，以保留可读性。
  
### <a name="successful-response-elements"></a>成功响应元素

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateAttachmentResponse](createattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [附件](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a>项目 CreateAttachment 请求示例

### <a name="description"></a>说明

CreateAttachment 请求的下面的示例演示如何创建项目附件。
  
### <a name="code"></a>代码

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

### <a name="comment"></a>Comment

必须提供附件的名称。
  
 **注释**已缩短的父项标识符和更改密钥，以保留可读性。 
  
### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [CreateAttachment](createattachment.md)
    
- [ParentItemId](parentitemid.md)
    
- [附件](attachments-ex15websvcsotherref.md)
    
- [ItemAttachment](itemattachment.md)
    
- [名称 (AttachmentType)](name-attachmenttype.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [Subject](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a>成功的项 CreateAttachment 响应示例

### <a name="description"></a>说明

下面的示例演示对 CreateAttachment 请求成功响应。
  
### <a name="code"></a>代码

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

### <a name="comment"></a>Comment

则响应中包含新附件的标识符。 它还包含根项目的标识符和更改项。 根项目包含附件的项目。 已缩短的项标识符和更改密钥，以保留可读性。
  
### <a name="successful-response-elements"></a>成功响应元素

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateAttachmentResponse](createattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [附件](attachments-ex15websvcsotherref.md)
    
- [ItemAttachment](itemattachment.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a>CreateAttachment 错误响应示例

### <a name="description"></a>说明

下面的示例演示对 CreateAttachment 请求错误响应。 错误是由于，未指定附件的名称。
  
### <a name="code"></a>代码

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

### <a name="error-response-elements"></a>错误响应元素

错误响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateAttachmentResponse](createattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [MessageXml](messagexml.md)
    
- [ExceptionFieldURI](exceptionfielduri.md)
    
- [附件](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a>注解

如果多个附件附加到单个往返中的项目，最后一个响应消息中的 RootItemChangeKey 是项的表示具有附件的新更改键。
  
## <a name="see-also"></a>另请参阅



[DeleteAttachment 操作](deleteattachment-operation.md)
  
[GetAttachment 操作](getattachment-operation.md)

