---
title: OofStatus （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: OofStatus 元素包含一个值，该值为发出 GetUMProperties 操作（UM web 服务）请求的用户 indicaties 统一消息 "外出" 状态。
ms.openlocfilehash: 80b1d5aa508579eec14637ed10c322b5fbb670da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460573"
---
# <a name="oofstatus-um-web-service"></a><span data-ttu-id="af34c-103">OofStatus （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="af34c-103">OofStatus (UM web service)</span></span>

<span data-ttu-id="af34c-104">**OofStatus**元素包含一个值，该值为发出[GETUMPROPERTIES 操作（UM web 服务）](getumproperties-operation-um-web-service.md)请求的用户 indicaties 统一消息 "外出" 状态。</span><span class="sxs-lookup"><span data-stu-id="af34c-104">The **OofStatus** element contains a value that indicaties the Unified Messaging Out of Office status for the user who is making a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="af34c-105">GetUMPropertiesResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="af34c-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
[<span data-ttu-id="af34c-106">OofStatus （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="af34c-106">OofStatus (UM web service)</span></span>](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="af34c-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="af34c-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af34c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="af34c-108">Attributes and elements</span></span>

<span data-ttu-id="af34c-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="af34c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af34c-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="af34c-110">Attributes</span></span>

<span data-ttu-id="af34c-111">无。</span><span class="sxs-lookup"><span data-stu-id="af34c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af34c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="af34c-112">Child elements</span></span>

<span data-ttu-id="af34c-113">无。</span><span class="sxs-lookup"><span data-stu-id="af34c-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af34c-114">父元素</span><span class="sxs-lookup"><span data-stu-id="af34c-114">Parent elements</span></span>

|<span data-ttu-id="af34c-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="af34c-115">**Element**</span></span>|<span data-ttu-id="af34c-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="af34c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af34c-117">GetUMPropertiesResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="af34c-117">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md) <br/> |<span data-ttu-id="af34c-118">定义对[GetUMProperties 操作（UM web 服务）](getumproperties-operation-um-web-service.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="af34c-118">Defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="af34c-119">文本值</span><span class="sxs-lookup"><span data-stu-id="af34c-119">Text value</span></span>

<span data-ttu-id="af34c-120">布尔文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="af34c-120">A Boolean text value is required.</span></span> <span data-ttu-id="af34c-121">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="af34c-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="af34c-122">True</span><span class="sxs-lookup"><span data-stu-id="af34c-122">True</span></span>
    
- <span data-ttu-id="af34c-123">False</span><span class="sxs-lookup"><span data-stu-id="af34c-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="af34c-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="af34c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af34c-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="af34c-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="af34c-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="af34c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="af34c-127">邮件</span><span class="sxs-lookup"><span data-stu-id="af34c-127">Messages</span></span>  <br/> |
|<span data-ttu-id="af34c-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="af34c-128">Validation File</span></span>  <br/> |<span data-ttu-id="af34c-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="af34c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="af34c-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="af34c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="af34c-131">False</span><span class="sxs-lookup"><span data-stu-id="af34c-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af34c-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af34c-132">See also</span></span>



[<span data-ttu-id="af34c-133">GetUMProperties 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="af34c-133">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)
  
[<span data-ttu-id="af34c-134">GetUMPropertiesResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="af34c-134">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)

