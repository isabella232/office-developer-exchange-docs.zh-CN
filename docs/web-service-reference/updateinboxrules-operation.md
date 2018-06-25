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
description: UpdateInboxRules 操作将指定的操作的更新身份验证的用户的收件箱规则。 UpdateInboxRules 用于创建收件箱规则，来设置收件箱规则，或删除收件箱规则。
ms.openlocfilehash: 6e979421d619fed6625fe05db86c1f8c6a7418c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838391"
---
# <a name="updateinboxrules-operation"></a><span data-ttu-id="608a8-104">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="608a8-104">UpdateInboxRules operation</span></span>

<span data-ttu-id="608a8-105">UpdateInboxRules 操作将指定的操作的更新身份验证的用户的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-105">The UpdateInboxRules operation updates the authenticated user's Inbox rules by applying the specified operations.</span></span> <span data-ttu-id="608a8-106">**UpdateInboxRules**用于创建收件箱规则，来设置收件箱规则，或删除收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-106">**UpdateInboxRules** is used to create an Inbox rule, to set an Inbox rule, or to delete an Inbox rule.</span></span> 
  
<span data-ttu-id="608a8-107">当您使用**UpdateInboxRules**操作时，Exchange Web 服务中删除客户端发送规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-107">When you use the **UpdateInboxRules** operation, Exchange Web Services deletes client-side send rules.</span></span> <span data-ttu-id="608a8-108">客户端发送规则存储在客户端在规则文件夹关联的信息 （从故障） 消息和其他地方。</span><span class="sxs-lookup"><span data-stu-id="608a8-108">Client-side send rules are stored on the client in the rule Folder Associated Information (FAI) Message and nowhere else.</span></span> <span data-ttu-id="608a8-109">EWS 删除默认情况下，Outlook 将重新创建它的期望值基于此规则从故障消息。</span><span class="sxs-lookup"><span data-stu-id="608a8-109">EWS deletes this rule FAI message by default, based on the expectation that Outlook will recreate it.</span></span> <span data-ttu-id="608a8-110">但是，Outlook 无法重新创建还不存在作为扩展规则，规则并且客户端发送规则不存在作为扩展规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-110">However, Outlook can't recreate rules that don't also exist as an extended rule, and client-side send rules don't exist as extended rules.</span></span> <span data-ttu-id="608a8-111">因此，这些规则都将丢失。</span><span class="sxs-lookup"><span data-stu-id="608a8-111">As a result, these rules are lost.</span></span> <span data-ttu-id="608a8-112">我们建议您考虑此设计解决方案时。</span><span class="sxs-lookup"><span data-stu-id="608a8-112">We suggest you consider this when designing your solution.</span></span> 
  
## <a name="updateinboxrules-create-rule-request-example"></a><span data-ttu-id="608a8-113">UpdateInboxRules （创建规则） 请求示例</span><span class="sxs-lookup"><span data-stu-id="608a8-113">UpdateInboxRules (Create Rule) request example</span></span>

<span data-ttu-id="608a8-114">可以使用 Exchange Web 服务在 Exchange 存储中的用户的邮箱中创建收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-114">You can use Exchange Web Services to create an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="608a8-115">使用[UpdateInboxRules](updateinboxrules.md)元素与[CreateRuleOperation](createruleoperation.md)元素结合使用以创建规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-115">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="608a8-116">说明</span><span class="sxs-lookup"><span data-stu-id="608a8-116">Description</span></span>

<span data-ttu-id="608a8-117">客户端构造请求 XML 并将其发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="608a8-117">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="608a8-118">代码</span><span class="sxs-lookup"><span data-stu-id="608a8-118">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="608a8-119">注释</span><span class="sxs-lookup"><span data-stu-id="608a8-119">Comments</span></span>

<span data-ttu-id="608a8-120">此示例将生成一个规则，将电子邮件将邮件移动到垃圾邮件文件夹如果电子邮件主题包含一个字符串，等于"Interesting"。</span><span class="sxs-lookup"><span data-stu-id="608a8-120">This example builds a rule that will move an e-mail message to the Junk E-mail folder if the e-mail subject contains a string that equals "Interesting".</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="608a8-121">请求元素</span><span class="sxs-lookup"><span data-stu-id="608a8-121">Request elements</span></span>

<span data-ttu-id="608a8-122">**UpdateInboxRules**请求中包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="608a8-122">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="608a8-123">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="608a8-123">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="608a8-124">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="608a8-124">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="608a8-125">操作</span><span class="sxs-lookup"><span data-stu-id="608a8-125">Operations</span></span>](operations.md)
    
<span data-ttu-id="608a8-126">[操作](operations.md)元素包含[CreateRuleOperation](createruleoperation.md)元素以创建规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-126">The [Operations](operations.md) element contains the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
## <a name="updateinboxrules-create-rule-response-example"></a><span data-ttu-id="608a8-127">UpdateInboxRules （创建规则） 响应示例</span><span class="sxs-lookup"><span data-stu-id="608a8-127">UpdateInboxRules (Create Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="608a8-128">说明</span><span class="sxs-lookup"><span data-stu-id="608a8-128">Description</span></span>

<span data-ttu-id="608a8-129">下面的简单对象访问协议 (SOAP) 正文示例演示创建规则**UpdateInboxRules**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="608a8-129">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that creates a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="608a8-130">代码</span><span class="sxs-lookup"><span data-stu-id="608a8-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
         ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="608a8-131">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="608a8-131">Successful response elements</span></span>

<span data-ttu-id="608a8-132">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="608a8-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="608a8-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="608a8-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="608a8-134">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="608a8-134">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="608a8-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="608a8-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="608a8-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="608a8-136">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a><span data-ttu-id="608a8-137">UpdateInboxRules （设置规则） 请求示例</span><span class="sxs-lookup"><span data-stu-id="608a8-137">UpdateInboxRules (Set Rule) request example</span></span>

<span data-ttu-id="608a8-138">您可以使用 Exchange Web 服务修改 Exchange 存储中的用户的邮箱中的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-138">You can use Exchange Web Services to modify an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="608a8-139">使用与[SetRuleOperation](setruleoperation.md)元素结合使用[UpdateInboxRules](updateinboxrules.md)元素修改的规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-139">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="608a8-140">说明</span><span class="sxs-lookup"><span data-stu-id="608a8-140">Description</span></span>

<span data-ttu-id="608a8-141">客户端构造请求 XML 并将其发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="608a8-141">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="608a8-142">代码</span><span class="sxs-lookup"><span data-stu-id="608a8-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <Operations xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
          <SetRuleOperation xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="608a8-143">注释</span><span class="sxs-lookup"><span data-stu-id="608a8-143">Comments</span></span>

<span data-ttu-id="608a8-144">本示例显示名称更改为"（修改） 这是垃圾邮件"。</span><span class="sxs-lookup"><span data-stu-id="608a8-144">This example changes the display name to "(Modified) This is Junk".</span></span>
  
> [!NOTE]
> <span data-ttu-id="608a8-145">为便于阅读，具有已缩短的**Id**值和[文件夹 Id](folderid.md)元素的**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="608a8-145">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="608a8-146">请求元素</span><span class="sxs-lookup"><span data-stu-id="608a8-146">Request elements</span></span>

<span data-ttu-id="608a8-147">**UpdateInboxRules**请求中包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="608a8-147">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="608a8-148">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="608a8-148">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="608a8-149">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="608a8-149">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="608a8-150">操作</span><span class="sxs-lookup"><span data-stu-id="608a8-150">Operations</span></span>](operations.md)
    
<span data-ttu-id="608a8-151">[操作](operations.md)元素包含要修改的规则的[SetRuleOperation](setruleoperation.md)元素。</span><span class="sxs-lookup"><span data-stu-id="608a8-151">The [Operations](operations.md) element contains the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
## <a name="updateinboxrules-set-rule-response-example"></a><span data-ttu-id="608a8-152">UpdateInboxRules （设置规则） 响应示例</span><span class="sxs-lookup"><span data-stu-id="608a8-152">UpdateInboxRules (Set Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="608a8-153">说明</span><span class="sxs-lookup"><span data-stu-id="608a8-153">Description</span></span>

<span data-ttu-id="608a8-154">下面的简单对象访问协议 (SOAP) 正文示例演示修改规则**UpdateInboxRules**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="608a8-154">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that modifies a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="608a8-155">代码</span><span class="sxs-lookup"><span data-stu-id="608a8-155">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
          ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="608a8-156">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="608a8-156">Successful response elements</span></span>

<span data-ttu-id="608a8-157">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="608a8-157">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="608a8-158">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="608a8-158">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="608a8-159">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="608a8-159">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="608a8-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="608a8-160">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="608a8-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="608a8-161">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a><span data-ttu-id="608a8-162">UpdateInboxRules （删除规则） 请求示例</span><span class="sxs-lookup"><span data-stu-id="608a8-162">UpdateInboxRules (Delete Rule) request example</span></span>

<span data-ttu-id="608a8-163">Exchange Web 服务用于删除 Exchange 存储中的用户的邮箱中的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-163">You can use Exchange Web Services to delete an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="608a8-164">将[UpdateInboxRules](updateinboxrules.md)中[DeleteRuleOperation](deleteruleoperation.md)元素结合使用，以删除规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-164">Use the [UpdateInboxRules](updateinboxrules.md) in conjunction with the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="608a8-165">说明</span><span class="sxs-lookup"><span data-stu-id="608a8-165">Description</span></span>

<span data-ttu-id="608a8-166">客户端构造请求 XML 并将其发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="608a8-166">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="608a8-167">代码</span><span class="sxs-lookup"><span data-stu-id="608a8-167">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="608a8-168">注释</span><span class="sxs-lookup"><span data-stu-id="608a8-168">Comments</span></span>

<span data-ttu-id="608a8-169">本示例删除现有的标识的规则。</span><span class="sxs-lookup"><span data-stu-id="608a8-169">This example deletes the existing identified rule.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="608a8-170">请求元素</span><span class="sxs-lookup"><span data-stu-id="608a8-170">Request elements</span></span>

<span data-ttu-id="608a8-171">**UpdateInboxRules**请求中包括以下元素：</span><span class="sxs-lookup"><span data-stu-id="608a8-171">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="608a8-172">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="608a8-172">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="608a8-173">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="608a8-173">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="608a8-174">操作</span><span class="sxs-lookup"><span data-stu-id="608a8-174">Operations</span></span>](operations.md)
    
<span data-ttu-id="608a8-175">[操作](operations.md)元素包含要删除的规则的[DeleteRuleOperation](deleteruleoperation.md)元素。</span><span class="sxs-lookup"><span data-stu-id="608a8-175">The [Operations](operations.md) element contains the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
## <a name="updateinboxrules-delete-rule-response-example"></a><span data-ttu-id="608a8-176">UpdateInboxRules （删除规则） 响应示例</span><span class="sxs-lookup"><span data-stu-id="608a8-176">UpdateInboxRules (Delete Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="608a8-177">说明</span><span class="sxs-lookup"><span data-stu-id="608a8-177">Description</span></span>

<span data-ttu-id="608a8-178">下面的简单对象访问协议 (SOAP) 正文示例演示删除规则**UpdateInboxRules**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="608a8-178">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that deletes a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="608a8-179">代码</span><span class="sxs-lookup"><span data-stu-id="608a8-179">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="608a8-180">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="608a8-180">Successful response elements</span></span>

<span data-ttu-id="608a8-181">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="608a8-181">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="608a8-182">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="608a8-182">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="608a8-183">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="608a8-183">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="608a8-184">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="608a8-184">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="608a8-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="608a8-185">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="608a8-186">另请参阅</span><span class="sxs-lookup"><span data-stu-id="608a8-186">See also</span></span>



[<span data-ttu-id="608a8-187">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="608a8-187">GetInboxRules operation</span></span>](getinboxrules-operation.md)

