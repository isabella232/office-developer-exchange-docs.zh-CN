---
title: MinorVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2ef4e181-7324-4c88-94a9-1cffefc8c008
description: MinorVersion元素表示为服务器的版本号。
ms.openlocfilehash: f1958aca014f3d8012201c74f817e8efcbb942ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826475"
---
# <a name="minorversion-soap"></a><span data-ttu-id="2fad6-103">MinorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2fad6-103">MinorVersion (SOAP)</span></span>

<span data-ttu-id="2fad6-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **MinorVersion**元素表示为服务器的版本号。</span><span class="sxs-lookup"><span data-stu-id="2fad6-104">The **MinorVersion** element represents minor version number for the server.</span></span> 
  
```XML
<MinorVersion/>
```

 <span data-ttu-id="2fad6-105">**int**</span><span class="sxs-lookup"><span data-stu-id="2fad6-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2fad6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2fad6-106">Attributes and elements</span></span>

<span data-ttu-id="2fad6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2fad6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2fad6-108">属性</span><span class="sxs-lookup"><span data-stu-id="2fad6-108">Attributes</span></span>

<span data-ttu-id="2fad6-109">无。</span><span class="sxs-lookup"><span data-stu-id="2fad6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2fad6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2fad6-110">Child elements</span></span>

<span data-ttu-id="2fad6-111">无。</span><span class="sxs-lookup"><span data-stu-id="2fad6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2fad6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2fad6-112">Parent elements</span></span>

|<span data-ttu-id="2fad6-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2fad6-113">**Element**</span></span>|<span data-ttu-id="2fad6-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2fad6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2fad6-115">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2fad6-115">ServerVersionInfo (SOAP)</span></span>](serverversioninfo-soap.md) <br/> |<span data-ttu-id="2fad6-116">包含处理请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="2fad6-116">Contains the version of the server that processed the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2fad6-117">文本值</span><span class="sxs-lookup"><span data-stu-id="2fad6-117">Text value</span></span>

<span data-ttu-id="2fad6-118">一个整数值，表示服务器处理该请求的次要版本数。</span><span class="sxs-lookup"><span data-stu-id="2fad6-118">An integer value that represents the minor version number of the server that processed the request.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2fad6-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="2fad6-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fad6-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="2fad6-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="2fad6-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="2fad6-121">Schema Name</span></span>  <br/> |<span data-ttu-id="2fad6-122">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="2fad6-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="2fad6-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="2fad6-123">Validation File</span></span>  <br/> |<span data-ttu-id="2fad6-124">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2fad6-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2fad6-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="2fad6-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="2fad6-126">True</span><span class="sxs-lookup"><span data-stu-id="2fad6-126">True</span></span>  <br/> |
   

