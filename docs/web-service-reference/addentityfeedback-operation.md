---
title: AddEntityFeedback 操作
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: AddEntityFeedback 操作返回与服务器端问题对应的错误信息。
ms.openlocfilehash: d4322bcc075c8c68b1f3d5f2ae22badea02be452
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546824"
---
# <a name="addentityfeedback-operation"></a>AddEntityFeedback 操作

**AddEntityFeedback** 操作返回与服务器端问题对应的错误信息。 
  
此操作依赖于要记录的事件的类型。 最重要的事件之一是 **EntityAdded**，对应于要选择的实体。 此操作是批处理，因此可用于记录单个请求中的条目批处理。 
  
## <a name="findpeople-request-examples"></a>FindPeople 请求示例

**AddEntityFeedback** 操作为客户端提供了一种记录与服务返回的实体交互的详细信息的方法。 这可用作一个信号，以改进每个客户端的后台相关性。 例如，客户端可以使用此操作提供有关从 FindPeople 返回的人 **实体的反馈**。
  
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

soap 请求包含单个元素 **EntityFeedbackEntries**。 这反过来包含 **EntityFeedbackEntry 对象的** 数组。 数组的每个条目都可以包含以下元素。 
  
|**请求参数**|**必需**|**说明**|**类型**|
|:-----|:-----|:-----|:-----|
|**ClientEventTimeUtc** <br/> |是  <br/> |事件发生在客户端上的 UTC 时间。  <br/> |日期时间  <br/> |
|**ClientEventTimeLocal** <br/> |是  <br/> |在客户端上发生事件的本地时间。  <br/> |日期时间  <br/> |
|**ClientId** <br/> |是  <br/> |客户端类型 (，例如Outlook、OWA 等) 。  <br/> |ClientIDType 枚举  <br/> |
|**ClientSessionId** <br/> |是  <br/> |GUID 标识会话 ID。 在客户端上生成。  <br/> |GUID  <br/> |
|**ClientVersion** <br/> |是  <br/> |客户端客户端版本 (例如 15.01.0101.000) 。  <br/> |String  <br/> |
|**EntityAddSource** <br/> |否  <br/> |EntityAded 的 (，例如 EntityRelevanceAPI、types、pasted) 。  <br/> |EntityAddSource 枚举  <br/> |
|**EntrySequenceNumber** <br/> |是  <br/> |每个客户端会话的增量整数。 用于检测数据丢失。  <br/> |Int  <br/> |
|**EventType** <br/> |是  <br/> |事件类型 (，例如 Entity Added、Entity Removed) 。  <br/> |String  <br/> |
|**JSONPropertyBag** <br/> |否  <br/> |与事件关联的其他属性 (键/值对的 JSON blob) 。  <br/> |JSON Blob  <br/> |
|**TargetEntityList** <br/> |否  <br/> |与事件关联的实体列表。  <br/> |JSON 字符串  <br/> |
|**TransactionId** <br/> |否  <br/> |ID (GUID) 将查询日志中的 ID 关联在一起。  <br/> |String  <br/> |
   
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
  
API 可以记录一批反馈条目，我们会记录所有能够记录的反馈条目。 此字段表示未记录的错误条目数。
    
#### <a name="errordetails"></a>ErrorDetails
  
与上述错误相关的详细信息由 分隔 `;` 。
    
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
|OutlookService  <br/> |
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

有关 EWS 通用的错误代码，请参阅 [ResponseCode](responsecode.md)。
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a>AddEntityFeedback 与 FindPeople 联合的示例

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


