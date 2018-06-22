---
title: EventCause （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: EventCause 元素包含一个值，指示 GetCallInfo 操作 （UM web 服务） 请求的响应中的呼叫事件的原因。
ms.openlocfilehash: dd73d93527bebb3b522ad0a6cdae5b9faee1a6a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754161"
---
# <a name="eventcause-um-web-service"></a><span data-ttu-id="25b58-103">EventCause （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="25b58-103">EventCause (UM web service)</span></span>

<span data-ttu-id="25b58-104">**EventCause**元素包含一个值，指示[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)请求的响应中的呼叫事件的原因。</span><span class="sxs-lookup"><span data-stu-id="25b58-104">The **EventCause** element contains a value that indicates the cause for a call event in a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="25b58-105">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="25b58-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="25b58-106">EventCause （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="25b58-106">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 <span data-ttu-id="25b58-107">**UMEventCause**</span><span class="sxs-lookup"><span data-stu-id="25b58-107">**UMEventCause**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25b58-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="25b58-108">Attributes and elements</span></span>

<span data-ttu-id="25b58-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="25b58-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25b58-110">属性</span><span class="sxs-lookup"><span data-stu-id="25b58-110">Attributes</span></span>

<span data-ttu-id="25b58-111">无。</span><span class="sxs-lookup"><span data-stu-id="25b58-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25b58-112">子元素</span><span class="sxs-lookup"><span data-stu-id="25b58-112">Child elements</span></span>

<span data-ttu-id="25b58-113">无。</span><span class="sxs-lookup"><span data-stu-id="25b58-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25b58-114">父元素</span><span class="sxs-lookup"><span data-stu-id="25b58-114">Parent elements</span></span>

|<span data-ttu-id="25b58-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="25b58-115">**Element**</span></span>|<span data-ttu-id="25b58-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="25b58-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25b58-117">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="25b58-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="25b58-118">定义[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="25b58-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25b58-119">文本值</span><span class="sxs-lookup"><span data-stu-id="25b58-119">Text value</span></span>

<span data-ttu-id="25b58-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="25b58-120">A text value is required.</span></span> <span data-ttu-id="25b58-121">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="25b58-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="25b58-122">无</span><span class="sxs-lookup"><span data-stu-id="25b58-122">None</span></span>
    
- <span data-ttu-id="25b58-123">UserBusy</span><span class="sxs-lookup"><span data-stu-id="25b58-123">UserBusy</span></span>
    
- <span data-ttu-id="25b58-124">NoAnswer</span><span class="sxs-lookup"><span data-stu-id="25b58-124">NoAnswer</span></span>
    
- <span data-ttu-id="25b58-125">其他</span><span class="sxs-lookup"><span data-stu-id="25b58-125">Other</span></span>
    
## <a name="element-information"></a><span data-ttu-id="25b58-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="25b58-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25b58-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="25b58-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="25b58-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="25b58-128">Schema Name</span></span>  <br/> |<span data-ttu-id="25b58-129">邮件</span><span class="sxs-lookup"><span data-stu-id="25b58-129">Messages</span></span>  <br/> |
|<span data-ttu-id="25b58-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="25b58-130">Validation File</span></span>  <br/> |<span data-ttu-id="25b58-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="25b58-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="25b58-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="25b58-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="25b58-133">False</span><span class="sxs-lookup"><span data-stu-id="25b58-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25b58-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="25b58-134">See also</span></span>



[<span data-ttu-id="25b58-135">GetCallInfo 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="25b58-135">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="25b58-136">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="25b58-136">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

