---
title: AddEntityFeedback 操作
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: AddEntityFeedback 操作将返回对应于服务器端问题的错误消息。
ms.openlocfilehash: a1027a0a1ee06cf3e83833b1d84c13d77b07c0b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458437"
---
# <a name="addentityfeedback-operation"></a>AddEntityFeedback 操作

**AddEntityFeedback**操作将返回对应于服务器端问题的错误消息。 
  
此操作取决于所记录的事件的类型。 最重要的事件之一是**EntityAdded**，它对应于所选的实体。 此操作是批处理操作，因此可用于在单个请求中记录批次条目。 
  
## <a name="findpeople-request-examples"></a>FindPeople 请求示例

**AddEntityFeedback**操作提供一种方法，使客户端可以记录与服务返回的实体进行交互的详细信息。 这可用作提高每个客户端的幕后相关性的信号。 例如，客户端可以使用此操作提供对**FindPeople**返回的人员实体的反馈。
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
            <m:EntityFeedbackEntries>
                  <t:EntityFeedbackEntry>
                        <t:ClientEventTimeUTC> 2015-07-05T22:16:18+00:00</t:ClientEventTimeUTC>
                        <t:ClientEventTimeLocal> 2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
                        <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
                        <t:ClientVersion>15.01.0101.01</t:ClientVersion>
                        <t:ClientId>Web</t:ClientId>
                        <t:TransactionId>123456789</t:TransactionId>
                        <t:EventType>EntityAdded</t:EventType>
                        <t:TargetEntityList>["a","b","c"]</t:TargetEntityList>
                        <t:SourceOfEntityAdded></t:SourceOfEntityAdded>
                        <t:JSONPropertyBag></t:JSONPropertyBag>
                  </t:EntityFeedbackEntry>
                  <t:EntityFeedbackEntry>
                  …
                  </t:EntityFeedbackEntry>
            </m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

### <a name="the-request-soap-body-contents"></a>请求 SOAP 正文内容

Soap 请求包含单个元素**EntityFeedbackEntries**。 这反过来又包含**EntityFeedbackEntry**对象的数组。 数组中的每个条目都可以包含以下元素。 
  
|**请求参数**|**必需**|**说明**|**类型**|
|:-----|:-----|:-----|:-----|
|**ClientEventTimeUtc** <br/> |是  <br/> |在客户端上事件发生时的 UTC 时间。  <br/> |日期/时间  <br/> |
|**ClientEventTimeLocal** <br/> |是  <br/> |在客户端上发生事件的本地时间。  <br/> |日期/时间  <br/> |
|**ClientId** <br/> |是  <br/> |客户端的类型（例如，Outlook、OWA 等）。  <br/> |ClientIDType 枚举  <br/> |
|**ClientSessionId** <br/> |是  <br/> |标识会话 ID 的 GUID。 在客户端上生成。  <br/> |GUID  <br/> |
|**ClientVersion** <br/> |是  <br/> |客户端的版本（例如，15.01.0101.000）。  <br/> |String  <br/> |
|**EntityAddSource** <br/> |否  <br/> |EntityAded 的源（例如，EntityRelevanceAPI、类型、粘贴）。  <br/> |EntityAddSource 枚举  <br/> |
|**EntrySequenceNumber** <br/> |是  <br/> |每个客户端会话递增整数。 用于检测数据丢失。  <br/> |Int  <br/> |
|**EventType** <br/> |是  <br/> |事件类型（例如，添加实体，删除实体）。  <br/> |String  <br/> |
|**JSONPropertyBag** <br/> |否  <br/> |与事件关联的其他属性（JSON blob 的键/值对）。  <br/> |JSON Blob  <br/> |
|**TargetEntityList** <br/> |否  <br/> |与事件关联的实体的列表。  <br/> |JSON 字符串  <br/> |
|**TransactionId** <br/> |否  <br/> |ID （GUID），用于关联查询日志中的 ID。  <br/> |String  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a>成功的 AddEntityFeedback 操作响应

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a>响应 SOAP 正文包含以下元素

#### <a name="errors"></a>错误 
  
API 可以记录一批反馈条目，我们记录了我们所能做的一切。 此字段表示未记录的错误条目数。
    
#### <a name="errordetails"></a>ErrorDetails
  
与以上分隔的错误相关的详细信息 `;` 。
    
### <a name="currently-supported-values"></a>当前支持的值

|**ClientIdType 枚举**|
|:-----|
|桌面  <br/> |
|Exchange  <br/> |
|IMAP4  <br/> |
|Lync  <br/> |
|MacMail  <br/> |
|MacOutlook  <br/> |
|移动设备  <br/> |
|其他  <br/> |
|Outlook  <br/> |
|Outlookservice.swift  <br/> |
|POP3  <br/> |
|平板电脑  <br/> |
|Web  <br/> |
   
|**EntityAddSource 枚举**|
|:-----|
|ActiveDirectory  <br/> |
|EntityRelevanceApi  <br/> |
|EntityRelevanceApiCache  <br/> |
|ExplicitTyping  <br/> |
|LocalCache  <br/> |
|LocalCacheAndEntityRelevanceAPI  <br/> |
|无  <br/> |
|其他  <br/> |
|Paste  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a>AddEntityFeedback 操作错误响应

有关对 EWS 通用的错误代码，请参阅[ResponseCode](responsecode.md)。
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a>AddEntityFeedback 与 FindPeople 结合使用的示例

#### <a name="findpeople-request"></a>FindPeople 请求
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
<soap:Body >
    <m:FindPeople>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:QueryString>user1</m:QueryString>
      <m:SearchPeopleSuggestionIndex>true</m:SearchPeopleSuggestionIndex>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>    
    
```

#### <a name="findpeople-response"></a>FindPeople 响应

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                    <PersonaId Id="AAUQAFjZ4UxX8SZCqSPFsmh0cSo=" />
                    <PersonaType>Person</PersonaType>
                    <CreationTime>2015-10-02T23:25:42</CreationTime>
                    <DisplayName>user2</DisplayName>
…
                  </Persona>
            </People>
            <TotalNumberOfPeopleInView>0</TotalNumberOfPeopleInView>
            <FirstMatchingRowIndex>0</FirstMatchingRowIndex>
            <FirstLoadedRowIndex>0</FirstLoadedRowIndex>
            <TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</TransactionId>
        </FindPeopleResponse>
    </s:Body>
</s:Envelope>

```

#### <a name="addentityfeedback-request"></a>AddEntityFeedback 请求

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
<m:EntityFeedbackEntries>
<t:EntityFeedbackEntry>
         <t:ClientEventTimeUtc>2015-07-05T22:16:18+00:00</t:ClientEventTimeUtc>
         <t:ClientEventTimeLocal>2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
         <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
         <t:ClientVersion>15.01.0101.01</t:ClientVersion>
         <t:ClientId>Web</t:ClientId>
         <t:TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</t:TransactionId>
         <t:EventType>EntityAdded</t:EventType>
         <t:TargetEntityList>["user1@ms7.com"]</t:TargetEntityList>
         <t:SourceOfEntityAdded>EntityRelevanceApi</t:SourceOfEntityAdded>
         <t:JSONPropertyBag></t:JSONPropertyBag>
</t:EntityFeedbackEntry>
</m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

> [!NOTE]
> 使用 FindPeople 响应事务 ID 作为 AddEntityFeedback 请求事务 ID。 
  
#### <a name="addentityfeedback-response"></a>AddEntityFeedback 响应

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


