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
# <a name="updateinboxrules-operation"></a><span data-ttu-id="5b0e6-104">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="5b0e6-104">UpdateInboxRules operation</span></span>

<span data-ttu-id="5b0e6-105">UpdateInboxRules 操作通过应用指定的操作来更新已通过身份验证的用户的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-105">The UpdateInboxRules operation updates the authenticated user's Inbox rules by applying the specified operations.</span></span> <span data-ttu-id="5b0e6-106">**UpdateInboxRules**用于创建收件箱规则、设置收件箱规则或删除收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-106">**UpdateInboxRules** is used to create an Inbox rule, to set an Inbox rule, or to delete an Inbox rule.</span></span> 
  
<span data-ttu-id="5b0e6-107">当您使用**UpdateInboxRules**操作时，Exchange Web 服务将删除客户端发送规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-107">When you use the **UpdateInboxRules** operation, Exchange Web Services deletes client-side send rules.</span></span> <span data-ttu-id="5b0e6-108">客户端发送规则存储在客户端上的规则文件夹相关信息（FAI）消息和其他地方。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-108">Client-side send rules are stored on the client in the rule Folder Associated Information (FAI) Message and nowhere else.</span></span> <span data-ttu-id="5b0e6-109">EWS 默认情况下，根据 Outlook 将重新创建的预期，EWS 删除此规则 FAI 邮件。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-109">EWS deletes this rule FAI message by default, based on the expectation that Outlook will recreate it.</span></span> <span data-ttu-id="5b0e6-110">但是，Outlook 无法重新创建也不作为扩展规则存在的规则，并且客户端发送规则不会作为扩展规则存在。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-110">However, Outlook can't recreate rules that don't also exist as an extended rule, and client-side send rules don't exist as extended rules.</span></span> <span data-ttu-id="5b0e6-111">因此，这些规则将丢失。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-111">As a result, these rules are lost.</span></span> <span data-ttu-id="5b0e6-112">我们建议您在设计解决方案时考虑这一点。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-112">We suggest you consider this when designing your solution.</span></span> 
  
## <a name="updateinboxrules-create-rule-request-example"></a><span data-ttu-id="5b0e6-113">UpdateInboxRules （Create Rule）请求示例</span><span class="sxs-lookup"><span data-stu-id="5b0e6-113">UpdateInboxRules (Create Rule) request example</span></span>

<span data-ttu-id="5b0e6-114">您可以使用 Exchange Web 服务在 Exchange 存储区中的用户邮箱中创建收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-114">You can use Exchange Web Services to create an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="5b0e6-115">将[UpdateInboxRules](updateinboxrules.md)元素与[CreateRuleOperation](createruleoperation.md)元素结合使用，以创建规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-115">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="5b0e6-116">Description</span><span class="sxs-lookup"><span data-stu-id="5b0e6-116">Description</span></span>

<span data-ttu-id="5b0e6-117">客户端构造请求 XML 并将其发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-117">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="5b0e6-118">代码</span><span class="sxs-lookup"><span data-stu-id="5b0e6-118">Code</span></span>

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

### <a name="comments"></a><span data-ttu-id="5b0e6-119">备注</span><span class="sxs-lookup"><span data-stu-id="5b0e6-119">Comments</span></span>

<span data-ttu-id="5b0e6-120">如果电子邮件主题包含一个等于 "有趣" 的字符串，则本示例将生成一个规则，以便将电子邮件移动到 "垃圾邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-120">This example builds a rule that will move an e-mail message to the Junk E-mail folder if the e-mail subject contains a string that equals "Interesting".</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="5b0e6-121">Request 元素</span><span class="sxs-lookup"><span data-stu-id="5b0e6-121">Request elements</span></span>

<span data-ttu-id="5b0e6-122">**UpdateInboxRules**请求包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="5b0e6-122">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="5b0e6-123">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="5b0e6-123">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="5b0e6-124">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="5b0e6-124">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="5b0e6-125">Operations</span><span class="sxs-lookup"><span data-stu-id="5b0e6-125">Operations</span></span>](operations.md)
    
<span data-ttu-id="5b0e6-126">[Operations](operations.md)元素包含用于创建规则的[CreateRuleOperation](createruleoperation.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-126">The [Operations](operations.md) element contains the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
## <a name="updateinboxrules-create-rule-response-example"></a><span data-ttu-id="5b0e6-127">UpdateInboxRules （创建规则）响应示例</span><span class="sxs-lookup"><span data-stu-id="5b0e6-127">UpdateInboxRules (Create Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="5b0e6-128">Description</span><span class="sxs-lookup"><span data-stu-id="5b0e6-128">Description</span></span>

<span data-ttu-id="5b0e6-129">下面的简单对象访问协议（SOAP）正文示例显示了对创建规则的**UpdateInboxRules**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-129">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that creates a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5b0e6-130">代码</span><span class="sxs-lookup"><span data-stu-id="5b0e6-130">Code</span></span>

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

### <a name="successful-response-elements"></a><span data-ttu-id="5b0e6-131">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="5b0e6-131">Successful response elements</span></span>

<span data-ttu-id="5b0e6-132">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5b0e6-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5b0e6-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5b0e6-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5b0e6-134">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="5b0e6-134">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="5b0e6-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5b0e6-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5b0e6-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5b0e6-136">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a><span data-ttu-id="5b0e6-137">UpdateInboxRules （Set Rule）请求示例</span><span class="sxs-lookup"><span data-stu-id="5b0e6-137">UpdateInboxRules (Set Rule) request example</span></span>

<span data-ttu-id="5b0e6-138">您可以使用 Exchange Web 服务修改 Exchange 存储中用户邮箱中的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-138">You can use Exchange Web Services to modify an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="5b0e6-139">将[UpdateInboxRules](updateinboxrules.md)元素与[SetRuleOperation](setruleoperation.md)元素结合使用，以修改规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-139">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="5b0e6-140">Description</span><span class="sxs-lookup"><span data-stu-id="5b0e6-140">Description</span></span>

<span data-ttu-id="5b0e6-141">客户端构造请求 XML 并将其发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-141">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="5b0e6-142">代码</span><span class="sxs-lookup"><span data-stu-id="5b0e6-142">Code</span></span>

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

### <a name="comments"></a><span data-ttu-id="5b0e6-143">备注</span><span class="sxs-lookup"><span data-stu-id="5b0e6-143">Comments</span></span>

<span data-ttu-id="5b0e6-144">本示例将显示名称更改为 "（已修改）这是垃圾邮件"。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-144">This example changes the display name to "(Modified) This is Junk".</span></span>
  
> [!NOTE]
> <span data-ttu-id="5b0e6-145">为了提高可读性， [FolderId](folderid.md)元素的**Id**和**ChangeKey**属性的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-145">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="5b0e6-146">Request 元素</span><span class="sxs-lookup"><span data-stu-id="5b0e6-146">Request elements</span></span>

<span data-ttu-id="5b0e6-147">**UpdateInboxRules**请求包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="5b0e6-147">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="5b0e6-148">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="5b0e6-148">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="5b0e6-149">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="5b0e6-149">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="5b0e6-150">Operations</span><span class="sxs-lookup"><span data-stu-id="5b0e6-150">Operations</span></span>](operations.md)
    
<span data-ttu-id="5b0e6-151">[Operations](operations.md)元素包含用于修改规则的[SetRuleOperation](setruleoperation.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-151">The [Operations](operations.md) element contains the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
## <a name="updateinboxrules-set-rule-response-example"></a><span data-ttu-id="5b0e6-152">UpdateInboxRules （Set Rule） response 示例</span><span class="sxs-lookup"><span data-stu-id="5b0e6-152">UpdateInboxRules (Set Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="5b0e6-153">Description</span><span class="sxs-lookup"><span data-stu-id="5b0e6-153">Description</span></span>

<span data-ttu-id="5b0e6-154">下面的简单对象访问协议（SOAP）正文示例显示了对修改规则的**UpdateInboxRules**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-154">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that modifies a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5b0e6-155">代码</span><span class="sxs-lookup"><span data-stu-id="5b0e6-155">Code</span></span>

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

### <a name="successful-response-elements"></a><span data-ttu-id="5b0e6-156">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="5b0e6-156">Successful response elements</span></span>

<span data-ttu-id="5b0e6-157">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5b0e6-157">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5b0e6-158">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5b0e6-158">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5b0e6-159">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="5b0e6-159">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="5b0e6-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5b0e6-160">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5b0e6-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5b0e6-161">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a><span data-ttu-id="5b0e6-162">UpdateInboxRules （删除规则）请求示例</span><span class="sxs-lookup"><span data-stu-id="5b0e6-162">UpdateInboxRules (Delete Rule) request example</span></span>

<span data-ttu-id="5b0e6-163">您可以使用 Exchange Web 服务在 Exchange 存储区中的用户邮箱中删除收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-163">You can use Exchange Web Services to delete an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="5b0e6-164">将[UpdateInboxRules](updateinboxrules.md)与[DeleteRuleOperation](deleteruleoperation.md)元素联合使用以删除规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-164">Use the [UpdateInboxRules](updateinboxrules.md) in conjunction with the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="5b0e6-165">Description</span><span class="sxs-lookup"><span data-stu-id="5b0e6-165">Description</span></span>

<span data-ttu-id="5b0e6-166">客户端构造请求 XML 并将其发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-166">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="5b0e6-167">代码</span><span class="sxs-lookup"><span data-stu-id="5b0e6-167">Code</span></span>

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

### <a name="comments"></a><span data-ttu-id="5b0e6-168">备注</span><span class="sxs-lookup"><span data-stu-id="5b0e6-168">Comments</span></span>

<span data-ttu-id="5b0e6-169">本示例删除现有的已识别规则。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-169">This example deletes the existing identified rule.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="5b0e6-170">Request 元素</span><span class="sxs-lookup"><span data-stu-id="5b0e6-170">Request elements</span></span>

<span data-ttu-id="5b0e6-171">**UpdateInboxRules**请求包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="5b0e6-171">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="5b0e6-172">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="5b0e6-172">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="5b0e6-173">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="5b0e6-173">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="5b0e6-174">Operations</span><span class="sxs-lookup"><span data-stu-id="5b0e6-174">Operations</span></span>](operations.md)
    
<span data-ttu-id="5b0e6-175">[Operations](operations.md)元素包含用于删除规则的[DeleteRuleOperation](deleteruleoperation.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-175">The [Operations](operations.md) element contains the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
## <a name="updateinboxrules-delete-rule-response-example"></a><span data-ttu-id="5b0e6-176">UpdateInboxRules （删除规则）响应示例</span><span class="sxs-lookup"><span data-stu-id="5b0e6-176">UpdateInboxRules (Delete Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="5b0e6-177">Description</span><span class="sxs-lookup"><span data-stu-id="5b0e6-177">Description</span></span>

<span data-ttu-id="5b0e6-178">下面的简单对象访问协议（SOAP）正文示例显示了对删除规则的**UpdateInboxRules**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="5b0e6-178">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that deletes a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5b0e6-179">代码</span><span class="sxs-lookup"><span data-stu-id="5b0e6-179">Code</span></span>

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

### <a name="successful-response-elements"></a><span data-ttu-id="5b0e6-180">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="5b0e6-180">Successful response elements</span></span>

<span data-ttu-id="5b0e6-181">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5b0e6-181">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5b0e6-182">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5b0e6-182">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5b0e6-183">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="5b0e6-183">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="5b0e6-184">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5b0e6-184">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5b0e6-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5b0e6-185">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="5b0e6-186">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5b0e6-186">See also</span></span>



[<span data-ttu-id="5b0e6-187">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="5b0e6-187">GetInboxRules operation</span></span>](getinboxrules-operation.md)

