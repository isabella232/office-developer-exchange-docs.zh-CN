---
title: GetRooms 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRooms
api_type:
- schema
ms.assetid: 5501ddc0-3bfa-4da6-8e15-4223ca5499a3
description: GetRooms 操作获取指定的房间列表中的聊天室。
ms.openlocfilehash: 3718c476881ae8aa538646464e7c61845d849562
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754676"
---
# <a name="getrooms-operation"></a><span data-ttu-id="0dcd2-103">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="0dcd2-103">GetRooms operation</span></span>

<span data-ttu-id="0dcd2-104">**GetRooms**操作获取指定的房间列表中的聊天室。</span><span class="sxs-lookup"><span data-stu-id="0dcd2-104">The **GetRooms** operation gets the rooms within the specified room list.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="0dcd2-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="0dcd2-105">SOAP Headers</span></span>

<span data-ttu-id="0dcd2-106">**GetRooms**操作可以使用列出并在下表中所述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="0dcd2-106">The **GetRooms** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="0dcd2-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="0dcd2-107">**Header**</span></span>|<span data-ttu-id="0dcd2-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="0dcd2-108">**Element**</span></span>|<span data-ttu-id="0dcd2-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="0dcd2-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0dcd2-110">模拟</span><span class="sxs-lookup"><span data-stu-id="0dcd2-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="0dcd2-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="0dcd2-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="0dcd2-112">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="0dcd2-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="0dcd2-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="0dcd2-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="0dcd2-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="0dcd2-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="0dcd2-115">标识用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="0dcd2-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="0dcd2-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="0dcd2-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="0dcd2-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0dcd2-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="0dcd2-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="0dcd2-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="0dcd2-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="0dcd2-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="0dcd2-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0dcd2-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="0dcd2-121">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="0dcd2-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getrooms-request-example"></a><span data-ttu-id="0dcd2-122">GetRooms 请求示例</span><span class="sxs-lookup"><span data-stu-id="0dcd2-122">GetRooms request example</span></span>

### <a name="description"></a><span data-ttu-id="0dcd2-123">说明</span><span class="sxs-lookup"><span data-stu-id="0dcd2-123">Description</span></span>

<span data-ttu-id="0dcd2-124">以下是获取与会议室列表相关联的聊天室的**GetRooms**请求的示例。</span><span class="sxs-lookup"><span data-stu-id="0dcd2-124">The following is an example of a **GetRooms** request that gets the rooms that are associated with a room list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0dcd2-125">代码</span><span class="sxs-lookup"><span data-stu-id="0dcd2-125">Code</span></span>

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
    <m:GetRooms>
      <m:RoomList>
        <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
      </m:RoomList>
    </m:GetRooms>
  </soap:Body>

```

### <a name="request-elements"></a><span data-ttu-id="0dcd2-126">请求元素</span><span class="sxs-lookup"><span data-stu-id="0dcd2-126">Request elements</span></span>

<span data-ttu-id="0dcd2-127">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0dcd2-127">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0dcd2-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0dcd2-128">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="0dcd2-129">GetRooms</span><span class="sxs-lookup"><span data-stu-id="0dcd2-129">GetRooms</span></span>](getrooms.md)
    
- [<span data-ttu-id="0dcd2-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="0dcd2-130">RoomList</span></span>](roomlist.md)
    
- [<span data-ttu-id="0dcd2-131">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0dcd2-131">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-getrooms-response-example"></a><span data-ttu-id="0dcd2-132">成功 GetRooms 响应示例</span><span class="sxs-lookup"><span data-stu-id="0dcd2-132">Successful GetRooms response example</span></span>

### <a name="description"></a><span data-ttu-id="0dcd2-133">说明</span><span class="sxs-lookup"><span data-stu-id="0dcd2-133">Description</span></span>

<span data-ttu-id="0dcd2-134">以下响应显示与会议室列表相关联的聊天室的电子邮件地址信息。</span><span class="sxs-lookup"><span data-stu-id="0dcd2-134">The following response shows the email address information for the rooms that are associated with the room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="0dcd2-135">代码</span><span class="sxs-lookup"><span data-stu-id="0dcd2-135">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:Rooms xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Room xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:Id>
            <t:Name>Room01</t:Name>
            <t:EmailAddress>Room01@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:Id>
            <t:Name>Room02</t:Name>
            <t:EmailAddress>Room02@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
      </m:Rooms>
    </GetRoomsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="successful-getrooms-response-elements"></a><span data-ttu-id="0dcd2-136">成功 GetRooms 响应元素</span><span class="sxs-lookup"><span data-stu-id="0dcd2-136">Successful GetRooms response elements</span></span>

<span data-ttu-id="0dcd2-137">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0dcd2-137">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0dcd2-138">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0dcd2-138">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0dcd2-139">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="0dcd2-139">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="0dcd2-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0dcd2-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0dcd2-141">聊天室</span><span class="sxs-lookup"><span data-stu-id="0dcd2-141">Rooms</span></span>](rooms.md)
    
- [<span data-ttu-id="0dcd2-142">聊天室</span><span class="sxs-lookup"><span data-stu-id="0dcd2-142">Room</span></span>](room.md)
    
- [<span data-ttu-id="0dcd2-143">名称 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="0dcd2-143">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="0dcd2-144">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0dcd2-144">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="0dcd2-145">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="0dcd2-145">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="0dcd2-146">MailboxType</span><span class="sxs-lookup"><span data-stu-id="0dcd2-146">MailboxType</span></span>](mailboxtype.md)
    
## <a name="getrooms-error-response-example"></a><span data-ttu-id="0dcd2-147">GetRooms 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="0dcd2-147">GetRooms Error response example</span></span>

### <a name="description"></a><span data-ttu-id="0dcd2-148">说明</span><span class="sxs-lookup"><span data-stu-id="0dcd2-148">Description</span></span>

<span data-ttu-id="0dcd2-149">下面的示例演示错误响应导致尝试获取会议室信息不存在的会议室列表。</span><span class="sxs-lookup"><span data-stu-id="0dcd2-149">The following example shows an error response caused by an attempt to get room information for a nonexistent room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="0dcd2-150">代码</span><span class="sxs-lookup"><span data-stu-id="0dcd2-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Error" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>No results were found.</MessageText>
      <ResponseCode>ErrorNameResolutionNoResults</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRoomsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="getrooms-error-response-elements"></a><span data-ttu-id="0dcd2-151">GetRooms 错误响应元素</span><span class="sxs-lookup"><span data-stu-id="0dcd2-151">GetRooms Error response elements</span></span>

<span data-ttu-id="0dcd2-152">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0dcd2-152">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0dcd2-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0dcd2-153">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0dcd2-154">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="0dcd2-154">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="0dcd2-155">MessageText</span><span class="sxs-lookup"><span data-stu-id="0dcd2-155">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0dcd2-156">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0dcd2-156">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0dcd2-157">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0dcd2-157">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="0dcd2-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0dcd2-158">See also</span></span>

- [<span data-ttu-id="0dcd2-159">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="0dcd2-159">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="0dcd2-160">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0dcd2-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

