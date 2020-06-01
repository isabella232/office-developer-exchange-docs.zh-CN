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
description: RemoveDelegate 操作将从用户的邮箱中删除一个或多个代理。
ms.openlocfilehash: b2e342225e7e79c44dcd86b76b4b7d47b16b860b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466596"
---
# <a name="removedelegate-operation"></a><span data-ttu-id="468c4-103">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="468c4-103">RemoveDelegate operation</span></span>

<span data-ttu-id="468c4-104">**RemoveDelegate**操作将从用户的邮箱中删除一个或多个代理。</span><span class="sxs-lookup"><span data-stu-id="468c4-104">The **RemoveDelegate** operation removes one or more delegates from a user's mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="468c4-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="468c4-105">SOAP Headers</span></span>

<span data-ttu-id="468c4-106">**RemoveDelegate**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="468c4-106">The **RemoveDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="468c4-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="468c4-107">**Header**</span></span>|<span data-ttu-id="468c4-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="468c4-108">**Element**</span></span>|<span data-ttu-id="468c4-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="468c4-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="468c4-110">模拟</span><span class="sxs-lookup"><span data-stu-id="468c4-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="468c4-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="468c4-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="468c4-112">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="468c4-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="468c4-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="468c4-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="468c4-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="468c4-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="468c4-115">标识要用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="468c4-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="468c4-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="468c4-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="468c4-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="468c4-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="468c4-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="468c4-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="468c4-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="468c4-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="468c4-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="468c4-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="468c4-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="468c4-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="removedelegate-request-example"></a><span data-ttu-id="468c4-122">RemoveDelegate 请求示例</span><span class="sxs-lookup"><span data-stu-id="468c4-122">RemoveDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="468c4-123">说明</span><span class="sxs-lookup"><span data-stu-id="468c4-123">Description</span></span>

<span data-ttu-id="468c4-124">下面的代码示例演示如何从 user1's 邮箱中删除两个代理。</span><span class="sxs-lookup"><span data-stu-id="468c4-124">The following code example shows how to remove two delegates from user1's mailbox.</span></span> <span data-ttu-id="468c4-125">在此示例中，将使用代理的主 SMTP 地址删除一个委派，并使用代理的安全标识符（SID）删除另一个委派。</span><span class="sxs-lookup"><span data-stu-id="468c4-125">In this example, one delegate is removed by using the delegate's primary SMTP address, and the other one is removed by using the delegate's security identifier (SID).</span></span>
  
### <a name="code"></a><span data-ttu-id="468c4-126">代码</span><span class="sxs-lookup"><span data-stu-id="468c4-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <RemoveDelegate xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="468c4-127">备注</span><span class="sxs-lookup"><span data-stu-id="468c4-127">Comments</span></span>

<span data-ttu-id="468c4-128">**RemoveDelegate**操作不要求指定的代理用户拥有邮箱或存在于 Active Directory 目录服务中。</span><span class="sxs-lookup"><span data-stu-id="468c4-128">The **RemoveDelegate** operation does not require the specified delegate user to have a mailbox or to exist in the Active Directory directory service.</span></span> <span data-ttu-id="468c4-129">如果委派条目是孤立的， **RemoveDelegate**操作将会成功。</span><span class="sxs-lookup"><span data-stu-id="468c4-129">The **RemoveDelegate** operation will succeed if the delegate entry is orphaned.</span></span> 
  
## <a name="removedelegate-response-example"></a><span data-ttu-id="468c4-130">RemoveDelegate 响应示例</span><span class="sxs-lookup"><span data-stu-id="468c4-130">RemoveDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="468c4-131">说明</span><span class="sxs-lookup"><span data-stu-id="468c4-131">Description</span></span>

<span data-ttu-id="468c4-132">下面的**RemoveDelegate**响应示例显示了对**RemoveDelegate**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="468c4-132">The following example of a **RemoveDelegate** response shows a successful response to a **RemoveDelegate** request.</span></span> <span data-ttu-id="468c4-133">响应包含从邮箱中删除的每个代理的**DelegateUserResponseMessageType**元素。</span><span class="sxs-lookup"><span data-stu-id="468c4-133">The response contains a **DelegateUserResponseMessageType** element for each delegate that is removed from the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="468c4-134">代码</span><span class="sxs-lookup"><span data-stu-id="468c4-134">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:RemoveDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              ResponseClass="Success" 
                              xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="removedelegate-error-response-example"></a><span data-ttu-id="468c4-135">RemoveDelegate 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="468c4-135">RemoveDelegate Error response example</span></span>

### <a name="description"></a><span data-ttu-id="468c4-136">说明</span><span class="sxs-lookup"><span data-stu-id="468c4-136">Description</span></span>

<span data-ttu-id="468c4-137">下面的**RemoveDelegate**错误响应示例显示请求删除不存在的代理的结果。</span><span class="sxs-lookup"><span data-stu-id="468c4-137">The following example of a **RemoveDelegate** error response shows the results of a request to remove a delegate that does not exist.</span></span> 
  
### <a name="code"></a><span data-ttu-id="468c4-138">代码</span><span class="sxs-lookup"><span data-stu-id="468c4-138">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:RemoveDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                              ResponseClass="Success"
                              xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="see-also"></a><span data-ttu-id="468c4-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="468c4-139">See also</span></span>



- [<span data-ttu-id="468c4-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="468c4-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

