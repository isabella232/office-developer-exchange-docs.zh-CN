---
title: CreateItem 操作（会议请求）
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
ms.assetid: fe136881-a804-456a-8552-8a1bea5eb9c8
description: CreateItem 操作用于响应会议请求。
ms.openlocfilehash: f9e6bd1742e6a30d08736ea67c0ff80b7a18e88a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457107"
---
# <a name="createitem-operation-meeting-request"></a><span data-ttu-id="5f5b8-103">CreateItem 操作（会议请求）</span><span class="sxs-lookup"><span data-stu-id="5f5b8-103">CreateItem operation (meeting request)</span></span>

<span data-ttu-id="5f5b8-104">CreateItem 操作用于响应会议请求。</span><span class="sxs-lookup"><span data-stu-id="5f5b8-104">The CreateItem operation is used to respond to meeting requests.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f5b8-105">备注</span><span class="sxs-lookup"><span data-stu-id="5f5b8-105">Remarks</span></span>

<span data-ttu-id="5f5b8-106">CreateItem 操作提供了三个用于响应会议请求的选项： "接受"、"暂定接受" 或 "拒绝"。</span><span class="sxs-lookup"><span data-stu-id="5f5b8-106">The CreateItem operation provides three options for responding to a meeting request: accept, tentatively accept, or decline.</span></span> 
  
## <a name="accept-meeting-request-example"></a><span data-ttu-id="5f5b8-107">接受会议请求示例</span><span class="sxs-lookup"><span data-stu-id="5f5b8-107">Accept Meeting request example</span></span>

### <a name="description"></a><span data-ttu-id="5f5b8-108">说明</span><span class="sxs-lookup"><span data-stu-id="5f5b8-108">Description</span></span>

<span data-ttu-id="5f5b8-109">下面的示例展示了如何接受会议请求邀请。</span><span class="sxs-lookup"><span data-stu-id="5f5b8-109">The following example shows how to accept a meeting request invitation.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f5b8-110">代码</span><span class="sxs-lookup"><span data-stu-id="5f5b8-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                MessageDisposition="SendAndSaveCopy">
      <Items>
        <AcceptItem xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <ReferenceItemId Id="AAAlAFVzZ"
                           ChangeKey="CwAAABYAA"/>
        </AcceptItem>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="5f5b8-111">备注</span><span class="sxs-lookup"><span data-stu-id="5f5b8-111">Comments</span></span>

<span data-ttu-id="5f5b8-112">若要暂时接受或拒绝会议请求，请使用[TentativelyAcceptItem](tentativelyacceptitem.md)或[DeclineItem](declineitem.md)元素代替[AcceptItem](acceptitem.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5f5b8-112">To tentatively accept or to decline the meeting request, use the [TentativelyAcceptItem](tentativelyacceptitem.md) or [DeclineItem](declineitem.md) elements in place of the [AcceptItem](acceptitem.md) element.</span></span> 
  
<span data-ttu-id="5f5b8-113">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="5f5b8-113">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="accepting-meeting-request-elements"></a><span data-ttu-id="5f5b8-114">接受会议请求元素</span><span class="sxs-lookup"><span data-stu-id="5f5b8-114">Accepting Meeting Request Elements</span></span>

<span data-ttu-id="5f5b8-115">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f5b8-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="5f5b8-116">CreateItem</span><span class="sxs-lookup"><span data-stu-id="5f5b8-116">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="5f5b8-117">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="5f5b8-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="5f5b8-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="5f5b8-118">AcceptItem</span></span>](acceptitem.md)
    
- [<span data-ttu-id="5f5b8-119">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="5f5b8-119">ReferenceItemId</span></span>](referenceitemid.md)
    
## <a name="successful-accept-meeting-response-example"></a><span data-ttu-id="5f5b8-120">成功的接受会议响应示例</span><span class="sxs-lookup"><span data-stu-id="5f5b8-120">Successful Accept Meeting response example</span></span>

### <a name="description"></a><span data-ttu-id="5f5b8-121">说明</span><span class="sxs-lookup"><span data-stu-id="5f5b8-121">Description</span></span>

<span data-ttu-id="5f5b8-122">下面的示例演示对 CreateItem 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="5f5b8-122">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f5b8-123">代码</span><span class="sxs-lookup"><span data-stu-id="5f5b8-123">Code</span></span>

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

### <a name="successful-response-elements"></a><span data-ttu-id="5f5b8-124">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="5f5b8-124">Successful response elements</span></span>

<span data-ttu-id="5f5b8-125">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f5b8-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5f5b8-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5f5b8-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5f5b8-127">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="5f5b8-127">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="5f5b8-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5f5b8-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5f5b8-129">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5f5b8-129">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="5f5b8-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5f5b8-130">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5f5b8-131">Items</span><span class="sxs-lookup"><span data-stu-id="5f5b8-131">Items</span></span>](items.md)
    
## <a name="accept-meeting-error-response-example"></a><span data-ttu-id="5f5b8-132">接受会议错误响应示例</span><span class="sxs-lookup"><span data-stu-id="5f5b8-132">Accept Meeting Error response example</span></span>

### <a name="description"></a><span data-ttu-id="5f5b8-133">说明</span><span class="sxs-lookup"><span data-stu-id="5f5b8-133">Description</span></span>

<span data-ttu-id="5f5b8-134">下面的示例演示对 CreateItem 请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="5f5b8-134">The following example shows an error response to CreateItem request.</span></span> <span data-ttu-id="5f5b8-135">此错误是由于尝试接受在 Exchange 存储中找不到的会议请求而引起的。</span><span class="sxs-lookup"><span data-stu-id="5f5b8-135">The error is caused by an attempt to accept a meeting request that cannot be found in the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f5b8-136">代码</span><span class="sxs-lookup"><span data-stu-id="5f5b8-136">Code</span></span>

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
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="5f5b8-137">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="5f5b8-137">Error response elements</span></span>

<span data-ttu-id="5f5b8-138">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f5b8-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="5f5b8-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5f5b8-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5f5b8-140">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="5f5b8-140">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="5f5b8-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5f5b8-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5f5b8-142">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5f5b8-142">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="5f5b8-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="5f5b8-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5f5b8-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5f5b8-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5f5b8-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5f5b8-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="5f5b8-146">Items</span><span class="sxs-lookup"><span data-stu-id="5f5b8-146">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="5f5b8-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f5b8-147">See also</span></span>



[<span data-ttu-id="5f5b8-148">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="5f5b8-148">CreateItem operation</span></span>](createitem-operation.md)
  
[<span data-ttu-id="5f5b8-149">CreateItem 操作（日历项目）</span><span class="sxs-lookup"><span data-stu-id="5f5b8-149">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)

