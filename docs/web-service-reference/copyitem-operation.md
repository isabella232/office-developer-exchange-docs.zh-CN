---
title: CopyItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItem
api_type:
- schema
ms.assetid: bcc68f9e-d511-4c29-bba6-ed535524624a
description: CopyItem 操作项复制，并将项目放入不同的文件夹。
ms.openlocfilehash: 95d2371e9185aa25f40eaec37dda54276a54d321
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753609"
---
# <a name="copyitem-operation"></a><span data-ttu-id="42144-103">CopyItem Operation</span><span class="sxs-lookup"><span data-stu-id="42144-103">CopyItem operation</span></span>

<span data-ttu-id="42144-104">**CopyItem**操作项复制，并将项目放入不同的文件夹。</span><span class="sxs-lookup"><span data-stu-id="42144-104">The **CopyItem** operation copies items and puts the items in a different folder.</span></span> 
  
## <a name="copyitem-request-example"></a><span data-ttu-id="42144-105">CopyItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="42144-105">CopyItem request example</span></span>

### <a name="description"></a><span data-ttu-id="42144-106">说明</span><span class="sxs-lookup"><span data-stu-id="42144-106">Description</span></span>

<span data-ttu-id="42144-107">**CopyItem**请求的下面的示例演示如何将项目复制到收件箱的请求的表单。</span><span class="sxs-lookup"><span data-stu-id="42144-107">The following example of a **CopyItem** request shows how to form a request to copy an item to the Inbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="42144-108">代码</span><span class="sxs-lookup"><span data-stu-id="42144-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </ToFolderId>
      <ItemIds>
        <t:ItemId Id="AS4AUnV="/>
      </ItemIds>
    </CopyItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="42144-109">注释</span><span class="sxs-lookup"><span data-stu-id="42144-109">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="42144-110">已缩短文件夹 ID 和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="42144-110">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="42144-111">请求元素</span><span class="sxs-lookup"><span data-stu-id="42144-111">Request elements</span></span>

<span data-ttu-id="42144-112">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="42144-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="42144-113">CopyItem</span><span class="sxs-lookup"><span data-stu-id="42144-113">CopyItem</span></span>](copyitem.md)
    
- [<span data-ttu-id="42144-114">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="42144-114">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="42144-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="42144-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="42144-116">ItemIds</span><span class="sxs-lookup"><span data-stu-id="42144-116">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="42144-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="42144-117">ItemId</span></span>](itemid.md)
    
> [!NOTE]
> <span data-ttu-id="42144-118">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="42144-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="42144-119">若要查找的请求邮件**CopyItem**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="42144-119">To find other options for the request message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="42144-120">启动[CopyItem](copyitem.md)元素。</span><span class="sxs-lookup"><span data-stu-id="42144-120">Start at the [CopyItem](copyitem.md) element.</span></span> 
  
## <a name="successful-copyitem-response"></a><span data-ttu-id="42144-121">成功的 CopyItem 响应</span><span class="sxs-lookup"><span data-stu-id="42144-121">Successful CopyItem Response</span></span>

### <a name="description"></a><span data-ttu-id="42144-122">说明</span><span class="sxs-lookup"><span data-stu-id="42144-122">Description</span></span>

<span data-ttu-id="42144-123">下面的示例演示对**CopyItem**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="42144-123">The following example shows a successful response to the **CopyItem** request.</span></span> 
  
<span data-ttu-id="42144-124">响应消息中返回的新项的项标识符。</span><span class="sxs-lookup"><span data-stu-id="42144-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="42144-125">项标识符到公用文件夹**CopyItem**操作不返回跨邮箱或邮箱的响应中。</span><span class="sxs-lookup"><span data-stu-id="42144-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **CopyItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="42144-126">代码</span><span class="sxs-lookup"><span data-stu-id="42144-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemID Id="AAMkAd" ChangeKey="FwAAABY" />
            </t:Message>
          </m:Items>
        </m:CopyItemResponseMessage>
      </m:ResponseMessages>
    </CopyItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="42144-127">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="42144-127">Successful response elements</span></span>

<span data-ttu-id="42144-128">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="42144-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="42144-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="42144-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="42144-130">CopyItemResponse</span><span class="sxs-lookup"><span data-stu-id="42144-130">CopyItemResponse</span></span>](copyitemresponse.md)
    
- [<span data-ttu-id="42144-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="42144-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="42144-132">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="42144-132">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md)
    
- [<span data-ttu-id="42144-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="42144-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="42144-134">Items</span><span class="sxs-lookup"><span data-stu-id="42144-134">Items</span></span>](items.md)
    
<span data-ttu-id="42144-135">若要查找的响应消息**CopyItem**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="42144-135">To find other options for the response message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="42144-136">启动[CopyItemResponse](copyitemresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="42144-136">Start at the [CopyItemResponse](copyitemresponse.md) element.</span></span> 
  
## <a name="copyitem-error-response"></a><span data-ttu-id="42144-137">CopyItem 错误响应</span><span class="sxs-lookup"><span data-stu-id="42144-137">CopyItem error response</span></span>

### <a name="description"></a><span data-ttu-id="42144-138">说明</span><span class="sxs-lookup"><span data-stu-id="42144-138">Description</span></span>

<span data-ttu-id="42144-139">下面的示例演示对**CopyItem**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="42144-139">The following example shows an error response to a **CopyItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="42144-140">代码</span><span class="sxs-lookup"><span data-stu-id="42144-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CopyItemResponseMessage>
      </m:ResponseMessages>
    </CopyItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="42144-141">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="42144-141">Error response elements</span></span>

<span data-ttu-id="42144-142">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="42144-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="42144-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="42144-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="42144-144">CopyItemResponse</span><span class="sxs-lookup"><span data-stu-id="42144-144">CopyItemResponse</span></span>](copyitemresponse.md)
    
- [<span data-ttu-id="42144-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="42144-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="42144-146">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="42144-146">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md)
    
- [<span data-ttu-id="42144-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="42144-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="42144-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="42144-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="42144-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="42144-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="42144-150">Items</span><span class="sxs-lookup"><span data-stu-id="42144-150">Items</span></span>](items.md)
    
<span data-ttu-id="42144-151">若要查找错误响应消息的**CopyItem**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="42144-151">To find other options for the error response message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="42144-152">启动[CopyItemResponse](copyitemresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="42144-152">Start at the [CopyItemResponse](copyitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42144-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42144-153">See also</span></span>



- [<span data-ttu-id="42144-154">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="42144-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

