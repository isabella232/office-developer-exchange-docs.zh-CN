---
title: InPlaceHoldConfigurationOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 921ecc73-b7e2-40a7-8458-68f18dd5a13b
description: InPlaceHoldConfigurationOnly 元素指定是否包含就地保留配置。
ms.openlocfilehash: ca364ee7d8a9e2e4a608f8f6c4ca5851fa7d4b64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466099"
---
# <a name="inplaceholdconfigurationonly"></a><span data-ttu-id="7afe6-103">InPlaceHoldConfigurationOnly</span><span class="sxs-lookup"><span data-stu-id="7afe6-103">InPlaceHoldConfigurationOnly</span></span>

<span data-ttu-id="7afe6-104">**InPlaceHoldConfigurationOnly**元素指定是否包含就地保留配置。</span><span class="sxs-lookup"><span data-stu-id="7afe6-104">The **InPlaceHoldConfigurationOnly** element specifies whether to include the in-place hold configuration.</span></span> 
  
```XML
<InPlaceHoldConfigurationOnly>true | false</InPlaceHoldConfigurationOnly>
```

 <span data-ttu-id="7afe6-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7afe6-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7afe6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7afe6-106">Attributes and elements</span></span>

<span data-ttu-id="7afe6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7afe6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7afe6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7afe6-108">Attributes</span></span>

<span data-ttu-id="7afe6-109">无。</span><span class="sxs-lookup"><span data-stu-id="7afe6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7afe6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7afe6-110">Child elements</span></span>

<span data-ttu-id="7afe6-111">无。</span><span class="sxs-lookup"><span data-stu-id="7afe6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7afe6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7afe6-112">Parent elements</span></span>

[<span data-ttu-id="7afe6-113">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7afe6-113">GetDiscoverySearchConfiguration</span></span>](getdiscoverysearchconfiguration.md)
  
## <a name="text-value"></a><span data-ttu-id="7afe6-114">文本值</span><span class="sxs-lookup"><span data-stu-id="7afe6-114">Text value</span></span>

<span data-ttu-id="7afe6-115">如果**InPlaceHoldConfigurationOnly**元素的文本值为**true** ，则表示包含就地保留配置。</span><span class="sxs-lookup"><span data-stu-id="7afe6-115">A text value of **true** for the **InPlaceHoldConfigurationOnly** element indicates that the in-place hold configuration is included.</span></span> <span data-ttu-id="7afe6-116">**如果值为 false** ，则表示不包含就地保留配置。</span><span class="sxs-lookup"><span data-stu-id="7afe6-116">A value of **false** indicates that the in-place hold configuration is not included.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7afe6-117">备注</span><span class="sxs-lookup"><span data-stu-id="7afe6-117">Remarks</span></span>

<span data-ttu-id="7afe6-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7afe6-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7afe6-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7afe6-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7afe6-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="7afe6-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7afe6-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="7afe6-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7afe6-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="7afe6-122">Schema name</span></span>  <br/> |<span data-ttu-id="7afe6-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="7afe6-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7afe6-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="7afe6-124">Validation file</span></span>  <br/> |<span data-ttu-id="7afe6-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7afe6-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7afe6-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="7afe6-126">Can be empty</span></span>  <br/> ||
   

