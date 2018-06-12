---
title: DomainSettingError (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 48c3f7b5-2ee0-42ce-97a1-a881e2f60327
description: DomainSettingError 元素表示检索域设置时出现错误。 这表示 GetDomainSettings 请求中的错误。
ms.openlocfilehash: 08b0a47acea8d35ec78efd701168a251771effac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753984"
---
# <a name="domainsettingerror-soap"></a><span data-ttu-id="025bb-104">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="025bb-104">DomainSettingError (SOAP)</span></span>

<span data-ttu-id="025bb-105">**DomainSettingError**元素表示检索域设置时出现错误。</span><span class="sxs-lookup"><span data-stu-id="025bb-105">The **DomainSettingError** element represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="025bb-106">这表示**GetDomainSettings**请求中的错误。</span><span class="sxs-lookup"><span data-stu-id="025bb-106">This represents an error from a **GetDomainSettings** request.</span></span> 
  
```XML
<DomainSettingError>
   <ErrorCode/>
   <ErrorMessage/>
   <SettingName/>
</DomainSettingError>
```

 <span data-ttu-id="025bb-107">**DomainSettingError**</span><span class="sxs-lookup"><span data-stu-id="025bb-107">**DomainSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="025bb-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="025bb-108">Attributes and elements</span></span>

<span data-ttu-id="025bb-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="025bb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="025bb-110">属性</span><span class="sxs-lookup"><span data-stu-id="025bb-110">Attributes</span></span>

<span data-ttu-id="025bb-111">无。</span><span class="sxs-lookup"><span data-stu-id="025bb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="025bb-112">子元素</span><span class="sxs-lookup"><span data-stu-id="025bb-112">Child elements</span></span>

|<span data-ttu-id="025bb-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="025bb-113">**Element**</span></span>|<span data-ttu-id="025bb-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="025bb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="025bb-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="025bb-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="025bb-116">标识与特定的请求相关联的错误代码。</span><span class="sxs-lookup"><span data-stu-id="025bb-116">Identifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="025bb-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="025bb-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="025bb-118">包含与特定的请求相关联的错误消息。</span><span class="sxs-lookup"><span data-stu-id="025bb-118">Contains the error message that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="025bb-119">SettingName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="025bb-119">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="025bb-120">代表设置的名称。</span><span class="sxs-lookup"><span data-stu-id="025bb-120">Represents the name of the setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="025bb-121">父元素</span><span class="sxs-lookup"><span data-stu-id="025bb-121">Parent elements</span></span>

|<span data-ttu-id="025bb-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="025bb-122">**Element**</span></span>|<span data-ttu-id="025bb-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="025bb-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="025bb-124">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="025bb-124">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="025bb-125">包含错误未能返回的设置的信息。</span><span class="sxs-lookup"><span data-stu-id="025bb-125">Contains error information for settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="025bb-126">文本值</span><span class="sxs-lookup"><span data-stu-id="025bb-126">Text value</span></span>

<span data-ttu-id="025bb-127">无。</span><span class="sxs-lookup"><span data-stu-id="025bb-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="025bb-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="025bb-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="025bb-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="025bb-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="025bb-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="025bb-130">Schema Name</span></span>  <br/> |<span data-ttu-id="025bb-131">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="025bb-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="025bb-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="025bb-132">Validation File</span></span>  <br/> |<span data-ttu-id="025bb-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="025bb-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="025bb-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="025bb-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="025bb-135">True</span><span class="sxs-lookup"><span data-stu-id="025bb-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="025bb-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="025bb-136">See also</span></span>

- [<span data-ttu-id="025bb-137">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="025bb-137">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

