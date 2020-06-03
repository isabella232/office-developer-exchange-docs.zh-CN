---
title: GetDomainSettingsRequest （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5ac0ff6d-9e02-4e4c-973d-cd9e076661d5
description: GetDomainSettingsRequest 元素表示 GetDomainSettings 操作（SOAP）操作请求。
ms.openlocfilehash: 400016d0817131fb70ec7ff3db7fbfdc1b51f8f9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460958"
---
# <a name="getdomainsettingsrequest-soap"></a><span data-ttu-id="81e1e-103">GetDomainSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="81e1e-103">GetDomainSettingsRequest (SOAP)</span></span>

<span data-ttu-id="81e1e-104">**GetDomainSettingsRequest**元素表示[GETDOMAINSETTINGS 操作（SOAP）](getdomainsettings-operation-soap.md)操作请求。</span><span class="sxs-lookup"><span data-stu-id="81e1e-104">The **GetDomainSettingsRequest** element represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<GetDomainSettingsRequest>
   <Domains/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetDomainSettingsRequest>
```

 <span data-ttu-id="81e1e-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="81e1e-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81e1e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="81e1e-106">Attributes and elements</span></span>

<span data-ttu-id="81e1e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="81e1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81e1e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="81e1e-108">Attributes</span></span>

<span data-ttu-id="81e1e-109">无。</span><span class="sxs-lookup"><span data-stu-id="81e1e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81e1e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="81e1e-110">Child elements</span></span>

|<span data-ttu-id="81e1e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="81e1e-111">**Element**</span></span>|<span data-ttu-id="81e1e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="81e1e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81e1e-113">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="81e1e-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="81e1e-114">代表域标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="81e1e-114">Represents a collection of domain identifiers.</span></span>  <br/> |
|[<span data-ttu-id="81e1e-115">RequestedSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="81e1e-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="81e1e-116">包含所请求的域配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="81e1e-116">Contains the names of the requested domain configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="81e1e-117">RequestedVersion （SOAP）</span><span class="sxs-lookup"><span data-stu-id="81e1e-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="81e1e-118">指定提供程序将使用的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="81e1e-118">Specifies the server version that the provider will use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="81e1e-119">父元素</span><span class="sxs-lookup"><span data-stu-id="81e1e-119">Parent elements</span></span>

<span data-ttu-id="81e1e-120">无。</span><span class="sxs-lookup"><span data-stu-id="81e1e-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="81e1e-121">文本值</span><span class="sxs-lookup"><span data-stu-id="81e1e-121">Text value</span></span>

<span data-ttu-id="81e1e-122">无。</span><span class="sxs-lookup"><span data-stu-id="81e1e-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81e1e-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="81e1e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81e1e-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="81e1e-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="81e1e-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="81e1e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="81e1e-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="81e1e-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="81e1e-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="81e1e-127">Validation File</span></span>  <br/> |<span data-ttu-id="81e1e-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="81e1e-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="81e1e-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="81e1e-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="81e1e-130">True</span><span class="sxs-lookup"><span data-stu-id="81e1e-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81e1e-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="81e1e-131">See also</span></span>



[<span data-ttu-id="81e1e-132">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="81e1e-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

