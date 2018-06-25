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
description: CallId 元素包含表示 GetCallInfo （UM web 服务） 请求或断开连接 （UM web 服务） 请求中的呼叫的标识符的值。
ms.openlocfilehash: 49690f41b9a002b05c7c9b1a1240073c7230ab92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753430"
---
# <a name="callid-um-web-service"></a><span data-ttu-id="208dd-103">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-103">CallId (UM web service)</span></span>

<span data-ttu-id="208dd-104">**CallId**元素包含表示[GetCallInfo （UM web 服务）](getcallinfo-um-web-service.md)请求或[断开连接 （UM web 服务）](disconnect-um-web-service.md)请求中的呼叫的标识符的值。</span><span class="sxs-lookup"><span data-stu-id="208dd-104">The **CallId** element contains the value that represents the identifier of the call in a [GetCallInfo (UM web service)](getcallinfo-um-web-service.md) request or [Disconnect (UM web service)](disconnect-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="208dd-105">GetCallInfo （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-105">GetCallInfo (UM web service)</span></span>](getcallinfo-um-web-service.md)
  
[<span data-ttu-id="208dd-106">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-106">CallId (UM web service)</span></span>](callid-um-web-service.md)
  
[<span data-ttu-id="208dd-107">断开连接 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-107">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md)
  
[<span data-ttu-id="208dd-108">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-108">CallId (UM web service)</span></span>](callid-um-web-service.md)
  
```xml
<CallId/>
```

 <span data-ttu-id="208dd-109">**string**</span><span class="sxs-lookup"><span data-stu-id="208dd-109">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="208dd-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="208dd-110">Attributes and elements</span></span>

<span data-ttu-id="208dd-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="208dd-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="208dd-112">属性</span><span class="sxs-lookup"><span data-stu-id="208dd-112">Attributes</span></span>

<span data-ttu-id="208dd-113">无。</span><span class="sxs-lookup"><span data-stu-id="208dd-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="208dd-114">子元素</span><span class="sxs-lookup"><span data-stu-id="208dd-114">Child elements</span></span>

<span data-ttu-id="208dd-115">无。</span><span class="sxs-lookup"><span data-stu-id="208dd-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="208dd-116">父元素</span><span class="sxs-lookup"><span data-stu-id="208dd-116">Parent elements</span></span>

|<span data-ttu-id="208dd-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="208dd-117">**Element**</span></span>|<span data-ttu-id="208dd-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="208dd-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="208dd-119">GetCallInfo （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-119">GetCallInfo (UM web service)</span></span>](getcallinfo-um-web-service.md) <br/> |<span data-ttu-id="208dd-120">定义一个请求以获取有关调用的信息。</span><span class="sxs-lookup"><span data-stu-id="208dd-120">Defines a request to get information about a call.</span></span>  <br/> |
|[<span data-ttu-id="208dd-121">断开连接 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-121">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md) <br/> |<span data-ttu-id="208dd-122">定义要断开呼叫的请求。</span><span class="sxs-lookup"><span data-stu-id="208dd-122">Defines a request to disconnect a call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="208dd-123">文本值</span><span class="sxs-lookup"><span data-stu-id="208dd-123">Text value</span></span>

<span data-ttu-id="208dd-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="208dd-124">A text value is required.</span></span> <span data-ttu-id="208dd-125">文本值表示呼叫的标识符。</span><span class="sxs-lookup"><span data-stu-id="208dd-125">The text value represents the identifier for a call.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="208dd-126">注解</span><span class="sxs-lookup"><span data-stu-id="208dd-126">Remarks</span></span>

<span data-ttu-id="208dd-127">若要初始呼叫，请使用[PlayOnPhone 操作 （UM web 服务）](playonphone-operation-um-web-service.md)或[PlayOnPhoneGreeting 操作 （UM web 服务）](playonphonegreeting-operation-um-web-service.md)。</span><span class="sxs-lookup"><span data-stu-id="208dd-127">To initial a call, use the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) or [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span> <span data-ttu-id="208dd-128">使用**CallId**元素文本值的[PlayOnPhoneResponse （UM web 服务）](playonphoneresponse-um-web-service.md)或[PlayOnPhoneGreetingResponse （UM web 服务）](playonphonegreetingresponse-um-web-service.md)元素中返回的文本值。</span><span class="sxs-lookup"><span data-stu-id="208dd-128">Use the text value that is returned in the [PlayOnPhoneResponse (UM web service)](playonphoneresponse-um-web-service.md) or [PlayOnPhoneGreetingResponse (UM web service)](playonphonegreetingresponse-um-web-service.md) elements for the **CallId** element text value.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="208dd-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="208dd-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="208dd-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="208dd-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="208dd-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="208dd-131">Schema Name</span></span>  <br/> |<span data-ttu-id="208dd-132">邮件</span><span class="sxs-lookup"><span data-stu-id="208dd-132">Messages</span></span>  <br/> |
|<span data-ttu-id="208dd-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="208dd-133">Validation File</span></span>  <br/> |<span data-ttu-id="208dd-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="208dd-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="208dd-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="208dd-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="208dd-136">False</span><span class="sxs-lookup"><span data-stu-id="208dd-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="208dd-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="208dd-137">See also</span></span>



[<span data-ttu-id="208dd-138">GetCallInfo 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-138">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="208dd-139">断开连接操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-139">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)
  
[<span data-ttu-id="208dd-140">PlayOnPhone 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-140">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)
  
[<span data-ttu-id="208dd-141">PlayOnPhoneGreeting 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="208dd-141">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

