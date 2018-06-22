---
title: 添加和删除代理人，在 Exchange 使用 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cc7760bf-633b-483a-84ae-b52f437af2d3
description: 了解如何添加委派给或从用户的邮箱删除代理人，在 Exchange 使用 EWS 托管 API 或 EWS。
ms.openlocfilehash: d55ef6c5c4e434603d293dbe30c6147ceb73b08b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752738"
---
# <a name="add-and-remove-delegates-by-using-ews-in-exchange"></a><span data-ttu-id="d9b5f-103">添加和删除代理人，在 Exchange 使用 EWS</span><span class="sxs-lookup"><span data-stu-id="d9b5f-103">Add and remove delegates by using EWS in Exchange</span></span>

<span data-ttu-id="d9b5f-104">了解如何添加委派给或从用户的邮箱删除代理人，在 Exchange 使用 EWS 托管 API 或 EWS。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-104">Learn how to add delegates to or remove delegates from users' mailboxes by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="d9b5f-105">您可以使用 EWS 托管 API 或 EWS 启用代理人来代表邮箱所有者操作或删除对邮箱的代理人的访问。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-105">You can use the EWS Managed API or EWS to enable delegates to act on behalf of a mailbox owner or remove a delegate's access to a mailbox.</span></span> <span data-ttu-id="d9b5f-106">添加作为代理人，并且授予权限，用户可以执行邮箱所有者代表的任务。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-106">Users who are added as a delegate, and are given permissions, can perform tasks on behalf of the mailbox owner.</span></span> <span data-ttu-id="d9b5f-107">例如，他们可以创建和发送的会议邀请、 发送电子邮件，并响应会议请求邮箱所有者的代表。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-107">For example, they can create and send meeting invitations, send emails, and respond to meeting requests on the mailbox owner's behalf.</span></span> 
  
<span data-ttu-id="d9b5f-108">**表 1。EWS 托管 API 方法和添加和删除代理人的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="d9b5f-108">**Table 1. EWS Managed API methods and EWS operations for adding and removing delegates**</span></span>

|<span data-ttu-id="d9b5f-109">**任务**</span><span class="sxs-lookup"><span data-stu-id="d9b5f-109">**Task**</span></span>|<span data-ttu-id="d9b5f-110">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="d9b5f-110">**EWS Managed API method**</span></span>|<span data-ttu-id="d9b5f-111">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="d9b5f-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9b5f-112">添加代理人</span><span class="sxs-lookup"><span data-stu-id="d9b5f-112">Add delegates</span></span>  <br/> |[<span data-ttu-id="d9b5f-113">ExchangeService.AddDelegates</span><span class="sxs-lookup"><span data-stu-id="d9b5f-113">ExchangeService.AddDelegates</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d9b5f-114">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="d9b5f-114">AddDelegate</span></span>](http://msdn.microsoft.com/library/646fb994-229e-4d90-8b95-6541191cb3ae%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="d9b5f-115">删除代理人</span><span class="sxs-lookup"><span data-stu-id="d9b5f-115">Remove delegates</span></span>  <br/> |[<span data-ttu-id="d9b5f-116">ExchangeService.RemoveDelegates</span><span class="sxs-lookup"><span data-stu-id="d9b5f-116">ExchangeService.RemoveDelegates</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d9b5f-117">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="d9b5f-117">RemoveDelegate</span></span>](http://msdn.microsoft.com/library/f21c5171-62e7-47c8-99b1-22e1ff5883bb%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="d9b5f-118">代理将被授予对文件夹的权限后，他们可以根据其[委派权限](delegate-access-and-ews-in-exchange.md#bk_delegateperms)的操作的文件夹和所有子文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-118">After a delegate is granted permissions to a folder, they can act on items in the folder and any subfolders, according to their [delegate permissions](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span> <span data-ttu-id="d9b5f-119">代理人权限仅适用于后授予代理访问创建的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-119">Permissions for delegates only apply to subfolders that are created after the delegate access was granted.</span></span> <span data-ttu-id="d9b5f-120">若要更新文件夹前现有文件夹或其他文件夹的权限，请参阅[设置文件夹在 Exchange 使用 EWS 的另一个用户的权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-120">To update folder permissions for pre-existing folders, or other folders, see [Set folder permissions for another user by using EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="d9b5f-121">请注意，代理人可以仅添加到已启用邮箱的帐户，包括已启用邮件的安全组。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-121">Note that delegates can only be added to mailbox-enabled accounts, including mail-enabled security groups.</span></span> <span data-ttu-id="d9b5f-122">默认情况下，单个 EWS 委派访问呼叫可以访问最多 255 不同的邮箱。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-122">By default, a single EWS delegate access call can access a maximum of 255 different mailboxes.</span></span>

<span data-ttu-id="d9b5f-123"><a name="bk_adddelegateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d9b5f-123"></span></span>

## <a name="add-delegates-by-using-the-ews-managed-api"></a><span data-ttu-id="d9b5f-124">使用 EWS 托管 API 添加代理人</span><span class="sxs-lookup"><span data-stu-id="d9b5f-124">Add delegates by using the EWS Managed API</span></span>

<span data-ttu-id="d9b5f-125">使用[AddDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) EWS 托管 API 方法，可以向邮箱添加代理。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-125">You can add delegates to a mailbox by using the [AddDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="d9b5f-126">在本示例、 新日历、 联系人和电子邮件[DelegateUser](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx)创建对象，并为其各自的文件夹每个委托获得[编辑权限](delegate-access-and-ews-in-exchange.md#bk_delegateperms)。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-126">In this example, a new calendar, contact, and email [DelegateUser](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx) object is created, and each delegate is given [Editor permissions](delegate-access-and-ews-in-exchange.md#bk_delegateperms) for their respective folder.</span></span> <span data-ttu-id="d9b5f-127">您可以修改任何[DelegatePermissions 属性](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx)，通过指定的文件夹添加委托的示例，并可以对任何[DelegateFolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx)枚举由指定的值设置权限。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-127">You can modify the example to add a delegate to any of the folders specified by the [DelegatePermissions properties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx), and you can set the permissions to any of the values specified by the [DelegateFolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) enumeration.</span></span> 
  
<span data-ttu-id="d9b5f-128">此示例假定该**服务**的邮箱所有者，是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和用户已经过身份验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-128">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<DelegateUserResponse> AddDelegates(ExchangeService service)
{
    // Create a list to hold the new delegates to add.
    List<DelegateUser> newDelegates = new System.Collections.Generic.List<DelegateUser>();
    // Create a new delegate that has editor access to the mailbox owner's Calendar folder.
    DelegateUser calendarDelegate = new DelegateUser("calendardelegate@contoso.com");
    calendarDelegate.Permissions.CalendarFolderPermissionLevel = DelegateFolderPermissionLevel.Editor;
    // Add the delegate to the list of new delegates.
    newDelegates.Add(calendarDelegate);
    // Create a new delegate that has editor access to the mailbox owner's Contacts folder.
    DelegateUser contactDelegate = new DelegateUser("contactdelegate@contoso.com");
    contactDelegate.Permissions.ContactsFolderPermissionLevel = DelegateFolderPermissionLevel.Editor;
    // Add the delegate to the list of new delegates.
    newDelegates.Add(contactDelegate);
            
    // Create a new delegate that has editor access to the mailbox owner's Inbox folder.
    DelegateUser emailDelegate = new DelegateUser("emaildelegate@contoso.com");
    emailDelegate.Permissions.InboxFolderPermissionLevel = DelegateFolderPermissionLevel.Editor;
    // Add the delegate to the list of new delegates.
    newDelegates.Add(emailDelegate);
    // Create a mailbox object that represents the mailbox owner.
    Mailbox mailbox = new Mailbox("primary@contoso.com");
    // Call the AddDelegates method to add the delegates to the target mailbox.
    Collection<DelegateUserResponse> response = service.AddDelegates(mailbox, MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe, newDelegates);
            
    foreach (DelegateUserResponse resp in response)
    {
        // Print out the result and the last eight characters of the item ID.
        Console.WriteLine("For delegate " + resp.DelegateUser.UserId.PrimarySmtpAddress.ToString());
        Console.WriteLine("Result: {0}", resp.Result);
        Console.WriteLine("Error Code: {0}", resp.ErrorCode);
        Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
        Console.WriteLine("\r\n");
    }
    return response;
}
```

<span data-ttu-id="d9b5f-129"><a name="bk_adddelegateews"> </a></span><span class="sxs-lookup"><span data-stu-id="d9b5f-129"></span></span>

## <a name="add-delegates-by-using-ews"></a><span data-ttu-id="d9b5f-130">使用 EWS 添加代理人</span><span class="sxs-lookup"><span data-stu-id="d9b5f-130">Add delegates by using EWS</span></span>

<span data-ttu-id="d9b5f-131">下面的代码示例演示如何使用[AddDelegate](http://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) EWS 操作添加单独的日历、 联系人和电子邮件的代理人。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-131">The following code example shows how to add separate calendar, contact, and email delegates by using the [AddDelegate](http://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="d9b5f-132">[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素中，指定要修改的邮箱和[DelegateUser](http://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx)元素中包含的[权限](delegate-access-and-ews-in-exchange.md#bk_delegateperms)设置的每个委托。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-132">The mailbox to modify is specified by the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element, and the [permission](delegate-access-and-ews-in-exchange.md#bk_delegateperms) settings for each delegate are contained in the [DelegateUser](http://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="d9b5f-133">每个代理人已被授予对其目标文件夹的编辑器权限。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-133">Each of the delegates has been granted Editor permissions to their target folder.</span></span> 
  
<span data-ttu-id="d9b5f-134">这也是 EWS 托管 API 时您使用**AddDelegates**方法[添加代理](#bk_adddelegateewsma)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-134">This is also the XML request that the EWS Managed API sends when you use the **AddDelegates** method to [add delegates](#bk_adddelegateewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:AddDelegate>
      <m:Mailbox>
        <t:EmailAddress>primary@contoso.com</t:EmailAddress>
      </m:Mailbox>
      <m:DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>calendardelegate@contoso.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>Editor</t:CalendarFolderPermissionLevel>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
            <t:InboxFolderPermissionLevel>None</t:InboxFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>None</t:ContactsFolderPermissionLevel>
            <t:NotesFolderPermissionLevel>None</t:NotesFolderPermissionLevel>
            <t:JournalFolderPermissionLevel>None</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>contactdelegate@contoso.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>None</t:CalendarFolderPermissionLevel>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
            <t:InboxFolderPermissionLevel>None</t:InboxFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>Editor</t:ContactsFolderPermissionLevel>
            <t:NotesFolderPermissionLevel>None</t:NotesFolderPermissionLevel>
            <t:JournalFolderPermissionLevel>None</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>emaildelegate@contoso.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>None</t:CalendarFolderPermissionLevel>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
            <t:InboxFolderPermissionLevel>Editor</t:InboxFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>None</t:ContactsFolderPermissionLevel>
            <t:NotesFolderPermissionLevel>None</t:NotesFolderPermissionLevel>
            <t:JournalFolderPermissionLevel>None</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
      </m:DelegateUsers>
      <m:DeliverMeetingRequests>DelegatesAndSendInformationToMe</m:DeliverMeetingRequests>
    </m:AddDelegate>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d9b5f-135">服务器响应**AddDelegate**请求使用[AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx)消息，其中包括**NoError**，这表明已成功创建代理人[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-135">The server responds to the **AddDelegate** request with an [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the delegates were successfully created.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="888"
                         MinorBuildNumber="9"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:AddDelegateResponse ResponseClass="Success"
                           xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1337771579-694202782-848329751-1535221</t:SID>
              <t:PrimarySmtpAddress>calendardelegate@contoso.com</t:PrimarySmtpAddress>
              <t:DisplayName>calendardelegate</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1337771579-694202782-848329751-1535264</t:SID>
              <t:PrimarySmtpAddress>contactdelegate@contoso.com</t:PrimarySmtpAddress>
              <t:DisplayName>contactdelegate</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1337771579-694202782-848329751-1535223</t:SID>
              <t:PrimarySmtpAddress>emaildelegate@contoso.com</t:PrimarySmtpAddress>
              <t:DisplayName>emaildelegate</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:AddDelegateResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="d9b5f-136"><a name="bk_removedelegateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d9b5f-136"></span></span>

## <a name="remove-delegates-by-using-the-ews-managed-api"></a><span data-ttu-id="d9b5f-137">使用 EWS 托管 API 删除代理人</span><span class="sxs-lookup"><span data-stu-id="d9b5f-137">Remove delegates by using the EWS Managed API</span></span>

<span data-ttu-id="d9b5f-138">可以通过使用[ExchangeService.RemoveDelegates](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) EWS 托管 API 方法从目标邮箱中删除代理人。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-138">You can remove delegates from a target mailbox by using the [ExchangeService.RemoveDelegates](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="d9b5f-139">本示例中，将删除[添加一个委托的示例](#bk_adddelegateewsma)中的委托权限集。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-139">In this example, the delegate permissions set in the [add a delegate example](#bk_adddelegateewsma) are removed.</span></span> 
  
<span data-ttu-id="d9b5f-140">此示例假定该**服务**的邮箱所有者，是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和用户已经过身份验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-140">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<DelegateUserResponse> RemoveDelegates(ExchangeService service)
{
    // Create a list to hold the delegates to delete.
    List<UserId> deletedDelegates = new System.Collections.Generic.List<UserId>();
    // Add the delegate to the list of new delegates.
    deletedDelegates.Add("calendardelegate@contoso.com");
    // Add the delegate to the list of new delegates.
    deletedDelegates.Add("contactdelegate@contoso.com");
    // Add the delegate to the list of new delegates.
    deletedDelegates.Add("emaildelegate@contoso.com");
    // Create a mailbox object that represents the mailbox owner.
    Mailbox mailbox = new Mailbox("primary@contoso.com");
    // Call the AddDelegates method to add the delegates to the target mailbox.
    Collection<DelegateUserResponse> response = service.RemoveDelegates(mailbox, deletedDelegates);
    foreach (DelegateUserResponse resp in response)
    {
        // Print out the result and the last eight characters of the item ID.
        Console.WriteLine("Result: {0}", resp.Result);
        Console.WriteLine("Error Code: {0}", resp.ErrorCode);
        Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
    }
    return response;
}
```

<span data-ttu-id="d9b5f-141"><a name="bk_removedelegateews"> </a></span><span class="sxs-lookup"><span data-stu-id="d9b5f-141"></span></span>

## <a name="remove-delegates-by-using-ews"></a><span data-ttu-id="d9b5f-142">使用 EWS 删除代理人</span><span class="sxs-lookup"><span data-stu-id="d9b5f-142">Remove delegates by using EWS</span></span>

<span data-ttu-id="d9b5f-143">可以通过使用[RemoveDelegate](http://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) EWS 操作从邮箱中删除代理人。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-143">You can remove delegates from a mailbox by using the [RemoveDelegate](http://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="d9b5f-144">本示例中，将删除[添加一个委托的示例](#bk_adddelegateews)中的委托权限集。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-144">In this example, the delegate permissions set in the [add a delegate example](#bk_adddelegateews) are removed.</span></span> 
  
<span data-ttu-id="d9b5f-145">这也是 EWS 托管 API 时您使用**RemoveDelegates**方法[删除代理人](#bk_removedelegateewsma)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-145">This is also the XML request that the EWS Managed API sends when you use the **RemoveDelegates** method to [remove delegates](#bk_removedelegateewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:RemoveDelegate>
      <m:Mailbox>
        <t:EmailAddress>primary@contoso.com</t:EmailAddress>
      </m:Mailbox>
      <m:UserIds>
        <t:UserId>
          <t:PrimarySmtpAddress>calendardelegate@contoso.com</t:PrimarySmtpAddress>
        </t:UserId>
        <t:UserId>
          <t:PrimarySmtpAddress>contactdelegate@contoso.com</t:PrimarySmtpAddress>
        </t:UserId>
        <t:UserId>
          <t:PrimarySmtpAddress>emaildelegate@contoso.com</t:PrimarySmtpAddress>
        </t:UserId>
      </m:UserIds>
    </m:RemoveDelegate>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d9b5f-146">服务器响应包含**NoError**，这表明已成功删除代理人[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的[AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx)消息的**RemoveDelegate**请求。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-146">The server responds to the **RemoveDelegate** request with a [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the delegates were successfully removed.</span></span>

<span data-ttu-id="d9b5f-147"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="d9b5f-147"></span></span>

## <a name="next-steps"></a><span data-ttu-id="d9b5f-148">后续步骤</span><span class="sxs-lookup"><span data-stu-id="d9b5f-148">Next steps</span></span>

<span data-ttu-id="d9b5f-149">代理人添加日历、 电子邮件，和任务文件夹之后，代理人可以访问文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-149">After you add delegates to calendar, email, and task folders, the delegate can access the items in the folders.</span></span> <span data-ttu-id="d9b5f-150">若要了解详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="d9b5f-150">To learn more, see the following articles:</span></span>
  
- [<span data-ttu-id="d9b5f-151">作为 Exchange 中使用 EWS 代理人的访问电子邮件</span><span class="sxs-lookup"><span data-stu-id="d9b5f-151">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d9b5f-152">在 Exchange 中使用 EWS 作为代理人访问日历</span><span class="sxs-lookup"><span data-stu-id="d9b5f-152">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d9b5f-153">作为代理人在 Exchange 使用 EWS 访问联系人</span><span class="sxs-lookup"><span data-stu-id="d9b5f-153">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
<span data-ttu-id="d9b5f-154">如果您为其添加代理人的文件夹包含授予委派访问权限之前创建的子文件夹，该委托不能访问这些没有其他权限的文件夹。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-154">If the folders for which you added delegates include child folders that were created before you granted the delegate access, the delegate will not be able to access those folders without additional permissions.</span></span> <span data-ttu-id="d9b5f-155">若要添加这些权限，或修改任何其他文件夹的权限，请参阅[设置文件夹在 Exchange 使用 EWS 的另一个用户的权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="d9b5f-155">To add these permissions, or modify permissions for any other folders, see [Set folder permissions for another user by using EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9b5f-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9b5f-156">See also</span></span>

- [<span data-ttu-id="d9b5f-157">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="d9b5f-157">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="d9b5f-158">添加 Exchange 2013： 以编程方式委派到的电子邮件帐户的用户</span><span class="sxs-lookup"><span data-stu-id="d9b5f-158">Exchange 2013: Add delegate users to an email account programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Adding-1024511f)   
- [<span data-ttu-id="d9b5f-159">Exchange 2013： 以编程方式与电子邮件帐户关联的更新代理人</span><span class="sxs-lookup"><span data-stu-id="d9b5f-159">Exchange 2013: Update delegates associated with email accounts programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Update-b40d3bac)   
- [<span data-ttu-id="d9b5f-160">Exchange 2013： 删除以编程方式与电子邮件帐户关联的代理人</span><span class="sxs-lookup"><span data-stu-id="d9b5f-160">Exchange 2013: Remove delegates associated with email accounts programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Remove-686f7714)
    

