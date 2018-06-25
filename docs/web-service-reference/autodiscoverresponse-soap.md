---
title: AutodiscoverResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 203a5ac3-ebd0-4514-acbe-bc1c74638127
description: AutodiscoverResponse (SOAP) 元素均表示的基元素的所有自动发现服务返回的响应。
ms.openlocfilehash: b92a71deb77e2b1dee42d970e2dc43a56044487a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753302"
---
# <a name="autodiscoverresponse-soap"></a><span data-ttu-id="44dd5-103">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44dd5-103">AutodiscoverResponse (SOAP)</span></span>

<span data-ttu-id="44dd5-104">**AutodiscoverResponse (SOAP)** 元素均表示的基元素的所有自动发现服务返回的响应。</span><span class="sxs-lookup"><span data-stu-id="44dd5-104">The **AutodiscoverResponse (SOAP)** element represents the base element for all responses that are returned by the Autodiscover service.</span></span> 
  
- [<span data-ttu-id="44dd5-105">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44dd5-105">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md)
  
```XML
<AutodiscoverResponse>
    <UserResponses/>
    <UserSettingErrors/>
    <UserSettings/>
</AutodiscoverResponse>

```

 <span data-ttu-id="44dd5-106">**AutodiscoverResponse**</span><span class="sxs-lookup"><span data-stu-id="44dd5-106">**AutodiscoverResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44dd5-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="44dd5-107">Attributes and elements</span></span>

<span data-ttu-id="44dd5-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="44dd5-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44dd5-109">属性</span><span class="sxs-lookup"><span data-stu-id="44dd5-109">Attributes</span></span>

<span data-ttu-id="44dd5-110">无。</span><span class="sxs-lookup"><span data-stu-id="44dd5-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44dd5-111">子元素</span><span class="sxs-lookup"><span data-stu-id="44dd5-111">Child elements</span></span>

|<span data-ttu-id="44dd5-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="44dd5-112">**Element**</span></span>|<span data-ttu-id="44dd5-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="44dd5-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44dd5-114">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44dd5-114">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="44dd5-115">代表[用户回音 (SOAP)](userresponse-soap.md)元素的集合。</span><span class="sxs-lookup"><span data-stu-id="44dd5-115">Represents a collection of [UserResponse (SOAP)](userresponse-soap.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="44dd5-116">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44dd5-116">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="44dd5-117">代表[UserSettingError (SOAP)](usersettingerror-soap.md)元素的集合。</span><span class="sxs-lookup"><span data-stu-id="44dd5-117">Represents a collection of [UserSettingError (SOAP)](usersettingerror-soap.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="44dd5-118">用户设置 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44dd5-118">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="44dd5-119">代表[UserSetting (SOAP)](usersetting-soap.md)元素的集合。</span><span class="sxs-lookup"><span data-stu-id="44dd5-119">Represents a collection of [UserSetting (SOAP)](usersetting-soap.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44dd5-120">父元素</span><span class="sxs-lookup"><span data-stu-id="44dd5-120">Parent elements</span></span>

<span data-ttu-id="44dd5-121">无。</span><span class="sxs-lookup"><span data-stu-id="44dd5-121">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="44dd5-122">文本值</span><span class="sxs-lookup"><span data-stu-id="44dd5-122">Text value</span></span>

<span data-ttu-id="44dd5-123">无。</span><span class="sxs-lookup"><span data-stu-id="44dd5-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44dd5-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="44dd5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44dd5-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="44dd5-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="44dd5-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="44dd5-126">Schema Name</span></span>  <br/> |<span data-ttu-id="44dd5-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="44dd5-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="44dd5-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="44dd5-128">Validation File</span></span>  <br/> |<span data-ttu-id="44dd5-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="44dd5-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="44dd5-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="44dd5-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="44dd5-131">True</span><span class="sxs-lookup"><span data-stu-id="44dd5-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44dd5-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="44dd5-132">See also</span></span>

- [<span data-ttu-id="44dd5-133">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44dd5-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="44dd5-134">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44dd5-134">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)
- [<span data-ttu-id="44dd5-135">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44dd5-135">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

