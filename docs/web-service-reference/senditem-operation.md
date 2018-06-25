---
title: SendItem Operation
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
description: SendItem 操作用于发送电子邮件的位于 Exchange 存储中。
ms.openlocfilehash: 780778b1599d0d5e5f4b6e5b58b67773bbe18cda
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827336"
---
# <a name="senditem-operation"></a><span data-ttu-id="3398e-103">SendItem Operation</span><span class="sxs-lookup"><span data-stu-id="3398e-103">SendItem operation</span></span>

<span data-ttu-id="3398e-104">SendItem 操作用于发送电子邮件的位于 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="3398e-104">The SendItem operation is used to send e-mail messages that are located in the Exchange store.</span></span>
  
## <a name="senditem-e-mail-message-request-example"></a><span data-ttu-id="3398e-105">SendItem （电子邮件） 请求示例</span><span class="sxs-lookup"><span data-stu-id="3398e-105">SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="3398e-106">说明</span><span class="sxs-lookup"><span data-stu-id="3398e-106">Description</span></span>

<span data-ttu-id="3398e-107">下面的示例演示如何发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="3398e-107">The following example shows how to send an e-mail message.</span></span>
  
### <a name="code"></a><span data-ttu-id="3398e-108">代码</span><span class="sxs-lookup"><span data-stu-id="3398e-108">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="CQAAABY+T" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="3398e-109">注释</span><span class="sxs-lookup"><span data-stu-id="3398e-109">Comments</span></span>

<span data-ttu-id="3398e-110">已缩短的项标识符，若要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="3398e-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="3398e-111">请求元素</span><span class="sxs-lookup"><span data-stu-id="3398e-111">Request elements</span></span>

<span data-ttu-id="3398e-112">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="3398e-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="3398e-113">SendItem</span><span class="sxs-lookup"><span data-stu-id="3398e-113">SendItem</span></span>](senditem.md)
    
- [<span data-ttu-id="3398e-114">ItemIds</span><span class="sxs-lookup"><span data-stu-id="3398e-114">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="3398e-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="3398e-115">ItemId</span></span>](itemid.md)
    
## <a name="successful-senditem-e-mail-message-response"></a><span data-ttu-id="3398e-116">成功 SendItem （电子邮件） 响应</span><span class="sxs-lookup"><span data-stu-id="3398e-116">Successful SendItem (E-mail Message) Response</span></span>

### <a name="description"></a><span data-ttu-id="3398e-117">说明</span><span class="sxs-lookup"><span data-stu-id="3398e-117">Description</span></span>

<span data-ttu-id="3398e-118">下面的示例演示了成功的 SendItem 响应。</span><span class="sxs-lookup"><span data-stu-id="3398e-118">The following example shows a successful SendItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="3398e-119">代码</span><span class="sxs-lookup"><span data-stu-id="3398e-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="3398e-120">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="3398e-120">Successful response elements</span></span>

<span data-ttu-id="3398e-121">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="3398e-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="3398e-122">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3398e-122">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3398e-123">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="3398e-123">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="3398e-124">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3398e-124">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="3398e-125">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3398e-125">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="3398e-126">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3398e-126">ResponseCode</span></span>](responsecode.md)
    
### <a name="comments"></a><span data-ttu-id="3398e-127">注释</span><span class="sxs-lookup"><span data-stu-id="3398e-127">Comments</span></span>

<span data-ttu-id="3398e-128">尝试发送电子邮件的主体的草稿文件夹位于 SendAndSaveCopy 选项设置为可分辨的文件夹以无提示方式将无法将发送邮件的副本移至可分辨已发送邮件已发送邮件中保存副本的代理人文件夹。</span><span class="sxs-lookup"><span data-stu-id="3398e-128">A delegate who tries to send an e-mail message that is located in the principal's Drafts folder with the SendAndSaveCopy option set to save a copy in the Sent Items distinguished folder will silently fail to move a copy of the sent item to the Sent Items distinguished folder.</span></span> <span data-ttu-id="3398e-129">项目将保留在的主体的草稿文件夹中。</span><span class="sxs-lookup"><span data-stu-id="3398e-129">The item will remain in the principal's Drafts folder.</span></span> <span data-ttu-id="3398e-130">此问题的解决方法是[DistinguishedFolderId](distinguishedfolderid.md)元素中指定的主体的邮箱。</span><span class="sxs-lookup"><span data-stu-id="3398e-130">The workaround for this issue is to specify the principal's mailbox in the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="3398e-131">代理人创建一封电子邮件，并将其保存到代理人的邮箱的草稿文件夹时要考虑的其他方案。</span><span class="sxs-lookup"><span data-stu-id="3398e-131">An additional scenario to consider is when a delegate creates an e-mail message and saves it to the Drafts folder of the delegate's mailbox.</span></span> <span data-ttu-id="3398e-132">如果代理尝试发送项目并将副本保存到的主体的已发送邮件的可分辨文件夹，将邮件发送正确，草稿邮件已发送的邮件未显示在代理人的或主体的代理人的草稿文件夹中保留发送项目文件夹，并响应为成功。</span><span class="sxs-lookup"><span data-stu-id="3398e-132">If the delegate tries to send the item and save a copy to the principal's Sent Items distinguished folder, the message is sent correctly, the draft message remains in the delegate's Drafts folder, the sent message does not appear in either the delegate's or principal's Sent Items folder, and the response is a success.</span></span>
  
## <a name="invalid-senditem-e-mail-message-request-example"></a><span data-ttu-id="3398e-133">无效的 SendItem （电子邮件） 请求示例</span><span class="sxs-lookup"><span data-stu-id="3398e-133">Invalid SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="3398e-134">说明</span><span class="sxs-lookup"><span data-stu-id="3398e-134">Description</span></span>

<span data-ttu-id="3398e-135">下面的代码示例显示了具有无效的标识符的请求的示例。</span><span class="sxs-lookup"><span data-stu-id="3398e-135">The following code sample shows an example of a request with an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="3398e-136">代码</span><span class="sxs-lookup"><span data-stu-id="3398e-136">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="%BadItemId%" ChangeKey="CQAAABYAAA" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="senditem-e-mail-message-error-response"></a><span data-ttu-id="3398e-137">SendItem （电子邮件） 错误响应</span><span class="sxs-lookup"><span data-stu-id="3398e-137">SendItem (E-mail Message) error response</span></span>

### <a name="description"></a><span data-ttu-id="3398e-138">说明</span><span class="sxs-lookup"><span data-stu-id="3398e-138">Description</span></span>

<span data-ttu-id="3398e-139">下面的示例演示包含无效的标识符的 SendItem 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="3398e-139">The following example shows an error response to a SendItem request that contains an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="3398e-140">代码</span><span class="sxs-lookup"><span data-stu-id="3398e-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="3398e-141">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="3398e-141">Error response elements</span></span>

<span data-ttu-id="3398e-142">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="3398e-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="3398e-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3398e-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3398e-144">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="3398e-144">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="3398e-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3398e-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="3398e-146">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3398e-146">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="3398e-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="3398e-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="3398e-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3398e-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3398e-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3398e-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="3398e-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3398e-150">See also</span></span>



[<span data-ttu-id="3398e-151">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="3398e-151">SendItem operation</span></span>](senditem-operation.md)
  
 <span data-ttu-id="3398e-152">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="3398e-152">**SendItemType**</span></span>


- [<span data-ttu-id="3398e-153">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3398e-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

