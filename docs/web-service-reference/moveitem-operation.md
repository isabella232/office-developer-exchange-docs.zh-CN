---
title: MoveItem 操作
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
description: MoveItem 操作用于将一个或多个项目移至单个目标文件夹。
ms.openlocfilehash: 6a455e483ad2e5c84b91cfaa7562f4f1ec46a112
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465679"
---
# <a name="moveitem-operation"></a><span data-ttu-id="39b38-103">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="39b38-103">MoveItem operation</span></span>

<span data-ttu-id="39b38-104">**MoveItem**操作用于将一个或多个项目移至单个目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="39b38-104">The **MoveItem** operation is used to move one or more items to a single destination folder.</span></span> 
  
## <a name="moveitem-request-example"></a><span data-ttu-id="39b38-105">MoveItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="39b38-105">MoveItem request example</span></span>

### <a name="description"></a><span data-ttu-id="39b38-106">说明</span><span class="sxs-lookup"><span data-stu-id="39b38-106">Description</span></span>

<span data-ttu-id="39b38-107">以下示例的**MoveItem**请求显示如何将项目移动到 "草稿" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="39b38-107">The following example of a **MoveItem** request shows how to move an item to the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="39b38-108">代码</span><span class="sxs-lookup"><span data-stu-id="39b38-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="39b38-109">备注</span><span class="sxs-lookup"><span data-stu-id="39b38-109">Comments</span></span>

<span data-ttu-id="39b38-110">[ToFolderId](tofolderid.md)元素指定要将项目移动到的文件夹。</span><span class="sxs-lookup"><span data-stu-id="39b38-110">The [ToFolderId](tofolderid.md) element specifies the folder to which the items will be moved.</span></span> <span data-ttu-id="39b38-111">请注意， [ItemIds](itemids.md)集合中列出的所有项将在目标文件夹中结束。</span><span class="sxs-lookup"><span data-stu-id="39b38-111">Note that all items listed in the [ItemIds](itemids.md) collection will end up in the destination folder.</span></span> <span data-ttu-id="39b38-112">您必须单独进行**MoveItem**调用，以将项目放在不同的目标文件夹中。</span><span class="sxs-lookup"><span data-stu-id="39b38-112">You must make separate **MoveItem** calls to place items in different destination folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="39b38-113">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="39b38-113">The item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="39b38-114">Request 元素</span><span class="sxs-lookup"><span data-stu-id="39b38-114">Request elements</span></span>

<span data-ttu-id="39b38-115">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="39b38-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="39b38-116">MoveItem</span><span class="sxs-lookup"><span data-stu-id="39b38-116">MoveItem</span></span>](moveitem.md)
    
- [<span data-ttu-id="39b38-117">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="39b38-117">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="39b38-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="39b38-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="39b38-119">ItemIds</span><span class="sxs-lookup"><span data-stu-id="39b38-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="39b38-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="39b38-120">ItemId</span></span>](itemid.md)
    
## <a name="moveitem-response-example"></a><span data-ttu-id="39b38-121">MoveItem 响应示例</span><span class="sxs-lookup"><span data-stu-id="39b38-121">MoveItem response example</span></span>

### <a name="description"></a><span data-ttu-id="39b38-122">说明</span><span class="sxs-lookup"><span data-stu-id="39b38-122">Description</span></span>

<span data-ttu-id="39b38-123">下面的示例演示对**MoveItem**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="39b38-123">The following example shows a successful response to a **MoveItem** request.</span></span> 
  
<span data-ttu-id="39b38-124">在响应消息中返回新项目的项目标识符。</span><span class="sxs-lookup"><span data-stu-id="39b38-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="39b38-125">在对跨邮箱或邮箱到公用文件夹**MoveItem**操作的响应中，不会返回项目标识符。</span><span class="sxs-lookup"><span data-stu-id="39b38-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **MoveItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="39b38-126">代码</span><span class="sxs-lookup"><span data-stu-id="39b38-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <MoveItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="39b38-127">备注</span><span class="sxs-lookup"><span data-stu-id="39b38-127">Comments</span></span>

<span data-ttu-id="39b38-128">如果移动成功， **MoveItem**操作将指示成功。</span><span class="sxs-lookup"><span data-stu-id="39b38-128">The **MoveItem** operation will indicate success if the move was successful.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="39b38-129">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="39b38-129">Successful response elements</span></span>

<span data-ttu-id="39b38-130">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="39b38-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="39b38-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="39b38-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="39b38-132">MoveItemResponse</span><span class="sxs-lookup"><span data-stu-id="39b38-132">MoveItemResponse</span></span>](moveitemresponse.md)
    
- [<span data-ttu-id="39b38-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="39b38-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="39b38-134">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="39b38-134">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md)
    
- [<span data-ttu-id="39b38-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="39b38-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="39b38-136">Items</span><span class="sxs-lookup"><span data-stu-id="39b38-136">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="39b38-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="39b38-137">See also</span></span>



- [<span data-ttu-id="39b38-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="39b38-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

