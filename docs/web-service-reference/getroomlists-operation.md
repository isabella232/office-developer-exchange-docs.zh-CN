---
title: GetRoomLists 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRoomLists
api_type:
- schema
ms.assetid: 55d451f9-547f-44ac-872e-9cb220ea7b7c
description: GetRoomLists 操作获取 Exchange 组织中可用的会议室列表。
ms.openlocfilehash: d1393a6a5e99b7e0a7e354d2b7dd035d04356ec2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458276"
---
# <a name="getroomlists-operation"></a><span data-ttu-id="0d006-103">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="0d006-103">GetRoomLists operation</span></span>

<span data-ttu-id="0d006-104">**GetRoomLists**操作获取 Exchange 组织中可用的会议室列表。</span><span class="sxs-lookup"><span data-stu-id="0d006-104">The **GetRoomLists** operation gets the room lists that are available within the Exchange organization.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="0d006-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="0d006-105">SOAP Headers</span></span>

<span data-ttu-id="0d006-106">**GetRoomLists**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="0d006-106">The **GetRoomLists** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="0d006-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="0d006-107">**Header**</span></span>|<span data-ttu-id="0d006-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="0d006-108">**Element**</span></span>|<span data-ttu-id="0d006-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d006-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d006-110">模拟</span><span class="sxs-lookup"><span data-stu-id="0d006-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="0d006-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="0d006-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="0d006-112">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="0d006-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="0d006-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="0d006-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="0d006-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="0d006-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="0d006-115">标识要用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="0d006-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="0d006-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="0d006-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="0d006-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0d006-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="0d006-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="0d006-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="0d006-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="0d006-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="0d006-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0d006-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="0d006-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="0d006-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getroomlists-request-example"></a><span data-ttu-id="0d006-122">GetRoomLists 请求示例</span><span class="sxs-lookup"><span data-stu-id="0d006-122">GetRoomLists request example</span></span>

### <a name="description"></a><span data-ttu-id="0d006-123">Description</span><span class="sxs-lookup"><span data-stu-id="0d006-123">Description</span></span>

<span data-ttu-id="0d006-124">下面是一个**GetRoomLists**请求的示例，该请求返回服务器上可用的会议室列表。</span><span class="sxs-lookup"><span data-stu-id="0d006-124">The following is an example of a **GetRoomLists** request that returns the room lists that are available on the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0d006-125">代码</span><span class="sxs-lookup"><span data-stu-id="0d006-125">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="0d006-126">Request 元素</span><span class="sxs-lookup"><span data-stu-id="0d006-126">Request elements</span></span>

<span data-ttu-id="0d006-127">在请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0d006-127">The following element is used in the request:</span></span>
  
- [<span data-ttu-id="0d006-128">GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="0d006-128">GetRoomLists</span></span>](getroomlists.md)
    
## <a name="successful-getroomlists-response-example"></a><span data-ttu-id="0d006-129">成功的 GetRoomLists 响应示例</span><span class="sxs-lookup"><span data-stu-id="0d006-129">Successful GetRoomLists response example</span></span>

### <a name="description"></a><span data-ttu-id="0d006-130">Description</span><span class="sxs-lookup"><span data-stu-id="0d006-130">Description</span></span>

<span data-ttu-id="0d006-131">下面的示例演示了对**GetRoomLists**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="0d006-131">The following is an example of a response to a **GetRoomLists** request.</span></span> <span data-ttu-id="0d006-132">此响应显示服务器上的一个会议室列表。</span><span class="sxs-lookup"><span data-stu-id="0d006-132">This response shows one room list on the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0d006-133">代码</span><span class="sxs-lookup"><span data-stu-id="0d006-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Address xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:Name>Room List</t:Name>
          <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
      </m:RoomLists>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-getroomlists-response-elements"></a><span data-ttu-id="0d006-134">成功的 GetRoomLists 响应元素</span><span class="sxs-lookup"><span data-stu-id="0d006-134">Successful GetRoomLists response elements</span></span>

<span data-ttu-id="0d006-135">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0d006-135">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0d006-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0d006-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0d006-137">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="0d006-137">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
    
- [<span data-ttu-id="0d006-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0d006-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0d006-139">RoomLists</span><span class="sxs-lookup"><span data-stu-id="0d006-139">RoomLists</span></span>](roomlists.md)
    
- [<span data-ttu-id="0d006-140">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0d006-140">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="0d006-141">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="0d006-141">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="0d006-142">MailboxType</span><span class="sxs-lookup"><span data-stu-id="0d006-142">MailboxType</span></span>](mailboxtype.md)
    
### <a name="getroomlists-error-response-example"></a><span data-ttu-id="0d006-143">GetRoomLists 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="0d006-143">GetRoomLists Error response example</span></span>

#### <a name="description"></a><span data-ttu-id="0d006-144">Description</span><span class="sxs-lookup"><span data-stu-id="0d006-144">Description</span></span>

<span data-ttu-id="0d006-145">下面的示例演示尝试从未定义任何会议室列表的服务器中获取会议室列表的响应。</span><span class="sxs-lookup"><span data-stu-id="0d006-145">The following example shows the response to an attempt to get room lists from a server that does not have any room lists defined.</span></span>
  
#### <a name="code"></a><span data-ttu-id="0d006-146">代码</span><span class="sxs-lookup"><span data-stu-id="0d006-146">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"/>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

#### <a name="getroomlists-error-response-elements"></a><span data-ttu-id="0d006-147">GetRoomLists 错误响应元素</span><span class="sxs-lookup"><span data-stu-id="0d006-147">GetRoomLists Error response elements</span></span>

<span data-ttu-id="0d006-148">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0d006-148">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="0d006-149">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0d006-149">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0d006-150">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="0d006-150">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
    
- [<span data-ttu-id="0d006-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0d006-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0d006-152">RoomLists</span><span class="sxs-lookup"><span data-stu-id="0d006-152">RoomLists</span></span>](roomlists.md)
    
## <a name="see-also"></a><span data-ttu-id="0d006-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0d006-153">See also</span></span>



[<span data-ttu-id="0d006-154">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="0d006-154">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="0d006-155">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0d006-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

