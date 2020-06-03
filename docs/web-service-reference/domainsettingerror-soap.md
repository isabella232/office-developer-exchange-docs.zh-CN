---
title: DomainSettingError （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 48c3f7b5-2ee0-42ce-97a1-a881e2f60327
description: DomainSettingError 元素表示检索域设置时发生的错误。 这表示来自 GetDomainSettings 请求的一个错误。
ms.openlocfilehash: 189a614e7629033c8db2f60b8fd3679835a696ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530710"
---
# <a name="domainsettingerror-soap"></a><span data-ttu-id="6c870-104">DomainSettingError （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c870-104">DomainSettingError (SOAP)</span></span>

<span data-ttu-id="6c870-105">**DomainSettingError**元素表示检索域设置时发生的错误。</span><span class="sxs-lookup"><span data-stu-id="6c870-105">The **DomainSettingError** element represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="6c870-106">这表示来自**GetDomainSettings**请求的一个错误。</span><span class="sxs-lookup"><span data-stu-id="6c870-106">This represents an error from a **GetDomainSettings** request.</span></span> 
  
```XML
<DomainSettingError>
   <ErrorCode/>
   <ErrorMessage/>
   <SettingName/>
</DomainSettingError>
```

 <span data-ttu-id="6c870-107">**DomainSettingError**</span><span class="sxs-lookup"><span data-stu-id="6c870-107">**DomainSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c870-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6c870-108">Attributes and elements</span></span>

<span data-ttu-id="6c870-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6c870-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c870-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="6c870-110">Attributes</span></span>

<span data-ttu-id="6c870-111">无。</span><span class="sxs-lookup"><span data-stu-id="6c870-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c870-112">子元素</span><span class="sxs-lookup"><span data-stu-id="6c870-112">Child elements</span></span>

|<span data-ttu-id="6c870-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c870-113">**Element**</span></span>|<span data-ttu-id="6c870-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c870-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c870-115">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c870-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="6c870-116">标识与特定请求相关联的错误代码。</span><span class="sxs-lookup"><span data-stu-id="6c870-116">Identifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="6c870-117">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c870-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="6c870-118">包含与特定请求相关联的错误消息。</span><span class="sxs-lookup"><span data-stu-id="6c870-118">Contains the error message that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="6c870-119">SettingName （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c870-119">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="6c870-120">表示设置的名称。</span><span class="sxs-lookup"><span data-stu-id="6c870-120">Represents the name of the setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6c870-121">父元素</span><span class="sxs-lookup"><span data-stu-id="6c870-121">Parent elements</span></span>

|<span data-ttu-id="6c870-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c870-122">**Element**</span></span>|<span data-ttu-id="6c870-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c870-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c870-124">DomainSettingErrors （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c870-124">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="6c870-125">包含无法返回的设置的错误消息。</span><span class="sxs-lookup"><span data-stu-id="6c870-125">Contains error information for settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6c870-126">文本值</span><span class="sxs-lookup"><span data-stu-id="6c870-126">Text value</span></span>

<span data-ttu-id="6c870-127">无。</span><span class="sxs-lookup"><span data-stu-id="6c870-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c870-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="6c870-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c870-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="6c870-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6c870-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="6c870-130">Schema Name</span></span>  <br/> |<span data-ttu-id="6c870-131">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="6c870-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6c870-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="6c870-132">Validation File</span></span>  <br/> |<span data-ttu-id="6c870-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6c870-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6c870-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="6c870-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c870-135">True</span><span class="sxs-lookup"><span data-stu-id="6c870-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c870-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c870-136">See also</span></span>

- [<span data-ttu-id="6c870-137">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6c870-137">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

