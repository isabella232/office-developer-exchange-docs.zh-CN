---
title: WebClientUrl （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7f8cb6d6-4aac-4a1f-8bec-2dcb90fc1df6
description: WebClientUrl 元素表示 Exchange web 客户端的 URL。
ms.openlocfilehash: bcf9c8d4fe80de8af4c9500e5e850558a8451d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464971"
---
# <a name="webclienturl-soap"></a><span data-ttu-id="6140f-103">WebClientUrl （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6140f-103">WebClientUrl (SOAP)</span></span>

<span data-ttu-id="6140f-104">**WebClientUrl**元素表示 Exchange web 客户端的 URL。</span><span class="sxs-lookup"><span data-stu-id="6140f-104">The **WebClientUrl** element represents the URL of an Exchange web client.</span></span> 
  
[<span data-ttu-id="6140f-105">UserSetting （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6140f-105">UserSetting (SOAP)</span></span>](usersetting-soap.md)
  
[<span data-ttu-id="6140f-106">WebClientUrls （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6140f-106">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)
  
[<span data-ttu-id="6140f-107">WebClientUrl （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6140f-107">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)
  
```XML
<WebClientUrl>
    <AuthenticationMethods/>
    <Url/>
</WebClientUrl>
```

 <span data-ttu-id="6140f-108">**WebClientUrl**</span><span class="sxs-lookup"><span data-stu-id="6140f-108">**WebClientUrl**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6140f-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6140f-109">Attributes and elements</span></span>

<span data-ttu-id="6140f-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6140f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6140f-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="6140f-111">Attributes</span></span>

<span data-ttu-id="6140f-112">无。</span><span class="sxs-lookup"><span data-stu-id="6140f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6140f-113">子元素</span><span class="sxs-lookup"><span data-stu-id="6140f-113">Child elements</span></span>

|<span data-ttu-id="6140f-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="6140f-114">**Element**</span></span>|<span data-ttu-id="6140f-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="6140f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6140f-116">AuthenticationMethods （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6140f-116">AuthenticationMethods (SOAP)</span></span>](authenticationmethods-soap.md) <br/> |<span data-ttu-id="6140f-117">表示在访问指定的 URL 时要使用的身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="6140f-117">Represents the authentication method to use when accessing the specified URL.</span></span>  <br/> |
|[<span data-ttu-id="6140f-118">Url （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6140f-118">Url (SOAP)</span></span>](url-soap.md) <br/> |<span data-ttu-id="6140f-119">表示 URL 的 web 地址。</span><span class="sxs-lookup"><span data-stu-id="6140f-119">Represents the web address for the URL.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6140f-120">父元素</span><span class="sxs-lookup"><span data-stu-id="6140f-120">Parent elements</span></span>

|<span data-ttu-id="6140f-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="6140f-121">**Element**</span></span>|<span data-ttu-id="6140f-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="6140f-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6140f-123">WebClientUrls （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6140f-123">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md) <br/> |<span data-ttu-id="6140f-124">表示一个用户设置，其中包含**WebClientUrl**元素的集合。</span><span class="sxs-lookup"><span data-stu-id="6140f-124">Represents a user setting that contains a collection of **WebClientUrl** elements.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="6140f-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="6140f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6140f-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="6140f-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6140f-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="6140f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="6140f-128">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="6140f-128">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6140f-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="6140f-129">Validation File</span></span>  <br/> |<span data-ttu-id="6140f-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6140f-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6140f-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="6140f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="6140f-132">True</span><span class="sxs-lookup"><span data-stu-id="6140f-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6140f-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6140f-133">See also</span></span>



[<span data-ttu-id="6140f-134">Url （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6140f-134">Url (SOAP)</span></span>](url-soap.md)
  
[<span data-ttu-id="6140f-135">WebClientUrls （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6140f-135">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)

