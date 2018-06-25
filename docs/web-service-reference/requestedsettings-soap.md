---
title: RequestedSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8d713d22-580c-49a5-99f5-ee532443e89a
description: RequestedSettings 元素包含请求的配置设置的名称。
ms.openlocfilehash: 025f86d417ea2041a3247ac67b065d75c8f75599
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827136"
---
# <a name="requestedsettings-soap"></a><span data-ttu-id="4e61d-103">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e61d-103">RequestedSettings (SOAP)</span></span>

<span data-ttu-id="4e61d-104">**RequestedSettings**元素包含请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="4e61d-104">The **RequestedSettings** element contains the names of the requested configuration settings.</span></span> 
  
```XML
<RequestedSettings>
   <Setting/>
</RequestedSettings>
```

 <span data-ttu-id="4e61d-105">**RequestedSettings**</span><span class="sxs-lookup"><span data-stu-id="4e61d-105">**RequestedSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e61d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4e61d-106">Attributes and elements</span></span>

<span data-ttu-id="4e61d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4e61d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e61d-108">属性</span><span class="sxs-lookup"><span data-stu-id="4e61d-108">Attributes</span></span>

<span data-ttu-id="4e61d-109">无。</span><span class="sxs-lookup"><span data-stu-id="4e61d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e61d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4e61d-110">Child elements</span></span>

|<span data-ttu-id="4e61d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e61d-111">**Element**</span></span>|<span data-ttu-id="4e61d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e61d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e61d-113">设置 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e61d-113">Setting (SOAP)</span></span>](setting-soap.md) <br/> |<span data-ttu-id="4e61d-114">代表要返回的配置设置。</span><span class="sxs-lookup"><span data-stu-id="4e61d-114">Represents a configuration setting to be returned.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4e61d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4e61d-115">Parent elements</span></span>

|<span data-ttu-id="4e61d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e61d-116">**Element**</span></span>|<span data-ttu-id="4e61d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e61d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e61d-118">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e61d-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="4e61d-119">表示检索指定的设置为一个或多个用户的请求。</span><span class="sxs-lookup"><span data-stu-id="4e61d-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="4e61d-120">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e61d-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="4e61d-121">包含请求的配置设置和目标用户。</span><span class="sxs-lookup"><span data-stu-id="4e61d-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="4e61d-122">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e61d-122">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="4e61d-123">代表[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="4e61d-123">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="4e61d-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="4e61d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e61d-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="4e61d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="4e61d-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="4e61d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="4e61d-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="4e61d-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="4e61d-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="4e61d-128">Validation File</span></span>  <br/> |<span data-ttu-id="4e61d-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4e61d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4e61d-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="4e61d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e61d-131">True</span><span class="sxs-lookup"><span data-stu-id="4e61d-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e61d-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4e61d-132">See also</span></span>



[<span data-ttu-id="4e61d-133">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e61d-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="4e61d-134">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e61d-134">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

