---
title: MajorBuildNumber (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7335b1c1-0b47-4452-a8cb-d19cddcfc281
description: MajorBuildNumber 元素均表示服务器的主要版本号。
ms.openlocfilehash: 2d6520b65f75c9fa14d236c99e96523baa3ddfb5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826329"
---
# <a name="majorbuildnumber-soap"></a><span data-ttu-id="882bc-103">MajorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="882bc-103">MajorBuildNumber (SOAP)</span></span>

<span data-ttu-id="882bc-104">**MajorBuildNumber**元素均表示服务器的主要版本号。</span><span class="sxs-lookup"><span data-stu-id="882bc-104">The **MajorBuildNumber** element represents major build number for the server.</span></span> 
  
```XML
<MajorBuildNumber/>
```

 <span data-ttu-id="882bc-105">**xs:int**</span><span class="sxs-lookup"><span data-stu-id="882bc-105">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="882bc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="882bc-106">Attributes and elements</span></span>

<span data-ttu-id="882bc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="882bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="882bc-108">属性</span><span class="sxs-lookup"><span data-stu-id="882bc-108">Attributes</span></span>

<span data-ttu-id="882bc-109">无。</span><span class="sxs-lookup"><span data-stu-id="882bc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="882bc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="882bc-110">Child elements</span></span>

<span data-ttu-id="882bc-111">无。</span><span class="sxs-lookup"><span data-stu-id="882bc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="882bc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="882bc-112">Parent elements</span></span>

|<span data-ttu-id="882bc-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="882bc-113">**Element**</span></span>|<span data-ttu-id="882bc-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="882bc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="882bc-115">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="882bc-115">ServerVersionInfo (SOAP)</span></span>](serverversioninfo-soap.md) <br/> |<span data-ttu-id="882bc-116">包含处理请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="882bc-116">Contains the version of the server that processed the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="882bc-117">文本值</span><span class="sxs-lookup"><span data-stu-id="882bc-117">Text value</span></span>

<span data-ttu-id="882bc-118">MajorBuildNumber 元素的文本值是一个整数，表示主版本号的服务器的处理请求。</span><span class="sxs-lookup"><span data-stu-id="882bc-118">The text value of the MajorBuildNumber element is an integer that represents the major build number of the server that processed the request.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="882bc-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="882bc-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="882bc-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="882bc-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="882bc-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="882bc-121">Schema Name</span></span>  <br/> |<span data-ttu-id="882bc-122">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="882bc-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="882bc-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="882bc-123">Validation File</span></span>  <br/> |<span data-ttu-id="882bc-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="882bc-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="882bc-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="882bc-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="882bc-126">True</span><span class="sxs-lookup"><span data-stu-id="882bc-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="882bc-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="882bc-127">See also</span></span>



[<span data-ttu-id="882bc-128">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="882bc-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="882bc-129">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="882bc-129">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="882bc-130">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="882bc-130">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

