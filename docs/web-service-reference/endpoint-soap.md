---
title: 终结点 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 630cdbb5-d1c7-422c-924a-abf5738e9e5e
description: 终结点元素指定的安全令牌服务终结点。
ms.openlocfilehash: 85e1ad785b35649238ac3944f51472addf617c20
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754121"
---
# <a name="endpoint-soap"></a><span data-ttu-id="1d1c2-103">终结点 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1d1c2-103">Endpoint (SOAP)</span></span>

<span data-ttu-id="1d1c2-104">**终结点**元素指定的安全令牌服务终结点。</span><span class="sxs-lookup"><span data-stu-id="1d1c2-104">The **Endpoint** element specifies the security token service endpoint.</span></span> 
  
```XML
<Endpoint/>
```

 <span data-ttu-id="1d1c2-105">**xs:anyURI**</span><span class="sxs-lookup"><span data-stu-id="1d1c2-105">**xs:anyURI**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d1c2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1d1c2-106">Attributes and elements</span></span>

<span data-ttu-id="1d1c2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1d1c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d1c2-108">属性</span><span class="sxs-lookup"><span data-stu-id="1d1c2-108">Attributes</span></span>

<span data-ttu-id="1d1c2-109">无</span><span class="sxs-lookup"><span data-stu-id="1d1c2-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d1c2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1d1c2-110">Child elements</span></span>

<span data-ttu-id="1d1c2-111">无</span><span class="sxs-lookup"><span data-stu-id="1d1c2-111">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1d1c2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1d1c2-112">Parent elements</span></span>

|<span data-ttu-id="1d1c2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1d1c2-113">**Element**</span></span>|<span data-ttu-id="1d1c2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1d1c2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d1c2-115">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1d1c2-115">TokenIssuer (SOAP)</span></span>](tokenissuer-soap.md) <br/> |<span data-ttu-id="1d1c2-116">指定安全令牌服务的 URI 和终结点。</span><span class="sxs-lookup"><span data-stu-id="1d1c2-116">Specifies the URI and Endpoint for the security token service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1d1c2-117">文本值</span><span class="sxs-lookup"><span data-stu-id="1d1c2-117">Text value</span></span>

<span data-ttu-id="1d1c2-118">文本值表示的终结点的安全令牌的 web 服务。</span><span class="sxs-lookup"><span data-stu-id="1d1c2-118">The text value represents the endpoint for the security token web service.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d1c2-119">注解</span><span class="sxs-lookup"><span data-stu-id="1d1c2-119">Remarks</span></span>

<span data-ttu-id="1d1c2-120">终结点用于通信的安全令牌的 web 服务。</span><span class="sxs-lookup"><span data-stu-id="1d1c2-120">The endpoint is used for communicating with the security token web service.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d1c2-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="1d1c2-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d1c2-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="1d1c2-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="1d1c2-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="1d1c2-123">Schema Name</span></span>  <br/> |<span data-ttu-id="1d1c2-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="1d1c2-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="1d1c2-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="1d1c2-125">Validation File</span></span>  <br/> |<span data-ttu-id="1d1c2-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1d1c2-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1d1c2-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="1d1c2-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d1c2-128">True</span><span class="sxs-lookup"><span data-stu-id="1d1c2-128">True</span></span>  <br/> |
   

