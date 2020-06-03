---
title: SendItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: 337b89ef-e1b7-45ed-92f3-8abe4200e4c7
description: SendItem 操作用于发送位于 Exchange 存储中的电子邮件。
ms.openlocfilehash: 9136379e50723211fe5a483c7f113da4fa125fc1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530336"
---
# <a name="senditem-operation"></a><span data-ttu-id="00ecc-103">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="00ecc-103">SendItem operation</span></span>

<span data-ttu-id="00ecc-104">SendItem 操作用于发送位于 Exchange 存储中的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="00ecc-104">The SendItem operation is used to send e-mail messages that are located in the Exchange store.</span></span>
  
## <a name="senditem-e-mail-message-request-example"></a><span data-ttu-id="00ecc-105">SendItem （电子邮件）请求示例</span><span class="sxs-lookup"><span data-stu-id="00ecc-105">SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="00ecc-106">Description</span><span class="sxs-lookup"><span data-stu-id="00ecc-106">Description</span></span>

<span data-ttu-id="00ecc-107">下面的示例演示如何发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="00ecc-107">The following example shows how to send an e-mail message.</span></span>
  
### <a name="code"></a><span data-ttu-id="00ecc-108">代码</span><span class="sxs-lookup"><span data-stu-id="00ecc-108">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="CQAAABY+T" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="00ecc-109">备注</span><span class="sxs-lookup"><span data-stu-id="00ecc-109">Comments</span></span>

<span data-ttu-id="00ecc-110">项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="00ecc-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="00ecc-111">Request 元素</span><span class="sxs-lookup"><span data-stu-id="00ecc-111">Request elements</span></span>

<span data-ttu-id="00ecc-112">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="00ecc-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="00ecc-113">SendItem</span><span class="sxs-lookup"><span data-stu-id="00ecc-113">SendItem</span></span>](senditem.md)
    
- [<span data-ttu-id="00ecc-114">ItemIds</span><span class="sxs-lookup"><span data-stu-id="00ecc-114">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="00ecc-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="00ecc-115">ItemId</span></span>](itemid.md)
    
## <a name="successful-senditem-e-mail-message-response"></a><span data-ttu-id="00ecc-116">成功的 SendItem （电子邮件）响应</span><span class="sxs-lookup"><span data-stu-id="00ecc-116">Successful SendItem (E-mail Message) Response</span></span>

### <a name="description"></a><span data-ttu-id="00ecc-117">Description</span><span class="sxs-lookup"><span data-stu-id="00ecc-117">Description</span></span>

<span data-ttu-id="00ecc-118">下面的示例展示了一个成功的 SendItem 响应。</span><span class="sxs-lookup"><span data-stu-id="00ecc-118">The following example shows a successful SendItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="00ecc-119">代码</span><span class="sxs-lookup"><span data-stu-id="00ecc-119">Code</span></span>

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
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="00ecc-120">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="00ecc-120">Successful response elements</span></span>

<span data-ttu-id="00ecc-121">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="00ecc-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="00ecc-122">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="00ecc-122">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="00ecc-123">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="00ecc-123">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="00ecc-124">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="00ecc-124">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="00ecc-125">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="00ecc-125">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="00ecc-126">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="00ecc-126">ResponseCode</span></span>](responsecode.md)
    
### <a name="comments"></a><span data-ttu-id="00ecc-127">备注</span><span class="sxs-lookup"><span data-stu-id="00ecc-127">Comments</span></span>

<span data-ttu-id="00ecc-128">尝试发送位于主体的 "草稿" 文件夹中且设置为 "已发送邮件可分辨" 文件夹中的电子邮件的代理将以无提示方式将已发送项目的副本移动到 "已发送邮件" 可分辨文件夹中。</span><span class="sxs-lookup"><span data-stu-id="00ecc-128">A delegate who tries to send an e-mail message that is located in the principal's Drafts folder with the SendAndSaveCopy option set to save a copy in the Sent Items distinguished folder will silently fail to move a copy of the sent item to the Sent Items distinguished folder.</span></span> <span data-ttu-id="00ecc-129">项目将保留在主体的 "草稿" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="00ecc-129">The item will remain in the principal's Drafts folder.</span></span> <span data-ttu-id="00ecc-130">此问题的解决方法是在[DistinguishedFolderId](distinguishedfolderid.md)元素中指定主体的邮箱。</span><span class="sxs-lookup"><span data-stu-id="00ecc-130">The workaround for this issue is to specify the principal's mailbox in the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="00ecc-131">另一个需要考虑的方案是，当代理创建一封电子邮件并将其保存到代理邮箱的 "草稿" 文件夹中时。</span><span class="sxs-lookup"><span data-stu-id="00ecc-131">An additional scenario to consider is when a delegate creates an e-mail message and saves it to the Drafts folder of the delegate's mailbox.</span></span> <span data-ttu-id="00ecc-132">如果代理尝试发送项目并将副本保存到主体的 "已发送邮件" 可分辨文件夹中，则邮件将被正确发送，草稿邮件仍保留在代理的 "草稿" 文件夹中，已发送的邮件不会显示在代理或主体的 "已发送邮件" 文件夹中，并且响应是成功的。</span><span class="sxs-lookup"><span data-stu-id="00ecc-132">If the delegate tries to send the item and save a copy to the principal's Sent Items distinguished folder, the message is sent correctly, the draft message remains in the delegate's Drafts folder, the sent message does not appear in either the delegate's or principal's Sent Items folder, and the response is a success.</span></span>
  
## <a name="invalid-senditem-e-mail-message-request-example"></a><span data-ttu-id="00ecc-133">无效的 SendItem （电子邮件）请求示例</span><span class="sxs-lookup"><span data-stu-id="00ecc-133">Invalid SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="00ecc-134">Description</span><span class="sxs-lookup"><span data-stu-id="00ecc-134">Description</span></span>

<span data-ttu-id="00ecc-135">以下代码示例显示了带有无效标识符的请求示例。</span><span class="sxs-lookup"><span data-stu-id="00ecc-135">The following code sample shows an example of a request with an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="00ecc-136">代码</span><span class="sxs-lookup"><span data-stu-id="00ecc-136">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="%BadItemId%" ChangeKey="CQAAABYAAA" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="senditem-e-mail-message-error-response"></a><span data-ttu-id="00ecc-137">SendItem （电子邮件）错误响应</span><span class="sxs-lookup"><span data-stu-id="00ecc-137">SendItem (E-mail Message) error response</span></span>

### <a name="description"></a><span data-ttu-id="00ecc-138">Description</span><span class="sxs-lookup"><span data-stu-id="00ecc-138">Description</span></span>

<span data-ttu-id="00ecc-139">下面的示例演示对包含无效标识符的 SendItem 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="00ecc-139">The following example shows an error response to a SendItem request that contains an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="00ecc-140">代码</span><span class="sxs-lookup"><span data-stu-id="00ecc-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="00ecc-141">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="00ecc-141">Error response elements</span></span>

<span data-ttu-id="00ecc-142">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="00ecc-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="00ecc-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="00ecc-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="00ecc-144">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="00ecc-144">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="00ecc-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="00ecc-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="00ecc-146">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="00ecc-146">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="00ecc-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="00ecc-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="00ecc-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="00ecc-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="00ecc-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="00ecc-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="00ecc-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="00ecc-150">See also</span></span>



[<span data-ttu-id="00ecc-151">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="00ecc-151">SendItem operation</span></span>](senditem-operation.md)
  
 <span data-ttu-id="00ecc-152">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="00ecc-152">**SendItemType**</span></span>


- [<span data-ttu-id="00ecc-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="00ecc-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

