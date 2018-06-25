---
title: FindConversation Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 2384908a-c203-45b6-98aa-efd6a4c23aac
description: FindConversation 操作枚举文件夹中的对话的列表。
ms.openlocfilehash: 7ef2167fef96a5e8441c543cac5b6800534c2eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754332"
---
# <a name="findconversation-operation"></a>FindConversation Operation

**FindConversation**操作枚举文件夹中的对话的列表。 
  
## <a name="findconversation-request-example"></a>FindConversation 请求示例

### <a name="description"></a>说明

**FindConversation**请求的下面的示例演示如何窗体的收件箱文件夹中找到的第一个对话的请求。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindConversation>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="1" Offset="0"/>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id ="inbox"/>
      </m:ParentFolderId>
    </m:FindConversation>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [RequestServerVersion](requestserverversion.md)
    
- [FindConversation](findconversation.md)
    
- [IndexedPageItemView](indexedpageitemview.md)
    
- [ParentFolderId](parentfolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
## <a name="successful-findconversation-response-example"></a>成功 FindConversation 响应示例

### <a name="description"></a>说明

下面的示例演示对**FindConversation**请求成功响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="91" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <FindConversationResponse ResponseClass="Success" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Conversations>
        <t:Conversation xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:ConversationId Id="AAQkADRlZDhjZDVlLzYtNDcyZi1i32hHpdc="/>
          <t:ConversationTopic>Have you heard about EWS?</t:ConversationTopic>
          <t:UniqueRecipients>
            <t:String>User1First User1Last</t:String>
          </t:UniqueRecipients>
          <t:GlobalUniqueRecipients>
            <t:String>User2First User2Last</t:String>
            <t:String>User1First User1Last</t:String>
          </t:GlobalUniqueRecipients>
          <t:UniqueSenders>
            <t:String>User2First User2Last</t:String>
          </t:UniqueSenders>
          <t:GlobalUniqueSenders>
            <t:String>User1First User1Last</t:String>
            <t:String>User2First User2Last</t:String>
          </t:GlobalUniqueSenders>
          <t:LastDeliveryTime>2010-02-09T02:20:49Z</t:LastDeliveryTime>
          <t:GlobalLastDeliveryTime>2010-02-09T02:21:01Z</t:GlobalLastDeliveryTime>
          <t:HasAttachments>false</t:HasAttachments>
          <t:GlobalHasAttachments>false</t:GlobalHasAttachments>
          <t:MessageCount>2</t:MessageCount>
          <t:GlobalMessageCount>5</t:GlobalMessageCount>
          <t:UnreadCount>0</t:UnreadCount>
          <t:Size>6474</t:Size>
          <t:GlobalSize>14497</t:GlobalSize>
          <t:ItemClasses>
            <t:ItemClass>IPM.Note</t:ItemClass>
          </t:ItemClasses>
          <t:GlobalItemClasses>
            <t:ItemClass>IPM.Note</t:ItemClass>
          </t:GlobalItemClasses>
          <t:Importance>Normal</t:Importance>
          <t:GlobalImportance>Normal</t:GlobalImportance>
          <t:ItemIds>
            <t:ItemId Id="AAMkADRlZDhjZDVlLTU3qaTQvcFtnmUZQY2FuFP93qPtAAAADXWyAAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAMkADRlZDhjZDVFtnmUZQY2vcFtnmUZQY2FuFP93qPtAAAADXWxAAA=" ChangeKey="CQAAAA=="/>
          </t:ItemIds>
          <t:GlobalItemIds>
            <t:ItemId Id="AAMkADRlZDhCQvcFtnmADU5PAACQvcFtnmUZQsdfFPPtAAAADad4AAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAqaTXQvcFtnmUZQAADU5NAACQvcFmUZQY2FuFP93qPtAAAADXWyAAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAMkFtnmUZQY2FuFP93qPtAAAADU5vcFtY2FuFP93qPtAAAADad3AAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAMkLTU3YzQvcFtnmUZQY2FuFP93qPtnmU2FuFP93qPtAAAADXWxAAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAMkADlLTU3YzYtNDAAAAAB1aGnYmUZQY2FPAmUZQY2FuqPtAAd2AAA=" ChangeKey="CQAAAA=="/>
          </t:GlobalItemIds>
        </t:Conversation>
      </Conversations>
    </FindConversationResponse>
  </s:Body>
</s:Envelope>
```

### <a name="comment"></a>Comment

在示例中的项目和对话标识符具有已缩短要保留可读性。
  
### <a name="successful-response-elements"></a>成功响应元素

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindConversationResponse](findconversationresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [对话 (ConversationType)](conversation-conversationtype.md)
    
- [ConversationId](conversationid.md)
    
- [ConversationTopic](conversationtopic.md)
    
- [UniqueRecipients](uniquerecipients.md)
    
- [字符串](string.md)
    
- [GlobalUniqueRecipients](globaluniquerecipients.md)
    
- [UniqueSenders](uniquesenders.md)
    
- [GlobalUniqueSenders](globaluniquesenders.md)
    
- [LastDeliveryTime](lastdeliverytime.md)
    
- [GlobalLastDeliveryTime](globallastdeliverytime.md)
    
- [HasAttachments](hasattachments.md)
    
- [GlobalHasAttachments](globalhasattachments.md)
    
- [MessageCount](messagecount.md)
    
- [GlobalMessageCount](globalmessagecount.md)
    
- [UnreadCount](unreadcount.md)
    
- [Size](size.md)
    
- [GlobalSize](globalsize.md)
    
- [ItemClasses (ArrayOfItemClassType)](itemclasses-arrayofitemclasstype.md)
    
- [ItemClass](itemclass.md)
    
- [GlobalItemClasses](globalitemclasses.md)
    
- [Importance](importance.md)
    
- [GlobalImportance](globalimportance.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
- [GlobalItemIds](globalitemids.md)
    
## <a name="findconversation-error-response-example"></a>FindConversation 错误响应示例

### <a name="description"></a>说明

下面的示例演示对**FindConversation**请求的架构验证错误导致出现错误响应。 
  
### <a name="code"></a>代码

```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body>
    <s:Fault>
      <faultcode xmlns:a="http://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
      <faultstring xml:lang="en-US">The request failed schema validation: The 'Id' attribute is invalid - The value 'inbox1' is invalid according to its datatype 'http://schemas.microsoft.com/exchange/services/2006/types:DistinguishedFolderIdNameType' - The Enumeration constraint failed.</faultstring>
      <detail>
        <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
        <t:MessageXml xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:LineNumber>14</t:LineNumber>
          <t:LinePosition>34</t:LinePosition>
          <t:Violation>The 'Id' attribute is invalid - The value 'inbox1' is invalid according to its datatype 'http://schemas.microsoft.com/exchange/services/2006/types:DistinguishedFolderIdNameType' - The Enumeration constraint failed.</t:Violation>
        </t:MessageXml>
      </detail>
    </s:Fault>
  </s:Body>
</s:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

错误响应中使用以下元素：
  
- faultcode
    
- faultstring
    
- 详细信息
    
- [ResponseCode](responsecode.md)
    
- 邮件
    
- [MessageXml](messagexml.md)
    
- LineNumber
    
- LinePosition
    
- 冲突
    
## <a name="see-also"></a>另请参阅



[ApplyConversationAction 操作](applyconversationaction-operation.md)


[Exchange 中的 EWS 操作](ews-operations-in-exchange.md)
  
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Conversations in EWS](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

