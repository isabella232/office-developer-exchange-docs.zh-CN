---
title: 要在 Exchange 使用 EWS 获取会议室列表
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 15980e4a-e41c-4194-829a-cadbdf365bf1
description: 了解如何通过使用 EWS 托管 API 或 EWS 从 Exchange 服务器获取组织中的所有会议室列表或单个会议室列表的列表。
ms.openlocfilehash: 404a31fb6c8d98bdbba4c79ed6912c333a44d04b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752779"
---
# <a name="get-room-lists-by-using-ews-in-exchange"></a><span data-ttu-id="8a33c-103">要在 Exchange 使用 EWS 获取会议室列表</span><span class="sxs-lookup"><span data-stu-id="8a33c-103">Get room lists by using EWS in Exchange</span></span>

<span data-ttu-id="8a33c-104">了解如何通过使用 EWS 托管 API 或 EWS 从 Exchange 服务器获取组织中的所有会议室列表或单个会议室列表的列表。</span><span class="sxs-lookup"><span data-stu-id="8a33c-104">Learn how to get a list of all the room lists in your organization or a single room list from an Exchange server by using the EWS Managed API or EWS.</span></span>
  
<span data-ttu-id="8a33c-105">您可以使用 EWS 托管 API 或 EWS 获取有关聊天室和聊天室在组织中的分组方式的信息。</span><span class="sxs-lookup"><span data-stu-id="8a33c-105">You can use the EWS Managed API or EWS to get information about rooms and how the rooms are grouped in your organization.</span></span> <span data-ttu-id="8a33c-106">会议室列表不存在默认设置。管理员需要创建并对其进行组织。</span><span class="sxs-lookup"><span data-stu-id="8a33c-106">Room lists don't exist by default; your administrator needs to create and organize them.</span></span> <span data-ttu-id="8a33c-107">通常情况下，它们被按位置或部门，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="8a33c-107">Typically, they're organized by location or department, as shown in the following example.</span></span>
  
<span data-ttu-id="8a33c-108">**Contoso 会议室列表名称和电子邮件地址**</span><span class="sxs-lookup"><span data-stu-id="8a33c-108">**Contoso room list names and email addresses**</span></span>

|<span data-ttu-id="8a33c-109">**会议室列表的名称**</span><span class="sxs-lookup"><span data-stu-id="8a33c-109">**Name of room list**</span></span>|<span data-ttu-id="8a33c-110">**会议室列表的电子邮件地址**</span><span class="sxs-lookup"><span data-stu-id="8a33c-110">**Email address of room list**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a33c-111">构建 11 会议室列表</span><span class="sxs-lookup"><span data-stu-id="8a33c-111">Building 11 room list</span></span>  <br/> |<span data-ttu-id="8a33c-112">Bldg11rooms@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8a33c-112">Bldg11rooms@contoso.com</span></span>  <br/> |
|<span data-ttu-id="8a33c-113">运行状况科学构建会议会议室列表</span><span class="sxs-lookup"><span data-stu-id="8a33c-113">Health Science Building Conference Room List</span></span>  <br/> |<span data-ttu-id="8a33c-114">HSbldgrooms@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="8a33c-114">HSbldgrooms@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="8a33c-115">会计 Floor 会议室</span><span class="sxs-lookup"><span data-stu-id="8a33c-115">Accounting Floor Meeting Rooms</span></span>  <br/> |<span data-ttu-id="8a33c-116">Acctfloor300@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8a33c-116">Acctfloor300@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="8a33c-117">会议室列表中的每个聊天室具有与其相关联的名称和电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="8a33c-117">Each room in a room list has a name and email address associated with it.</span></span>
  
<span data-ttu-id="8a33c-118">**Contoso 聊天室名称和电子邮件地址**</span><span class="sxs-lookup"><span data-stu-id="8a33c-118">**Contoso room names and email addresses**</span></span>

|<span data-ttu-id="8a33c-119">**会议室的名称**</span><span class="sxs-lookup"><span data-stu-id="8a33c-119">**Name of room**</span></span>|<span data-ttu-id="8a33c-120">**会议室的电子邮件地址**</span><span class="sxs-lookup"><span data-stu-id="8a33c-120">**Email address of room**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a33c-121">Conf 会议室 11/101 (8) AV</span><span class="sxs-lookup"><span data-stu-id="8a33c-121">Conf Room 11/101 (8) AV</span></span>  <br/> |<span data-ttu-id="8a33c-122">Cf11101@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8a33c-122">Cf11101@contoso.com</span></span>  <br/> |
|<span data-ttu-id="8a33c-123">HS 演示实验室 (100)</span><span class="sxs-lookup"><span data-stu-id="8a33c-123">HS Demonstration Lab (100)</span></span>  <br/> |<span data-ttu-id="8a33c-124">Hs101@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="8a33c-124">Hs101@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="8a33c-125">Accounting 305 WB</span><span class="sxs-lookup"><span data-stu-id="8a33c-125">Accounting 305 WB</span></span>  <br/> |<span data-ttu-id="8a33c-126">Acct305@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8a33c-126">Acct305@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="8a33c-127">您可以获取所有会议室列表都包含使用[ExchangeService.GetRoomLists](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS 托管 API 方法或[GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) EWS 操作的列表。</span><span class="sxs-lookup"><span data-stu-id="8a33c-127">You can get a list that contains all room lists by using either the [ExchangeService.GetRoomLists](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="8a33c-128">您可以通过使用[GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS 托管 API 方法或[GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS 操作提供其电子邮件地址中包含的位置或部门的所有聊天室的单个会议室列表。</span><span class="sxs-lookup"><span data-stu-id="8a33c-128">You can retrieve a single room list that contains all the rooms for a location or department by supplying its email address by using the [GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="8a33c-129">会议室列表相关联的聊天室的集合后，您可以然后搜索要标识聊天室或聊天室您希望，通过电子邮件地址，或要查找的名称，例如"AV"或"实验室"中的关键字的集合。</span><span class="sxs-lookup"><span data-stu-id="8a33c-129">When you have a collection of rooms associated with a room list, you can then search through the collection to identify the room or rooms you want, either by email address, or by looking for key words in the name, such as "AV", or "Lab".</span></span> 
  
## <a name="get-all-room-lists-by-using-the-ews-managed-api"></a><span data-ttu-id="8a33c-130">通过使用 EWS 托管 API 获取所有会议室列表</span><span class="sxs-lookup"><span data-stu-id="8a33c-130">Get all room lists by using the EWS Managed API</span></span>
<span data-ttu-id="8a33c-131"><a name="bk_GetRoomListewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="8a33c-131"></span></span>

<span data-ttu-id="8a33c-132">下面的示例演示如何获取使用[GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx)方法包含您的组织中的所有会议室列表的列表。</span><span class="sxs-lookup"><span data-stu-id="8a33c-132">The following example shows how to get a list that contains all the room lists in your organization by using the [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) method.</span></span> 
  
<span data-ttu-id="8a33c-133">此示例假定您具有身份验证向 Exchange 服务器，并已获取名为**服务** [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="8a33c-133">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

## <a name="get-all-room-lists-by-using-ews"></a><span data-ttu-id="8a33c-134">通过使用 EWS 获取所有会议室列表</span><span class="sxs-lookup"><span data-stu-id="8a33c-134">Get all room lists by using EWS</span></span>
<span data-ttu-id="8a33c-135"><a name="bk_GetRoomListews"> </a></span><span class="sxs-lookup"><span data-stu-id="8a33c-135"></span></span>

<span data-ttu-id="8a33c-136">下面的示例演示如何使用[GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx)操作获取贵组织的所有[RoomLists](http://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx)的集合。</span><span class="sxs-lookup"><span data-stu-id="8a33c-136">The following example shows how to get a collection of all your organization's [RoomLists](http://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) by using the [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="8a33c-137">这也是使用 EWS 托管 API[获取所有会议室列表](#bk_GetRoomListewsma)时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="8a33c-137">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all room lists](#bk_GetRoomListewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="8a33c-138">服务器响应[GetRoomListsResponse](http://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx)邮件，其中包含您的组织的聊天室列表的[GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx)请求。</span><span class="sxs-lookup"><span data-stu-id="8a33c-138">The server responds to the [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) request with a [GetRoomListsResponse](http://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) message that contains the room lists for your organization.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="868" MinorBuildNumber="8" Version="V2_9" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomListsResponse ResponseClass="Success" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-the-ews-managed-api"></a><span data-ttu-id="8a33c-139">通过使用 EWS 托管 API 获取会议室列表中的所有聊天室</span><span class="sxs-lookup"><span data-stu-id="8a33c-139">Get all the rooms in a room list by using the EWS Managed API</span></span>
<span data-ttu-id="8a33c-140"><a name="bk_FindRoomewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="8a33c-140"></span></span>

<span data-ttu-id="8a33c-141">下面的示例演示如何使用[GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx)方法获取会议室列表中的聊天室的集合。</span><span class="sxs-lookup"><span data-stu-id="8a33c-141">The following example shows how to get a collection of rooms in a room list by using the [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) method.</span></span> 
  
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-ews"></a><span data-ttu-id="8a33c-142">通过使用 EWS 获取会议室列表中的所有聊天室</span><span class="sxs-lookup"><span data-stu-id="8a33c-142">Get all the rooms in a room list by using EWS</span></span>
<span data-ttu-id="8a33c-143"><a name="bk_FindRoomews"> </a></span><span class="sxs-lookup"><span data-stu-id="8a33c-143"></span></span>

<span data-ttu-id="8a33c-144">下面的示例演示如何使用[GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx)操作获取[RoomList](http://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx)中[聊天室](http://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx)的列表。</span><span class="sxs-lookup"><span data-stu-id="8a33c-144">The following example shows how to get a list of [rooms](http://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) in a [RoomList](http://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) by using the [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="8a33c-145">这也是使用 EWS 托管 API[获取会议室列表中的所有聊天室](#bk_FindRoomewsma)时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="8a33c-145">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all the rooms in a room list](#bk_FindRoomewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="8a33c-146">服务器响应[GetRoomsResponse](http://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx)邮件，其中包含聊天室列表中的聊天室的[GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx)请求。</span><span class="sxs-lookup"><span data-stu-id="8a33c-146">The server responds to the [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) request with a [GetRoomsResponse](http://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) message that contains the rooms in the room list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="873" MinorBuildNumber="9" 
                         Version="V2_9" xmlns:h="http://scemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomsResponse ResponseClass="Success" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
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

## <a name="see-also"></a><span data-ttu-id="8a33c-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a33c-147">See also</span></span>


- [<span data-ttu-id="8a33c-148">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8a33c-148">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="8a33c-149">要在 Exchange 使用 EWS 获取忙/闲信息</span><span class="sxs-lookup"><span data-stu-id="8a33c-149">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8a33c-150">创建和管理会议室邮箱</span><span class="sxs-lookup"><span data-stu-id="8a33c-150">Create and Manage Room Mailboxes</span></span>](http://technet.microsoft.com/en-us/library/jj215781%28v=exchg.150%29.aspx)
    

