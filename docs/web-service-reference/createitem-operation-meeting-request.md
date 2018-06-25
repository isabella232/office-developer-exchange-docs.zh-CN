---
title: CreateItem operation，（会议请求）
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
description: 使用 CreateItem operation 响应会议请求。
ms.openlocfilehash: a8aea688e46376906554952ce8ec45022cf613e9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753663"
---
# <a name="createitem-operation-meeting-request"></a><span data-ttu-id="a9e80-103">CreateItem operation，（会议请求）</span><span class="sxs-lookup"><span data-stu-id="a9e80-103">CreateItem operation (meeting request)</span></span>

<span data-ttu-id="a9e80-104">使用 CreateItem operation 响应会议请求。</span><span class="sxs-lookup"><span data-stu-id="a9e80-104">The CreateItem operation is used to respond to meeting requests.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9e80-105">注解</span><span class="sxs-lookup"><span data-stu-id="a9e80-105">Remarks</span></span>

<span data-ttu-id="a9e80-106">CreateItem operation，提供用于响应会议请求的三个选项： 接受、 暂时接受或拒绝。</span><span class="sxs-lookup"><span data-stu-id="a9e80-106">The CreateItem operation provides three options for responding to a meeting request: accept, tentatively accept, or decline.</span></span> 
  
## <a name="accept-meeting-request-example"></a><span data-ttu-id="a9e80-107">接受会议请求示例</span><span class="sxs-lookup"><span data-stu-id="a9e80-107">Accept Meeting request example</span></span>

### <a name="description"></a><span data-ttu-id="a9e80-108">说明</span><span class="sxs-lookup"><span data-stu-id="a9e80-108">Description</span></span>

<span data-ttu-id="a9e80-109">下面的示例演示如何接受会议请求的邀请。</span><span class="sxs-lookup"><span data-stu-id="a9e80-109">The following example shows how to accept a meeting request invitation.</span></span>
  
### <a name="code"></a><span data-ttu-id="a9e80-110">代码</span><span class="sxs-lookup"><span data-stu-id="a9e80-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                MessageDisposition="SendAndSaveCopy">
      <Items>
        <AcceptItem xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <ReferenceItemId Id="AAAlAFVzZ"
                           ChangeKey="CwAAABYAA"/>
        </AcceptItem>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="a9e80-111">注释</span><span class="sxs-lookup"><span data-stu-id="a9e80-111">Comments</span></span>

<span data-ttu-id="a9e80-112">若要暂时接受或拒绝会议请求中，使用来代替[AcceptItem](acceptitem.md)元素[TentativelyAcceptItem](tentativelyacceptitem.md)或[DeclineItem](declineitem.md)元素。</span><span class="sxs-lookup"><span data-stu-id="a9e80-112">To tentatively accept or to decline the meeting request, use the [TentativelyAcceptItem](tentativelyacceptitem.md) or [DeclineItem](declineitem.md) elements in place of the [AcceptItem](acceptitem.md) element.</span></span> 
  
<span data-ttu-id="a9e80-113">已缩短的项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="a9e80-113">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="accepting-meeting-request-elements"></a><span data-ttu-id="a9e80-114">接受会议请求元素</span><span class="sxs-lookup"><span data-stu-id="a9e80-114">Accepting Meeting Request Elements</span></span>

<span data-ttu-id="a9e80-115">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a9e80-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a9e80-116">CreateItem</span><span class="sxs-lookup"><span data-stu-id="a9e80-116">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="a9e80-117">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="a9e80-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="a9e80-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="a9e80-118">AcceptItem</span></span>](acceptitem.md)
    
- [<span data-ttu-id="a9e80-119">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="a9e80-119">ReferenceItemId</span></span>](referenceitemid.md)
    
## <a name="successful-accept-meeting-response-example"></a><span data-ttu-id="a9e80-120">成功接受会议响应示例</span><span class="sxs-lookup"><span data-stu-id="a9e80-120">Successful Accept Meeting response example</span></span>

### <a name="description"></a><span data-ttu-id="a9e80-121">说明</span><span class="sxs-lookup"><span data-stu-id="a9e80-121">Description</span></span>

<span data-ttu-id="a9e80-122">下面的示例演示对 CreateItem 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="a9e80-122">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="a9e80-123">代码</span><span class="sxs-lookup"><span data-stu-id="a9e80-123">Code</span></span>

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

### <a name="successful-response-elements"></a><span data-ttu-id="a9e80-124">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="a9e80-124">Successful response elements</span></span>

<span data-ttu-id="a9e80-125">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a9e80-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a9e80-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a9e80-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a9e80-127">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="a9e80-127">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="a9e80-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a9e80-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a9e80-129">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a9e80-129">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="a9e80-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a9e80-130">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a9e80-131">Items</span><span class="sxs-lookup"><span data-stu-id="a9e80-131">Items</span></span>](items.md)
    
## <a name="accept-meeting-error-response-example"></a><span data-ttu-id="a9e80-132">接受会议错误响应示例</span><span class="sxs-lookup"><span data-stu-id="a9e80-132">Accept Meeting Error response example</span></span>

### <a name="description"></a><span data-ttu-id="a9e80-133">说明</span><span class="sxs-lookup"><span data-stu-id="a9e80-133">Description</span></span>

<span data-ttu-id="a9e80-134">下面的示例演示对 CreateItem 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="a9e80-134">The following example shows an error response to CreateItem request.</span></span> <span data-ttu-id="a9e80-135">错误由尝试接受会议请求的找不到 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="a9e80-135">The error is caused by an attempt to accept a meeting request that cannot be found in the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="a9e80-136">代码</span><span class="sxs-lookup"><span data-stu-id="a9e80-136">Code</span></span>

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
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="a9e80-137">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="a9e80-137">Error response elements</span></span>

<span data-ttu-id="a9e80-138">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a9e80-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="a9e80-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a9e80-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a9e80-140">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="a9e80-140">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="a9e80-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a9e80-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a9e80-142">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a9e80-142">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="a9e80-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="a9e80-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a9e80-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a9e80-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a9e80-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a9e80-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="a9e80-146">Items</span><span class="sxs-lookup"><span data-stu-id="a9e80-146">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="a9e80-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a9e80-147">See also</span></span>



[<span data-ttu-id="a9e80-148">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="a9e80-148">CreateItem operation</span></span>](createitem-operation.md)
  
[<span data-ttu-id="a9e80-149">CreateItem operation，（日历项）</span><span class="sxs-lookup"><span data-stu-id="a9e80-149">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)

