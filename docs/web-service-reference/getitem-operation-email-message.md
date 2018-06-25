---
title: GetItem 操作 （电子邮件）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: e8492e3b-1c8d-4b14-8070-9530f8306edd
description: GetItem operation，允许用户访问有关电子邮件的信息。
ms.openlocfilehash: 133a893ec7cd0c206d9db573f8b952eb3c2286df
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754601"
---
# <a name="getitem-operation-email-message"></a><span data-ttu-id="0cd44-103">GetItem 操作 （电子邮件）</span><span class="sxs-lookup"><span data-stu-id="0cd44-103">GetItem operation (email message)</span></span>

<span data-ttu-id="0cd44-104">GetItem operation，允许用户访问有关电子邮件的信息。</span><span class="sxs-lookup"><span data-stu-id="0cd44-104">The GetItem operation allows the user to access information about e-mail messages.</span></span>
  
## <a name="using-the-getitem-operation-for-messages"></a><span data-ttu-id="0cd44-105">使用 GetItem 操作的邮件</span><span class="sxs-lookup"><span data-stu-id="0cd44-105">Using the GetItem Operation for Messages</span></span>

<span data-ttu-id="0cd44-106">GetItem 请求必须具有以下信息：</span><span class="sxs-lookup"><span data-stu-id="0cd44-106">The GetItem request must have the following information:</span></span>
  
- <span data-ttu-id="0cd44-107">要确定要返回的项目信息的[ItemId](itemid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="0cd44-107">The [ItemId](itemid.md) element to identify the item information to return.</span></span> 
    
- <span data-ttu-id="0cd44-108">要确定要返回的项目属性的[ItemShape](itemshape.md)元素。</span><span class="sxs-lookup"><span data-stu-id="0cd44-108">The [ItemShape](itemshape.md) element to identify the item properties to return.</span></span> 
    
## <a name="getitem-request-example"></a><span data-ttu-id="0cd44-109">GetItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="0cd44-109">GetItem request example</span></span>

### <a name="description"></a><span data-ttu-id="0cd44-110">说明</span><span class="sxs-lookup"><span data-stu-id="0cd44-110">Description</span></span>

<span data-ttu-id="0cd44-111">GetItem 请求的下面的示例演示如何访问有关电子邮件的信息。</span><span class="sxs-lookup"><span data-stu-id="0cd44-111">The following example of a GetItem request shows how to access information about e-mail messages.</span></span>
  
### <a name="code"></a><span data-ttu-id="0cd44-112">代码</span><span class="sxs-lookup"><span data-stu-id="0cd44-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xmlns:xsd="http://www.w3.org/2001/XMLSchema"
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem
      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="request-elements"></a><span data-ttu-id="0cd44-113">请求元素</span><span class="sxs-lookup"><span data-stu-id="0cd44-113">Request elements</span></span>

<span data-ttu-id="0cd44-114">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0cd44-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0cd44-115">GetItem</span><span class="sxs-lookup"><span data-stu-id="0cd44-115">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="0cd44-116">ItemShape</span><span class="sxs-lookup"><span data-stu-id="0cd44-116">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="0cd44-117">BaseShape</span><span class="sxs-lookup"><span data-stu-id="0cd44-117">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="0cd44-118">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="0cd44-118">IncludeMimeContent</span></span>](includemimecontent.md)
    
- [<span data-ttu-id="0cd44-119">ItemIds</span><span class="sxs-lookup"><span data-stu-id="0cd44-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="0cd44-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="0cd44-120">ItemId</span></span>](itemid.md)
    
## <a name="successful-getitem-e-mail-message-response-example"></a><span data-ttu-id="0cd44-121">成功 GetItem （电子邮件） 响应示例</span><span class="sxs-lookup"><span data-stu-id="0cd44-121">Successful GetItem (E-mail Message) response example</span></span>

### <a name="description"></a><span data-ttu-id="0cd44-122">说明</span><span class="sxs-lookup"><span data-stu-id="0cd44-122">Description</span></span>

<span data-ttu-id="0cd44-123">下面的示例演示对 GetItem 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="0cd44-123">The following example shows a successful response to the GetItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="0cd44-124">代码</span><span class="sxs-lookup"><span data-stu-id="0cd44-124">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="0cd44-125">注释</span><span class="sxs-lookup"><span data-stu-id="0cd44-125">Comments</span></span>

<span data-ttu-id="0cd44-126">MIME 内容、 文件夹和项标识符已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="0cd44-126">The MIME content, folder, and item identifiers have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="0cd44-127">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="0cd44-127">Successful response elements</span></span>

<span data-ttu-id="0cd44-128">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0cd44-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0cd44-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0cd44-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0cd44-130">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="0cd44-130">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="0cd44-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0cd44-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0cd44-132">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0cd44-132">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="0cd44-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0cd44-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0cd44-134">Items</span><span class="sxs-lookup"><span data-stu-id="0cd44-134">Items</span></span>](items.md)
    
- [<span data-ttu-id="0cd44-135">Message</span><span class="sxs-lookup"><span data-stu-id="0cd44-135">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="0cd44-136">MimeContent</span><span class="sxs-lookup"><span data-stu-id="0cd44-136">MimeContent</span></span>](mimecontent.md)
    
- [<span data-ttu-id="0cd44-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="0cd44-137">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="0cd44-138">Subject</span><span class="sxs-lookup"><span data-stu-id="0cd44-138">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="0cd44-139">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="0cd44-139">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="0cd44-140">Body</span><span class="sxs-lookup"><span data-stu-id="0cd44-140">Body</span></span>](body.md)
    
- [<span data-ttu-id="0cd44-141">Size</span><span class="sxs-lookup"><span data-stu-id="0cd44-141">Size</span></span>](size.md)
    
- [<span data-ttu-id="0cd44-142">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="0cd44-142">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="0cd44-143">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="0cd44-143">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="0cd44-144">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="0cd44-144">ResponseObjects</span></span>](responseobjects.md)
    
- [<span data-ttu-id="0cd44-145">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="0cd44-145">ReplyToItem</span></span>](replytoitem.md)
    
- [<span data-ttu-id="0cd44-146">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="0cd44-146">ReplyAllToItem</span></span>](replyalltoitem.md)
    
- [<span data-ttu-id="0cd44-147">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="0cd44-147">ForwardItem</span></span>](forwarditem.md)
    
- [<span data-ttu-id="0cd44-148">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="0cd44-148">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="0cd44-149">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="0cd44-149">ToRecipients</span></span>](torecipients.md)
    
- [<span data-ttu-id="0cd44-150">Mailbox</span><span class="sxs-lookup"><span data-stu-id="0cd44-150">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="0cd44-151">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="0cd44-151">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="0cd44-152">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0cd44-152">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="0cd44-153">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="0cd44-153">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="0cd44-154">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="0cd44-154">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md)
    
- [<span data-ttu-id="0cd44-155">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="0cd44-155">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md)
    
- [<span data-ttu-id="0cd44-156">发件人</span><span class="sxs-lookup"><span data-stu-id="0cd44-156">From</span></span>](from.md)
    
- [<span data-ttu-id="0cd44-157">IsRead</span><span class="sxs-lookup"><span data-stu-id="0cd44-157">IsRead</span></span>](isread.md)
    
## <a name="getitem-e-mail-message-error-response-example"></a><span data-ttu-id="0cd44-158">GetItem （电子邮件） 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="0cd44-158">GetItem (E-mail Message) Error response example</span></span>

### <a name="description"></a><span data-ttu-id="0cd44-159">说明</span><span class="sxs-lookup"><span data-stu-id="0cd44-159">Description</span></span>

<span data-ttu-id="0cd44-160">下面的示例演示对 GetItem 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="0cd44-160">The following example shows an error response to a GetItem request.</span></span> <span data-ttu-id="0cd44-161">尝试获取无效的其他属性由导致错误。</span><span class="sxs-lookup"><span data-stu-id="0cd44-161">The error was caused by an attempt to get an invalid additional property.</span></span>
  
### <a name="code"></a><span data-ttu-id="0cd44-162">代码</span><span class="sxs-lookup"><span data-stu-id="0cd44-162">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="0cd44-163">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="0cd44-163">Error response elements</span></span>

<span data-ttu-id="0cd44-164">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0cd44-164">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="0cd44-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0cd44-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0cd44-166">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="0cd44-166">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="0cd44-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0cd44-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0cd44-168">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0cd44-168">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="0cd44-169">MessageText</span><span class="sxs-lookup"><span data-stu-id="0cd44-169">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0cd44-170">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0cd44-170">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0cd44-171">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0cd44-171">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="0cd44-172">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0cd44-172">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="0cd44-173">FieldURI</span><span class="sxs-lookup"><span data-stu-id="0cd44-173">FieldURI</span></span>](fielduri.md)
    
## <a name="see-also"></a><span data-ttu-id="0cd44-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0cd44-174">See also</span></span>



[<span data-ttu-id="0cd44-175">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="0cd44-175">GetItem operation</span></span>](getitem-operation.md)

