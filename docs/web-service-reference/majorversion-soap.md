---
title: MajorVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0b2a83cf-e173-4073-9603-b2ea3b36ec1a
description: MajorVersion元素表示为服务器的主版本号。
ms.openlocfilehash: ca619d4c36e17ca9a811019f0a13b45353cab1e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826333"
---
# <a name="majorversion-soap"></a><span data-ttu-id="0edb5-103">MajorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0edb5-103">MajorVersion (SOAP)</span></span>

<span data-ttu-id="0edb5-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **MajorVersion**元素表示为服务器的主版本号。</span><span class="sxs-lookup"><span data-stu-id="0edb5-104">The **MajorVersion** element represents the major version number for the server.</span></span> 
  
```XML
<MajorVersion/>
```

 <span data-ttu-id="0edb5-105">**int**</span><span class="sxs-lookup"><span data-stu-id="0edb5-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0edb5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0edb5-106">Attributes and elements</span></span>

<span data-ttu-id="0edb5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0edb5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0edb5-108">属性</span><span class="sxs-lookup"><span data-stu-id="0edb5-108">Attributes</span></span>

<span data-ttu-id="0edb5-109">无。</span><span class="sxs-lookup"><span data-stu-id="0edb5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0edb5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0edb5-110">Child elements</span></span>

<span data-ttu-id="0edb5-111">无。</span><span class="sxs-lookup"><span data-stu-id="0edb5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0edb5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0edb5-112">Parent elements</span></span>

|<span data-ttu-id="0edb5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0edb5-113">**Element**</span></span>|<span data-ttu-id="0edb5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0edb5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0edb5-115">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0edb5-115">ServerVersionInfo (SOAP)</span></span>](serverversioninfo-soap.md) <br/> |<span data-ttu-id="0edb5-116">包含处理请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="0edb5-116">Contains the version of the server that processed the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0edb5-117">文本值</span><span class="sxs-lookup"><span data-stu-id="0edb5-117">Text value</span></span>

<span data-ttu-id="0edb5-118">**MajorVersion**元素的文本值是一个整数，表示处理请求的服务器的主版本号。</span><span class="sxs-lookup"><span data-stu-id="0edb5-118">The text value for the **MajorVersion** element is an integer that represents the major version number of the server that processed the request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0edb5-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="0edb5-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0edb5-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="0edb5-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0edb5-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="0edb5-121">Schema Name</span></span>  <br/> |<span data-ttu-id="0edb5-122">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="0edb5-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0edb5-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="0edb5-123">Validation File</span></span>  <br/> |<span data-ttu-id="0edb5-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0edb5-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0edb5-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="0edb5-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="0edb5-126">True</span><span class="sxs-lookup"><span data-stu-id="0edb5-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0edb5-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0edb5-127">See also</span></span>



[<span data-ttu-id="0edb5-128">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0edb5-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="0edb5-129">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0edb5-129">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

