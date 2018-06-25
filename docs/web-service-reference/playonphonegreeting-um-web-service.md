---
title: PlayOnPhoneGreeting （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 43eda596-3609-4e1b-8502-1db2636535cf
description: PlayOnPhoneGreeting 元素定义要播放的统一消息电话问候语的请求。
ms.openlocfilehash: c30140fc60b9e902517b4cc18deb9b61efa61e0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826836"
---
# <a name="playonphonegreeting-um-web-service"></a><span data-ttu-id="cbdd0-103">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cbdd0-103">PlayOnPhoneGreeting (UM web service)</span></span>

<span data-ttu-id="cbdd0-104">**PlayOnPhoneGreeting**元素定义要播放的统一消息电话问候语的请求。</span><span class="sxs-lookup"><span data-stu-id="cbdd0-104">The **PlayOnPhoneGreeting** element defines a request to play a Unified Messaging greeting on a telephone.</span></span> 
  
[<span data-ttu-id="cbdd0-105">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cbdd0-105">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md)
  
```xml
<PlayOnPhoneGreeting>
  <GreetingType/>
  <DialString/>
</PlayOnPhoneGreeting>
```

 <span data-ttu-id="cbdd0-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="cbdd0-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cbdd0-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cbdd0-107">Attributes and elements</span></span>

<span data-ttu-id="cbdd0-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cbdd0-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbdd0-109">属性</span><span class="sxs-lookup"><span data-stu-id="cbdd0-109">Attributes</span></span>

<span data-ttu-id="cbdd0-110">无。</span><span class="sxs-lookup"><span data-stu-id="cbdd0-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cbdd0-111">子元素</span><span class="sxs-lookup"><span data-stu-id="cbdd0-111">Child elements</span></span>

|<span data-ttu-id="cbdd0-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="cbdd0-112">**Element**</span></span>|<span data-ttu-id="cbdd0-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="cbdd0-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbdd0-114">GreetingType （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cbdd0-114">GreetingType (UM web service)</span></span>](greetingtype-um-web-service.md) <br/> |<span data-ttu-id="cbdd0-115">定义问候语[PlayOnPhoneGreeting 操作 （UM web 服务）](playonphonegreeting-operation-um-web-service.md)请求中使用的类型。</span><span class="sxs-lookup"><span data-stu-id="cbdd0-115">Defines the type of greeting to use in a [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) request.</span></span>  <br/> |
|[<span data-ttu-id="cbdd0-116">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cbdd0-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="cbdd0-117">包含要拨打的电话号码的值。</span><span class="sxs-lookup"><span data-stu-id="cbdd0-117">Contains the value for the telephone number to dial.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cbdd0-118">父元素</span><span class="sxs-lookup"><span data-stu-id="cbdd0-118">Parent elements</span></span>

<span data-ttu-id="cbdd0-119">无。</span><span class="sxs-lookup"><span data-stu-id="cbdd0-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cbdd0-120">文本值</span><span class="sxs-lookup"><span data-stu-id="cbdd0-120">Text value</span></span>

<span data-ttu-id="cbdd0-121">无。</span><span class="sxs-lookup"><span data-stu-id="cbdd0-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cbdd0-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="cbdd0-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbdd0-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="cbdd0-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cbdd0-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="cbdd0-124">Schema Name</span></span>  <br/> |<span data-ttu-id="cbdd0-125">邮件</span><span class="sxs-lookup"><span data-stu-id="cbdd0-125">Messages</span></span>  <br/> |
|<span data-ttu-id="cbdd0-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="cbdd0-126">Validation File</span></span>  <br/> |<span data-ttu-id="cbdd0-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cbdd0-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cbdd0-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="cbdd0-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="cbdd0-129">False</span><span class="sxs-lookup"><span data-stu-id="cbdd0-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbdd0-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cbdd0-130">See also</span></span>



[<span data-ttu-id="cbdd0-131">PlayOnPhoneGreeting 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cbdd0-131">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

