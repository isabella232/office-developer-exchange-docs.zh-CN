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
description: ServerVersionInfo 元素包含处理请求的服务器的版本。
ms.openlocfilehash: b54b4833361ec78c7f8213473af4638965c7ddae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467646"
---
# <a name="serverversioninfo-soap"></a><span data-ttu-id="cc759-103">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cc759-103">ServerVersionInfo (SOAP)</span></span>

<span data-ttu-id="cc759-104">**ServerVersionInfo**元素包含处理请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="cc759-104">The **ServerVersionInfo** element contains the version of the server that processed the request.</span></span> 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 <span data-ttu-id="cc759-105">**ServerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="cc759-105">**ServerVersionInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc759-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cc759-106">Attributes and elements</span></span>

<span data-ttu-id="cc759-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cc759-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc759-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cc759-108">Attributes</span></span>

<span data-ttu-id="cc759-109">无。</span><span class="sxs-lookup"><span data-stu-id="cc759-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc759-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cc759-110">Child elements</span></span>

|<span data-ttu-id="cc759-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cc759-111">**Element**</span></span>|<span data-ttu-id="cc759-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cc759-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc759-113">MajorVersion （SOAP）</span><span class="sxs-lookup"><span data-stu-id="cc759-113">MajorVersion (SOAP)</span></span>](majorversion-soap.md) <br/> |<span data-ttu-id="cc759-114">服务器的主版本号。</span><span class="sxs-lookup"><span data-stu-id="cc759-114">The major version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="cc759-115">MinorVersion （SOAP）</span><span class="sxs-lookup"><span data-stu-id="cc759-115">MinorVersion (SOAP)</span></span>](minorversion-soap.md) <br/> |<span data-ttu-id="cc759-116">服务器的次要版本号。</span><span class="sxs-lookup"><span data-stu-id="cc759-116">The minor version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="cc759-117">MajorBuildNumber （SOAP）</span><span class="sxs-lookup"><span data-stu-id="cc759-117">MajorBuildNumber (SOAP)</span></span>](majorbuildnumber-soap.md) <br/> |<span data-ttu-id="cc759-118">服务器的主要内部版本号。</span><span class="sxs-lookup"><span data-stu-id="cc759-118">The major build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="cc759-119">MinorBuildNumber （SOAP）</span><span class="sxs-lookup"><span data-stu-id="cc759-119">MinorBuildNumber (SOAP)</span></span>](minorbuildnumber-soap.md) <br/> |<span data-ttu-id="cc759-120">服务器的次要内部版本号。</span><span class="sxs-lookup"><span data-stu-id="cc759-120">The minor build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="cc759-121">版本 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cc759-121">Version (SOAP)</span></span>](version-soap.md) <br/> |<span data-ttu-id="cc759-122">服务器产品版本的说明。</span><span class="sxs-lookup"><span data-stu-id="cc759-122">A description of the server product version.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cc759-123">父元素</span><span class="sxs-lookup"><span data-stu-id="cc759-123">Parent elements</span></span>

<span data-ttu-id="cc759-124">无。</span><span class="sxs-lookup"><span data-stu-id="cc759-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc759-125">说明</span><span class="sxs-lookup"><span data-stu-id="cc759-125">Remarks</span></span>

<span data-ttu-id="cc759-126">此元素在 SOAP 标头中返回。</span><span class="sxs-lookup"><span data-stu-id="cc759-126">This element is returned in the SOAP header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc759-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="cc759-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc759-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="cc759-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="cc759-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="cc759-129">Schema Name</span></span>  <br/> |<span data-ttu-id="cc759-130">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="cc759-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="cc759-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="cc759-131">Validation File</span></span>  <br/> |<span data-ttu-id="cc759-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cc759-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cc759-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="cc759-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="cc759-134">True</span><span class="sxs-lookup"><span data-stu-id="cc759-134">True</span></span>  <br/> |
   

