---
title: GetCallInfoResponse （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: GetCallInfoResponse 元素定义 GetCallInfo 操作 （UM web 服务） 请求的响应。
ms.openlocfilehash: d9658dd9cb47f925e05dc21a8651c98dce1f0a2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754479"
---
# <a name="getcallinforesponse-um-web-service"></a><span data-ttu-id="241e1-103">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="241e1-103">GetCallInfoResponse (UM web service)</span></span>

<span data-ttu-id="241e1-104">**GetCallInfoResponse**元素定义[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="241e1-104">The **GetCallInfoResponse** element defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="241e1-105">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="241e1-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <CallState/>
  <EventCause/>
</GetCallInfoResponse>
```

 <span data-ttu-id="241e1-106">**UMCallInfo**</span><span class="sxs-lookup"><span data-stu-id="241e1-106">**UMCallInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="241e1-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="241e1-107">Attributes and elements</span></span>

<span data-ttu-id="241e1-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="241e1-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="241e1-109">属性</span><span class="sxs-lookup"><span data-stu-id="241e1-109">Attributes</span></span>

<span data-ttu-id="241e1-110">无。</span><span class="sxs-lookup"><span data-stu-id="241e1-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="241e1-111">子元素</span><span class="sxs-lookup"><span data-stu-id="241e1-111">Child elements</span></span>

|<span data-ttu-id="241e1-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="241e1-112">**Element**</span></span>|<span data-ttu-id="241e1-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="241e1-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="241e1-114">CallState</span><span class="sxs-lookup"><span data-stu-id="241e1-114">CallState</span></span>  <br/> |<span data-ttu-id="241e1-115">包含一个值，指示的呼叫状态[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)请求信息。</span><span class="sxs-lookup"><span data-stu-id="241e1-115">Contains a value that indicates the status of a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.</span></span>  <br/> |
|<span data-ttu-id="241e1-116">EventCause</span><span class="sxs-lookup"><span data-stu-id="241e1-116">EventCause</span></span>  <br/> |<span data-ttu-id="241e1-117">包含一个值，指示呼叫事件的原因[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)请求信息。</span><span class="sxs-lookup"><span data-stu-id="241e1-117">Contains a value that indicates the cause of an event for a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="241e1-118">父元素</span><span class="sxs-lookup"><span data-stu-id="241e1-118">Parent elements</span></span>

<span data-ttu-id="241e1-119">无。</span><span class="sxs-lookup"><span data-stu-id="241e1-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="241e1-120">文本值</span><span class="sxs-lookup"><span data-stu-id="241e1-120">Text value</span></span>

<span data-ttu-id="241e1-121">无。</span><span class="sxs-lookup"><span data-stu-id="241e1-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="241e1-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="241e1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="241e1-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="241e1-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="241e1-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="241e1-124">Schema Name</span></span>  <br/> |<span data-ttu-id="241e1-125">邮件</span><span class="sxs-lookup"><span data-stu-id="241e1-125">Messages</span></span>  <br/> |
|<span data-ttu-id="241e1-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="241e1-126">Validation File</span></span>  <br/> |<span data-ttu-id="241e1-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="241e1-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="241e1-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="241e1-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="241e1-129">False</span><span class="sxs-lookup"><span data-stu-id="241e1-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="241e1-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="241e1-130">See also</span></span>



[<span data-ttu-id="241e1-131">GetCallInfo 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="241e1-131">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="241e1-132">CallState （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="241e1-132">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
[<span data-ttu-id="241e1-133">EventCause （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="241e1-133">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)

