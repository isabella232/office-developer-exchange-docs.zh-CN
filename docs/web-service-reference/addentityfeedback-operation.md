---
title: AddEntityFeedback 操作
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: AddEntityFeedback 操作返回对应于服务器端问题的错误信息。
ms.openlocfilehash: b695806f543827d78aea139ffcbd7e4af58b9fef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753111"
---
# <a name="addentityfeedback-operation"></a>AddEntityFeedback 操作

**AddEntityFeedback**操作返回对应于服务器端问题的错误信息。 
  
此操作依赖于被记录的事件的类型。 最重要的事件之一是**EntityAdded**，此名称对应于所选实体。 此操作是批次，因此它可以用于在单个请求日志条目的批次。 
  
## <a name="findpeople-request-examples"></a>FindPeople 请求示例

**AddEntityFeedback**操作提供了一种客户端日志服务返回的实体的交互的详细信息的方法。 这可以用作信号以提高相关性后台每个客户端。 例如，客户端可以使用此操作从**FindPeople**返回的人员实体上提供的反馈。
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Soap 请求包含单个元素**EntityFeedbackEntries**。 反过来，其中包含**EntityFeedbackEntry**对象的数组。 该数组中的每个条目可以包含以下元素。 
  
|**请求参数**|**必需**|**说明**|**类型**|
|:-----|:-----|:-----|:-----|
|**ClientEventTimeUtc** <br/> |是  <br/> |UTC 时间在事件发生在客户端上。  <br/> |日期时间  <br/> |
|**ClientEventTimeLocal** <br/> |是  <br/> |事件发生在客户端的本地时间。  <br/> |日期时间  <br/> |
|**ClientId** <br/> |是  <br/> |客户端 （例如，Outlook、 OWA 等） 的类型。  <br/> |ClientIDType 枚举  <br/> |
|**ClientSessionId** <br/> |是  <br/> |GUID 标识会话 id。 生成客户端上。  <br/> |GUID  <br/> |
|**ClientVersion** <br/> |是  <br/> |版本的客户端 (例如，15.01.0101.000)。  <br/> |String  <br/> |
|**EntityAddSource** <br/> |否  <br/> |EntityAded （例如，EntityRelevanceAPI，类型，粘贴） 源。  <br/> |EntityAddSource 枚举  <br/> |
|**EntrySequenceNumber** <br/> |是  <br/> |每个客户端会话增量整数。 用于检测数据丢失。  <br/> |Int  <br/> |
|**EventType** <br/> |是  <br/> |（例如，添加实体，实体删除） 的事件的类型。  <br/> |String  <br/> |
|**JSONPropertyBag** <br/> |否  <br/> |(的键/值对的 JSON blob) 的事件相关联的其他属性。  <br/> |JSON Blob  <br/> |
|**TargetEntityList** <br/> |否  <br/> |与事件关联的实体的列表。  <br/> |JSON 字符串  <br/> |
|**TransactionId** <br/> |否  <br/> |ID (GUID) 关联查询日志中的 ID。  <br/> |String  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a>成功 AddEntityFeedback 操作响应

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a>响应 SOAP 正文中包含以下元素

#### <a name="errors"></a>错误 
  
API 可以记录的批次的反馈条目，我们记录所有我们可以。 此字段表示没有记录的错误条目数。
    
#### <a name="errordetails"></a>ErrorDetails
  
与上面的错误的详细信息所分隔的`;`。
    
### <a name="currently-supported-values"></a>当前受支持的值

|**ClientIdType 枚举**|
|:-----|
|台式机  <br/> |
|Exchange  <br/> |
|IMAP4  <br/> |
|Lync  <br/> |
|MacMail  <br/> |
|MacOutlook  <br/> |
|移动  <br/> |
|其他  <br/> |
|Outlook  <br/> |
|OutlookService  <br/> |
|POP3  <br/> |
|平板电脑  <br/> |
|Web  <br/> |
   
|**EntityAddSource 枚举**|
|:-----|
|与 active Directory  <br/> |
|EntityRelevanceApi  <br/> |
|EntityRelevanceApiCache  <br/> |
|ExplicitTyping  <br/> |
|LocalCache  <br/> |
|LocalCacheAndEntityRelevanceAPI  <br/> |
|无  <br/> |
|其他  <br/> |
|粘贴  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a>AddEntityFeedback 操作错误响应

是通用的 EWS 的错误代码，请参阅[ResponseCode](responsecode.md)。
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a>与 FindPeople 结合使用的 AddEntityFeedback 示例

#### <a name="findpeople-request"></a>FindPeople 请求
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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
> 使用 FindPeople 响应事务 ID 作为 AddEntityFeedback 请求事务的 id。 
  
#### <a name="addentityfeedback-response"></a>AddEntityFeedback 响应

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


