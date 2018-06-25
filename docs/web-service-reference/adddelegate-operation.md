---
title: AddDelegate 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegate
api_type:
- schema
ms.assetid: 012d8cc5-648c-4ba0-a155-15c422b1e994
description: AddDelegate 操作添加一个或多个代理人到主体的邮箱和设置特定的访问权限。
ms.openlocfilehash: 28d4ded2625efc3d6eade44f5fafc06c2ffca7ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753101"
---
# <a name="adddelegate-operation"></a><span data-ttu-id="b4e9b-103">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="b4e9b-103">AddDelegate operation</span></span>

<span data-ttu-id="b4e9b-104">**AddDelegate**操作添加一个或多个代理人到主体的邮箱和设置特定的访问权限。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-104">The **AddDelegate** operation adds one or more delegates to a principal's mailbox and sets specific access permissions.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="b4e9b-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="b4e9b-105">SOAP headers</span></span>

<span data-ttu-id="b4e9b-106">**AddDelegate**操作可以使用列出并在下表中所述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-106">The **AddDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="b4e9b-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="b4e9b-107">**Header**</span></span>|<span data-ttu-id="b4e9b-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="b4e9b-108">**Element**</span></span>|<span data-ttu-id="b4e9b-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="b4e9b-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4e9b-110">模拟</span><span class="sxs-lookup"><span data-stu-id="b4e9b-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="b4e9b-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="b4e9b-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="b4e9b-112">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="b4e9b-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="b4e9b-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="b4e9b-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="b4e9b-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="b4e9b-115">标识用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="b4e9b-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="b4e9b-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="b4e9b-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="b4e9b-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="b4e9b-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="b4e9b-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b4e9b-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="b4e9b-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b4e9b-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="b4e9b-121">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="adddelegate-request-example"></a><span data-ttu-id="b4e9b-122">AddDelegate 请求示例</span><span class="sxs-lookup"><span data-stu-id="b4e9b-122">AddDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="b4e9b-123">说明</span><span class="sxs-lookup"><span data-stu-id="b4e9b-123">Description</span></span>

<span data-ttu-id="b4e9b-124">**AddDelegate**请求的下面的示例演示尝试向 user1 委派权限授予文件夹所拥有的 user2。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-124">The following example of an **AddDelegate** request shows an attempt to give user1 delegate permissions on folders that are owned by user2.</span></span> <span data-ttu-id="b4e9b-125">User1 将授予 user2 的日历文件夹和审阅者级别为 user2 的联系人文件夹的权限的作者级权限。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-125">User1 is given Author-level permissions to user2's Calendar folder and Reviewer-level permissions to user2's Contacts folder.</span></span> <span data-ttu-id="b4e9b-126">User1 将不会收到会议邮件的副本，并且将无法查看 user2 的邮箱中的专用的项目。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-126">User1 will not receive copies of meeting messages and will be unable to view private items in user2's mailbox.</span></span> <span data-ttu-id="b4e9b-127">会议请求将发送到 user1 和 user2。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-127">Meeting requests will be sent to both user1 and user2.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b4e9b-128">代码</span><span class="sxs-lookup"><span data-stu-id="b4e9b-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <AddDelegate>
      <Mailbox>
        <t:EmailAddress>user2@example.com</t:EmailAddress>
      </Mailbox>
      <DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user1@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>Author</t:CalendarFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>Reviewer</t:ContactsFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
      </DelegateUsers>
      <DeliverMeetingRequests>DelegatesAndMe</DeliverMeetingRequests>
    </AddDelegate>
  </soap:Body>
</soap:Envelope>
```

## <a name="adddelegate-response-example"></a><span data-ttu-id="b4e9b-129">AddDelegate 响应示例</span><span class="sxs-lookup"><span data-stu-id="b4e9b-129">AddDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="b4e9b-130">说明</span><span class="sxs-lookup"><span data-stu-id="b4e9b-130">Description</span></span>

<span data-ttu-id="b4e9b-131">**AddDelegate**响应的下面的示例演示对**AddDelegate**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-131">The following example of an **AddDelegate** response shows a successful response to an **AddDelegate** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b4e9b-132">代码</span><span class="sxs-lookup"><span data-stu-id="b4e9b-132">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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
              <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
            </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:AddDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="adddelegate-error-response-example"></a><span data-ttu-id="b4e9b-133">AddDelegate 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="b4e9b-133">AddDelegate error response example</span></span>

### <a name="description"></a><span data-ttu-id="b4e9b-134">说明</span><span class="sxs-lookup"><span data-stu-id="b4e9b-134">Description</span></span>

<span data-ttu-id="b4e9b-135">下面的示例演示对添加已添加到的主体的邮箱代理人的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-135">The following example shows the response to a request to add a delegate who has already been added to the principal's mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="b4e9b-136">代码</span><span class="sxs-lookup"><span data-stu-id="b4e9b-136">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                           ResponseClass="Success"
                           xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Error">
          <m:MessageText>The user is already a delegate for the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorDelegateAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      </m:AddDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="b4e9b-137">注释</span><span class="sxs-lookup"><span data-stu-id="b4e9b-137">Comments</span></span>

<span data-ttu-id="b4e9b-138">如果尝试添加代理时返回的 ErrorDelegateAlreadyExists 响应代码，使用[GetDelegate 操作](getdelegate-operation.md)获得代理人，当前的所有权限，然后使用[UpdateDelegate 操作](updatedelegate-operation.md)设置新的权限。</span><span class="sxs-lookup"><span data-stu-id="b4e9b-138">If the ErrorDelegateAlreadyExists response code is returned when you try to add a delegate, use the [GetDelegate operation](getdelegate-operation.md) to get all the current permissions for the delegate, and then use the [UpdateDelegate operation](updatedelegate-operation.md) to set the new permissions.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4e9b-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b4e9b-139">See also</span></span>

- [<span data-ttu-id="b4e9b-140">添加代理人</span><span class="sxs-lookup"><span data-stu-id="b4e9b-140">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

