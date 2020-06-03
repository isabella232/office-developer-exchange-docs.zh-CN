---
title: GetMailTips 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMailTips
api_type:
- schema
ms.assetid: 025483ec-a9f3-4735-8a95-d26e30ea7974
description: GetMailTips 操作获取指定邮箱的邮件提示信息。
ms.openlocfilehash: 41a4bb99ee7ae4e416ec8a106968bb7869e60345
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458654"
---
# <a name="getmailtips-operation"></a><span data-ttu-id="f013c-103">GetMailTips 操作</span><span class="sxs-lookup"><span data-stu-id="f013c-103">GetMailTips operation</span></span>

<span data-ttu-id="f013c-104">**GetMailTips**操作获取指定邮箱的邮件提示信息。</span><span class="sxs-lookup"><span data-stu-id="f013c-104">The **GetMailTips** operation gets the mail tips information for the specified mailbox.</span></span> 
  
## <a name="getmailtips-request-example"></a><span data-ttu-id="f013c-105">GetMailTips 请求示例</span><span class="sxs-lookup"><span data-stu-id="f013c-105">GetMailTips request example</span></span>

### <a name="description"></a><span data-ttu-id="f013c-106">Description</span><span class="sxs-lookup"><span data-stu-id="f013c-106">Description</span></span>

<span data-ttu-id="f013c-107">客户端构造请求 XML 并将其发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="f013c-107">The client constructs the request XML and sends it to the server.</span></span> <span data-ttu-id="f013c-108">请求标识客户端的发送方式、要检索其邮件提示的邮箱以及请求的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="f013c-108">The request identifies who the client is sending as, the mailbox to retrieve the mail tips for, and what mail tips are requested.</span></span> <span data-ttu-id="f013c-109">在此示例中，客户端请求返回选定邮箱的所有邮件提示。</span><span class="sxs-lookup"><span data-stu-id="f013c-109">In this example, the client requests that all mail tips be returned for the selected mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="f013c-110">代码</span><span class="sxs-lookup"><span data-stu-id="f013c-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"> 
  <soap:Header> 
    <t:RequestServerVersion Version="Exchange2010" /> 
  </soap:Header> 
  <soap:Body> 
    <GetMailTips xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"> 
      <SendingAs> 
        <t:EmailAddress> user1@contoso.com </t:EmailAddress> 
        <t:RoutingType>SMTP</t:RoutingType> 
      </SendingAs> 
      <Recipients> 
        <t:Mailbox> 
          <t:EmailAddress> user2@contoso.com </t:EmailAddress> 
          <t:RoutingType>SMTP</t:RoutingType> 
        </t:Mailbox> 
      </Recipients> 
      <MailTipsRequested>All</MailTipsRequested> 
    </GetMailTips> 
  </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="f013c-111">Request 元素</span><span class="sxs-lookup"><span data-stu-id="f013c-111">Request elements</span></span>

<span data-ttu-id="f013c-112">请求中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f013c-112">The following elements are included in the request:</span></span>
  
- [<span data-ttu-id="f013c-113">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="f013c-113">GetMailTips</span></span>](getmailtips.md)
    
- [<span data-ttu-id="f013c-114">SendingAs</span><span class="sxs-lookup"><span data-stu-id="f013c-114">SendingAs</span></span>](sendingas.md)
    
- [<span data-ttu-id="f013c-115">收件人（ArrayOfRecipientsType）</span><span class="sxs-lookup"><span data-stu-id="f013c-115">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md)
    
- [<span data-ttu-id="f013c-116">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="f013c-116">MailTipsRequested</span></span>](mailtipsrequested.md)
    
## <a name="successful-getmailtips-response-example"></a><span data-ttu-id="f013c-117">成功的 GetMailTips 响应示例</span><span class="sxs-lookup"><span data-stu-id="f013c-117">Successful GetMailTips response example</span></span>

### <a name="description"></a><span data-ttu-id="f013c-118">Description</span><span class="sxs-lookup"><span data-stu-id="f013c-118">Description</span></span>

<span data-ttu-id="f013c-119">下面的简单对象访问协议（SOAP）正文示例显示了对**GetMailTips**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="f013c-119">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetMailTips** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="f013c-120">代码</span><span class="sxs-lookup"><span data-stu-id="f013c-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"> 
  <s:Header> 
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="0" MajorBuildNumber="536" MinorBuildNumber="0" Version="Exchange2010" 
xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:xsd="http://www.w3.org/2001/XMLSchema"/> 
  </s:Header> 
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <GetMailTipsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"> 
      <ResponseCode>NoError</ResponseCode> 
      <ResponseMessages> 
        <MailTipsResponseMessageType ResponseClass="Success"> 
        <ResponseCode>NoError</ResponseCode> 
        <m:MailTips xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"> 20 / 29 [MS-OXWMT] — v20100517 Mail Tips Web Service Extensions Copyright © 2010 Microsoft Corporation. Release: Monday, May 17, 2010 
          <t:RecipientAddress xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"> 
          <t:Name/> 
          <t:EmailAddress>user2@contoso.com</t:EmailAddress> 
          <t:RoutingType>SMTP</t:RoutingType> 
          </t:RecipientAddress> 
          <t:PendingMailTips xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/> 
          <t:OutOfOffice xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"> 
            <t:ReplyBody> 
              <t:Message/> 
            </t:ReplyBody> 
          </t:OutOfOffice> 
          <t:MailboxFull xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:MailboxFull> 
          <t:CustomMailTip xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">Hello World Mailtips</t:CustomMailTip> 
          <t:TotalMemberCount xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">1</t:TotalMemberCount> 
          <t:ExternalMemberCount xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">0</t:ExternalMemberCount> 
          <t:MaxMessageSize xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">10485760</t:MaxMessageSize> 
          <t:DeliveryRestricted xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:DeliveryRestricted> 
          <t:IsModerated xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:IsModerated> 
          <t:InvalidRecipient xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:InvalidRecipient> 
        </m:MailTips> 
        </MailTipsResponseMessageType> 
      </ResponseMessages> 
    </GetMailTipsResponse> 
  </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="f013c-121">Response 元素</span><span class="sxs-lookup"><span data-stu-id="f013c-121">Response elements</span></span>

<span data-ttu-id="f013c-122">响应中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f013c-122">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="f013c-123">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f013c-123">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f013c-124">邮件提示</span><span class="sxs-lookup"><span data-stu-id="f013c-124">MailTips</span></span>](mailtips.md)
    
## <a name="see-also"></a><span data-ttu-id="f013c-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f013c-125">See also</span></span>



[<span data-ttu-id="f013c-126">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="f013c-126">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="f013c-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f013c-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

