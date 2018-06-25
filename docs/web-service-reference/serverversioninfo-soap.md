---
title: ServerVersionInfo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8662647b-e50a-4774-9ba3-a951ae6df781
description: ServerVersionInfo 元素包含处理请求的服务器版本。
ms.openlocfilehash: b02071e4997aba91fb538d52df2612fe6fd32800
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827385"
---
# <a name="serverversioninfo-soap"></a><span data-ttu-id="ad65d-103">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad65d-103">ServerVersionInfo (SOAP)</span></span>

<span data-ttu-id="ad65d-104">**ServerVersionInfo**元素包含处理请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="ad65d-104">The **ServerVersionInfo** element contains the version of the server that processed the request.</span></span> 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 <span data-ttu-id="ad65d-105">**ServerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="ad65d-105">**ServerVersionInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad65d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ad65d-106">Attributes and elements</span></span>

<span data-ttu-id="ad65d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ad65d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad65d-108">属性</span><span class="sxs-lookup"><span data-stu-id="ad65d-108">Attributes</span></span>

<span data-ttu-id="ad65d-109">无。</span><span class="sxs-lookup"><span data-stu-id="ad65d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad65d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ad65d-110">Child elements</span></span>

|<span data-ttu-id="ad65d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ad65d-111">**Element**</span></span>|<span data-ttu-id="ad65d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ad65d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad65d-113">MajorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad65d-113">MajorVersion (SOAP)</span></span>](majorversion-soap.md) <br/> |<span data-ttu-id="ad65d-114">服务器的主要版本号。</span><span class="sxs-lookup"><span data-stu-id="ad65d-114">The major version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="ad65d-115">MinorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad65d-115">MinorVersion (SOAP)</span></span>](minorversion-soap.md) <br/> |<span data-ttu-id="ad65d-116">服务器的次要版本号。</span><span class="sxs-lookup"><span data-stu-id="ad65d-116">The minor version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="ad65d-117">MajorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad65d-117">MajorBuildNumber (SOAP)</span></span>](majorbuildnumber-soap.md) <br/> |<span data-ttu-id="ad65d-118">服务器的主要版本号。</span><span class="sxs-lookup"><span data-stu-id="ad65d-118">The major build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="ad65d-119">MinorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad65d-119">MinorBuildNumber (SOAP)</span></span>](minorbuildnumber-soap.md) <br/> |<span data-ttu-id="ad65d-120">服务器的次要版本号。</span><span class="sxs-lookup"><span data-stu-id="ad65d-120">The minor build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="ad65d-121">版本 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad65d-121">Version (SOAP)</span></span>](version-soap.md) <br/> |<span data-ttu-id="ad65d-122">服务器产品版本的说明。</span><span class="sxs-lookup"><span data-stu-id="ad65d-122">A description of the server product version.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ad65d-123">父元素</span><span class="sxs-lookup"><span data-stu-id="ad65d-123">Parent elements</span></span>

<span data-ttu-id="ad65d-124">无。</span><span class="sxs-lookup"><span data-stu-id="ad65d-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad65d-125">注解</span><span class="sxs-lookup"><span data-stu-id="ad65d-125">Remarks</span></span>

<span data-ttu-id="ad65d-126">此元素的 SOAP 标头中返回。</span><span class="sxs-lookup"><span data-stu-id="ad65d-126">This element is returned in the SOAP header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad65d-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="ad65d-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad65d-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="ad65d-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ad65d-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="ad65d-129">Schema Name</span></span>  <br/> |<span data-ttu-id="ad65d-130">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="ad65d-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ad65d-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="ad65d-131">Validation File</span></span>  <br/> |<span data-ttu-id="ad65d-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ad65d-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ad65d-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="ad65d-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad65d-134">True</span><span class="sxs-lookup"><span data-stu-id="ad65d-134">True</span></span>  <br/> |
   

