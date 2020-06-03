---
title: 使用 Exchange 中的 EWS 获取会议室列表
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 15980e4a-e41c-4194-829a-cadbdf365bf1
description: 了解如何使用 EWS 托管 API 或 EWS 从 Exchange 服务器获取组织中所有会议室列表或单个会议室列表中的列表。
localization_priority: Priority
ms.openlocfilehash: 7c571b0550f861552cdbe8c5b30138101c9fc788
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455791"
---
# <a name="get-room-lists-by-using-ews-in-exchange"></a><span data-ttu-id="201d8-103">使用 Exchange 中的 EWS 获取会议室列表</span><span class="sxs-lookup"><span data-stu-id="201d8-103">Get room lists by using EWS in Exchange</span></span>

<span data-ttu-id="201d8-104">了解如何使用 EWS 托管 API 或 EWS 从 Exchange 服务器获取组织中所有会议室列表或单个会议室列表中的列表。</span><span class="sxs-lookup"><span data-stu-id="201d8-104">Learn how to get a list of all the room lists in your organization or a single room list from an Exchange server by using the EWS Managed API or EWS.</span></span>
  
<span data-ttu-id="201d8-105">您可以使用 EWS 托管 API 或 EWS 获取有关聊天室以及如何在组织中对聊天室进行分组的信息。</span><span class="sxs-lookup"><span data-stu-id="201d8-105">You can use the EWS Managed API or EWS to get information about rooms and how the rooms are grouped in your organization.</span></span> <span data-ttu-id="201d8-106">默认情况下，会议室列表不存在;您的管理员需要创建和组织它们。</span><span class="sxs-lookup"><span data-stu-id="201d8-106">Room lists don't exist by default; your administrator needs to create and organize them.</span></span> <span data-ttu-id="201d8-107">通常情况下，它们按位置或部门组织，如以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="201d8-107">Typically, they're organized by location or department, as shown in the following example.</span></span>
  
<span data-ttu-id="201d8-108">**Contoso 会议室列表名称和电子邮件地址**</span><span class="sxs-lookup"><span data-stu-id="201d8-108">**Contoso room list names and email addresses**</span></span>

|<span data-ttu-id="201d8-109">**会议室列表的名称**</span><span class="sxs-lookup"><span data-stu-id="201d8-109">**Name of room list**</span></span>|<span data-ttu-id="201d8-110">**会议室列表的电子邮件地址**</span><span class="sxs-lookup"><span data-stu-id="201d8-110">**Email address of room list**</span></span>|
|:-----|:-----|
|<span data-ttu-id="201d8-111">构建11个会议室列表</span><span class="sxs-lookup"><span data-stu-id="201d8-111">Building 11 room list</span></span>  <br/> |<span data-ttu-id="201d8-112">Bldg11rooms@contoso.com</span><span class="sxs-lookup"><span data-stu-id="201d8-112">Bldg11rooms@contoso.com</span></span>  <br/> |
|<span data-ttu-id="201d8-113">保健科学建筑物会议室列表</span><span class="sxs-lookup"><span data-stu-id="201d8-113">Health Science Building Conference Room List</span></span>  <br/> |<span data-ttu-id="201d8-114">HSbldgrooms@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="201d8-114">HSbldgrooms@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="201d8-115">会计车间会议室</span><span class="sxs-lookup"><span data-stu-id="201d8-115">Accounting Floor Meeting Rooms</span></span>  <br/> |<span data-ttu-id="201d8-116">Acctfloor300@contoso.com</span><span class="sxs-lookup"><span data-stu-id="201d8-116">Acctfloor300@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="201d8-117">会议室列表中的每个会议室都具有与其关联的名称和电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="201d8-117">Each room in a room list has a name and email address associated with it.</span></span>
  
<span data-ttu-id="201d8-118">**Contoso 会议室名称和电子邮件地址**</span><span class="sxs-lookup"><span data-stu-id="201d8-118">**Contoso room names and email addresses**</span></span>

|<span data-ttu-id="201d8-119">**聊天室的名称**</span><span class="sxs-lookup"><span data-stu-id="201d8-119">**Name of room**</span></span>|<span data-ttu-id="201d8-120">**聊天室的电子邮件地址**</span><span class="sxs-lookup"><span data-stu-id="201d8-120">**Email address of room**</span></span>|
|:-----|:-----|
|<span data-ttu-id="201d8-121">会议房间11/101 （8） AV</span><span class="sxs-lookup"><span data-stu-id="201d8-121">Conf Room 11/101 (8) AV</span></span>  <br/> |<span data-ttu-id="201d8-122">Cf11101@contoso.com</span><span class="sxs-lookup"><span data-stu-id="201d8-122">Cf11101@contoso.com</span></span>  <br/> |
|<span data-ttu-id="201d8-123">HS 演示实验室（100）</span><span class="sxs-lookup"><span data-stu-id="201d8-123">HS Demonstration Lab (100)</span></span>  <br/> |<span data-ttu-id="201d8-124">Hs101@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="201d8-124">Hs101@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="201d8-125">会计 305 WB</span><span class="sxs-lookup"><span data-stu-id="201d8-125">Accounting 305 WB</span></span>  <br/> |<span data-ttu-id="201d8-126">Acct305@contoso.com</span><span class="sxs-lookup"><span data-stu-id="201d8-126">Acct305@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="201d8-127">您可以使用[ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS 托管 API 方法或[GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) ews 操作获取包含所有会议室列表的列表。</span><span class="sxs-lookup"><span data-stu-id="201d8-127">You can get a list that contains all room lists by using either the [ExchangeService.GetRoomLists](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="201d8-128">您可以通过使用[GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS 托管 API 方法或[GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS 操作，通过提供其电子邮件地址，来检索包含某个位置或部门的所有会议室的单个会议室列表。</span><span class="sxs-lookup"><span data-stu-id="201d8-128">You can retrieve a single room list that contains all the rooms for a location or department by supplying its email address by using the [GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="201d8-129">当您具有与会议室列表关联的文件室集合时，您可以通过电子邮件地址或通过查找名称中的关键字（如 "AV" 或 "Lab"），在集合中搜索以标识所需的聊天室或聊天室。</span><span class="sxs-lookup"><span data-stu-id="201d8-129">When you have a collection of rooms associated with a room list, you can then search through the collection to identify the room or rooms you want, either by email address, or by looking for key words in the name, such as "AV", or "Lab".</span></span> 
  
## <a name="get-all-room-lists-by-using-the-ews-managed-api"></a><span data-ttu-id="201d8-130">使用 EWS 托管 API 获取所有会议室列表</span><span class="sxs-lookup"><span data-stu-id="201d8-130">Get all room lists by using the EWS Managed API</span></span>
<span data-ttu-id="201d8-131"><a name="bk_GetRoomListewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="201d8-131"><a name="bk_GetRoomListewsma"> </a></span></span>

<span data-ttu-id="201d8-132">下面的示例演示如何使用[GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx)方法获取包含组织中所有会议室列表的列表。</span><span class="sxs-lookup"><span data-stu-id="201d8-132">The following example shows how to get a list that contains all the room lists in your organization by using the [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) method.</span></span> 
  
<span data-ttu-id="201d8-133">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="201d8-133">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
// Return all the room lists in the organization.
// This method call results in a GetRoomLists call to EWS.
EmailAddressCollection myRoomLists = service.GetRoomLists();
// Display the room lists.
foreach (EmailAddress address in myRoomLists)
{
    Console.WriteLine("Email Address: {0} Mailbox Type: {1}", address.Address, address.MailboxType);
}

```

## <a name="get-all-room-lists-by-using-ews"></a><span data-ttu-id="201d8-134">使用 EWS 获取所有会议室列表</span><span class="sxs-lookup"><span data-stu-id="201d8-134">Get all room lists by using EWS</span></span>
<span data-ttu-id="201d8-135"><a name="bk_GetRoomListews"> </a></span><span class="sxs-lookup"><span data-stu-id="201d8-135"><a name="bk_GetRoomListews"> </a></span></span>

<span data-ttu-id="201d8-136">下面的示例演示如何使用[GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx)操作获取组织中所有[RoomLists](https://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx)的集合。</span><span class="sxs-lookup"><span data-stu-id="201d8-136">The following example shows how to get a collection of all your organization's [RoomLists](https://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) by using the [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="201d8-137">这也是当您使用 EWS 托管 API[获取所有聊天室列表](#bk_GetRoomListewsma)时，EWS 托管 api 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="201d8-137">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all room lists](#bk_GetRoomListewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="201d8-138">服务器使用包含您的组织的聊天室列表的[GetRoomListsResponse](https://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx)消息对[GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx)请求做出响应。</span><span class="sxs-lookup"><span data-stu-id="201d8-138">The server responds to the [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) request with a [GetRoomListsResponse](https://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) message that contains the room lists for your organization.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="868" MinorBuildNumber="8" Version="V2_9" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomListsResponse ResponseClass="Success" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:RoomLists>
        <t:Address>
          <t:Name>Contoso Building 1 Room List</t:Name>
          <t:EmailAddress>bldg1rooms@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
        <t:Address>
          <t:Name>Contoso Building 2 Room List</t:Name>
          <t:EmailAddress>bldg2rooms@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
        <t:Address>
          <t:Name>Contoso Building 3 Room List</t:Name>
          <t:EmailAddress>bldg3rooms@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
      </m:RoomLists>
    </m:GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="get-all-the-rooms-in-a-room-list-by-using-the-ews-managed-api"></a><span data-ttu-id="201d8-139">使用 EWS 托管 API 获取会议室列表中的所有聊天室</span><span class="sxs-lookup"><span data-stu-id="201d8-139">Get all the rooms in a room list by using the EWS Managed API</span></span>
<span data-ttu-id="201d8-140"><a name="bk_FindRoomewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="201d8-140"><a name="bk_FindRoomewsma"> </a></span></span>

<span data-ttu-id="201d8-141">下面的示例演示如何使用[GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx)方法在会议室列表中获取聊天室的集合。</span><span class="sxs-lookup"><span data-stu-id="201d8-141">The following example shows how to get a collection of rooms in a room list by using the [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) method.</span></span> 
  
```cs
EmailAddress myRoomList = "bldg3rooms@contoso.com";
// This method call results in a GetRooms call to EWS.
System.Collections.ObjectModel.Collection<EmailAddress> myRoomAddresses = service.GetRooms(myRoomList);
// Display the individual rooms.
foreach (EmailAddress address in myRoomAddresses)
{
    Console.WriteLine("Email Address: {0}", address.Address);
}

```

## <a name="get-all-the-rooms-in-a-room-list-by-using-ews"></a><span data-ttu-id="201d8-142">使用 EWS 获取会议室列表中的所有聊天室</span><span class="sxs-lookup"><span data-stu-id="201d8-142">Get all the rooms in a room list by using EWS</span></span>
<span data-ttu-id="201d8-143"><a name="bk_FindRoomews"> </a></span><span class="sxs-lookup"><span data-stu-id="201d8-143"><a name="bk_FindRoomews"> </a></span></span>

<span data-ttu-id="201d8-144">下面的示例演示如何使用[GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx)操作获取[RoomList](https://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx)中的[聊天室](https://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx)列表。</span><span class="sxs-lookup"><span data-stu-id="201d8-144">The following example shows how to get a list of [rooms](https://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) in a [RoomList](https://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) by using the [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="201d8-145">这也是当您使用 EWS 托管 API[获取会议室列表中的所有聊天室](#bk_FindRoomewsma)时，EWS 托管 api 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="201d8-145">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all the rooms in a room list](#bk_FindRoomewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetRooms>
      <m:RoomList>
        <t:EmailAddress>bldg3rooms@contoso.com</t:EmailAddress>
      </m:RoomList>
    </m:GetRooms>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="201d8-146">服务器使用包含会议室列表中的聊天室的[GetRoomsResponse](https://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx)消息对[GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx)请求做出响应。</span><span class="sxs-lookup"><span data-stu-id="201d8-146">The server responds to the [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) request with a [GetRoomsResponse](https://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) message that contains the rooms in the room list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="873" MinorBuildNumber="9" 
                         Version="V2_9" xmlns:h="http://scemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomsResponse ResponseClass="Success" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://scemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:Rooms>
        <t:Room>
          <t:Id>
            <t:Name>Conf Room 3/101 (16) AV</t:Name>
            <t:EmailAddress>cf3101@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room>
          <t:Id>
            <t:Name>Conf Room 3/102 (8) AV</t:Name>
            <t:EmailAddress>cf3102@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room>
          <t:Id>
            <t:Name>Conf Room 3/103 (14) AV RoundTable</t:Name>
            <t:EmailAddress>cf3103@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
      </m:Rooms>
    </m:GetRoomsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="201d8-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="201d8-147">See also</span></span>


- [<span data-ttu-id="201d8-148">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="201d8-148">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="201d8-149">使用 Exchange 中的 EWS 获取忙/闲信息</span><span class="sxs-lookup"><span data-stu-id="201d8-149">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="201d8-150">创建和管理会议室邮箱</span><span class="sxs-lookup"><span data-stu-id="201d8-150">Create and Manage Room Mailboxes</span></span>](https://technet.microsoft.com/library/jj215781%28v=exchg.150%29.aspx)
    

