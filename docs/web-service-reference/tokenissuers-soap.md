---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: TokenIssuers 元素表示 TokenIssuer (SOAP) 集合。
ms.openlocfilehash: b070d85b32d5bce8461ac4e930329f237885bad7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838256"
---
# <a name="tokenissuers-soap"></a><span data-ttu-id="b249c-103">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b249c-103">TokenIssuers (SOAP)</span></span>

<span data-ttu-id="b249c-104">**TokenIssuers**元素表示[TokenIssuer (SOAP)](tokenissuer-soap.md)集合。</span><span class="sxs-lookup"><span data-stu-id="b249c-104">The **TokenIssuers** elements represents the [TokenIssuer (SOAP)](tokenissuer-soap.md) collection.</span></span> 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 <span data-ttu-id="b249c-105">**TokenIssuers**</span><span class="sxs-lookup"><span data-stu-id="b249c-105">**TokenIssuers**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b249c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b249c-106">Attributes and elements</span></span>

<span data-ttu-id="b249c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b249c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b249c-108">属性</span><span class="sxs-lookup"><span data-stu-id="b249c-108">Attributes</span></span>

<span data-ttu-id="b249c-109">无</span><span class="sxs-lookup"><span data-stu-id="b249c-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b249c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b249c-110">Child elements</span></span>

|<span data-ttu-id="b249c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b249c-111">**Element**</span></span>|<span data-ttu-id="b249c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b249c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b249c-113">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b249c-113">TokenIssuer (SOAP)</span></span>](tokenissuer-soap.md) <br/> |<span data-ttu-id="b249c-114">指定安全令牌服务的[Uri (SOAP)](uri-soap.md)和[终结点 (SOAP)](endpoint-soap.md) 。</span><span class="sxs-lookup"><span data-stu-id="b249c-114">Specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b249c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b249c-115">Parent elements</span></span>

|<span data-ttu-id="b249c-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b249c-116">**Element**</span></span>|<span data-ttu-id="b249c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b249c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b249c-118">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b249c-118">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="b249c-119">包含[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)响应。</span><span class="sxs-lookup"><span data-stu-id="b249c-119">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b249c-120">注解</span><span class="sxs-lookup"><span data-stu-id="b249c-120">Remarks</span></span>

<span data-ttu-id="b249c-121">**TokenIssuers**代表[TokenIssuer (SOAP)](tokenissuer-soap.md)元素，用于自动发现的集合。</span><span class="sxs-lookup"><span data-stu-id="b249c-121">The **TokenIssuers** represents a collection of [TokenIssuer (SOAP)](tokenissuer-soap.md) elements to be used in the Autodiscovery.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b249c-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="b249c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b249c-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="b249c-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b249c-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="b249c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="b249c-125">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="b249c-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b249c-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="b249c-126">Validation File</span></span>  <br/> |<span data-ttu-id="b249c-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b249c-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b249c-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="b249c-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="b249c-129">True</span><span class="sxs-lookup"><span data-stu-id="b249c-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b249c-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b249c-130">See also</span></span>



[<span data-ttu-id="b249c-131">Exchange 的自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="b249c-131">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="b249c-132">SOAP Exchange 2013 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="b249c-132">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

