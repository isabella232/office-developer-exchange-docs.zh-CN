---
title: RequestedVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 962036c9-9b13-4669-bed2-2502c0f5aabe
description: RequestedVersion元素指定客户端需要在处理请求的最小服务版本。
ms.openlocfilehash: ded276b3eb2c70b6edd39ca12289098de2b3faea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459165"
---
# <a name="requestedversion-soap"></a><span data-ttu-id="a75e0-103">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a75e0-103">RequestedVersion (SOAP)</span></span>

<span data-ttu-id="a75e0-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **RequestedVersion**元素指定客户端需要在处理请求的最小服务版本。</span><span class="sxs-lookup"><span data-stu-id="a75e0-104">The **RequestedVersion** element specifies the minimum service version that the client wants the request to be processed on.</span></span> 
  
```XML
<RequestedVersion/>
```

 <span data-ttu-id="a75e0-105">**ExchangeVersion**</span><span class="sxs-lookup"><span data-stu-id="a75e0-105">**ExchangeVersion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a75e0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a75e0-106">Attributes and elements</span></span>

<span data-ttu-id="a75e0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a75e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a75e0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a75e0-108">Attributes</span></span>

<span data-ttu-id="a75e0-109">无。</span><span class="sxs-lookup"><span data-stu-id="a75e0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a75e0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a75e0-110">Child elements</span></span>

<span data-ttu-id="a75e0-111">无。</span><span class="sxs-lookup"><span data-stu-id="a75e0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a75e0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a75e0-112">Parent elements</span></span>

|<span data-ttu-id="a75e0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a75e0-113">**Element**</span></span>|<span data-ttu-id="a75e0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a75e0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a75e0-115">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a75e0-115">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="a75e0-116">包含请求的配置设置和目标用户。</span><span class="sxs-lookup"><span data-stu-id="a75e0-116">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="a75e0-117">请求 (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a75e0-117">Request (GetDomainSettings) (SOAP)</span></span>](request-getdomainsettingssoap.md) <br/> |<span data-ttu-id="a75e0-118">表示一个请求以获取域设置。</span><span class="sxs-lookup"><span data-stu-id="a75e0-118">Represents a request to get domain settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a75e0-119">文本值</span><span class="sxs-lookup"><span data-stu-id="a75e0-119">Text value</span></span>

<span data-ttu-id="a75e0-120">**RequestedVersion**元素的文本值可以是Exchange2010、 Exchange2010_SP1、 Exchange2010_SP2或Exchange2013。</span><span class="sxs-lookup"><span data-stu-id="a75e0-120">The text value for the **RequestedVersion** element can be Exchange2010, Exchange2010_SP1, Exchange2010_SP2, or Exchange2013.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a75e0-121">备注</span><span class="sxs-lookup"><span data-stu-id="a75e0-121">Remarks</span></span>

<span data-ttu-id="a75e0-122">如果此元素不存在，则使用最新的服务版本。</span><span class="sxs-lookup"><span data-stu-id="a75e0-122">If this element is not present, the latest service version is used.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a75e0-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="a75e0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a75e0-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="a75e0-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="a75e0-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="a75e0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a75e0-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="a75e0-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="a75e0-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="a75e0-127">Validation File</span></span>  <br/> |<span data-ttu-id="a75e0-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a75e0-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a75e0-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="a75e0-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="a75e0-130">False</span><span class="sxs-lookup"><span data-stu-id="a75e0-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a75e0-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a75e0-131">See also</span></span>



[<span data-ttu-id="a75e0-132">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a75e0-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="a75e0-133">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a75e0-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

