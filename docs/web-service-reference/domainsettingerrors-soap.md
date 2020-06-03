---
title: DomainSettingErrors （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a4ce19de-f560-4984-8047-ecbbc86c9b91
description: DomainSettingsErrors 元素包含无法返回的设置的错误消息。
ms.openlocfilehash: 4e7ee29c2bc680a1938b75189c2ac3c214f7d2b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530703"
---
# <a name="domainsettingerrors-soap"></a><span data-ttu-id="c2632-103">DomainSettingErrors （SOAP）</span><span class="sxs-lookup"><span data-stu-id="c2632-103">DomainSettingErrors (SOAP)</span></span>

<span data-ttu-id="c2632-104">**DomainSettingsErrors**元素包含无法返回的设置的错误消息。</span><span class="sxs-lookup"><span data-stu-id="c2632-104">The **DomainSettingsErrors** element contains error information for settings that could not be returned.</span></span> 
  
```XML
<DomainSettingsErrors>
   <DomainSettingsError/>
</DomainSettingsErrors>
```

 <span data-ttu-id="c2632-105">**DomainSettingsErrors**</span><span class="sxs-lookup"><span data-stu-id="c2632-105">**DomainSettingsErrors**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2632-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c2632-106">Attributes and elements</span></span>

<span data-ttu-id="c2632-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c2632-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2632-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c2632-108">Attributes</span></span>

<span data-ttu-id="c2632-109">无。</span><span class="sxs-lookup"><span data-stu-id="c2632-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2632-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c2632-110">Child elements</span></span>

|<span data-ttu-id="c2632-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c2632-111">**Element**</span></span>|<span data-ttu-id="c2632-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c2632-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2632-113">DomainSettingError （SOAP）</span><span class="sxs-lookup"><span data-stu-id="c2632-113">DomainSettingError (SOAP)</span></span>](domainsettingerror-soap.md) <br/> |<span data-ttu-id="c2632-114">表示检索域设置时发生的错误。</span><span class="sxs-lookup"><span data-stu-id="c2632-114">Represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="c2632-115">这表示[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)操作请求中的一个错误。</span><span class="sxs-lookup"><span data-stu-id="c2632-115">This represents an error from a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c2632-116">父元素</span><span class="sxs-lookup"><span data-stu-id="c2632-116">Parent elements</span></span>

|<span data-ttu-id="c2632-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="c2632-117">**Element**</span></span>|<span data-ttu-id="c2632-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="c2632-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2632-119">DomainResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="c2632-119">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="c2632-120">包含指定域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="c2632-120">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c2632-121">文本值</span><span class="sxs-lookup"><span data-stu-id="c2632-121">Text value</span></span>

<span data-ttu-id="c2632-122">无。</span><span class="sxs-lookup"><span data-stu-id="c2632-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2632-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="c2632-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2632-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="c2632-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="c2632-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="c2632-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c2632-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="c2632-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="c2632-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="c2632-127">Validation File</span></span>  <br/> |<span data-ttu-id="c2632-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c2632-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c2632-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="c2632-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="c2632-130">True</span><span class="sxs-lookup"><span data-stu-id="c2632-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2632-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2632-131">See also</span></span>

- [<span data-ttu-id="c2632-132">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c2632-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

