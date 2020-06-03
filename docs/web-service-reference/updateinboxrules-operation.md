---
title: UpdateInboxRules 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: f982a237-471e-45c5-a2b5-468cfc53150b
description: UpdateInboxRules 操作通过应用指定的操作来更新已通过身份验证的用户的收件箱规则。 UpdateInboxRules 用于创建收件箱规则、设置收件箱规则或删除收件箱规则。
ms.openlocfilehash: a6ced4be25c6fe4649ad649ba01194791548bf67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530998"
---
# <a name="updateinboxrules-operation"></a>UpdateInboxRules 操作

UpdateInboxRules 操作通过应用指定的操作来更新已通过身份验证的用户的收件箱规则。 **UpdateInboxRules**用于创建收件箱规则、设置收件箱规则或删除收件箱规则。 
  
当您使用**UpdateInboxRules**操作时，Exchange Web 服务将删除客户端发送规则。 客户端发送规则存储在客户端上的规则文件夹相关信息（FAI）消息和其他地方。 EWS 默认情况下，根据 Outlook 将重新创建的预期，EWS 删除此规则 FAI 邮件。 但是，Outlook 无法重新创建也不作为扩展规则存在的规则，并且客户端发送规则不会作为扩展规则存在。 因此，这些规则将丢失。 我们建议您在设计解决方案时考虑这一点。 
  
## <a name="updateinboxrules-create-rule-request-example"></a>UpdateInboxRules （Create Rule）请求示例

您可以使用 Exchange Web 服务在 Exchange 存储区中的用户邮箱中创建收件箱规则。 将[UpdateInboxRules](updateinboxrules.md)元素与[CreateRuleOperation](createruleoperation.md)元素结合使用，以创建规则。 
  
### <a name="description"></a>Description

客户端构造请求 XML 并将其发送到服务器。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <m:Operations>
          <t:CreateRuleOperation>
            <t:Rule>
              <t:DisplayName>MoveInterestingToJunk</t:DisplayName>
              <t:Priority>1</t:Priority>
              <t:IsEnabled>true</t:IsEnabled>
              <t:Conditions>
                <t:ContainsSubjectStrings>
                  <t:String>Interesting</t:String>
                </t:ContainsSubjectStrings>
              </t:Conditions>
              <t:Exceptions />
              <t:Actions>
                <t:MoveToFolder>
                  <t:DistinguishedFolderId Id="junkemail" />
                </t:MoveToFolder>
              </t:Actions>
            </t:Rule>
          </t:CreateRuleOperation>
        </m:Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a>备注

如果电子邮件主题包含一个等于 "有趣" 的字符串，则本示例将生成一个规则，以便将电子邮件移动到 "垃圾邮件" 文件夹。
  
### <a name="request-elements"></a>Request 元素

**UpdateInboxRules**请求包括以下元素： 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
[Operations](operations.md)元素包含用于创建规则的[CreateRuleOperation](createruleoperation.md)元素。 
  
## <a name="updateinboxrules-create-rule-response-example"></a>UpdateInboxRules （创建规则）响应示例

### <a name="description"></a>Description

下面的简单对象访问协议（SOAP）正文示例显示了对创建规则的**UpdateInboxRules**请求的成功响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
         ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>成功的响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a>UpdateInboxRules （Set Rule）请求示例

您可以使用 Exchange Web 服务修改 Exchange 存储中用户邮箱中的收件箱规则。 将[UpdateInboxRules](updateinboxrules.md)元素与[SetRuleOperation](setruleoperation.md)元素结合使用，以修改规则。 
  
### <a name="description"></a>Description

客户端构造请求 XML 并将其发送到服务器。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <Operations xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
          <SetRuleOperation xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
            <Rule>
              <RuleId>Nh8AAAAwW/w=</RuleId>
              <DisplayName>(Modified) This is Junk</DisplayName>
              <Priority>1</Priority>
              <IsEnabled>true</IsEnabled>
              <Conditions>
                <ContainsSubjectStrings>
                  <String>Interesting</String>
                </ContainsSubjectStrings>
              </Conditions>
              <Actions>
                <MoveToFolder>
                  <FolderId Id="AAMkADQ1YTE1" ChangeKey="AQAAAA==" />
                </MoveToFolder>
              </Actions>
            </Rule>
          </SetRuleOperation>
        </Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a>备注

本示例将显示名称更改为 "（已修改）这是垃圾邮件"。
  
> [!NOTE]
> 为了提高可读性， [FolderId](folderid.md)元素的**Id**和**ChangeKey**属性的值已缩短。 
  
### <a name="request-elements"></a>Request 元素

**UpdateInboxRules**请求包括以下元素： 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
[Operations](operations.md)元素包含用于修改规则的[SetRuleOperation](setruleoperation.md)元素。 
  
## <a name="updateinboxrules-set-rule-response-example"></a>UpdateInboxRules （Set Rule） response 示例

### <a name="description"></a>Description

下面的简单对象访问协议（SOAP）正文示例显示了对修改规则的**UpdateInboxRules**请求的成功响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
          ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>成功的响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a>UpdateInboxRules （删除规则）请求示例

您可以使用 Exchange Web 服务在 Exchange 存储区中的用户邮箱中删除收件箱规则。 将[UpdateInboxRules](updateinboxrules.md)与[DeleteRuleOperation](deleteruleoperation.md)元素联合使用以删除规则。 
  
### <a name="description"></a>Description

客户端构造请求 XML 并将其发送到服务器。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <m:Operations>
          <t:DeleteRuleOperation>
            <t:RuleId>Nh8AAAAwW/U=</t:RuleId>
          </t:DeleteRuleOperation>
        </m:Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a>备注

本示例删除现有的已识别规则。
  
### <a name="request-elements"></a>Request 元素

**UpdateInboxRules**请求包括以下元素： 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
[Operations](operations.md)元素包含用于删除规则的[DeleteRuleOperation](deleteruleoperation.md)元素。 
  
## <a name="updateinboxrules-delete-rule-response-example"></a>UpdateInboxRules （删除规则）响应示例

### <a name="description"></a>Description

下面的简单对象访问协议（SOAP）正文示例显示了对删除规则的**UpdateInboxRules**请求的成功响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>成功的响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="see-also"></a>另请参阅



[GetInboxRules 操作](getinboxrules-operation.md)

