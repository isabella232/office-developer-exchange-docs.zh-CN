---
title: CreateItem 操作（电子邮件）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1
description: CreateItem 操作用于创建电子邮件。
ms.openlocfilehash: 74784d72ed14fa139c616cd11740a62efd17b338
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536466"
---
# <a name="createitem-operation-email-message"></a>CreateItem 操作（电子邮件）

CreateItem 操作用于创建电子邮件。
  
## <a name="createitem-request-example"></a>CreateItem 请求示例

### <a name="description"></a>说明

CreateItem 请求的以下示例显示如何创建新电子邮件、发送邮件并将其副本保存在"草稿"文件夹中。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem MessageDisposition="SendAndSaveCopy" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </SavedItemFolderId>
      <Items>
        <t:Message>
          <t:ItemClass>IPM.Note</t:ItemClass>
          <t:Subject>Project Action</t:Subject>
          <t:Body BodyType="Text">Priority - Update specification</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sschmidt@example.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
          <t:IsRead>false</t:IsRead>
        </t:Message>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>请求元素

请求中会使用下列元素： 
  
- [CreateItem](createitem.md)
    
- [SavedItemFolderId](saveditemfolderid.md)
    
- [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [消息](message-ex15websvcsotherref.md)
    
- [ItemClass](itemclass.md)
    
- [主题](subject.md)
    
- [正文](body.md)
    
- [ToRecipients](torecipients.md)
    
- [邮箱](mailbox.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [IsRead](isread.md)
    
若要查找 CreateItem 操作的请求消息的其他选项，请浏览架构层次结构。 从 [CreateItem 元素](createitem.md) 开始。 
  
## <a name="successful-createitem-response"></a>成功的 CreateItem 响应

### <a name="description"></a>说明

以下示例显示了对 CreateItem 请求的成功响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>成功的响应元素

响应中包含以下元素： 
  
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items](items.md)
    
若要查找 CreateItem 操作的响应消息的其他选项，请浏览架构层次结构。 从 [CreateItemResponse 元素](createitemresponse.md) 开始。 
  
## <a name="error-createitem-response"></a>错误 CreateItem 响应

### <a name="description"></a>说明

以下示例显示对 CreateItem 请求的错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>The user account which was used to submit this request does not have the right to send mail on behalf of the specified sending account.</m:MessageText>
          <m:ResponseCode>ErrorSendAsDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

错误响应中会使用下列元素： 
  
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Items](items.md)
    
若要查找 CreateItem 操作的错误响应消息的其他选项，请浏览架构层次结构。 从 [CreateItemResponse 元素](createitemresponse.md) 开始。 
  
## <a name="see-also"></a>另请参阅



[CreateItem 操作](createitem-operation.md)

