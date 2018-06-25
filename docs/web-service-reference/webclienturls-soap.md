---
title: WebClientUrls (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: fdfe6059-a861-4fa2-a20e-ee6ab820bee9
description: WebClientUrls 元素均表示包含 WebClientUrl (SOAP) 元素的集合的用户设置。
ms.openlocfilehash: 8d5d6aec67ab183743d7aae9f5d1f303d2949cd0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838545"
---
# <a name="webclienturls-soap"></a><span data-ttu-id="56715-103">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="56715-103">WebClientUrls (SOAP)</span></span>

<span data-ttu-id="56715-104">**WebClientUrls**元素均表示包含[WebClientUrl (SOAP)](webclienturl-soap.md)元素的集合的用户设置。</span><span class="sxs-lookup"><span data-stu-id="56715-104">The **WebClientUrls** element represents a user setting that contains a collection of [WebClientUrl (SOAP)](webclienturl-soap.md) elements.</span></span> 
  
[<span data-ttu-id="56715-105">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="56715-105">UserSetting (SOAP)</span></span>](usersetting-soap.md)
  
[<span data-ttu-id="56715-106">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="56715-106">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)
  
[<span data-ttu-id="56715-107">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="56715-107">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)
  
```XML
<WebClientUrls>
     <WebClientUrl/>
</WebClientUrls>

```

 <span data-ttu-id="56715-108">**WebClientUrls**</span><span class="sxs-lookup"><span data-stu-id="56715-108">**WebClientUrls**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="56715-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="56715-109">Attributes and elements</span></span>

<span data-ttu-id="56715-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="56715-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56715-111">属性</span><span class="sxs-lookup"><span data-stu-id="56715-111">Attributes</span></span>

<span data-ttu-id="56715-112">无。</span><span class="sxs-lookup"><span data-stu-id="56715-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="56715-113">子元素</span><span class="sxs-lookup"><span data-stu-id="56715-113">Child elements</span></span>

|<span data-ttu-id="56715-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="56715-114">**Element**</span></span>|<span data-ttu-id="56715-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="56715-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56715-116">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="56715-116">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md) <br/> |<span data-ttu-id="56715-117">表示 Exchange 客户端的 URL。</span><span class="sxs-lookup"><span data-stu-id="56715-117">Represents an Exchange client URL.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="56715-118">父元素</span><span class="sxs-lookup"><span data-stu-id="56715-118">Parent elements</span></span>

|<span data-ttu-id="56715-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="56715-119">**Element**</span></span>|<span data-ttu-id="56715-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="56715-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56715-121">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="56715-121">UserSetting (SOAP)</span></span>](usersetting-soap.md) <br/> |<span data-ttu-id="56715-122">代表 GetUserSettings 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="56715-122">Represents a response to a GetUserSettings request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="56715-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="56715-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56715-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="56715-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="56715-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="56715-125">Schema Name</span></span>  <br/> |<span data-ttu-id="56715-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="56715-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="56715-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="56715-127">Validation File</span></span>  <br/> |<span data-ttu-id="56715-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="56715-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="56715-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="56715-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="56715-130">True</span><span class="sxs-lookup"><span data-stu-id="56715-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56715-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="56715-131">See also</span></span>



[<span data-ttu-id="56715-132">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="56715-132">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)

