---
title: dialString （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- dialString
api_type:
- schema
ms.assetid: d1e3cd23-48fe-4ebc-a5c5-2226d223f800
description: DialString 元素包含要拨打的电话号码的值。
ms.openlocfilehash: f27934fa73ead75ab50e99a79c01cb6a1062e3d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753862"
---
# <a name="dialstring-um-web-service"></a><span data-ttu-id="557ed-103">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-103">dialString (UM web service)</span></span>

<span data-ttu-id="557ed-104">**DialString**元素包含要拨打的电话号码的值。</span><span class="sxs-lookup"><span data-stu-id="557ed-104">The **dialString** element contains the value for the telephone number to dial.</span></span> 
  
- [<span data-ttu-id="557ed-105">PlayOnPhone （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-105">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md) 
- [<span data-ttu-id="557ed-106">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-106">dialString (UM web service)</span></span>](dialstring-um-web-service.md) 
- [<span data-ttu-id="557ed-107">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-107">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md) 
- [<span data-ttu-id="557ed-108">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-108">dialString (UM web service)</span></span>](dialstring-um-web-service.md)
  
```xml
<dialString/>
```

 <span data-ttu-id="557ed-109">**string**</span><span class="sxs-lookup"><span data-stu-id="557ed-109">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="557ed-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="557ed-110">Attributes and elements</span></span>

<span data-ttu-id="557ed-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="557ed-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="557ed-112">属性</span><span class="sxs-lookup"><span data-stu-id="557ed-112">Attributes</span></span>

<span data-ttu-id="557ed-113">无。</span><span class="sxs-lookup"><span data-stu-id="557ed-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="557ed-114">子元素</span><span class="sxs-lookup"><span data-stu-id="557ed-114">Child elements</span></span>

<span data-ttu-id="557ed-115">无。</span><span class="sxs-lookup"><span data-stu-id="557ed-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="557ed-116">父元素</span><span class="sxs-lookup"><span data-stu-id="557ed-116">Parent elements</span></span>

|<span data-ttu-id="557ed-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="557ed-117">**Element**</span></span>|<span data-ttu-id="557ed-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="557ed-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="557ed-119">PlayOnPhone （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-119">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md) <br/> |<span data-ttu-id="557ed-120">定义在电话上播放消息的请求。</span><span class="sxs-lookup"><span data-stu-id="557ed-120">Defines a request to play a message on a telephone.</span></span>  <br/> |
|[<span data-ttu-id="557ed-121">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-121">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md) <br/> |<span data-ttu-id="557ed-122">定义在电话上播放问候语的请求。</span><span class="sxs-lookup"><span data-stu-id="557ed-122">Defines a request to play a greeting on a telephone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="557ed-123">文本值</span><span class="sxs-lookup"><span data-stu-id="557ed-123">Text value</span></span>

<span data-ttu-id="557ed-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="557ed-124">A text value is required.</span></span> <span data-ttu-id="557ed-125">文本值必须包含有效的分机号码。</span><span class="sxs-lookup"><span data-stu-id="557ed-125">The text value must contain a valid dialing number.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="557ed-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="557ed-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="557ed-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="557ed-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="557ed-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="557ed-128">Schema Name</span></span>  <br/> |<span data-ttu-id="557ed-129">邮件</span><span class="sxs-lookup"><span data-stu-id="557ed-129">Messages</span></span>  <br/> |
|<span data-ttu-id="557ed-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="557ed-130">Validation File</span></span>  <br/> |<span data-ttu-id="557ed-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="557ed-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="557ed-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="557ed-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="557ed-133">False</span><span class="sxs-lookup"><span data-stu-id="557ed-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="557ed-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="557ed-134">See also</span></span>

- [<span data-ttu-id="557ed-135">PlayOnPhone （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-135">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md)  
- [<span data-ttu-id="557ed-136">PlayOnPhone 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-136">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)  
- [<span data-ttu-id="557ed-137">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-137">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md)  
- [<span data-ttu-id="557ed-138">PlayOnPhoneGreeting 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="557ed-138">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

