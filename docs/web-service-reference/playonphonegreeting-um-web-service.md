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
description: PlayOnPhoneGreeting 元素定义一个请求，以在电话上播放统一消息问候语。
ms.openlocfilehash: 197e4ba671e1711b73b1e7c239339db589357581
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529922"
---
# <a name="playonphonegreeting-um-web-service"></a><span data-ttu-id="36666-103">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="36666-103">PlayOnPhoneGreeting (UM web service)</span></span>

<span data-ttu-id="36666-104">**PlayOnPhoneGreeting**元素定义一个请求，以在电话上播放统一消息问候语。</span><span class="sxs-lookup"><span data-stu-id="36666-104">The **PlayOnPhoneGreeting** element defines a request to play a Unified Messaging greeting on a telephone.</span></span> 
  
[<span data-ttu-id="36666-105">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="36666-105">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md)
  
```xml
<PlayOnPhoneGreeting>
  <GreetingType/>
  <DialString/>
</PlayOnPhoneGreeting>
```

 <span data-ttu-id="36666-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="36666-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36666-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="36666-107">Attributes and elements</span></span>

<span data-ttu-id="36666-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="36666-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36666-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="36666-109">Attributes</span></span>

<span data-ttu-id="36666-110">无。</span><span class="sxs-lookup"><span data-stu-id="36666-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36666-111">子元素</span><span class="sxs-lookup"><span data-stu-id="36666-111">Child elements</span></span>

|<span data-ttu-id="36666-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="36666-112">**Element**</span></span>|<span data-ttu-id="36666-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="36666-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36666-114">GreetingType （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="36666-114">GreetingType (UM web service)</span></span>](greetingtype-um-web-service.md) <br/> |<span data-ttu-id="36666-115">定义要在[PlayOnPhoneGreeting 操作（UM web 服务）](playonphonegreeting-operation-um-web-service.md)请求中使用的问候语的类型。</span><span class="sxs-lookup"><span data-stu-id="36666-115">Defines the type of greeting to use in a [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) request.</span></span>  <br/> |
|[<span data-ttu-id="36666-116">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="36666-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="36666-117">包含要拨打的电话号码的值。</span><span class="sxs-lookup"><span data-stu-id="36666-117">Contains the value for the telephone number to dial.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="36666-118">父元素</span><span class="sxs-lookup"><span data-stu-id="36666-118">Parent elements</span></span>

<span data-ttu-id="36666-119">无。</span><span class="sxs-lookup"><span data-stu-id="36666-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="36666-120">文本值</span><span class="sxs-lookup"><span data-stu-id="36666-120">Text value</span></span>

<span data-ttu-id="36666-121">无。</span><span class="sxs-lookup"><span data-stu-id="36666-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36666-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="36666-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36666-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="36666-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="36666-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="36666-124">Schema Name</span></span>  <br/> |<span data-ttu-id="36666-125">邮件</span><span class="sxs-lookup"><span data-stu-id="36666-125">Messages</span></span>  <br/> |
|<span data-ttu-id="36666-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="36666-126">Validation File</span></span>  <br/> |<span data-ttu-id="36666-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="36666-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="36666-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="36666-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="36666-129">False</span><span class="sxs-lookup"><span data-stu-id="36666-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36666-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36666-130">See also</span></span>



[<span data-ttu-id="36666-131">PlayOnPhoneGreeting 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="36666-131">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

