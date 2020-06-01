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
description: GetRooms 操作获取指定会议室列表中的会议室。
ms.openlocfilehash: 4cb124b96637b9fcdca15595faebb2ce4d304de0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460545"
---
# <a name="getrooms-operation"></a><span data-ttu-id="5693b-103">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="5693b-103">GetRooms operation</span></span>

<span data-ttu-id="5693b-104">**GetRooms**操作获取指定会议室列表中的会议室。</span><span class="sxs-lookup"><span data-stu-id="5693b-104">The **GetRooms** operation gets the rooms within the specified room list.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="5693b-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="5693b-105">SOAP Headers</span></span>

<span data-ttu-id="5693b-106">**GetRooms**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="5693b-106">The **GetRooms** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="5693b-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="5693b-107">**Header**</span></span>|<span data-ttu-id="5693b-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="5693b-108">**Element**</span></span>|<span data-ttu-id="5693b-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="5693b-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5693b-110">模拟</span><span class="sxs-lookup"><span data-stu-id="5693b-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="5693b-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="5693b-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="5693b-112">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="5693b-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="5693b-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="5693b-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="5693b-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="5693b-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="5693b-115">标识要用于访问邮箱的 RFC3066 区域性。</span><span class="sxs-lookup"><span data-stu-id="5693b-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="5693b-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="5693b-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="5693b-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="5693b-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="5693b-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="5693b-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="5693b-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="5693b-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="5693b-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5693b-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="5693b-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="5693b-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getrooms-request-example"></a><span data-ttu-id="5693b-122">GetRooms 请求示例</span><span class="sxs-lookup"><span data-stu-id="5693b-122">GetRooms request example</span></span>

### <a name="description"></a><span data-ttu-id="5693b-123">说明</span><span class="sxs-lookup"><span data-stu-id="5693b-123">Description</span></span>

<span data-ttu-id="5693b-124">下面是一个**GetRooms**请求的示例，该请求获取与会议室列表相关联的会议室。</span><span class="sxs-lookup"><span data-stu-id="5693b-124">The following is an example of a **GetRooms** request that gets the rooms that are associated with a room list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5693b-125">代码</span><span class="sxs-lookup"><span data-stu-id="5693b-125">Code</span></span>

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
    <m:GetRooms>
      <m:RoomList>
        <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
      </m:RoomList>
    </m:GetRooms>
  </soap:Body>

```

### <a name="request-elements"></a><span data-ttu-id="5693b-126">Request 元素</span><span class="sxs-lookup"><span data-stu-id="5693b-126">Request elements</span></span>

<span data-ttu-id="5693b-127">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5693b-127">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="5693b-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="5693b-128">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="5693b-129">GetRooms</span><span class="sxs-lookup"><span data-stu-id="5693b-129">GetRooms</span></span>](getrooms.md)
    
- [<span data-ttu-id="5693b-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="5693b-130">RoomList</span></span>](roomlist.md)
    
- [<span data-ttu-id="5693b-131">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="5693b-131">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-getrooms-response-example"></a><span data-ttu-id="5693b-132">成功的 GetRooms 响应示例</span><span class="sxs-lookup"><span data-stu-id="5693b-132">Successful GetRooms response example</span></span>

### <a name="description"></a><span data-ttu-id="5693b-133">说明</span><span class="sxs-lookup"><span data-stu-id="5693b-133">Description</span></span>

<span data-ttu-id="5693b-134">以下响应显示与会议室列表关联的聊天室的电子邮件地址信息。</span><span class="sxs-lookup"><span data-stu-id="5693b-134">The following response shows the email address information for the rooms that are associated with the room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="5693b-135">代码</span><span class="sxs-lookup"><span data-stu-id="5693b-135">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:Rooms xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Room xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:Id>
            <t:Name>Room01</t:Name>
            <t:EmailAddress>Room01@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="successful-getrooms-response-elements"></a><span data-ttu-id="5693b-136">成功的 GetRooms 响应元素</span><span class="sxs-lookup"><span data-stu-id="5693b-136">Successful GetRooms response elements</span></span>

<span data-ttu-id="5693b-137">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5693b-137">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5693b-138">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5693b-138">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5693b-139">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="5693b-139">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="5693b-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5693b-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5693b-141">所属</span><span class="sxs-lookup"><span data-stu-id="5693b-141">Rooms</span></span>](rooms.md)
    
- [<span data-ttu-id="5693b-142">房间</span><span class="sxs-lookup"><span data-stu-id="5693b-142">Room</span></span>](room.md)
    
- [<span data-ttu-id="5693b-143">名称（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="5693b-143">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="5693b-144">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="5693b-144">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="5693b-145">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="5693b-145">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="5693b-146">MailboxType</span><span class="sxs-lookup"><span data-stu-id="5693b-146">MailboxType</span></span>](mailboxtype.md)
    
## <a name="getrooms-error-response-example"></a><span data-ttu-id="5693b-147">GetRooms 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="5693b-147">GetRooms Error response example</span></span>

### <a name="description"></a><span data-ttu-id="5693b-148">说明</span><span class="sxs-lookup"><span data-stu-id="5693b-148">Description</span></span>

<span data-ttu-id="5693b-149">下面的示例演示由于尝试获取不存在的会议室列表的会议室信息而导致的错误响应。</span><span class="sxs-lookup"><span data-stu-id="5693b-149">The following example shows an error response caused by an attempt to get room information for a nonexistent room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="5693b-150">代码</span><span class="sxs-lookup"><span data-stu-id="5693b-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Error" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>No results were found.</MessageText>
      <ResponseCode>ErrorNameResolutionNoResults</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRoomsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="getrooms-error-response-elements"></a><span data-ttu-id="5693b-151">GetRooms 错误响应元素</span><span class="sxs-lookup"><span data-stu-id="5693b-151">GetRooms Error response elements</span></span>

<span data-ttu-id="5693b-152">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5693b-152">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5693b-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5693b-153">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5693b-154">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="5693b-154">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="5693b-155">MessageText</span><span class="sxs-lookup"><span data-stu-id="5693b-155">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5693b-156">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5693b-156">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5693b-157">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5693b-157">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="5693b-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5693b-158">See also</span></span>

- [<span data-ttu-id="5693b-159">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="5693b-159">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="5693b-160">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5693b-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

