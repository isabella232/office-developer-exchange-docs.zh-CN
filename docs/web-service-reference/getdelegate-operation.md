---
title: GetDelegate 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 849b2c9e-4685-4bd1-9adb-aba0fcc52650
description: GetDelegate 操作中检索指定邮箱的代理设置。
ms.openlocfilehash: bd1a0add54ee5fd1c23b4ba09a921a9061afa394
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754510"
---
# <a name="getdelegate-operation"></a><span data-ttu-id="cadb6-103">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="cadb6-103">GetDelegate operation</span></span>

<span data-ttu-id="cadb6-104">**GetDelegate**操作中检索指定邮箱的代理设置。</span><span class="sxs-lookup"><span data-stu-id="cadb6-104">The **GetDelegate** operation retrieves the delegate settings for a specified mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="cadb6-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="cadb6-105">SOAP Headers</span></span>

<span data-ttu-id="cadb6-106">**GetDelegate**操作可以使用列出并在下表中所述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="cadb6-106">The **GetDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="cadb6-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="cadb6-107">**Header**</span></span>|<span data-ttu-id="cadb6-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="cadb6-108">**Element**</span></span>|<span data-ttu-id="cadb6-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="cadb6-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cadb6-110">模拟</span><span class="sxs-lookup"><span data-stu-id="cadb6-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="cadb6-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="cadb6-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="cadb6-112">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="cadb6-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="cadb6-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="cadb6-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="cadb6-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="cadb6-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="cadb6-115">标识用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="cadb6-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="cadb6-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="cadb6-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="cadb6-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="cadb6-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="cadb6-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="cadb6-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="cadb6-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="cadb6-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="cadb6-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cadb6-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="cadb6-121">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="cadb6-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getdelegate-request-example"></a><span data-ttu-id="cadb6-122">GetDelegate 请求示例</span><span class="sxs-lookup"><span data-stu-id="cadb6-122">GetDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="cadb6-123">说明</span><span class="sxs-lookup"><span data-stu-id="cadb6-123">Description</span></span>

<span data-ttu-id="cadb6-124">下面的代码示例演示如何检索所有 user3 的邮箱设置的代理人的代理设置。</span><span class="sxs-lookup"><span data-stu-id="cadb6-124">The following code example shows how to retrieve the delegate settings for all the delegates that are set on user3's mailbox.</span></span> <span data-ttu-id="cadb6-125">在响应中返回的每个用户的所有权限。</span><span class="sxs-lookup"><span data-stu-id="cadb6-125">All the permissions for each user are returned in the response.</span></span>
  
### <a name="code"></a><span data-ttu-id="cadb6-126">代码</span><span class="sxs-lookup"><span data-stu-id="cadb6-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <GetDelegate xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                 IncludePermissions="true">
      <Mailbox>
        <t:EmailAddress>user3@example.com</t:EmailAddress>
      </Mailbox>
    </GetDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="cadb6-127">注释</span><span class="sxs-lookup"><span data-stu-id="cadb6-127">Comments</span></span>

<span data-ttu-id="cadb6-128">[UserId](userid.md)元素用于指定各个用户，而不是返回所有用户邮箱中具有代理访问权限。</span><span class="sxs-lookup"><span data-stu-id="cadb6-128">You can use the [UserId](userid.md) element to specify individual users instead of returning all users who have delegate access permissions on the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cadb6-129">Exchange Web Services (EWS) 不支持管理组代理人。</span><span class="sxs-lookup"><span data-stu-id="cadb6-129">Exchange Web Services (EWS) does not support managing group delegates.</span></span> <span data-ttu-id="cadb6-130">如果主体已安全组代理人调用**GetDelegate**操作，EWS 将返回错误。</span><span class="sxs-lookup"><span data-stu-id="cadb6-130">EWS will return an error if the **GetDelegate** operation is called for a principal that has a security group delegate.</span></span> 
  
## <a name="getdelegate-response-example"></a><span data-ttu-id="cadb6-131">GetDelegate 响应示例</span><span class="sxs-lookup"><span data-stu-id="cadb6-131">GetDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="cadb6-132">说明</span><span class="sxs-lookup"><span data-stu-id="cadb6-132">Description</span></span>

<span data-ttu-id="cadb6-133">**GetDelegate**响应的下面的示例演示对**GetDelegate**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="cadb6-133">The following example of a **GetDelegate** response shows a successful response to a **GetDelegate** request.</span></span> <span data-ttu-id="cadb6-134">则响应中包含有关委派访问权限的信息，代理人可以查看专用项目，无论代理接收副本的会议邮件，并向其会议是否已传送请求。</span><span class="sxs-lookup"><span data-stu-id="cadb6-134">The response contains information about the delegate access permissions, whether the delegate can view private items, whether the delegate receives copies of meeting messages, and to whom meeting requests were delivered.</span></span> 
  
### <a name="code"></a><span data-ttu-id="cadb6-135">代码</span><span class="sxs-lookup"><span data-stu-id="cadb6-135">Code</span></span>

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
    <m:GetDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                           ResponseClass="Success" 
                           xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
              <t:UserId>
                <t:SID>S-1-5-21-1333220396-2200287332-232816053-1116</t:SID>
                <t:PrimarySmtpAddress>User1@example.com</t:PrimarySmtpAddress>
                <t:DisplayName>User1</t:DisplayName>
              </t:UserId>
              <t:DelegatePermissions>
                <t:CalendarFolderPermissionLevel>Author</t:CalendarFolderPermissionLevel>
                <t:ContactsFolderPermissionLevel>Reviewer</t:ContactsFolderPermissionLevel>
              </t:DelegatePermissions>
              <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
            </m:DelegateUser>
          </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      <m:DeliverMeetingRequests>DelegatesAndMe</m:DeliverMeetingRequests>
      </m:GetDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="cadb6-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cadb6-136">See also</span></span>



- [<span data-ttu-id="cadb6-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cadb6-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

