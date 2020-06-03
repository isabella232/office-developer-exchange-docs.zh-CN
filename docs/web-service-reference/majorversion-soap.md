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
ms.openlocfilehash: 2c564b110ec7497a2e9c92a00bfb7f376a657849
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44531005"
---
# <a name="majorversion-soap"></a><span data-ttu-id="36877-103">MajorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36877-103">MajorVersion (SOAP)</span></span>

<span data-ttu-id="36877-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **MajorVersion**元素表示为服务器的主版本号。</span><span class="sxs-lookup"><span data-stu-id="36877-104">The **MajorVersion** element represents the major version number for the server.</span></span> 
  
```XML
<MajorVersion/>
```

 <span data-ttu-id="36877-105">**int**</span><span class="sxs-lookup"><span data-stu-id="36877-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36877-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="36877-106">Attributes and elements</span></span>

<span data-ttu-id="36877-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="36877-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36877-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="36877-108">Attributes</span></span>

<span data-ttu-id="36877-109">无。</span><span class="sxs-lookup"><span data-stu-id="36877-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36877-110">子元素</span><span class="sxs-lookup"><span data-stu-id="36877-110">Child elements</span></span>

<span data-ttu-id="36877-111">无。</span><span class="sxs-lookup"><span data-stu-id="36877-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="36877-112">父元素</span><span class="sxs-lookup"><span data-stu-id="36877-112">Parent elements</span></span>

|<span data-ttu-id="36877-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="36877-113">**Element**</span></span>|<span data-ttu-id="36877-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="36877-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36877-115">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36877-115">ServerVersionInfo (SOAP)</span></span>](serverversioninfo-soap.md) <br/> |<span data-ttu-id="36877-116">包含处理请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="36877-116">Contains the version of the server that processed the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36877-117">文本值</span><span class="sxs-lookup"><span data-stu-id="36877-117">Text value</span></span>

<span data-ttu-id="36877-118">**MajorVersion**元素的文本值是一个整数，表示处理请求的服务器的主版本号。</span><span class="sxs-lookup"><span data-stu-id="36877-118">The text value for the **MajorVersion** element is an integer that represents the major version number of the server that processed the request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="36877-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="36877-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36877-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="36877-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="36877-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="36877-121">Schema Name</span></span>  <br/> |<span data-ttu-id="36877-122">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="36877-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="36877-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="36877-123">Validation File</span></span>  <br/> |<span data-ttu-id="36877-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="36877-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="36877-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="36877-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="36877-126">True</span><span class="sxs-lookup"><span data-stu-id="36877-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36877-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36877-127">See also</span></span>



[<span data-ttu-id="36877-128">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36877-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="36877-129">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36877-129">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

