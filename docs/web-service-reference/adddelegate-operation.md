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
description: AddDelegate 操作将一个或多个委派添加到主体的邮箱，并设置特定的访问权限。
ms.openlocfilehash: 80adbe71d69be1025dc9593c6a9002bc68fdcb76
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466512"
---
# <a name="adddelegate-operation"></a><span data-ttu-id="f915d-103">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="f915d-103">AddDelegate operation</span></span>

<span data-ttu-id="f915d-104">**AddDelegate**操作将一个或多个委派添加到主体的邮箱，并设置特定的访问权限。</span><span class="sxs-lookup"><span data-stu-id="f915d-104">The **AddDelegate** operation adds one or more delegates to a principal's mailbox and sets specific access permissions.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="f915d-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="f915d-105">SOAP headers</span></span>

<span data-ttu-id="f915d-106">**AddDelegate**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="f915d-106">The **AddDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="f915d-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="f915d-107">**Header**</span></span>|<span data-ttu-id="f915d-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="f915d-108">**Element**</span></span>|<span data-ttu-id="f915d-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="f915d-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f915d-110">模拟</span><span class="sxs-lookup"><span data-stu-id="f915d-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="f915d-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f915d-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f915d-112">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="f915d-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="f915d-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f915d-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="f915d-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f915d-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="f915d-115">标识要用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="f915d-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="f915d-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="f915d-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="f915d-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f915d-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f915d-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="f915d-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="f915d-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="f915d-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="f915d-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f915d-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f915d-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="f915d-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="adddelegate-request-example"></a><span data-ttu-id="f915d-122">AddDelegate 请求示例</span><span class="sxs-lookup"><span data-stu-id="f915d-122">AddDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="f915d-123">说明</span><span class="sxs-lookup"><span data-stu-id="f915d-123">Description</span></span>

<span data-ttu-id="f915d-124">下面的**AddDelegate**请求示例显示了向用户2拥有的文件夹授予对 user1 委派权限的尝试。</span><span class="sxs-lookup"><span data-stu-id="f915d-124">The following example of an **AddDelegate** request shows an attempt to give user1 delegate permissions on folders that are owned by user2.</span></span> <span data-ttu-id="f915d-125">User1 拥有对 user2's 联系人文件夹的 user2's 日历文件夹和审阅者级别权限的作者级别权限。</span><span class="sxs-lookup"><span data-stu-id="f915d-125">User1 is given Author-level permissions to user2's Calendar folder and Reviewer-level permissions to user2's Contacts folder.</span></span> <span data-ttu-id="f915d-126">User1 将不会收到会议邮件的副本，并且无法查看 user2's 邮箱中的私人项目。</span><span class="sxs-lookup"><span data-stu-id="f915d-126">User1 will not receive copies of meeting messages and will be unable to view private items in user2's mailbox.</span></span> <span data-ttu-id="f915d-127">将向 user1 和用户2发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="f915d-127">Meeting requests will be sent to both user1 and user2.</span></span> 
  
### <a name="code"></a><span data-ttu-id="f915d-128">代码</span><span class="sxs-lookup"><span data-stu-id="f915d-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="adddelegate-response-example"></a><span data-ttu-id="f915d-129">AddDelegate 响应示例</span><span class="sxs-lookup"><span data-stu-id="f915d-129">AddDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="f915d-130">说明</span><span class="sxs-lookup"><span data-stu-id="f915d-130">Description</span></span>

<span data-ttu-id="f915d-131">下面的**AddDelegate**响应示例显示了对**AddDelegate**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="f915d-131">The following example of an **AddDelegate** response shows a successful response to an **AddDelegate** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="f915d-132">代码</span><span class="sxs-lookup"><span data-stu-id="f915d-132">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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
              <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
            </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:AddDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="adddelegate-error-response-example"></a><span data-ttu-id="f915d-133">AddDelegate 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="f915d-133">AddDelegate error response example</span></span>

### <a name="description"></a><span data-ttu-id="f915d-134">说明</span><span class="sxs-lookup"><span data-stu-id="f915d-134">Description</span></span>

<span data-ttu-id="f915d-135">下面的示例演示对添加代理（已添加到主体邮箱）的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="f915d-135">The following example shows the response to a request to add a delegate who has already been added to the principal's mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="f915d-136">代码</span><span class="sxs-lookup"><span data-stu-id="f915d-136">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                           ResponseClass="Success"
                           xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="f915d-137">备注</span><span class="sxs-lookup"><span data-stu-id="f915d-137">Comments</span></span>

<span data-ttu-id="f915d-138">如果在尝试添加委派时返回 ErrorDelegateAlreadyExists 响应代码，请使用[GetDelegate 操作](getdelegate-operation.md)获取代理的所有当前权限，然后使用[UpdateDelegate 操作](updatedelegate-operation.md)来设置新权限。</span><span class="sxs-lookup"><span data-stu-id="f915d-138">If the ErrorDelegateAlreadyExists response code is returned when you try to add a delegate, use the [GetDelegate operation](getdelegate-operation.md) to get all the current permissions for the delegate, and then use the [UpdateDelegate operation](updatedelegate-operation.md) to set the new permissions.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f915d-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f915d-139">See also</span></span>

- [<span data-ttu-id="f915d-140">添加委派</span><span class="sxs-lookup"><span data-stu-id="f915d-140">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

