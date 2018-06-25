---
title: AnonymousAccessAllowed (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bf819a65-30f2-4881-a34f-cb30a9c2b6a7
description: AnonymousAccessAllowed 元素指示文档共享位置是否需要身份验证的用户。
ms.openlocfilehash: 7ca208aa0d75b254463400a5e207079d722fc0a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753154"
---
# <a name="anonymousaccessallowed-soap"></a><span data-ttu-id="40acc-103">AnonymousAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="40acc-103">AnonymousAccessAllowed (SOAP)</span></span>

<span data-ttu-id="40acc-104">**AnonymousAccessAllowed**元素指示文档共享位置是否需要身份验证的用户。</span><span class="sxs-lookup"><span data-stu-id="40acc-104">The **AnonymousAccessAllowed** element indicates whether a document sharing location requires an authenticated user.</span></span> 
  
```XML
<AnonymousAccessAllowed /> 
```

 <span data-ttu-id="40acc-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="40acc-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="40acc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="40acc-106">Attributes and elements</span></span>

<span data-ttu-id="40acc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="40acc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40acc-108">属性</span><span class="sxs-lookup"><span data-stu-id="40acc-108">Attributes</span></span>

<span data-ttu-id="40acc-109">无。</span><span class="sxs-lookup"><span data-stu-id="40acc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40acc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="40acc-110">Child elements</span></span>

<span data-ttu-id="40acc-111">无。</span><span class="sxs-lookup"><span data-stu-id="40acc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="40acc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="40acc-112">Parent elements</span></span>

|<span data-ttu-id="40acc-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="40acc-113">**Element**</span></span>|<span data-ttu-id="40acc-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="40acc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40acc-115">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="40acc-115">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="40acc-116">代表共享位置为文档的位置和元数据信息。</span><span class="sxs-lookup"><span data-stu-id="40acc-116">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="40acc-117">文本值</span><span class="sxs-lookup"><span data-stu-id="40acc-117">Text value</span></span>

<span data-ttu-id="40acc-118">**AnonymousAccessAllowed**元素的布尔值指示共享位置是否需要身份验证的用户。</span><span class="sxs-lookup"><span data-stu-id="40acc-118">The Boolean value of the **AnonymousAccessAllowed** element indicates whether the sharing location requires an authenticated user.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="40acc-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="40acc-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40acc-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="40acc-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="40acc-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="40acc-121">Schema Name</span></span>  <br/> |<span data-ttu-id="40acc-122">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="40acc-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="40acc-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="40acc-123">Validation File</span></span>  <br/> |<span data-ttu-id="40acc-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="40acc-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="40acc-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="40acc-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="40acc-126">True</span><span class="sxs-lookup"><span data-stu-id="40acc-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40acc-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="40acc-127">See also</span></span>

- [<span data-ttu-id="40acc-128">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="40acc-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="40acc-129">Exchange 的自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="40acc-129">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="40acc-130">SOAP Exchange 2013 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="40acc-130">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

