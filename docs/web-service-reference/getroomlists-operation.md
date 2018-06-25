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
description: GetRoomLists 操作获取 Exchange 组织内可用会议室列表。
ms.openlocfilehash: 139a669bfc6b7c4bc9bd9c07f9f9cf52954860c0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754672"
---
# <a name="getroomlists-operation"></a><span data-ttu-id="757c0-103">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="757c0-103">GetRoomLists operation</span></span>

<span data-ttu-id="757c0-104">**GetRoomLists**操作获取 Exchange 组织内可用会议室列表。</span><span class="sxs-lookup"><span data-stu-id="757c0-104">The **GetRoomLists** operation gets the room lists that are available within the Exchange organization.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="757c0-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="757c0-105">SOAP Headers</span></span>

<span data-ttu-id="757c0-106">**GetRoomLists**操作可以使用列出并在下表中所述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="757c0-106">The **GetRoomLists** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="757c0-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="757c0-107">**Header**</span></span>|<span data-ttu-id="757c0-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="757c0-108">**Element**</span></span>|<span data-ttu-id="757c0-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="757c0-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="757c0-110">模拟</span><span class="sxs-lookup"><span data-stu-id="757c0-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="757c0-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="757c0-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="757c0-112">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="757c0-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="757c0-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="757c0-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="757c0-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="757c0-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="757c0-115">标识用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="757c0-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="757c0-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="757c0-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="757c0-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="757c0-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="757c0-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="757c0-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="757c0-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="757c0-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="757c0-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="757c0-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="757c0-121">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="757c0-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getroomlists-request-example"></a><span data-ttu-id="757c0-122">GetRoomLists 请求示例</span><span class="sxs-lookup"><span data-stu-id="757c0-122">GetRoomLists request example</span></span>

### <a name="description"></a><span data-ttu-id="757c0-123">说明</span><span class="sxs-lookup"><span data-stu-id="757c0-123">Description</span></span>

<span data-ttu-id="757c0-124">下面是一个返回服务器上的可用会议室列表**GetRoomLists**请求示例。</span><span class="sxs-lookup"><span data-stu-id="757c0-124">The following is an example of a **GetRoomLists** request that returns the room lists that are available on the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="757c0-125">代码</span><span class="sxs-lookup"><span data-stu-id="757c0-125">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="757c0-126">请求元素</span><span class="sxs-lookup"><span data-stu-id="757c0-126">Request elements</span></span>

<span data-ttu-id="757c0-127">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="757c0-127">The following element is used in the request:</span></span>
  
- [<span data-ttu-id="757c0-128">GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="757c0-128">GetRoomLists</span></span>](getroomlists.md)
    
## <a name="successful-getroomlists-response-example"></a><span data-ttu-id="757c0-129">成功 GetRoomLists 响应示例</span><span class="sxs-lookup"><span data-stu-id="757c0-129">Successful GetRoomLists response example</span></span>

### <a name="description"></a><span data-ttu-id="757c0-130">说明</span><span class="sxs-lookup"><span data-stu-id="757c0-130">Description</span></span>

<span data-ttu-id="757c0-131">下面是响应的**GetRoomLists**请求的示例。</span><span class="sxs-lookup"><span data-stu-id="757c0-131">The following is an example of a response to a **GetRoomLists** request.</span></span> <span data-ttu-id="757c0-132">此响应的服务器上显示一个会议室列表。</span><span class="sxs-lookup"><span data-stu-id="757c0-132">This response shows one room list on the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="757c0-133">代码</span><span class="sxs-lookup"><span data-stu-id="757c0-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Address xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="successful-getroomlists-response-elements"></a><span data-ttu-id="757c0-134">成功 GetRoomLists 响应元素</span><span class="sxs-lookup"><span data-stu-id="757c0-134">Successful GetRoomLists response elements</span></span>

<span data-ttu-id="757c0-135">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="757c0-135">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="757c0-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="757c0-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="757c0-137">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="757c0-137">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
    
- [<span data-ttu-id="757c0-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="757c0-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="757c0-139">RoomLists</span><span class="sxs-lookup"><span data-stu-id="757c0-139">RoomLists</span></span>](roomlists.md)
    
- [<span data-ttu-id="757c0-140">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="757c0-140">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="757c0-141">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="757c0-141">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="757c0-142">MailboxType</span><span class="sxs-lookup"><span data-stu-id="757c0-142">MailboxType</span></span>](mailboxtype.md)
    
### <a name="getroomlists-error-response-example"></a><span data-ttu-id="757c0-143">GetRoomLists 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="757c0-143">GetRoomLists Error response example</span></span>

#### <a name="description"></a><span data-ttu-id="757c0-144">说明</span><span class="sxs-lookup"><span data-stu-id="757c0-144">Description</span></span>

<span data-ttu-id="757c0-145">下面的示例演示对尝试从没有定义任何会议室列表服务器获取会议室列表的响应。</span><span class="sxs-lookup"><span data-stu-id="757c0-145">The following example shows the response to an attempt to get room lists from a server that does not have any room lists defined.</span></span>
  
#### <a name="code"></a><span data-ttu-id="757c0-146">代码</span><span class="sxs-lookup"><span data-stu-id="757c0-146">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"/>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

#### <a name="getroomlists-error-response-elements"></a><span data-ttu-id="757c0-147">GetRoomLists 错误响应元素</span><span class="sxs-lookup"><span data-stu-id="757c0-147">GetRoomLists Error response elements</span></span>

<span data-ttu-id="757c0-148">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="757c0-148">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="757c0-149">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="757c0-149">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="757c0-150">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="757c0-150">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
    
- [<span data-ttu-id="757c0-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="757c0-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="757c0-152">RoomLists</span><span class="sxs-lookup"><span data-stu-id="757c0-152">RoomLists</span></span>](roomlists.md)
    
## <a name="see-also"></a><span data-ttu-id="757c0-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="757c0-153">See also</span></span>



[<span data-ttu-id="757c0-154">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="757c0-154">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="757c0-155">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="757c0-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

