---
title: GetItem 操作（电子邮件）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetItem
api_type:
- schema
ms.assetid: e8492e3b-1c8d-4b14-8070-9530f8306edd
description: GetItem 操作允许用户访问有关电子邮件的信息。
localization_priority: Priority
ms.openlocfilehash: f8be01cad3d4c4534f66593cbe8bcee477726972
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459992"
---
# <a name="getitem-operation-email-message"></a><span data-ttu-id="7ddc3-103">GetItem 操作（电子邮件）</span><span class="sxs-lookup"><span data-stu-id="7ddc3-103">GetItem operation (email message)</span></span>

<span data-ttu-id="7ddc3-104">GetItem 操作允许用户访问有关电子邮件的信息。</span><span class="sxs-lookup"><span data-stu-id="7ddc3-104">The GetItem operation allows the user to access information about e-mail messages.</span></span>
  
## <a name="using-the-getitem-operation-for-messages"></a><span data-ttu-id="7ddc3-105">对邮件使用 GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="7ddc3-105">Using the GetItem Operation for Messages</span></span>

<span data-ttu-id="7ddc3-106">GetItem 请求必须包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="7ddc3-106">The GetItem request must have the following information:</span></span>
  
- <span data-ttu-id="7ddc3-107">用于标识要返回的项信息的[ItemId](itemid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="7ddc3-107">The [ItemId](itemid.md) element to identify the item information to return.</span></span> 
    
- <span data-ttu-id="7ddc3-108">用于标识要返回的项属性的[ItemShape](itemshape.md)元素。</span><span class="sxs-lookup"><span data-stu-id="7ddc3-108">The [ItemShape](itemshape.md) element to identify the item properties to return.</span></span> 
    
## <a name="getitem-request-example"></a><span data-ttu-id="7ddc3-109">GetItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="7ddc3-109">GetItem request example</span></span>

### <a name="description"></a><span data-ttu-id="7ddc3-110">Description</span><span class="sxs-lookup"><span data-stu-id="7ddc3-110">Description</span></span>

<span data-ttu-id="7ddc3-111">以下示例的 GetItem 请求显示了如何访问有关电子邮件的信息。</span><span class="sxs-lookup"><span data-stu-id="7ddc3-111">The following example of a GetItem request shows how to access information about e-mail messages.</span></span>
  
### <a name="code"></a><span data-ttu-id="7ddc3-112">代码</span><span class="sxs-lookup"><span data-stu-id="7ddc3-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xmlns:xsd="http://www.w3.org/2001/XMLSchema"
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem
      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>Default</t:BaseShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAlAF" ChangeKey="CQAAAB" />
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="7ddc3-113">Request 元素</span><span class="sxs-lookup"><span data-stu-id="7ddc3-113">Request elements</span></span>

<span data-ttu-id="7ddc3-114">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="7ddc3-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="7ddc3-115">GetItem</span><span class="sxs-lookup"><span data-stu-id="7ddc3-115">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="7ddc3-116">ItemShape</span><span class="sxs-lookup"><span data-stu-id="7ddc3-116">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="7ddc3-117">BaseShape</span><span class="sxs-lookup"><span data-stu-id="7ddc3-117">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="7ddc3-118">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="7ddc3-118">IncludeMimeContent</span></span>](includemimecontent.md)
    
- [<span data-ttu-id="7ddc3-119">ItemIds</span><span class="sxs-lookup"><span data-stu-id="7ddc3-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="7ddc3-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="7ddc3-120">ItemId</span></span>](itemid.md)
    
## <a name="successful-getitem-e-mail-message-response-example"></a><span data-ttu-id="7ddc3-121">成功的 GetItem （电子邮件）响应示例</span><span class="sxs-lookup"><span data-stu-id="7ddc3-121">Successful GetItem (E-mail Message) response example</span></span>

### <a name="description"></a><span data-ttu-id="7ddc3-122">Description</span><span class="sxs-lookup"><span data-stu-id="7ddc3-122">Description</span></span>

<span data-ttu-id="7ddc3-123">下面的示例演示对 GetItem 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="7ddc3-123">The following example shows a successful response to the GetItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="7ddc3-124">代码</span><span class="sxs-lookup"><span data-stu-id="7ddc3-124">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:MimeContent CharacterSet="UTF-8">UmVjZWl</t:MimeContent>
              <t:ItemId Id="AAAlAFVz" ChangeKey="CQAAAB" />
              <t:Subject />
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="HTML">
                <html dir="ltr">
                  <head>
                    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
                      <meta content="MSHTML 6.00.3790.2759" name="GENERATOR">
                        <style title="owaParaStyle">P { MARGIN-TOP: 0px; MARGIN-BOTTOM: 0px } </style>
                      </head>
                  <body ocsi="x">
                    <div dir="ltr">
                      <font face="Tahoma" color="#000000" size="2"></font>&amp;nbsp;
                    </div>
                  </body>
                </html>
              </t:Body>
              <t:Size>881</t:Size>
              <t:DateTimeSent>2006-10-28T01:37:06Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-10-28T01:37:06Z</t:DateTimeCreated>
              <t:ResponseObjects>
                <t:ReplyToItem />
                <t:ReplyAllToItem />
                <t:ForwardItem />
              </t:ResponseObjects>
              <t:HasAttachments>false</t:HasAttachments>
              <t:ToRecipients>
                <t:Mailbox>
                  <t:Name>User1</t:Name>
                  <t:EmailAddress>User1@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:ToRecipients>
              <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
              <t:IsDeliveryReceiptRequested>false</t:IsDeliveryReceiptRequested>
              <t:From>
                <t:Mailbox>
                  <t:Name>User2</t:Name>
                  <t:EmailAddress>User2@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:From>
              <t:IsRead>false</t:IsRead>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="7ddc3-125">备注</span><span class="sxs-lookup"><span data-stu-id="7ddc3-125">Comments</span></span>

<span data-ttu-id="7ddc3-126">MIME 内容、文件夹和项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="7ddc3-126">The MIME content, folder, and item identifiers have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="7ddc3-127">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="7ddc3-127">Successful response elements</span></span>

<span data-ttu-id="7ddc3-128">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="7ddc3-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="7ddc3-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7ddc3-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7ddc3-130">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="7ddc3-130">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="7ddc3-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7ddc3-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7ddc3-132">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7ddc3-132">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="7ddc3-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7ddc3-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7ddc3-134">Items</span><span class="sxs-lookup"><span data-stu-id="7ddc3-134">Items</span></span>](items.md)
    
- [<span data-ttu-id="7ddc3-135">消息</span><span class="sxs-lookup"><span data-stu-id="7ddc3-135">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="7ddc3-136">MimeContent</span><span class="sxs-lookup"><span data-stu-id="7ddc3-136">MimeContent</span></span>](mimecontent.md)
    
- [<span data-ttu-id="7ddc3-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="7ddc3-137">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="7ddc3-138">主题</span><span class="sxs-lookup"><span data-stu-id="7ddc3-138">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="7ddc3-139">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="7ddc3-139">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="7ddc3-140">Body</span><span class="sxs-lookup"><span data-stu-id="7ddc3-140">Body</span></span>](body.md)
    
- [<span data-ttu-id="7ddc3-141">大小</span><span class="sxs-lookup"><span data-stu-id="7ddc3-141">Size</span></span>](size.md)
    
- [<span data-ttu-id="7ddc3-142">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="7ddc3-142">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="7ddc3-143">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="7ddc3-143">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="7ddc3-144">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="7ddc3-144">ResponseObjects</span></span>](responseobjects.md)
    
- [<span data-ttu-id="7ddc3-145">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="7ddc3-145">ReplyToItem</span></span>](replytoitem.md)
    
- [<span data-ttu-id="7ddc3-146">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="7ddc3-146">ReplyAllToItem</span></span>](replyalltoitem.md)
    
- [<span data-ttu-id="7ddc3-147">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="7ddc3-147">ForwardItem</span></span>](forwarditem.md)
    
- [<span data-ttu-id="7ddc3-148">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="7ddc3-148">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="7ddc3-149">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="7ddc3-149">ToRecipients</span></span>](torecipients.md)
    
- [<span data-ttu-id="7ddc3-150">邮箱</span><span class="sxs-lookup"><span data-stu-id="7ddc3-150">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="7ddc3-151">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="7ddc3-151">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="7ddc3-152">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="7ddc3-152">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="7ddc3-153">RoutingType （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="7ddc3-153">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="7ddc3-154">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="7ddc3-154">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md)
    
- [<span data-ttu-id="7ddc3-155">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="7ddc3-155">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md)
    
- [<span data-ttu-id="7ddc3-156">From</span><span class="sxs-lookup"><span data-stu-id="7ddc3-156">From</span></span>](from.md)
    
- [<span data-ttu-id="7ddc3-157">IsRead</span><span class="sxs-lookup"><span data-stu-id="7ddc3-157">IsRead</span></span>](isread.md)
    
## <a name="getitem-e-mail-message-error-response-example"></a><span data-ttu-id="7ddc3-158">GetItem （电子邮件）错误响应示例</span><span class="sxs-lookup"><span data-stu-id="7ddc3-158">GetItem (E-mail Message) Error response example</span></span>

### <a name="description"></a><span data-ttu-id="7ddc3-159">Description</span><span class="sxs-lookup"><span data-stu-id="7ddc3-159">Description</span></span>

<span data-ttu-id="7ddc3-160">下面的示例演示对 GetItem 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="7ddc3-160">The following example shows an error response to a GetItem request.</span></span> <span data-ttu-id="7ddc3-161">错误是由尝试获取无效的附加属性引起的。</span><span class="sxs-lookup"><span data-stu-id="7ddc3-161">The error was caused by an attempt to get an invalid additional property.</span></span>
  
### <a name="code"></a><span data-ttu-id="7ddc3-162">代码</span><span class="sxs-lookup"><span data-stu-id="7ddc3-162">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Error">
          <m:MessageText>Property is not valid for this object type.</m:MessageText>
          <m:ResponseCode>ErrorInvalidPropertyRequest</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:FieldURI FieldURI="meeting:AssociatedCalendarItemId" />
          </m:MessageXml>
          <m:Items />
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="7ddc3-163">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="7ddc3-163">Error response elements</span></span>

<span data-ttu-id="7ddc3-164">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="7ddc3-164">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="7ddc3-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7ddc3-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7ddc3-166">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="7ddc3-166">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="7ddc3-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7ddc3-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7ddc3-168">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7ddc3-168">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="7ddc3-169">MessageText</span><span class="sxs-lookup"><span data-stu-id="7ddc3-169">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="7ddc3-170">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7ddc3-170">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7ddc3-171">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7ddc3-171">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="7ddc3-172">MessageXml</span><span class="sxs-lookup"><span data-stu-id="7ddc3-172">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="7ddc3-173">FieldURI</span><span class="sxs-lookup"><span data-stu-id="7ddc3-173">FieldURI</span></span>](fielduri.md)
    
## <a name="see-also"></a><span data-ttu-id="7ddc3-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ddc3-174">See also</span></span>



[<span data-ttu-id="7ddc3-175">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="7ddc3-175">GetItem operation</span></span>](getitem-operation.md)

