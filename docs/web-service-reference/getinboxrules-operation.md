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
description: GetInboxRules 操作使用 Exchange Web 服务检索已标识用户的邮箱中的收件箱规则。
ms.openlocfilehash: f4c4c03f55c9f32be4a067024f4387888edd5fe9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457933"
---
# <a name="getinboxrules-operation"></a><span data-ttu-id="af807-103">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="af807-103">GetInboxRules operation</span></span>

<span data-ttu-id="af807-104">**GetInboxRules**操作使用 Exchange Web 服务检索已标识用户的邮箱中的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="af807-104">The **GetInboxRules** operation uses Exchange Web Services to retrieve Inbox rules in the identified user's mailbox.</span></span> 
  
## <a name="getinboxrules-request-example"></a><span data-ttu-id="af807-105">GetInboxRules 请求示例</span><span class="sxs-lookup"><span data-stu-id="af807-105">GetInboxRules request example</span></span>

### <a name="description"></a><span data-ttu-id="af807-106">Description</span><span class="sxs-lookup"><span data-stu-id="af807-106">Description</span></span>

<span data-ttu-id="af807-107">下面的示例演示客户端发送到服务器的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="af807-107">The following example shows the request XML that the client sends to the server.</span></span> <span data-ttu-id="af807-108">请求在[MailboxSmtpAddress](mailboxsmtpaddress.md)元素中标识用户。</span><span class="sxs-lookup"><span data-stu-id="af807-108">The request identifies the user in the [MailboxSmtpAddress](mailboxsmtpaddress.md) element.</span></span> <span data-ttu-id="af807-109">标识的用户的所有收件箱规则将在响应中返回。</span><span class="sxs-lookup"><span data-stu-id="af807-109">All Inbox rules for the identified user are to be returned in the response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="af807-110">代码</span><span class="sxs-lookup"><span data-stu-id="af807-110">Code</span></span>

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

### <a name="request-elements"></a><span data-ttu-id="af807-111">Request 元素</span><span class="sxs-lookup"><span data-stu-id="af807-111">Request elements</span></span>

<span data-ttu-id="af807-112">该请求包含以下可选元素：</span><span class="sxs-lookup"><span data-stu-id="af807-112">The request includes the following optional element:</span></span>
  
- [<span data-ttu-id="af807-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="af807-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getinboxrules-response-example"></a><span data-ttu-id="af807-114">成功的 GetInboxRules 响应示例</span><span class="sxs-lookup"><span data-stu-id="af807-114">Successful GetInboxRules response example</span></span>

### <a name="description"></a><span data-ttu-id="af807-115">Description</span><span class="sxs-lookup"><span data-stu-id="af807-115">Description</span></span>

<span data-ttu-id="af807-116">下面的简单对象访问协议（SOAP）正文示例显示了对**GetInboxRules**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="af807-116">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetInboxRules** request.</span></span> <span data-ttu-id="af807-117">在此示例中，响应包含一个规则。</span><span class="sxs-lookup"><span data-stu-id="af807-117">In this example, the response includes one rule.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af807-118">[FolderId](folderid.md)元素的**Id**和**ChangeKey**属性的值已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="af807-118">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="af807-119">代码</span><span class="sxs-lookup"><span data-stu-id="af807-119">Code</span></span>

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

### <a name="response-elements"></a><span data-ttu-id="af807-120">Response 元素</span><span class="sxs-lookup"><span data-stu-id="af807-120">Response elements</span></span>

<span data-ttu-id="af807-121">响应中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="af807-121">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="af807-122">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="af807-122">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
    
- [<span data-ttu-id="af807-123">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="af807-123">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="af807-124">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="af807-124">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md)
    
- [<span data-ttu-id="af807-125">InboxRules</span><span class="sxs-lookup"><span data-stu-id="af807-125">InboxRules</span></span>](inboxrules.md)
    
## <a name="see-also"></a><span data-ttu-id="af807-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af807-126">See also</span></span>



[<span data-ttu-id="af807-127">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="af807-127">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)

