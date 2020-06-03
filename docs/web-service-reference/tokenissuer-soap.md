---
title: TokenIssuer （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: TokenIssuer 元素指定安全令牌服务的 Uri （SOAP）和终结点（SOAP）。
ms.openlocfilehash: e9c0b4140de26c7ff05daf4e863b3e8a17fedc62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526324"
---
# <a name="tokenissuer-soap"></a><span data-ttu-id="98037-103">TokenIssuer （SOAP）</span><span class="sxs-lookup"><span data-stu-id="98037-103">TokenIssuer (SOAP)</span></span>

<span data-ttu-id="98037-104">**TokenIssuer**元素指定安全令牌服务的[Uri （Soap）](uri-soap.md)和[终结点（soap）](endpoint-soap.md) 。</span><span class="sxs-lookup"><span data-stu-id="98037-104">The **TokenIssuer** element specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span> 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 <span data-ttu-id="98037-105">**TokenIssuer**</span><span class="sxs-lookup"><span data-stu-id="98037-105">**TokenIssuer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98037-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="98037-106">Attributes and elements</span></span>

<span data-ttu-id="98037-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="98037-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98037-108">属性</span><span class="sxs-lookup"><span data-stu-id="98037-108">Attributes</span></span>

<span data-ttu-id="98037-109">无</span><span class="sxs-lookup"><span data-stu-id="98037-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="98037-110">子元素</span><span class="sxs-lookup"><span data-stu-id="98037-110">Child elements</span></span>

|<span data-ttu-id="98037-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="98037-111">**Element**</span></span>|<span data-ttu-id="98037-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="98037-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98037-113">Uri （SOAP）</span><span class="sxs-lookup"><span data-stu-id="98037-113">Uri (SOAP)</span></span>](uri-soap.md) <br/> |<span data-ttu-id="98037-114">颁发安全令牌的 security token service 的 URI。</span><span class="sxs-lookup"><span data-stu-id="98037-114">The URI of the security token service that issued the security token.</span></span>  <br/> |
|[<span data-ttu-id="98037-115">终结点（SOAP）</span><span class="sxs-lookup"><span data-stu-id="98037-115">Endpoint (SOAP)</span></span>](endpoint-soap.md) <br/> |<span data-ttu-id="98037-116">Web 服务终结点 URI。</span><span class="sxs-lookup"><span data-stu-id="98037-116">The web service Endpoint URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="98037-117">父元素</span><span class="sxs-lookup"><span data-stu-id="98037-117">Parent elements</span></span>

|<span data-ttu-id="98037-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="98037-118">**Element**</span></span>|<span data-ttu-id="98037-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="98037-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98037-120">TokenIssuers （SOAP）</span><span class="sxs-lookup"><span data-stu-id="98037-120">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="98037-121">表示安全令牌服务[Uri （soap）](uri-soap.md)和[终结点（soap）](endpoint-soap.md)的集合。</span><span class="sxs-lookup"><span data-stu-id="98037-121">Represents a collection of security token service [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98037-122">备注</span><span class="sxs-lookup"><span data-stu-id="98037-122">Remarks</span></span>

<span data-ttu-id="98037-123">使用**TokenIssuer**元素来指定安全令牌在使用安全令牌时的服务。</span><span class="sxs-lookup"><span data-stu-id="98037-123">Use the **TokenIssuer** element to specify the security token service when using security tokens.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="98037-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="98037-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98037-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="98037-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="98037-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="98037-126">Schema Name</span></span>  <br/> |<span data-ttu-id="98037-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="98037-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="98037-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="98037-128">Validation File</span></span>  <br/> |<span data-ttu-id="98037-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="98037-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="98037-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="98037-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="98037-131">True</span><span class="sxs-lookup"><span data-stu-id="98037-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98037-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="98037-132">See also</span></span>



[<span data-ttu-id="98037-133">Exchange 的自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="98037-133">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="98037-134">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="98037-134">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

