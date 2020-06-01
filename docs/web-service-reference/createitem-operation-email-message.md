---
title: CreateItem 操作（电子邮件）
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
description: CreateItem 操作用于创建电子邮件。
ms.openlocfilehash: 384ed8ff653029c2b7db0b36986d85842b0a06cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457114"
---
# <a name="createitem-operation-email-message"></a><span data-ttu-id="d3ad5-103">CreateItem 操作（电子邮件）</span><span class="sxs-lookup"><span data-stu-id="d3ad5-103">CreateItem operation (email message)</span></span>

<span data-ttu-id="d3ad5-104">CreateItem 操作用于创建电子邮件。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-104">The CreateItem operation is used to create e-mail messages.</span></span>
  
## <a name="createitem-request-example"></a><span data-ttu-id="d3ad5-105">CreateItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="d3ad5-105">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="d3ad5-106">说明</span><span class="sxs-lookup"><span data-stu-id="d3ad5-106">Description</span></span>

<span data-ttu-id="d3ad5-107">下面的 CreateItem 请求示例演示如何创建新的电子邮件，发送邮件，并将其副本保存在 "草稿" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-107">The following example of a CreateItem request shows how to create a new e-mail message, send the message, and save a copy of it in the drafts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="d3ad5-108">代码</span><span class="sxs-lookup"><span data-stu-id="d3ad5-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem MessageDisposition="SendAndSaveCopy" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="request-elements"></a><span data-ttu-id="d3ad5-109">Request 元素</span><span class="sxs-lookup"><span data-stu-id="d3ad5-109">Request elements</span></span>

<span data-ttu-id="d3ad5-110">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="d3ad5-110">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="d3ad5-111">CreateItem</span><span class="sxs-lookup"><span data-stu-id="d3ad5-111">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="d3ad5-112">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="d3ad5-112">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="d3ad5-113">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="d3ad5-113">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="d3ad5-114">邮件</span><span class="sxs-lookup"><span data-stu-id="d3ad5-114">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d3ad5-115">ItemClass</span><span class="sxs-lookup"><span data-stu-id="d3ad5-115">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="d3ad5-116">主题</span><span class="sxs-lookup"><span data-stu-id="d3ad5-116">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="d3ad5-117">Body</span><span class="sxs-lookup"><span data-stu-id="d3ad5-117">Body</span></span>](body.md)
    
- [<span data-ttu-id="d3ad5-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="d3ad5-118">ToRecipients</span></span>](torecipients.md)
    
- [<span data-ttu-id="d3ad5-119">邮箱</span><span class="sxs-lookup"><span data-stu-id="d3ad5-119">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="d3ad5-120">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="d3ad5-120">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="d3ad5-121">IsRead</span><span class="sxs-lookup"><span data-stu-id="d3ad5-121">IsRead</span></span>](isread.md)
    
<span data-ttu-id="d3ad5-122">若要查找 CreateItem 操作的请求消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-122">To find other options for the request message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="d3ad5-123">从[CreateItem](createitem.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-123">Start at the [CreateItem](createitem.md) element.</span></span> 
  
## <a name="successful-createitem-response"></a><span data-ttu-id="d3ad5-124">成功的 CreateItem 响应</span><span class="sxs-lookup"><span data-stu-id="d3ad5-124">Successful CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="d3ad5-125">说明</span><span class="sxs-lookup"><span data-stu-id="d3ad5-125">Description</span></span>

<span data-ttu-id="d3ad5-126">下面的示例演示对 CreateItem 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-126">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="d3ad5-127">代码</span><span class="sxs-lookup"><span data-stu-id="d3ad5-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="d3ad5-128">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="d3ad5-128">Successful response elements</span></span>

<span data-ttu-id="d3ad5-129">响应中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d3ad5-129">The following elements are included in the response:</span></span> 
  
- [<span data-ttu-id="d3ad5-130">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="d3ad5-130">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="d3ad5-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d3ad5-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d3ad5-132">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d3ad5-132">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="d3ad5-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d3ad5-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d3ad5-134">Items</span><span class="sxs-lookup"><span data-stu-id="d3ad5-134">Items</span></span>](items.md)
    
<span data-ttu-id="d3ad5-135">若要查找 CreateItem 操作的响应邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-135">To find other options for the response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="d3ad5-136">从[CreateItemResponse](createitemresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-136">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="error-createitem-response"></a><span data-ttu-id="d3ad5-137">错误 CreateItem 响应</span><span class="sxs-lookup"><span data-stu-id="d3ad5-137">Error CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="d3ad5-138">说明</span><span class="sxs-lookup"><span data-stu-id="d3ad5-138">Description</span></span>

<span data-ttu-id="d3ad5-139">下面的示例演示对 CreateItem 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-139">The following example shows an error response to a CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="d3ad5-140">代码</span><span class="sxs-lookup"><span data-stu-id="d3ad5-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="d3ad5-141">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="d3ad5-141">Error response elements</span></span>

<span data-ttu-id="d3ad5-142">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="d3ad5-142">The following elements are used in the error response:</span></span> 
  
- [<span data-ttu-id="d3ad5-143">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="d3ad5-143">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="d3ad5-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d3ad5-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d3ad5-145">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d3ad5-145">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="d3ad5-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="d3ad5-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d3ad5-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d3ad5-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d3ad5-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d3ad5-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="d3ad5-149">Items</span><span class="sxs-lookup"><span data-stu-id="d3ad5-149">Items</span></span>](items.md)
    
<span data-ttu-id="d3ad5-150">若要查找 CreateItem 操作的错误响应消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-150">To find other options for the error response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="d3ad5-151">从[CreateItemResponse](createitemresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="d3ad5-151">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3ad5-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d3ad5-152">See also</span></span>



[<span data-ttu-id="d3ad5-153">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="d3ad5-153">CreateItem operation</span></span>](createitem-operation.md)

