---
title: UpdateItem 操作 （联系人）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 298fdd71-a83d-4407-9728-4f0a8e2d857c
description: UpdateItem 操作用于更新 Exchange 存储中的联系人项属性。
ms.openlocfilehash: f2a501ce8e69068cd30b58011adf4defc68ce365
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838396"
---
# <a name="updateitem-operation-contact"></a>UpdateItem 操作 （联系人）

UpdateItem 操作用于更新 Exchange 存储中的联系人项属性。
  
## <a name="updateitem-contact-request-example"></a>UpdateItem （联系人） 请求示例

### <a name="description"></a>说明

下面的代码示例演示如何更新联系人的电子邮件地址。
  
### <a name="code"></a>代码

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                ConflictResolution="AlwaysOverwrite">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAA=" ChangeKey="EQAAABYi" />
          <t:Updates>
            <t:SetItemField>
              <t:IndexedFieldURI FieldURI="contacts:EmailAddress" FieldIndex="EmailAddress1"/>
              <t:Contact>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">changedemail@example.com</t:Entry>
                </t:EmailAddresses>
              </t:Contact>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

已缩短的项标识符，若要保留可读性。
  
### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [更新 （项）](updates-item.md)
    
- [SetItemField](setitemfield.md)
    
- [IndexedFieldURI](indexedfielduri.md)
    
- [Contact](contact.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [条目 （电子邮件地址）](entry-emailaddress.md)
    
## <a name="successful-updateitem-contact-response"></a>成功 UpdateItem （联系人） 响应

### <a name="description"></a>说明

下面的代码示例显示成功的 UpdateItem 响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAtAE=" ChangeKey="EQAAABYx" />
            </t:Contact>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

已缩短的项标识符，若要保留可读性。
  
### <a name="successful-response-elements"></a>成功响应元素

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateItemResponse](updateitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateItemResponseMessage](updateitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [项目 (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Contact](contact.md)
    
- [ItemId](itemid.md)
    
## <a name="invalid-updateitem-contact-request-example"></a>无效的 UpdateItem （联系人） 请求示例

### <a name="description"></a>说明

下面的代码示例显示了无效的请求。
  
### <a name="code"></a>代码

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                ConflictResolution="AlwaysOverwrite">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEF=" ChangeKey="EQAAABYi" />
          <t:Updates>
            <t:SetItemField>
              <t:IndexedFieldURI FieldURI="contacts:EmailAddress" FieldIndex="EmailAddress4"/>
              <t:Contact>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress4">changedemail2@example.com</t:Entry>
                </t:EmailAddresses>
              </t:Contact>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

已缩短的项标识符，若要保留可读性。
  
## <a name="updateitem-contact-error-response"></a>UpdateItem （联系人） 错误响应

### <a name="description"></a>说明

下面的代码示例演示 UpdateItem （联系人） 请求错误响应。
  
### <a name="code"></a>代码

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <soap:faultcode>Client</soap:faultcode>
      <soap:faultstring>The request failed schema validation.</soap:faultstring>
      <detail>
        <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The 'Key' attribute is invalid - The value 'EmailAddress4' is invalid according to its data type 'http://schemas.microsoft.com/exchange/services/2006/types:EmailAddressKeyType' - The Enumeration constraint failed.</e:Message>
        <e:Line xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">17</e:Line>
        <e:Position xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">19</e:Position>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

消息或类型架构中未定义一些错误响应导致通过架构验证错误 SOAP 正文中使用的元素。 **详细信息**元素包含有关错误的信息。 [ResponseCode](responsecode.md)元素包含错误代码。 如果有的话，[消息](message-ex15websvcsotherref.md)元素包含错误的说明。 **行**元素描述发生架构验证错误的行号。 **位置**元素描述从 XML 文档的最左侧的字符的位置。 
  
## <a name="see-also"></a>另请参阅



[UpdateItem 操作](updateitem-operation.md)

