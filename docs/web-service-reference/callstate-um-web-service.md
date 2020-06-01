---
title: CallState （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: CallState 元素包含一个值，该值指示呼叫的状态。
ms.openlocfilehash: 44614c460286ff49ebc2373263c1827c6be5cc08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454608"
---
# <a name="callstate-um-web-service"></a><span data-ttu-id="b1b57-103">CallState （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b1b57-103">CallState (UM web service)</span></span>

<span data-ttu-id="b1b57-104">**CallState**元素包含一个值，该值指示呼叫的状态。</span><span class="sxs-lookup"><span data-stu-id="b1b57-104">The **CallState** element contains a value that indicates the status of a call.</span></span> 
  
[<span data-ttu-id="b1b57-105">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b1b57-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="b1b57-106">CallState （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b1b57-106">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 <span data-ttu-id="b1b57-107">**UMCallState**</span><span class="sxs-lookup"><span data-stu-id="b1b57-107">**UMCallState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1b57-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b1b57-108">Attributes and elements</span></span>

<span data-ttu-id="b1b57-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b1b57-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1b57-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="b1b57-110">Attributes</span></span>

<span data-ttu-id="b1b57-111">无。</span><span class="sxs-lookup"><span data-stu-id="b1b57-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1b57-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b1b57-112">Child elements</span></span>

<span data-ttu-id="b1b57-113">无。</span><span class="sxs-lookup"><span data-stu-id="b1b57-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b1b57-114">父元素</span><span class="sxs-lookup"><span data-stu-id="b1b57-114">Parent elements</span></span>

|<span data-ttu-id="b1b57-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="b1b57-115">**Element**</span></span>|<span data-ttu-id="b1b57-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="b1b57-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1b57-117">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b1b57-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="b1b57-118">定义对[GetCallInfo 操作（UM web 服务）](getcallinfo-operation-um-web-service.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="b1b57-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b1b57-119">文本值</span><span class="sxs-lookup"><span data-stu-id="b1b57-119">Text value</span></span>

<span data-ttu-id="b1b57-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="b1b57-120">A text value is required.</span></span> <span data-ttu-id="b1b57-121">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="b1b57-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="b1b57-122">待机</span><span class="sxs-lookup"><span data-stu-id="b1b57-122">Idle</span></span>
    
- <span data-ttu-id="b1b57-123">正在连接</span><span class="sxs-lookup"><span data-stu-id="b1b57-123">Connecting</span></span>
    
- <span data-ttu-id="b1b57-124">收到</span><span class="sxs-lookup"><span data-stu-id="b1b57-124">Alerted</span></span>
    
- <span data-ttu-id="b1b57-125">已连接</span><span class="sxs-lookup"><span data-stu-id="b1b57-125">Connected</span></span>
    
- <span data-ttu-id="b1b57-126">已断开连接</span><span class="sxs-lookup"><span data-stu-id="b1b57-126">Disconnected</span></span>
    
- <span data-ttu-id="b1b57-127">即将</span><span class="sxs-lookup"><span data-stu-id="b1b57-127">Incoming</span></span>
    
- <span data-ttu-id="b1b57-128">传输</span><span class="sxs-lookup"><span data-stu-id="b1b57-128">Transferring</span></span>
    
- <span data-ttu-id="b1b57-129">发送</span><span class="sxs-lookup"><span data-stu-id="b1b57-129">Forwarding</span></span>
    
## <a name="element-information"></a><span data-ttu-id="b1b57-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="b1b57-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1b57-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="b1b57-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="b1b57-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="b1b57-132">Schema Name</span></span>  <br/> |<span data-ttu-id="b1b57-133">邮件</span><span class="sxs-lookup"><span data-stu-id="b1b57-133">Messages</span></span>  <br/> |
|<span data-ttu-id="b1b57-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="b1b57-134">Validation File</span></span>  <br/> |<span data-ttu-id="b1b57-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b1b57-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1b57-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="b1b57-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1b57-137">False</span><span class="sxs-lookup"><span data-stu-id="b1b57-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1b57-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b1b57-138">See also</span></span>



[<span data-ttu-id="b1b57-139">GetCallInfo 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b1b57-139">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="b1b57-140">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b1b57-140">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

