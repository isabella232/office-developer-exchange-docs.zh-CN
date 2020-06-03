---
title: CreateItem （AcceptSharingInvitation）
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
ms.assetid: 710c893a-3037-4f04-b336-aefedd36c406
description: CreateItem 操作用于接受共享其他用户的日历或联系人数据的邀请。
ms.openlocfilehash: eda846b72f42fe886497b355d9cddade7c5f4044
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457513"
---
# <a name="createitem-acceptsharinginvitation"></a><span data-ttu-id="98458-103">CreateItem （AcceptSharingInvitation）</span><span class="sxs-lookup"><span data-stu-id="98458-103">CreateItem (AcceptSharingInvitation)</span></span>

<span data-ttu-id="98458-104">**CreateItem**操作用于接受共享其他用户的日历或联系人数据的邀请。</span><span class="sxs-lookup"><span data-stu-id="98458-104">The **CreateItem** operation is used to accept an invitation to share another user's calendar or contacts data.</span></span> 
  
## <a name="accept-sharing-invitation-request-example"></a><span data-ttu-id="98458-105">接受共享邀请请求示例</span><span class="sxs-lookup"><span data-stu-id="98458-105">Accept Sharing Invitation request example</span></span>

### <a name="description"></a><span data-ttu-id="98458-106">Description</span><span class="sxs-lookup"><span data-stu-id="98458-106">Description</span></span>

<span data-ttu-id="98458-107">下面的示例展示了如何接受共享邀请。</span><span class="sxs-lookup"><span data-stu-id="98458-107">The following example shows how to accept a sharing invitation.</span></span>
  
### <a name="code"></a><span data-ttu-id="98458-108">代码</span><span class="sxs-lookup"><span data-stu-id="98458-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Items xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <AcceptSharingInvitation xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <ReferenceItemId Id="AAAlAFVzZ" ChangeKey="CwAAABYAA" />
        </AcceptSharingInvitation>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="98458-109">Request 元素</span><span class="sxs-lookup"><span data-stu-id="98458-109">Request elements</span></span>

<span data-ttu-id="98458-110">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="98458-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="98458-111">CreateItem</span><span class="sxs-lookup"><span data-stu-id="98458-111">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="98458-112">Items</span><span class="sxs-lookup"><span data-stu-id="98458-112">Items</span></span>](items.md)
    
- [<span data-ttu-id="98458-113">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="98458-113">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md)
    
- [<span data-ttu-id="98458-114">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="98458-114">ReferenceItemId</span></span>](referenceitemid.md)
    
### <a name="comments"></a><span data-ttu-id="98458-115">备注</span><span class="sxs-lookup"><span data-stu-id="98458-115">Comments</span></span>

<span data-ttu-id="98458-116">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="98458-116">The item identifier and change key have been shortened to preserve readability.</span></span>
  
## <a name="successful-accept-sharing-invitation-response-example"></a><span data-ttu-id="98458-117">成功的接受共享邀请响应示例</span><span class="sxs-lookup"><span data-stu-id="98458-117">Successful Accept Sharing Invitation response example</span></span>

### <a name="description"></a><span data-ttu-id="98458-118">Description</span><span class="sxs-lookup"><span data-stu-id="98458-118">Description</span></span>

<span data-ttu-id="98458-119">下面的示例演示对**CreateItem**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="98458-119">The following example shows a successful response to a **CreateItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="98458-120">代码</span><span class="sxs-lookup"><span data-stu-id="98458-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
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

### <a name="successful-response-elements"></a><span data-ttu-id="98458-121">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="98458-121">Successful response elements</span></span>

<span data-ttu-id="98458-122">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="98458-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="98458-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="98458-123">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="98458-124">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="98458-124">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="98458-125">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="98458-125">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="98458-126">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="98458-126">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="98458-127">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="98458-127">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="98458-128">Items</span><span class="sxs-lookup"><span data-stu-id="98458-128">Items</span></span>](items.md)
    
## <a name="accept-sharing-invitation-error-response-example"></a><span data-ttu-id="98458-129">接受共享邀请错误响应示例</span><span class="sxs-lookup"><span data-stu-id="98458-129">Accept Sharing Invitation Error response example</span></span>

### <a name="description"></a><span data-ttu-id="98458-130">Description</span><span class="sxs-lookup"><span data-stu-id="98458-130">Description</span></span>

<span data-ttu-id="98458-131">下面的示例演示对**CreateItem**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="98458-131">The following example shows an error response to a **CreateItem** request.</span></span> <span data-ttu-id="98458-132">此错误是由于尝试接受在 Exchange 存储中找不到的共享邀请而引起的。</span><span class="sxs-lookup"><span data-stu-id="98458-132">The error is caused by an attempt to accept a sharing invitation that cannot be found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="98458-133">代码</span><span class="sxs-lookup"><span data-stu-id="98458-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
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

### <a name="error-response-elements"></a><span data-ttu-id="98458-134">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="98458-134">Error response elements</span></span>

<span data-ttu-id="98458-135">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="98458-135">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="98458-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="98458-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="98458-137">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="98458-137">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="98458-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="98458-138">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="98458-139">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="98458-139">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="98458-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="98458-140">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="98458-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="98458-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="98458-142">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="98458-142">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="98458-143">Items</span><span class="sxs-lookup"><span data-stu-id="98458-143">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="98458-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="98458-144">See also</span></span>



[<span data-ttu-id="98458-145">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="98458-145">CreateItem operation</span></span>](createitem-operation.md)

