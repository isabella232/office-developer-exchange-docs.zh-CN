---
title: CallId （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallId
api_type:
- schema
ms.assetid: 2e044109-8bf3-488c-a654-459ac62fa1e7
description: CallId 元素包含一个值，该值表示 GetCallInfo （UM web 服务）请求或断开连接（UM web 服务）请求中的调用的标识符。
ms.openlocfilehash: 5d5f596d4a98cbfb4b53be04278dae2305fc10c3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529453"
---
# <a name="callid-um-web-service"></a><span data-ttu-id="46028-103">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-103">CallId (UM web service)</span></span>

<span data-ttu-id="46028-104">**CallId**元素包含一个值，该值表示[GetCallInfo （um web 服务）](getcallinfo-um-web-service.md)请求或[断开连接（um web 服务）](disconnect-um-web-service.md)请求中的调用的标识符。</span><span class="sxs-lookup"><span data-stu-id="46028-104">The **CallId** element contains the value that represents the identifier of the call in a [GetCallInfo (UM web service)](getcallinfo-um-web-service.md) request or [Disconnect (UM web service)](disconnect-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="46028-105">GetCallInfo （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-105">GetCallInfo (UM web service)</span></span>](getcallinfo-um-web-service.md)
  
[<span data-ttu-id="46028-106">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-106">CallId (UM web service)</span></span>](callid-um-web-service.md)
  
[<span data-ttu-id="46028-107">断开连接（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-107">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md)
  
[<span data-ttu-id="46028-108">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-108">CallId (UM web service)</span></span>](callid-um-web-service.md)
  
```xml
<CallId/>
```

 <span data-ttu-id="46028-109">**string**</span><span class="sxs-lookup"><span data-stu-id="46028-109">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46028-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="46028-110">Attributes and elements</span></span>

<span data-ttu-id="46028-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="46028-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46028-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="46028-112">Attributes</span></span>

<span data-ttu-id="46028-113">无。</span><span class="sxs-lookup"><span data-stu-id="46028-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46028-114">子元素</span><span class="sxs-lookup"><span data-stu-id="46028-114">Child elements</span></span>

<span data-ttu-id="46028-115">无。</span><span class="sxs-lookup"><span data-stu-id="46028-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="46028-116">父元素</span><span class="sxs-lookup"><span data-stu-id="46028-116">Parent elements</span></span>

|<span data-ttu-id="46028-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="46028-117">**Element**</span></span>|<span data-ttu-id="46028-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="46028-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46028-119">GetCallInfo （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-119">GetCallInfo (UM web service)</span></span>](getcallinfo-um-web-service.md) <br/> |<span data-ttu-id="46028-120">定义获取有关调用的信息的请求。</span><span class="sxs-lookup"><span data-stu-id="46028-120">Defines a request to get information about a call.</span></span>  <br/> |
|[<span data-ttu-id="46028-121">断开连接（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-121">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md) <br/> |<span data-ttu-id="46028-122">定义断开呼叫连接的请求。</span><span class="sxs-lookup"><span data-stu-id="46028-122">Defines a request to disconnect a call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="46028-123">文本值</span><span class="sxs-lookup"><span data-stu-id="46028-123">Text value</span></span>

<span data-ttu-id="46028-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="46028-124">A text value is required.</span></span> <span data-ttu-id="46028-125">文本值表示调用的标识符。</span><span class="sxs-lookup"><span data-stu-id="46028-125">The text value represents the identifier for a call.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46028-126">备注</span><span class="sxs-lookup"><span data-stu-id="46028-126">Remarks</span></span>

<span data-ttu-id="46028-127">若要初始呼叫，请使用[PlayOnPhone 操作（um web 服务）](playonphone-operation-um-web-service.md)或[PLAYONPHONEGREETING 操作（um web 服务）](playonphonegreeting-operation-um-web-service.md)。</span><span class="sxs-lookup"><span data-stu-id="46028-127">To initial a call, use the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) or [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span> <span data-ttu-id="46028-128">使用**CallId**元素文本值的[PlayOnPhoneResponse （um web 服务）](playonphoneresponse-um-web-service.md)或[PlayOnPhoneGreetingResponse （um web 服务）](playonphonegreetingresponse-um-web-service.md)元素中返回的文本值。</span><span class="sxs-lookup"><span data-stu-id="46028-128">Use the text value that is returned in the [PlayOnPhoneResponse (UM web service)](playonphoneresponse-um-web-service.md) or [PlayOnPhoneGreetingResponse (UM web service)](playonphonegreetingresponse-um-web-service.md) elements for the **CallId** element text value.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="46028-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="46028-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46028-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="46028-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="46028-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="46028-131">Schema Name</span></span>  <br/> |<span data-ttu-id="46028-132">邮件</span><span class="sxs-lookup"><span data-stu-id="46028-132">Messages</span></span>  <br/> |
|<span data-ttu-id="46028-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="46028-133">Validation File</span></span>  <br/> |<span data-ttu-id="46028-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="46028-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="46028-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="46028-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="46028-136">False</span><span class="sxs-lookup"><span data-stu-id="46028-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46028-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="46028-137">See also</span></span>



[<span data-ttu-id="46028-138">GetCallInfo 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-138">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="46028-139">断开连接操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-139">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)
  
[<span data-ttu-id="46028-140">PlayOnPhone 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-140">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)
  
[<span data-ttu-id="46028-141">PlayOnPhoneGreeting 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="46028-141">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

