---
title: GetInboxRules 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetInboxRules
api_type:
- schema
ms.assetid: b4b2701a-4a23-4acc-8c75-19f7955ad7ae
description: GetInboxRules 操作使用 Exchange Web 服务检索标识用户邮箱中的收件箱规则。
ms.openlocfilehash: 3e312ed08494b92c212595d081454b5f2ca6117e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546250"
---
# <a name="getinboxrules-operation"></a>GetInboxRules 操作

**GetInboxRules** 操作Exchange Web 服务检索标识用户邮箱中的收件箱规则。 
  
## <a name="getinboxrules-request-example"></a>GetInboxRules 请求示例

### <a name="description"></a>说明

以下示例显示客户端发送到服务器的请求 XML。 请求标识 [MailboxSmtpAddress](mailboxsmtpaddress.md) 元素中的用户。 将在响应中返回标识用户的所有收件箱规则。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetInboxRules>
      <m:MailboxSmtpAddress>User1@Contoso.com</m:MailboxSmtpAddress>
    </m:GetInboxRules>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>请求元素

请求包括以下可选元素：
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## <a name="successful-getinboxrules-response-example"></a>成功的 GetInboxRules 响应示例

### <a name="description"></a>说明

下面的 soap Simple Object Access Protocol (SOAP) 示例显示了 **对 GetInboxRules** 请求的成功响应。 本示例中，响应包含一个规则。 
  
> [!NOTE]
> 已缩短 [FolderId](folderid.md)元素 **的 Id** 和 **ChangeKey** 属性的值以保持可读性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
        MinorVersion="1" MajorBuildNumber="139"
        MinorBuildNumber="0"
        Version="Exchange2010_SP1"
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetInboxRulesResponse ResponseClass="Success"
        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <OutlookRuleBlobExists>true</OutlookRuleBlobExists>
      <InboxRules>
        <Rule xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <RuleId>dCsAAABjzvA=</RuleId>
          <DisplayName>MoveInterestingToJunk</DisplayName>
          <Priority>1</Priority>
          <IsEnabled>true</IsEnabled>
          <Conditions>
            <ContainsSubjectStrings>
              <String>Interesting</String>
            </ContainsSubjectStrings>
          </Conditions>
          <Actions>
            <MoveToFolder>
              <FolderId ChangeKey="AQAAAA==" Id="AAMkAGYzZjZm" />
            </MoveToFolder>
          </Actions>
        </Rule>
      </InboxRules>
    </GetInboxRulesResponse>
  </s:Body>
</s:Envelope>
```

### <a name="response-elements"></a>Response 元素

响应中包含以下元素：
  
- [GetInboxRulesResponse](getinboxrulesresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [OutlookRuleBlobExists](outlookruleblobexists.md)
    
- [InboxRules](inboxrules.md)
    
## <a name="see-also"></a>另请参阅



[UpdateInboxRules 操作](updateinboxrules-operation.md)

