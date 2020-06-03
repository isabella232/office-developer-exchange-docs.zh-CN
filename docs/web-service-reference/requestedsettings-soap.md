---
title: RequestedSettings （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8d713d22-580c-49a5-99f5-ee532443e89a
description: RequestedSettings 元素包含所请求的配置设置的名称。
ms.openlocfilehash: e94c02d8f92d7aaac619c58f093c536cc1a098bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465294"
---
# <a name="requestedsettings-soap"></a><span data-ttu-id="39473-103">RequestedSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="39473-103">RequestedSettings (SOAP)</span></span>

<span data-ttu-id="39473-104">**RequestedSettings**元素包含所请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="39473-104">The **RequestedSettings** element contains the names of the requested configuration settings.</span></span> 
  
```XML
<RequestedSettings>
   <Setting/>
</RequestedSettings>
```

 <span data-ttu-id="39473-105">**RequestedSettings**</span><span class="sxs-lookup"><span data-stu-id="39473-105">**RequestedSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39473-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="39473-106">Attributes and elements</span></span>

<span data-ttu-id="39473-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="39473-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39473-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="39473-108">Attributes</span></span>

<span data-ttu-id="39473-109">无。</span><span class="sxs-lookup"><span data-stu-id="39473-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39473-110">子元素</span><span class="sxs-lookup"><span data-stu-id="39473-110">Child elements</span></span>

|<span data-ttu-id="39473-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="39473-111">**Element**</span></span>|<span data-ttu-id="39473-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="39473-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39473-113">设置（SOAP）</span><span class="sxs-lookup"><span data-stu-id="39473-113">Setting (SOAP)</span></span>](setting-soap.md) <br/> |<span data-ttu-id="39473-114">表示要返回的配置设置。</span><span class="sxs-lookup"><span data-stu-id="39473-114">Represents a configuration setting to be returned.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39473-115">父元素</span><span class="sxs-lookup"><span data-stu-id="39473-115">Parent elements</span></span>

|<span data-ttu-id="39473-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="39473-116">**Element**</span></span>|<span data-ttu-id="39473-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="39473-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39473-118">GetUserSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="39473-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="39473-119">表示检索一个或多个用户的指定设置的请求。</span><span class="sxs-lookup"><span data-stu-id="39473-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="39473-120">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="39473-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="39473-121">包含请求的配置设置和目标用户。</span><span class="sxs-lookup"><span data-stu-id="39473-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="39473-122">GetDomainSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="39473-122">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="39473-123">表示[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="39473-123">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="39473-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="39473-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39473-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="39473-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="39473-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="39473-126">Schema Name</span></span>  <br/> |<span data-ttu-id="39473-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="39473-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="39473-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="39473-128">Validation File</span></span>  <br/> |<span data-ttu-id="39473-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="39473-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="39473-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="39473-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="39473-131">True</span><span class="sxs-lookup"><span data-stu-id="39473-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39473-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="39473-132">See also</span></span>



[<span data-ttu-id="39473-133">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="39473-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="39473-134">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="39473-134">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

