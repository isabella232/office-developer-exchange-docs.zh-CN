---
title: MoveItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: dcf40fa7-7796-4a5c-bf5b-7a509a18d208
description: MoveItem 操作用于将一个或多个项目移至的单个目标文件夹。
ms.openlocfilehash: c5619befb02ec20ef0911992484dcc00cc2c5e92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826492"
---
# <a name="moveitem-operation"></a><span data-ttu-id="d2a56-103">MoveItem Operation</span><span class="sxs-lookup"><span data-stu-id="d2a56-103">MoveItem operation</span></span>

<span data-ttu-id="d2a56-104">**MoveItem**操作用于将一个或多个项目移至的单个目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="d2a56-104">The **MoveItem** operation is used to move one or more items to a single destination folder.</span></span> 
  
## <a name="moveitem-request-example"></a><span data-ttu-id="d2a56-105">MoveItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="d2a56-105">MoveItem request example</span></span>

### <a name="description"></a><span data-ttu-id="d2a56-106">说明</span><span class="sxs-lookup"><span data-stu-id="d2a56-106">Description</span></span>

<span data-ttu-id="d2a56-107">**MoveItem**请求的下面的示例演示如何将项目移动到草稿文件夹。</span><span class="sxs-lookup"><span data-stu-id="d2a56-107">The following example of a **MoveItem** request shows how to move an item to the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d2a56-108">代码</span><span class="sxs-lookup"><span data-stu-id="d2a56-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ToFolderId>
        <t:DistinguishedFolderId Id="drafts"/>
      </ToFolderId>
      <ItemIds>
        <t:ItemId Id="AAAtAEF/swbAAA=" ChangeKey="EwAAABYA/s4b"/>
      </ItemIds>
    </MoveItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="d2a56-109">注释</span><span class="sxs-lookup"><span data-stu-id="d2a56-109">Comments</span></span>

<span data-ttu-id="d2a56-110">[ToFolderId](tofolderid.md)元素指定项目将移动到的文件夹。</span><span class="sxs-lookup"><span data-stu-id="d2a56-110">The [ToFolderId](tofolderid.md) element specifies the folder to which the items will be moved.</span></span> <span data-ttu-id="d2a56-111">请注意，列出[ItemIds](itemids.md)集合中的所有项目将都最终目标文件夹中。</span><span class="sxs-lookup"><span data-stu-id="d2a56-111">Note that all items listed in the [ItemIds](itemids.md) collection will end up in the destination folder.</span></span> <span data-ttu-id="d2a56-112">您必须进行单独**MoveItem**呼叫将项目放在不同的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="d2a56-112">You must make separate **MoveItem** calls to place items in different destination folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d2a56-113">已缩短的项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="d2a56-113">The item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="d2a56-114">请求元素</span><span class="sxs-lookup"><span data-stu-id="d2a56-114">Request elements</span></span>

<span data-ttu-id="d2a56-115">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="d2a56-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="d2a56-116">MoveItem</span><span class="sxs-lookup"><span data-stu-id="d2a56-116">MoveItem</span></span>](moveitem.md)
    
- [<span data-ttu-id="d2a56-117">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="d2a56-117">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="d2a56-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="d2a56-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="d2a56-119">ItemIds</span><span class="sxs-lookup"><span data-stu-id="d2a56-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="d2a56-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="d2a56-120">ItemId</span></span>](itemid.md)
    
## <a name="moveitem-response-example"></a><span data-ttu-id="d2a56-121">MoveItem 响应示例</span><span class="sxs-lookup"><span data-stu-id="d2a56-121">MoveItem response example</span></span>

### <a name="description"></a><span data-ttu-id="d2a56-122">说明</span><span class="sxs-lookup"><span data-stu-id="d2a56-122">Description</span></span>

<span data-ttu-id="d2a56-123">下面的示例演示对**MoveItem**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="d2a56-123">The following example shows a successful response to a **MoveItem** request.</span></span> 
  
<span data-ttu-id="d2a56-124">响应消息中返回的新项的项标识符。</span><span class="sxs-lookup"><span data-stu-id="d2a56-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="d2a56-125">项标识符到公用文件夹**MoveItem**操作不返回跨邮箱或邮箱的响应中。</span><span class="sxs-lookup"><span data-stu-id="d2a56-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **MoveItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d2a56-126">代码</span><span class="sxs-lookup"><span data-stu-id="d2a56-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <MoveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemID Id="AAMkAd" ChangeKey="FwAAABY" />
            </t:Message>
          </m:Items>
        </m:MoveItemResponseMessage>
      </m:ResponseMessages>
    </MoveItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="d2a56-127">注释</span><span class="sxs-lookup"><span data-stu-id="d2a56-127">Comments</span></span>

<span data-ttu-id="d2a56-128">如果移动不成功，则**MoveItem**操作将指示成功。</span><span class="sxs-lookup"><span data-stu-id="d2a56-128">The **MoveItem** operation will indicate success if the move was successful.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="d2a56-129">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="d2a56-129">Successful response elements</span></span>

<span data-ttu-id="d2a56-130">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="d2a56-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d2a56-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d2a56-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d2a56-132">MoveItemResponse</span><span class="sxs-lookup"><span data-stu-id="d2a56-132">MoveItemResponse</span></span>](moveitemresponse.md)
    
- [<span data-ttu-id="d2a56-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d2a56-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d2a56-134">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d2a56-134">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md)
    
- [<span data-ttu-id="d2a56-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d2a56-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d2a56-136">Items</span><span class="sxs-lookup"><span data-stu-id="d2a56-136">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="d2a56-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2a56-137">See also</span></span>



- [<span data-ttu-id="d2a56-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d2a56-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

