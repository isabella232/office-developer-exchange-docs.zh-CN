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
description: CallState 元素包含一个值，指示的呼叫状态。
ms.openlocfilehash: e751c2e38783c6634a44d8e1b830a9224cdf300a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753431"
---
# <a name="callstate-um-web-service"></a><span data-ttu-id="5bcca-103">CallState （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5bcca-103">CallState (UM web service)</span></span>

<span data-ttu-id="5bcca-104">**CallState**元素包含一个值，指示的呼叫状态。</span><span class="sxs-lookup"><span data-stu-id="5bcca-104">The **CallState** element contains a value that indicates the status of a call.</span></span> 
  
[<span data-ttu-id="5bcca-105">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5bcca-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="5bcca-106">CallState （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5bcca-106">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 <span data-ttu-id="5bcca-107">**UMCallState**</span><span class="sxs-lookup"><span data-stu-id="5bcca-107">**UMCallState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5bcca-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5bcca-108">Attributes and elements</span></span>

<span data-ttu-id="5bcca-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5bcca-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5bcca-110">属性</span><span class="sxs-lookup"><span data-stu-id="5bcca-110">Attributes</span></span>

<span data-ttu-id="5bcca-111">无。</span><span class="sxs-lookup"><span data-stu-id="5bcca-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5bcca-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5bcca-112">Child elements</span></span>

<span data-ttu-id="5bcca-113">无。</span><span class="sxs-lookup"><span data-stu-id="5bcca-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5bcca-114">父元素</span><span class="sxs-lookup"><span data-stu-id="5bcca-114">Parent elements</span></span>

|<span data-ttu-id="5bcca-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="5bcca-115">**Element**</span></span>|<span data-ttu-id="5bcca-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5bcca-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5bcca-117">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5bcca-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="5bcca-118">定义对[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="5bcca-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5bcca-119">文本值</span><span class="sxs-lookup"><span data-stu-id="5bcca-119">Text value</span></span>

<span data-ttu-id="5bcca-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="5bcca-120">A text value is required.</span></span> <span data-ttu-id="5bcca-121">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="5bcca-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="5bcca-122">空闲时间</span><span class="sxs-lookup"><span data-stu-id="5bcca-122">Idle</span></span>
    
- <span data-ttu-id="5bcca-123">正在连接</span><span class="sxs-lookup"><span data-stu-id="5bcca-123">Connecting</span></span>
    
- <span data-ttu-id="5bcca-124">收到通知</span><span class="sxs-lookup"><span data-stu-id="5bcca-124">Alerted</span></span>
    
- <span data-ttu-id="5bcca-125">已连接</span><span class="sxs-lookup"><span data-stu-id="5bcca-125">Connected</span></span>
    
- <span data-ttu-id="5bcca-126">已断开连接</span><span class="sxs-lookup"><span data-stu-id="5bcca-126">Disconnected</span></span>
    
- <span data-ttu-id="5bcca-127">传入</span><span class="sxs-lookup"><span data-stu-id="5bcca-127">Incoming</span></span>
    
- <span data-ttu-id="5bcca-128">转接</span><span class="sxs-lookup"><span data-stu-id="5bcca-128">Transferring</span></span>
    
- <span data-ttu-id="5bcca-129">转接</span><span class="sxs-lookup"><span data-stu-id="5bcca-129">Forwarding</span></span>
    
## <a name="element-information"></a><span data-ttu-id="5bcca-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="5bcca-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5bcca-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="5bcca-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="5bcca-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="5bcca-132">Schema Name</span></span>  <br/> |<span data-ttu-id="5bcca-133">邮件</span><span class="sxs-lookup"><span data-stu-id="5bcca-133">Messages</span></span>  <br/> |
|<span data-ttu-id="5bcca-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="5bcca-134">Validation File</span></span>  <br/> |<span data-ttu-id="5bcca-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5bcca-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5bcca-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="5bcca-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="5bcca-137">False</span><span class="sxs-lookup"><span data-stu-id="5bcca-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bcca-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5bcca-138">See also</span></span>



[<span data-ttu-id="5bcca-139">GetCallInfo 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5bcca-139">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="5bcca-140">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5bcca-140">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

