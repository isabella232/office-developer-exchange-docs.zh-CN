---
title: WebClientUrl (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7f8cb6d6-4aac-4a1f-8bec-2dcb90fc1df6
description: WebClientUrl 元素均表示 Exchange web 客户端的 URL。
ms.openlocfilehash: 649845018acee1706a96f9e37475a6d5c5fa0aa7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838550"
---
# <a name="webclienturl-soap"></a><span data-ttu-id="6dc42-103">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6dc42-103">WebClientUrl (SOAP)</span></span>

<span data-ttu-id="6dc42-104">**WebClientUrl**元素均表示 Exchange web 客户端的 URL。</span><span class="sxs-lookup"><span data-stu-id="6dc42-104">The **WebClientUrl** element represents the URL of an Exchange web client.</span></span> 
  
[<span data-ttu-id="6dc42-105">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6dc42-105">UserSetting (SOAP)</span></span>](usersetting-soap.md)
  
[<span data-ttu-id="6dc42-106">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6dc42-106">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)
  
[<span data-ttu-id="6dc42-107">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6dc42-107">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)
  
```XML
<WebClientUrl>
    <AuthenticationMethods/>
    <Url/>
</WebClientUrl>
```

 <span data-ttu-id="6dc42-108">**WebClientUrl**</span><span class="sxs-lookup"><span data-stu-id="6dc42-108">**WebClientUrl**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6dc42-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6dc42-109">Attributes and elements</span></span>

<span data-ttu-id="6dc42-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6dc42-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6dc42-111">属性</span><span class="sxs-lookup"><span data-stu-id="6dc42-111">Attributes</span></span>

<span data-ttu-id="6dc42-112">无。</span><span class="sxs-lookup"><span data-stu-id="6dc42-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6dc42-113">子元素</span><span class="sxs-lookup"><span data-stu-id="6dc42-113">Child elements</span></span>

|<span data-ttu-id="6dc42-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="6dc42-114">**Element**</span></span>|<span data-ttu-id="6dc42-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="6dc42-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6dc42-116">AuthenticationMethods (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6dc42-116">AuthenticationMethods (SOAP)</span></span>](authenticationmethods-soap.md) <br/> |<span data-ttu-id="6dc42-117">表示访问指定的 URL 时要使用的身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="6dc42-117">Represents the authentication method to use when accessing the specified URL.</span></span>  <br/> |
|[<span data-ttu-id="6dc42-118">Url (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6dc42-118">Url (SOAP)</span></span>](url-soap.md) <br/> |<span data-ttu-id="6dc42-119">表示用于 URL 的 web 地址。</span><span class="sxs-lookup"><span data-stu-id="6dc42-119">Represents the web address for the URL.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6dc42-120">父元素</span><span class="sxs-lookup"><span data-stu-id="6dc42-120">Parent elements</span></span>

|<span data-ttu-id="6dc42-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="6dc42-121">**Element**</span></span>|<span data-ttu-id="6dc42-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="6dc42-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6dc42-123">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6dc42-123">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md) <br/> |<span data-ttu-id="6dc42-124">代表包含**WebClientUrl**元素的集合的用户设置。</span><span class="sxs-lookup"><span data-stu-id="6dc42-124">Represents a user setting that contains a collection of **WebClientUrl** elements.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="6dc42-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="6dc42-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6dc42-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="6dc42-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6dc42-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="6dc42-127">Schema Name</span></span>  <br/> |<span data-ttu-id="6dc42-128">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="6dc42-128">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6dc42-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="6dc42-129">Validation File</span></span>  <br/> |<span data-ttu-id="6dc42-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6dc42-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6dc42-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="6dc42-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="6dc42-132">True</span><span class="sxs-lookup"><span data-stu-id="6dc42-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6dc42-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6dc42-133">See also</span></span>



[<span data-ttu-id="6dc42-134">Url (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6dc42-134">Url (SOAP)</span></span>](url-soap.md)
  
[<span data-ttu-id="6dc42-135">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6dc42-135">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)

