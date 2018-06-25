---
title: RemoveDelegate 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegate
api_type:
- schema
ms.assetid: 1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a
description: RemoveDelegate 操作从用户的邮箱中删除一个或多个代理人。
ms.openlocfilehash: 6f3371d19bd8a7fd967d4959d85037ae6b51f6aa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827088"
---
# <a name="removedelegate-operation"></a><span data-ttu-id="2e5de-103">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="2e5de-103">RemoveDelegate operation</span></span>

<span data-ttu-id="2e5de-104">**RemoveDelegate**操作从用户的邮箱中删除一个或多个代理人。</span><span class="sxs-lookup"><span data-stu-id="2e5de-104">The **RemoveDelegate** operation removes one or more delegates from a user's mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="2e5de-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="2e5de-105">SOAP Headers</span></span>

<span data-ttu-id="2e5de-106">**RemoveDelegate**操作可以使用列出并在下表中所述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="2e5de-106">The **RemoveDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="2e5de-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="2e5de-107">**Header**</span></span>|<span data-ttu-id="2e5de-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="2e5de-108">**Element**</span></span>|<span data-ttu-id="2e5de-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e5de-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e5de-110">模拟</span><span class="sxs-lookup"><span data-stu-id="2e5de-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="2e5de-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="2e5de-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="2e5de-112">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="2e5de-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="2e5de-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="2e5de-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="2e5de-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="2e5de-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="2e5de-115">标识用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="2e5de-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="2e5de-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="2e5de-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="2e5de-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2e5de-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2e5de-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="2e5de-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="2e5de-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="2e5de-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="2e5de-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2e5de-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2e5de-121">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="2e5de-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="removedelegate-request-example"></a><span data-ttu-id="2e5de-122">RemoveDelegate 请求示例</span><span class="sxs-lookup"><span data-stu-id="2e5de-122">RemoveDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="2e5de-123">说明</span><span class="sxs-lookup"><span data-stu-id="2e5de-123">Description</span></span>

<span data-ttu-id="2e5de-124">下面的代码示例演示如何删除 user1 的邮箱的两个委派。</span><span class="sxs-lookup"><span data-stu-id="2e5de-124">The following code example shows how to remove two delegates from user1's mailbox.</span></span> <span data-ttu-id="2e5de-125">本示例中，使用代理人的主 SMTP 地址，删除了一名代理人和另一个已使用代理人的安全标识符 (SID)。</span><span class="sxs-lookup"><span data-stu-id="2e5de-125">In this example, one delegate is removed by using the delegate's primary SMTP address, and the other one is removed by using the delegate's security identifier (SID).</span></span>
  
### <a name="code"></a><span data-ttu-id="2e5de-126">代码</span><span class="sxs-lookup"><span data-stu-id="2e5de-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <RemoveDelegate xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>user1@example.com</t:EmailAddress>
      </Mailbox>
      <UserIds>
        <t:UserId>
          <t:PrimarySmtpAddress>user2@example.com</t:PrimarySmtpAddress>
        </t:UserId>
        <t:UserId>
          <t:SID>S-1-5-21-1333220396-2200287332-232816053-1118</t:SID>
        </t:UserId>
      </UserIds>
    </RemoveDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="2e5de-127">注释</span><span class="sxs-lookup"><span data-stu-id="2e5de-127">Comments</span></span>

<span data-ttu-id="2e5de-128">**RemoveDelegate**操作不需要让邮箱或 Active Directory 目录服务中存在的指定的代理用户。</span><span class="sxs-lookup"><span data-stu-id="2e5de-128">The **RemoveDelegate** operation does not require the specified delegate user to have a mailbox or to exist in the Active Directory directory service.</span></span> <span data-ttu-id="2e5de-129">如果孤立委托条目，将会成功**RemoveDelegate**操作。</span><span class="sxs-lookup"><span data-stu-id="2e5de-129">The **RemoveDelegate** operation will succeed if the delegate entry is orphaned.</span></span> 
  
## <a name="removedelegate-response-example"></a><span data-ttu-id="2e5de-130">RemoveDelegate 响应示例</span><span class="sxs-lookup"><span data-stu-id="2e5de-130">RemoveDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="2e5de-131">说明</span><span class="sxs-lookup"><span data-stu-id="2e5de-131">Description</span></span>

<span data-ttu-id="2e5de-132">**RemoveDelegate**响应的下面的示例演示对**RemoveDelegate**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="2e5de-132">The following example of a **RemoveDelegate** response shows a successful response to a **RemoveDelegate** request.</span></span> <span data-ttu-id="2e5de-133">则响应中包含的每个已从邮箱中删除的委托**DelegateUserResponseMessageType**元素。</span><span class="sxs-lookup"><span data-stu-id="2e5de-133">The response contains a **DelegateUserResponseMessageType** element for each delegate that is removed from the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2e5de-134">代码</span><span class="sxs-lookup"><span data-stu-id="2e5de-134">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" 
                         MinorVersion="1" 
                         MajorBuildNumber="206" 
                         MinorBuildNumber="0" 
                         Version="Exchange2007_SP1" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:RemoveDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              ResponseClass="Success" 
                              xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      </m:RemoveDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="removedelegate-error-response-example"></a><span data-ttu-id="2e5de-135">RemoveDelegate 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="2e5de-135">RemoveDelegate Error response example</span></span>

### <a name="description"></a><span data-ttu-id="2e5de-136">说明</span><span class="sxs-lookup"><span data-stu-id="2e5de-136">Description</span></span>

<span data-ttu-id="2e5de-137">**RemoveDelegate**错误响应下面的示例显示删除不存在一个代理的请求的结果。</span><span class="sxs-lookup"><span data-stu-id="2e5de-137">The following example of a **RemoveDelegate** error response shows the results of a request to remove a delegate that does not exist.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2e5de-138">代码</span><span class="sxs-lookup"><span data-stu-id="2e5de-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8"
                         MinorVersion="1"
                         MajorBuildNumber="206"
                         MinorBuildNumber="0"
                         Version="Exchange2007_SP1"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:RemoveDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                              ResponseClass="Success"
                              xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Error">
          <m:MessageText>The user is not a delegate for the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorNotDelegate</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:RemoveDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="2e5de-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2e5de-139">See also</span></span>



- [<span data-ttu-id="2e5de-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2e5de-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

