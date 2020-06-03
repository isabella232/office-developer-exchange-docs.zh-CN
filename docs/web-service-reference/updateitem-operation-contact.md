---
title: UpdateItem 操作（联系人）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 298fdd71-a83d-4407-9728-4f0a8e2d857c
description: UpdateItem 操作用于更新 Exchange 存储中的联系人项目属性。
ms.openlocfilehash: 66e1b91ea3154d8a501339aed7b398970e8f5392
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459824"
---
# <a name="updateitem-operation-contact"></a><span data-ttu-id="0be7e-103">UpdateItem 操作（联系人）</span><span class="sxs-lookup"><span data-stu-id="0be7e-103">UpdateItem operation (contact)</span></span>

<span data-ttu-id="0be7e-104">UpdateItem 操作用于更新 Exchange 存储中的联系人项目属性。</span><span class="sxs-lookup"><span data-stu-id="0be7e-104">The UpdateItem operation is used to update contact item properties in the Exchange store.</span></span>
  
## <a name="updateitem-contact-request-example"></a><span data-ttu-id="0be7e-105">UpdateItem （Contact）请求示例</span><span class="sxs-lookup"><span data-stu-id="0be7e-105">UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="0be7e-106">Description</span><span class="sxs-lookup"><span data-stu-id="0be7e-106">Description</span></span>

<span data-ttu-id="0be7e-107">下面的代码示例演示如何更新联系人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="0be7e-107">The following code example shows how to update the e-mail address of a contact.</span></span>
  
### <a name="code"></a><span data-ttu-id="0be7e-108">代码</span><span class="sxs-lookup"><span data-stu-id="0be7e-108">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                ConflictResolution="AlwaysOverwrite">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAA=" ChangeKey="EQAAABYi" />
          <t:Updates>
            <t:SetItemField>
              <t:IndexedFieldURI FieldURI="contacts:EmailAddress" FieldIndex="EmailAddress1"/>
              <t:Contact>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">changedemail@example.com</t:Entry>
                </t:EmailAddresses>
              </t:Contact>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0be7e-109">备注</span><span class="sxs-lookup"><span data-stu-id="0be7e-109">Comments</span></span>

<span data-ttu-id="0be7e-110">项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="0be7e-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="0be7e-111">Request 元素</span><span class="sxs-lookup"><span data-stu-id="0be7e-111">Request elements</span></span>

<span data-ttu-id="0be7e-112">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0be7e-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0be7e-113">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="0be7e-113">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="0be7e-114">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="0be7e-114">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="0be7e-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="0be7e-115">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="0be7e-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="0be7e-116">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="0be7e-117">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="0be7e-117">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="0be7e-118">SetItemField</span><span class="sxs-lookup"><span data-stu-id="0be7e-118">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="0be7e-119">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="0be7e-119">IndexedFieldURI</span></span>](indexedfielduri.md)
    
- [<span data-ttu-id="0be7e-120">联系人</span><span class="sxs-lookup"><span data-stu-id="0be7e-120">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="0be7e-121">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="0be7e-121">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="0be7e-122">条目（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="0be7e-122">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
## <a name="successful-updateitem-contact-response"></a><span data-ttu-id="0be7e-123">成功的 UpdateItem （联系人）响应</span><span class="sxs-lookup"><span data-stu-id="0be7e-123">Successful UpdateItem (Contact) Response</span></span>

### <a name="description"></a><span data-ttu-id="0be7e-124">Description</span><span class="sxs-lookup"><span data-stu-id="0be7e-124">Description</span></span>

<span data-ttu-id="0be7e-125">下面的代码示例演示一个成功的 UpdateItem 响应。</span><span class="sxs-lookup"><span data-stu-id="0be7e-125">The following code example shows a successful UpdateItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="0be7e-126">代码</span><span class="sxs-lookup"><span data-stu-id="0be7e-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAtAE=" ChangeKey="EQAAABYx" />
            </t:Contact>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0be7e-127">备注</span><span class="sxs-lookup"><span data-stu-id="0be7e-127">Comments</span></span>

<span data-ttu-id="0be7e-128">项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="0be7e-128">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="0be7e-129">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="0be7e-129">Successful response elements</span></span>

<span data-ttu-id="0be7e-130">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0be7e-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0be7e-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0be7e-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0be7e-132">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="0be7e-132">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="0be7e-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0be7e-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0be7e-134">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0be7e-134">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="0be7e-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0be7e-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0be7e-136">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="0be7e-136">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="0be7e-137">联系人</span><span class="sxs-lookup"><span data-stu-id="0be7e-137">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="0be7e-138">ItemId</span><span class="sxs-lookup"><span data-stu-id="0be7e-138">ItemId</span></span>](itemid.md)
    
## <a name="invalid-updateitem-contact-request-example"></a><span data-ttu-id="0be7e-139">无效的 UpdateItem （Contact）请求示例</span><span class="sxs-lookup"><span data-stu-id="0be7e-139">Invalid UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="0be7e-140">Description</span><span class="sxs-lookup"><span data-stu-id="0be7e-140">Description</span></span>

<span data-ttu-id="0be7e-141">下面的代码示例演示一个无效请求。</span><span class="sxs-lookup"><span data-stu-id="0be7e-141">The following code example shows an invalid request.</span></span>
  
### <a name="code"></a><span data-ttu-id="0be7e-142">代码</span><span class="sxs-lookup"><span data-stu-id="0be7e-142">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                ConflictResolution="AlwaysOverwrite">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEF=" ChangeKey="EQAAABYi" />
          <t:Updates>
            <t:SetItemField>
              <t:IndexedFieldURI FieldURI="contacts:EmailAddress" FieldIndex="EmailAddress4"/>
              <t:Contact>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress4">changedemail2@example.com</t:Entry>
                </t:EmailAddresses>
              </t:Contact>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0be7e-143">备注</span><span class="sxs-lookup"><span data-stu-id="0be7e-143">Comments</span></span>

<span data-ttu-id="0be7e-144">项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="0be7e-144">The item identifier has been shortened to preserve readability.</span></span>
  
## <a name="updateitem-contact-error-response"></a><span data-ttu-id="0be7e-145">UpdateItem （联系人）错误响应</span><span class="sxs-lookup"><span data-stu-id="0be7e-145">UpdateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="0be7e-146">Description</span><span class="sxs-lookup"><span data-stu-id="0be7e-146">Description</span></span>

<span data-ttu-id="0be7e-147">下面的代码示例演示对 UpdateItem （联系人）请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="0be7e-147">The following code example shows an error response to an UpdateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="0be7e-148">代码</span><span class="sxs-lookup"><span data-stu-id="0be7e-148">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <soap:faultcode>Client</soap:faultcode>
      <soap:faultstring>The request failed schema validation.</soap:faultstring>
      <detail>
        <e:ResponseCode xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">The 'Key' attribute is invalid - The value 'EmailAddress4' is invalid according to its data type 'https://schemas.microsoft.com/exchange/services/2006/types:EmailAddressKeyType' - The Enumeration constraint failed.</e:Message>
        <e:Line xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">17</e:Line>
        <e:Position xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">19</e:Position>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0be7e-149">备注</span><span class="sxs-lookup"><span data-stu-id="0be7e-149">Comments</span></span>

<span data-ttu-id="0be7e-150">在架构验证错误所导致的错误响应的 SOAP 正文中使用的一些元素不在消息或类型架构中定义。</span><span class="sxs-lookup"><span data-stu-id="0be7e-150">Some elements that are used in the SOAP body of an error response that is caused by a schema validation error are not defined in the messages or types schemas.</span></span> <span data-ttu-id="0be7e-151">**Detail**元素包含有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="0be7e-151">The **detail** element contains information about the error.</span></span> <span data-ttu-id="0be7e-152">[ResponseCode](responsecode.md)元素包含错误代码。</span><span class="sxs-lookup"><span data-stu-id="0be7e-152">The [ResponseCode](responsecode.md) element contains the error code.</span></span> <span data-ttu-id="0be7e-153">[Message](message-ex15websvcsotherref.md)元素包含有关错误的说明（如果有的话）。</span><span class="sxs-lookup"><span data-stu-id="0be7e-153">The [Message](message-ex15websvcsotherref.md) element contains an explanation for the error, if one is available.</span></span> <span data-ttu-id="0be7e-154">**Line**元素描述发生架构验证错误的行号。</span><span class="sxs-lookup"><span data-stu-id="0be7e-154">The **Line** element describes the line number where the schema validation error occurred.</span></span> <span data-ttu-id="0be7e-155">**Position**元素描述从 XML 文档的最左侧字符到的位置。</span><span class="sxs-lookup"><span data-stu-id="0be7e-155">The **Position** element describes the position from the leftmost character of the XML document.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0be7e-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0be7e-156">See also</span></span>



[<span data-ttu-id="0be7e-157">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="0be7e-157">UpdateItem operation</span></span>](updateitem-operation.md)

