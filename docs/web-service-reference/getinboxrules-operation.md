---
title: GetInboxRules 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRules
api_type:
- schema
ms.assetid: b4b2701a-4a23-4acc-8c75-19f7955ad7ae
description: GetInboxRules 操作使用 Exchange Web 服务检索标识的用户的邮箱中的收件箱规则。
ms.openlocfilehash: f8a5068b1f189cc6fd5feef6dfec29204a0b8887
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754582"
---
# <a name="getinboxrules-operation"></a><span data-ttu-id="b6b45-103">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="b6b45-103">GetInboxRules operation</span></span>

<span data-ttu-id="b6b45-104">**GetInboxRules**操作使用 Exchange Web 服务检索标识的用户的邮箱中的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="b6b45-104">The **GetInboxRules** operation uses Exchange Web Services to retrieve Inbox rules in the identified user's mailbox.</span></span> 
  
## <a name="getinboxrules-request-example"></a><span data-ttu-id="b6b45-105">GetInboxRules 请求示例</span><span class="sxs-lookup"><span data-stu-id="b6b45-105">GetInboxRules request example</span></span>

### <a name="description"></a><span data-ttu-id="b6b45-106">说明</span><span class="sxs-lookup"><span data-stu-id="b6b45-106">Description</span></span>

<span data-ttu-id="b6b45-107">下面的示例演示请求客户端发送到服务器的 XML。</span><span class="sxs-lookup"><span data-stu-id="b6b45-107">The following example shows the request XML that the client sends to the server.</span></span> <span data-ttu-id="b6b45-108">请求标识[MailboxSmtpAddress](mailboxsmtpaddress.md)元素中的用户。</span><span class="sxs-lookup"><span data-stu-id="b6b45-108">The request identifies the user in the [MailboxSmtpAddress](mailboxsmtpaddress.md) element.</span></span> <span data-ttu-id="b6b45-109">标识用户的所有收件箱规则的响应中返回。</span><span class="sxs-lookup"><span data-stu-id="b6b45-109">All Inbox rules for the identified user are to be returned in the response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b6b45-110">代码</span><span class="sxs-lookup"><span data-stu-id="b6b45-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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

### <a name="request-elements"></a><span data-ttu-id="b6b45-111">请求元素</span><span class="sxs-lookup"><span data-stu-id="b6b45-111">Request elements</span></span>

<span data-ttu-id="b6b45-112">请求中包括以下可选元素：</span><span class="sxs-lookup"><span data-stu-id="b6b45-112">The request includes the following optional element:</span></span>
  
- [<span data-ttu-id="b6b45-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="b6b45-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getinboxrules-response-example"></a><span data-ttu-id="b6b45-114">成功 GetInboxRules 响应示例</span><span class="sxs-lookup"><span data-stu-id="b6b45-114">Successful GetInboxRules response example</span></span>

### <a name="description"></a><span data-ttu-id="b6b45-115">说明</span><span class="sxs-lookup"><span data-stu-id="b6b45-115">Description</span></span>

<span data-ttu-id="b6b45-116">下面的简单对象访问协议 (SOAP) 正文示例演示对**GetInboxRules**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="b6b45-116">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetInboxRules** request.</span></span> <span data-ttu-id="b6b45-117">本示例中，该响应包括一个规则。</span><span class="sxs-lookup"><span data-stu-id="b6b45-117">In this example, the response includes one rule.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b6b45-118">已缩短的**Id**值和[文件夹 Id](folderid.md)元素的**更改密钥**属性，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="b6b45-118">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b6b45-119">代码</span><span class="sxs-lookup"><span data-stu-id="b6b45-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
        MinorVersion="1" MajorBuildNumber="139"
        MinorBuildNumber="0"
        Version="Exchange2010_SP1"
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetInboxRulesResponse ResponseClass="Success"
        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <OutlookRuleBlobExists>true</OutlookRuleBlobExists>
      <InboxRules>
        <Rule xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="response-elements"></a><span data-ttu-id="b6b45-120">响应元素</span><span class="sxs-lookup"><span data-stu-id="b6b45-120">Response elements</span></span>

<span data-ttu-id="b6b45-121">在响应中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="b6b45-121">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="b6b45-122">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="b6b45-122">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
    
- [<span data-ttu-id="b6b45-123">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b6b45-123">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b6b45-124">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="b6b45-124">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md)
    
- [<span data-ttu-id="b6b45-125">InboxRules</span><span class="sxs-lookup"><span data-stu-id="b6b45-125">InboxRules</span></span>](inboxrules.md)
    
## <a name="see-also"></a><span data-ttu-id="b6b45-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b6b45-126">See also</span></span>



[<span data-ttu-id="b6b45-127">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="b6b45-127">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)

