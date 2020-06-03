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
description: GetDelegate 操作检索指定邮箱的代理设置。
ms.openlocfilehash: 400bf5d1cafcbb789aaa749c62c7a908622d4ddb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461063"
---
# <a name="getdelegate-operation"></a><span data-ttu-id="7a7e0-103">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="7a7e0-103">GetDelegate operation</span></span>

<span data-ttu-id="7a7e0-104">**GetDelegate**操作检索指定邮箱的代理设置。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-104">The **GetDelegate** operation retrieves the delegate settings for a specified mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="7a7e0-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="7a7e0-105">SOAP Headers</span></span>

<span data-ttu-id="7a7e0-106">**GetDelegate**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-106">The **GetDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="7a7e0-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="7a7e0-107">**Header**</span></span>|<span data-ttu-id="7a7e0-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a7e0-108">**Element**</span></span>|<span data-ttu-id="7a7e0-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a7e0-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7a7e0-110">模拟</span><span class="sxs-lookup"><span data-stu-id="7a7e0-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="7a7e0-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="7a7e0-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="7a7e0-112">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="7a7e0-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="7a7e0-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="7a7e0-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="7a7e0-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="7a7e0-115">标识要用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="7a7e0-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="7a7e0-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="7a7e0-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="7a7e0-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="7a7e0-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="7a7e0-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="7a7e0-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="7a7e0-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7a7e0-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="7a7e0-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getdelegate-request-example"></a><span data-ttu-id="7a7e0-122">GetDelegate 请求示例</span><span class="sxs-lookup"><span data-stu-id="7a7e0-122">GetDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="7a7e0-123">Description</span><span class="sxs-lookup"><span data-stu-id="7a7e0-123">Description</span></span>

<span data-ttu-id="7a7e0-124">下面的代码示例演示如何检索 user3's 邮箱上设置的所有代理的代理设置。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-124">The following code example shows how to retrieve the delegate settings for all the delegates that are set on user3's mailbox.</span></span> <span data-ttu-id="7a7e0-125">在响应中返回每个用户的所有权限。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-125">All the permissions for each user are returned in the response.</span></span>
  
### <a name="code"></a><span data-ttu-id="7a7e0-126">代码</span><span class="sxs-lookup"><span data-stu-id="7a7e0-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <GetDelegate xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                 IncludePermissions="true">
      <Mailbox>
        <t:EmailAddress>user3@example.com</t:EmailAddress>
      </Mailbox>
    </GetDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="7a7e0-127">备注</span><span class="sxs-lookup"><span data-stu-id="7a7e0-127">Comments</span></span>

<span data-ttu-id="7a7e0-128">您可以使用[UserId](userid.md)元素来指定单个用户，而不是返回对邮箱具有代理访问权限的所有用户。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-128">You can use the [UserId](userid.md) element to specify individual users instead of returning all users who have delegate access permissions on the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7a7e0-129">Exchange Web 服务（EWS）不支持管理组委派。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-129">Exchange Web Services (EWS) does not support managing group delegates.</span></span> <span data-ttu-id="7a7e0-130">如果为具有安全组委派的主体调用**GetDelegate**操作，EWS 将返回错误。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-130">EWS will return an error if the **GetDelegate** operation is called for a principal that has a security group delegate.</span></span> 
  
## <a name="getdelegate-response-example"></a><span data-ttu-id="7a7e0-131">GetDelegate 响应示例</span><span class="sxs-lookup"><span data-stu-id="7a7e0-131">GetDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="7a7e0-132">Description</span><span class="sxs-lookup"><span data-stu-id="7a7e0-132">Description</span></span>

<span data-ttu-id="7a7e0-133">下面的**GetDelegate**响应示例显示了对**GetDelegate**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-133">The following example of a **GetDelegate** response shows a successful response to a **GetDelegate** request.</span></span> <span data-ttu-id="7a7e0-134">响应包含有关代理访问权限的信息，代理是否可以查看私人项目、代理是否接收会议邮件的副本以及会议请求的送达者。</span><span class="sxs-lookup"><span data-stu-id="7a7e0-134">The response contains information about the delegate access permissions, whether the delegate can view private items, whether the delegate receives copies of meeting messages, and to whom meeting requests were delivered.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7a7e0-135">代码</span><span class="sxs-lookup"><span data-stu-id="7a7e0-135">Code</span></span>

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
    <m:GetDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                           ResponseClass="Success" 
                           xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="see-also"></a><span data-ttu-id="7a7e0-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a7e0-136">See also</span></span>



- [<span data-ttu-id="7a7e0-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7a7e0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

