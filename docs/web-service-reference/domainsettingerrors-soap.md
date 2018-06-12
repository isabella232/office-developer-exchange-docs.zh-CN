---
title: DomainSettingErrors (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a4ce19de-f560-4984-8047-ecbbc86c9b91
description: DomainSettingsErrors 元素包含错误未能返回的设置信息。
ms.openlocfilehash: 6ecd23bc556ca32d724581a28cc7c117c6853207
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753991"
---
# <a name="domainsettingerrors-soap"></a><span data-ttu-id="bfe1a-103">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bfe1a-103">DomainSettingErrors (SOAP)</span></span>

<span data-ttu-id="bfe1a-104">**DomainSettingsErrors**元素包含错误未能返回的设置信息。</span><span class="sxs-lookup"><span data-stu-id="bfe1a-104">The **DomainSettingsErrors** element contains error information for settings that could not be returned.</span></span> 
  
```XML
<DomainSettingsErrors>
   <DomainSettingsError/>
</DomainSettingsErrors>
```

 <span data-ttu-id="bfe1a-105">**DomainSettingsErrors**</span><span class="sxs-lookup"><span data-stu-id="bfe1a-105">**DomainSettingsErrors**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bfe1a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bfe1a-106">Attributes and elements</span></span>

<span data-ttu-id="bfe1a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bfe1a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bfe1a-108">属性</span><span class="sxs-lookup"><span data-stu-id="bfe1a-108">Attributes</span></span>

<span data-ttu-id="bfe1a-109">无。</span><span class="sxs-lookup"><span data-stu-id="bfe1a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bfe1a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bfe1a-110">Child elements</span></span>

|<span data-ttu-id="bfe1a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="bfe1a-111">**Element**</span></span>|<span data-ttu-id="bfe1a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="bfe1a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfe1a-113">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bfe1a-113">DomainSettingError (SOAP)</span></span>](domainsettingerror-soap.md) <br/> |<span data-ttu-id="bfe1a-114">代表检索域设置时出现的错误。</span><span class="sxs-lookup"><span data-stu-id="bfe1a-114">Represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="bfe1a-115">这表示[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)操作要求中的错误。</span><span class="sxs-lookup"><span data-stu-id="bfe1a-115">This represents an error from a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bfe1a-116">父元素</span><span class="sxs-lookup"><span data-stu-id="bfe1a-116">Parent elements</span></span>

|<span data-ttu-id="bfe1a-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="bfe1a-117">**Element**</span></span>|<span data-ttu-id="bfe1a-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="bfe1a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfe1a-119">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bfe1a-119">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="bfe1a-120">包含指定的域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="bfe1a-120">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bfe1a-121">文本值</span><span class="sxs-lookup"><span data-stu-id="bfe1a-121">Text value</span></span>

<span data-ttu-id="bfe1a-122">无。</span><span class="sxs-lookup"><span data-stu-id="bfe1a-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bfe1a-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="bfe1a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfe1a-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="bfe1a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="bfe1a-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="bfe1a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="bfe1a-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="bfe1a-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="bfe1a-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="bfe1a-127">Validation File</span></span>  <br/> |<span data-ttu-id="bfe1a-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bfe1a-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bfe1a-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="bfe1a-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="bfe1a-130">True</span><span class="sxs-lookup"><span data-stu-id="bfe1a-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfe1a-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bfe1a-131">See also</span></span>

- [<span data-ttu-id="bfe1a-132">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bfe1a-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

