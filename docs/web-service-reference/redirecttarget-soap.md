---
title: RedirectTarget （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: RedirectTarget （SOAP）元素包含重定向 URL 或电子邮件地址的目标。
ms.openlocfilehash: 092d575560379d43b12dd98a3efa155b59c31450
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462197"
---
# <a name="redirecttarget-soap"></a><span data-ttu-id="d2084-103">RedirectTarget （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d2084-103">RedirectTarget (SOAP)</span></span>

<span data-ttu-id="d2084-104">[RedirectTarget （SOAP）](redirecttarget-soap.md)元素包含重定向 URL 或电子邮件地址的目标。</span><span class="sxs-lookup"><span data-stu-id="d2084-104">The [RedirectTarget (SOAP)](redirecttarget-soap.md) element contains the target of the redirection URL or e-mail address.</span></span> 
  
```XML
<RedirectTarget/>
```

 <span data-ttu-id="d2084-105">**string**</span><span class="sxs-lookup"><span data-stu-id="d2084-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2084-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d2084-106">Attributes and elements</span></span>

<span data-ttu-id="d2084-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d2084-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2084-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d2084-108">Attributes</span></span>

<span data-ttu-id="d2084-109">无。</span><span class="sxs-lookup"><span data-stu-id="d2084-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2084-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d2084-110">Child elements</span></span>

<span data-ttu-id="d2084-111">无。</span><span class="sxs-lookup"><span data-stu-id="d2084-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2084-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d2084-112">Parent elements</span></span>

|<span data-ttu-id="d2084-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d2084-113">**Element**</span></span>|<span data-ttu-id="d2084-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d2084-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2084-115">UserResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d2084-115">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="d2084-116">表示对单个用户的 GetUserSettings 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="d2084-116">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
|[<span data-ttu-id="d2084-117">DomainResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d2084-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="d2084-118">包含指定域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="d2084-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d2084-119">文本值</span><span class="sxs-lookup"><span data-stu-id="d2084-119">Text value</span></span>

<span data-ttu-id="d2084-120">该文本值包含应用于后续 GetUserSettings 或 GetDomainSettings 请求的重定向 URL 或电子邮件地址的目标。</span><span class="sxs-lookup"><span data-stu-id="d2084-120">The text value contains the target of the redirection URL or e-mail address that should be used for a subsequent GetUserSettings or GetDomainSettings request.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2084-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="d2084-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2084-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="d2084-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d2084-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="d2084-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d2084-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="d2084-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d2084-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="d2084-125">Validation File</span></span>  <br/> |<span data-ttu-id="d2084-126">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="d2084-126">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d2084-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="d2084-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2084-128">True</span><span class="sxs-lookup"><span data-stu-id="d2084-128">True</span></span>  <br/> |
   

