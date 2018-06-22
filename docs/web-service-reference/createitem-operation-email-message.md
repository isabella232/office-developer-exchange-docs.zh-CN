---
title: CreateItem operation，（电子邮件）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1
description: CreateItem operation，用于创建电子邮件。
ms.openlocfilehash: 591209165cfbafc2d5f4036dd8fab6659523a044
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753661"
---
# <a name="createitem-operation-email-message"></a><span data-ttu-id="52efa-103">CreateItem operation，（电子邮件）</span><span class="sxs-lookup"><span data-stu-id="52efa-103">CreateItem operation (email message)</span></span>

<span data-ttu-id="52efa-104">CreateItem operation，用于创建电子邮件。</span><span class="sxs-lookup"><span data-stu-id="52efa-104">The CreateItem operation is used to create e-mail messages.</span></span>
  
## <a name="createitem-request-example"></a><span data-ttu-id="52efa-105">CreateItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="52efa-105">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="52efa-106">说明</span><span class="sxs-lookup"><span data-stu-id="52efa-106">Description</span></span>

<span data-ttu-id="52efa-107">CreateItem 请求的下面的示例演示如何创建新的电子邮件、 发送该邮件，并将它的一个副本保存在草稿文件夹。</span><span class="sxs-lookup"><span data-stu-id="52efa-107">The following example of a CreateItem request shows how to create a new e-mail message, send the message, and save a copy of it in the drafts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="52efa-108">代码</span><span class="sxs-lookup"><span data-stu-id="52efa-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem MessageDisposition="SendAndSaveCopy" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </SavedItemFolderId>
      <Items>
        <t:Message>
          <t:ItemClass>IPM.Note</t:ItemClass>
          <t:Subject>Project Action</t:Subject>
          <t:Body BodyType="Text">Priority - Update specification</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sschmidt@example.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
          <t:IsRead>false</t:IsRead>
        </t:Message>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="52efa-109">请求元素</span><span class="sxs-lookup"><span data-stu-id="52efa-109">Request elements</span></span>

<span data-ttu-id="52efa-110">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="52efa-110">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="52efa-111">CreateItem</span><span class="sxs-lookup"><span data-stu-id="52efa-111">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="52efa-112">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="52efa-112">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="52efa-113">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="52efa-113">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="52efa-114">Message</span><span class="sxs-lookup"><span data-stu-id="52efa-114">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="52efa-115">ItemClass</span><span class="sxs-lookup"><span data-stu-id="52efa-115">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="52efa-116">Subject</span><span class="sxs-lookup"><span data-stu-id="52efa-116">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="52efa-117">Body</span><span class="sxs-lookup"><span data-stu-id="52efa-117">Body</span></span>](body.md)
    
- [<span data-ttu-id="52efa-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="52efa-118">ToRecipients</span></span>](torecipients.md)
    
- [<span data-ttu-id="52efa-119">Mailbox</span><span class="sxs-lookup"><span data-stu-id="52efa-119">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="52efa-120">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="52efa-120">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="52efa-121">IsRead</span><span class="sxs-lookup"><span data-stu-id="52efa-121">IsRead</span></span>](isread.md)
    
<span data-ttu-id="52efa-122">若要查找的请求邮件 CreateItem 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="52efa-122">To find other options for the request message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="52efa-123">启动[CreateItem](createitem.md)元素。</span><span class="sxs-lookup"><span data-stu-id="52efa-123">Start at the [CreateItem](createitem.md) element.</span></span> 
  
## <a name="successful-createitem-response"></a><span data-ttu-id="52efa-124">成功的 CreateItem 响应</span><span class="sxs-lookup"><span data-stu-id="52efa-124">Successful CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="52efa-125">说明</span><span class="sxs-lookup"><span data-stu-id="52efa-125">Description</span></span>

<span data-ttu-id="52efa-126">下面的示例演示对 CreateItem 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="52efa-126">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="52efa-127">代码</span><span class="sxs-lookup"><span data-stu-id="52efa-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="52efa-128">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="52efa-128">Successful response elements</span></span>

<span data-ttu-id="52efa-129">在响应中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="52efa-129">The following elements are included in the response:</span></span> 
  
- [<span data-ttu-id="52efa-130">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="52efa-130">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="52efa-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="52efa-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="52efa-132">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="52efa-132">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="52efa-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="52efa-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="52efa-134">Items</span><span class="sxs-lookup"><span data-stu-id="52efa-134">Items</span></span>](items.md)
    
<span data-ttu-id="52efa-135">若要查找的响应消息 CreateItem 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="52efa-135">To find other options for the response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="52efa-136">启动[CreateItemResponse](createitemresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="52efa-136">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="error-createitem-response"></a><span data-ttu-id="52efa-137">错误 CreateItem 响应</span><span class="sxs-lookup"><span data-stu-id="52efa-137">Error CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="52efa-138">说明</span><span class="sxs-lookup"><span data-stu-id="52efa-138">Description</span></span>

<span data-ttu-id="52efa-139">下面的示例演示对 CreateItem 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="52efa-139">The following example shows an error response to a CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="52efa-140">代码</span><span class="sxs-lookup"><span data-stu-id="52efa-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>The user account which was used to submit this request does not have the right to send mail on behalf of the specified sending account.</m:MessageText>
          <m:ResponseCode>ErrorSendAsDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="52efa-141">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="52efa-141">Error response elements</span></span>

<span data-ttu-id="52efa-142">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="52efa-142">The following elements are used in the error response:</span></span> 
  
- [<span data-ttu-id="52efa-143">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="52efa-143">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="52efa-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="52efa-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="52efa-145">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="52efa-145">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="52efa-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="52efa-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="52efa-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="52efa-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="52efa-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="52efa-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="52efa-149">Items</span><span class="sxs-lookup"><span data-stu-id="52efa-149">Items</span></span>](items.md)
    
<span data-ttu-id="52efa-150">若要查找错误响应消息的 CreateItem 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="52efa-150">To find other options for the error response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="52efa-151">启动[CreateItemResponse](createitemresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="52efa-151">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52efa-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52efa-152">See also</span></span>



[<span data-ttu-id="52efa-153">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="52efa-153">CreateItem operation</span></span>](createitem-operation.md)

