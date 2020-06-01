---
title: TokenIssuers （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: TokenIssuers 元素表示 TokenIssuer （SOAP）集合。
ms.openlocfilehash: 352487ad3fd9c1ee7de756a109fb98a49d0cdcd7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457072"
---
# <a name="tokenissuers-soap"></a><span data-ttu-id="6d727-103">TokenIssuers （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6d727-103">TokenIssuers (SOAP)</span></span>

<span data-ttu-id="6d727-104">**TokenIssuers**元素表示[TokenIssuer （SOAP）](tokenissuer-soap.md)集合。</span><span class="sxs-lookup"><span data-stu-id="6d727-104">The **TokenIssuers** elements represents the [TokenIssuer (SOAP)](tokenissuer-soap.md) collection.</span></span> 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 <span data-ttu-id="6d727-105">**TokenIssuers**</span><span class="sxs-lookup"><span data-stu-id="6d727-105">**TokenIssuers**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d727-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6d727-106">Attributes and elements</span></span>

<span data-ttu-id="6d727-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6d727-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d727-108">属性</span><span class="sxs-lookup"><span data-stu-id="6d727-108">Attributes</span></span>

<span data-ttu-id="6d727-109">无</span><span class="sxs-lookup"><span data-stu-id="6d727-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d727-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6d727-110">Child elements</span></span>

|<span data-ttu-id="6d727-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6d727-111">**Element**</span></span>|<span data-ttu-id="6d727-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6d727-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d727-113">TokenIssuer （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6d727-113">TokenIssuer (SOAP)</span></span>](tokenissuer-soap.md) <br/> |<span data-ttu-id="6d727-114">指定安全令牌服务的[Uri （soap）](uri-soap.md)和[终结点（soap）](endpoint-soap.md) 。</span><span class="sxs-lookup"><span data-stu-id="6d727-114">Specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6d727-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6d727-115">Parent elements</span></span>

|<span data-ttu-id="6d727-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6d727-116">**Element**</span></span>|<span data-ttu-id="6d727-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6d727-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d727-118">GetFederationInformationResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6d727-118">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="6d727-119">包含[GetFederationInformation 操作（SOAP）](getfederationinformation-operation-soap.md)响应。</span><span class="sxs-lookup"><span data-stu-id="6d727-119">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d727-120">备注</span><span class="sxs-lookup"><span data-stu-id="6d727-120">Remarks</span></span>

<span data-ttu-id="6d727-121">**TokenIssuers**表示要在自动发现中使用的[TokenIssuer （SOAP）](tokenissuer-soap.md)元素的集合。</span><span class="sxs-lookup"><span data-stu-id="6d727-121">The **TokenIssuers** represents a collection of [TokenIssuer (SOAP)](tokenissuer-soap.md) elements to be used in the Autodiscovery.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6d727-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="6d727-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d727-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="6d727-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6d727-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="6d727-124">Schema Name</span></span>  <br/> |<span data-ttu-id="6d727-125">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="6d727-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6d727-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="6d727-126">Validation File</span></span>  <br/> |<span data-ttu-id="6d727-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6d727-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6d727-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="6d727-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="6d727-129">True</span><span class="sxs-lookup"><span data-stu-id="6d727-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d727-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6d727-130">See also</span></span>



[<span data-ttu-id="6d727-131">Exchange 的自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="6d727-131">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="6d727-132">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="6d727-132">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

