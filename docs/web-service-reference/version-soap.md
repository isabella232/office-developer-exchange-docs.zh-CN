---
title: 版本 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 47c9216e-6bfe-48c8-a27a-26f70db8e8d5
description: Version 元素表示服务器产品版本的说明。
ms.openlocfilehash: b8284880646cb82e6af6715523467021f080b8e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838529"
---
# <a name="version-soap"></a><span data-ttu-id="25b2f-103">版本 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="25b2f-103">Version (SOAP)</span></span>

<span data-ttu-id="25b2f-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Version** 元素表示服务器产品版本的说明。</span><span class="sxs-lookup"><span data-stu-id="25b2f-104">The **Version** element represents a description of the server product version.</span></span> 
  
```XML
<Version/>
```

 <span data-ttu-id="25b2f-105">**string**</span><span class="sxs-lookup"><span data-stu-id="25b2f-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25b2f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="25b2f-106">Attributes and elements</span></span>

<span data-ttu-id="25b2f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="25b2f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25b2f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="25b2f-108">Attributes</span></span>

<span data-ttu-id="25b2f-109">无。</span><span class="sxs-lookup"><span data-stu-id="25b2f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25b2f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="25b2f-110">Child elements</span></span>

<span data-ttu-id="25b2f-111">无。</span><span class="sxs-lookup"><span data-stu-id="25b2f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25b2f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="25b2f-112">Parent elements</span></span>

|<span data-ttu-id="25b2f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="25b2f-113">**Element**</span></span>|<span data-ttu-id="25b2f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="25b2f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25b2f-115">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="25b2f-115">ServerVersionInfo (SOAP)</span></span>](serverversioninfo-soap.md) <br/> |<span data-ttu-id="25b2f-116">包含处理请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="25b2f-116">Contains the version of the server that processed the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25b2f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="25b2f-117">Text value</span></span>

<span data-ttu-id="25b2f-118">**Version** 元素的值是服务器产品版本的说明。</span><span class="sxs-lookup"><span data-stu-id="25b2f-118">The value of the **Version** element is a description of the server product version.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="25b2f-119">说明</span><span class="sxs-lookup"><span data-stu-id="25b2f-119">Remarks</span></span>

<span data-ttu-id="25b2f-120">**Version** 元素包含在响应的 SOAP 标头中。</span><span class="sxs-lookup"><span data-stu-id="25b2f-120">The **Version** element is contained in the SOAP header of a response.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="25b2f-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="25b2f-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25b2f-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="25b2f-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="25b2f-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="25b2f-123">Schema Name</span></span>  <br/> |<span data-ttu-id="25b2f-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="25b2f-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="25b2f-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="25b2f-125">Validation File</span></span>  <br/> |<span data-ttu-id="25b2f-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="25b2f-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="25b2f-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="25b2f-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="25b2f-128">True</span><span class="sxs-lookup"><span data-stu-id="25b2f-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25b2f-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="25b2f-129">See also</span></span>



[<span data-ttu-id="25b2f-130">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="25b2f-130">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="25b2f-131">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="25b2f-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="25b2f-132">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="25b2f-132">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

