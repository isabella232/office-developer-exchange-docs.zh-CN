---
title: UpdateDelegate 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: 03f618ac-ad1a-4772-9b81-c5bb0f12d6ab
description: UpdateDelegate 操作将更新对主体邮箱的委派权限。
ms.openlocfilehash: b7cf5325d925f8d6588115a8657a2077e940f9d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468556"
---
# <a name="updatedelegate-operation"></a><span data-ttu-id="415a9-103">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="415a9-103">UpdateDelegate operation</span></span>

<span data-ttu-id="415a9-104">**UpdateDelegate**操作将更新对主体邮箱的委派权限。</span><span class="sxs-lookup"><span data-stu-id="415a9-104">The **UpdateDelegate** operation updates delegate permissions on a principal's mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="415a9-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="415a9-105">SOAP Headers</span></span>

<span data-ttu-id="415a9-106">**UpdateDelegate**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="415a9-106">The **UpdateDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="415a9-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="415a9-107">**Header**</span></span>|<span data-ttu-id="415a9-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="415a9-108">**Element**</span></span>|<span data-ttu-id="415a9-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="415a9-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="415a9-110">模拟</span><span class="sxs-lookup"><span data-stu-id="415a9-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="415a9-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="415a9-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="415a9-112">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="415a9-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="415a9-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="415a9-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="415a9-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="415a9-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="415a9-115">标识要用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="415a9-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="415a9-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="415a9-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="415a9-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="415a9-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="415a9-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="415a9-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="415a9-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="415a9-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="415a9-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="415a9-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="415a9-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="415a9-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="updatedelegate-request-example"></a><span data-ttu-id="415a9-122">UpdateDelegate 请求示例</span><span class="sxs-lookup"><span data-stu-id="415a9-122">UpdateDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="415a9-123">Description</span><span class="sxs-lookup"><span data-stu-id="415a9-123">Description</span></span>

<span data-ttu-id="415a9-124">下面的**UpdateDelegate**请求示例演示如何在 user1's 帐户上更新委派权限。</span><span class="sxs-lookup"><span data-stu-id="415a9-124">The following example of an **UpdateDelegate** request shows you how to update delegate permissions on user1's account.</span></span> <span data-ttu-id="415a9-125">为操作2授予 "任务" 文件夹的 "无" 权限级别，并向其授予查看私人性质项目的权限。</span><span class="sxs-lookup"><span data-stu-id="415a9-125">User2 is granted the None permission level for the Tasks folder and is granted permission to view private items.</span></span> <span data-ttu-id="415a9-126">User3 将为 "日记" 文件夹授予 "审阅者" 权限。</span><span class="sxs-lookup"><span data-stu-id="415a9-126">User3 is granted Reviewer permissions for the Journal folder.</span></span> <span data-ttu-id="415a9-127">将会议请求发送给代理，并向 User1 发送有关请求的信息。</span><span class="sxs-lookup"><span data-stu-id="415a9-127">Meeting requests are sent to the delegates, and information about the request is sent to User1.</span></span> 
  
### <a name="code"></a><span data-ttu-id="415a9-128">代码</span><span class="sxs-lookup"><span data-stu-id="415a9-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <UpdateDelegate xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>user1@example.com</t:EmailAddress>
      </Mailbox>
      <DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user2@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ViewPrivateItems>true</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user3@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:JournalFolderPermissionLevel>Reviewer</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
        </t:DelegateUser>
      </DelegateUsers>
      <DeliverMeetingRequests>DelegatesAndSendInformationToMe</DeliverMeetingRequests>
    </UpdateDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="415a9-129">备注</span><span class="sxs-lookup"><span data-stu-id="415a9-129">Comments</span></span>

<span data-ttu-id="415a9-130">[UpdateDelegate](updatedelegate.md)请求不要求将更新应用到委派。</span><span class="sxs-lookup"><span data-stu-id="415a9-130">The [UpdateDelegate](updatedelegate.md) request does not require that updates be applied to delegates.</span></span> <span data-ttu-id="415a9-131">客户端只能更改**DeliverMeetingMessage**设置。</span><span class="sxs-lookup"><span data-stu-id="415a9-131">Clients can change only the **DeliverMeetingMessage** setting.</span></span> 
  
## <a name="updatedelegate-response-example"></a><span data-ttu-id="415a9-132">UpdateDelegate 响应示例</span><span class="sxs-lookup"><span data-stu-id="415a9-132">UpdateDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="415a9-133">Description</span><span class="sxs-lookup"><span data-stu-id="415a9-133">Description</span></span>

<span data-ttu-id="415a9-134">下面的示例演示对**UpdateDelegate**操作的成功响应。</span><span class="sxs-lookup"><span data-stu-id="415a9-134">The following example shows a successful response to an **UpdateDelegate** operation.</span></span> 
  
### <a name="code"></a><span data-ttu-id="415a9-135">代码</span><span class="sxs-lookup"><span data-stu-id="415a9-135">Code</span></span>

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
    <m:UpdateDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                              ResponseClass="Success"
                              xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1333220396-2200287332-232816053-1117</t:SID>
              <t:PrimarySmtpAddress>User2@example.com</t:PrimarySmtpAddress>
              <t:DisplayName>User2</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>true</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>true</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1333220396-2200287332-232816053-1118</t:SID>
              <t:PrimarySmtpAddress>User3@example.com</t:PrimarySmtpAddress>
              <t:DisplayName>User3</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>true</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:UpdateDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="updatedelegate-error-response-example"></a><span data-ttu-id="415a9-136">UpdateDelegate 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="415a9-136">UpdateDelegate Error response example</span></span>

### <a name="description"></a><span data-ttu-id="415a9-137">Description</span><span class="sxs-lookup"><span data-stu-id="415a9-137">Description</span></span>

<span data-ttu-id="415a9-138">下面的示例演示对**UpdateDelegate**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="415a9-138">The following example shows an error response to an **UpdateDelegate** request.</span></span> <span data-ttu-id="415a9-139">由于委派在主体的代理列表中不存在，因此生成错误。</span><span class="sxs-lookup"><span data-stu-id="415a9-139">The error was generated because the delegate does not exist in the principal's delegate list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="415a9-140">代码</span><span class="sxs-lookup"><span data-stu-id="415a9-140">Code</span></span>

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
    <m:UpdateDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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
      </m:UpdateDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="415a9-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="415a9-141">See also</span></span>



- [<span data-ttu-id="415a9-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="415a9-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

