---
title: OptedInto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 083a23d9-acc3-4c15-9d30-c20bf7e6808d
description: OptedInto 元素指定一个布尔值，该值指示用户是否选择保留策略。
ms.openlocfilehash: 1095a8c2527546b8c945dd7efb5c0218f9a151c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468766"
---
# <a name="optedinto"></a><span data-ttu-id="1d70c-103">OptedInto</span><span class="sxs-lookup"><span data-stu-id="1d70c-103">OptedInto</span></span>

<span data-ttu-id="1d70c-104">**OptedInto**元素指定一个布尔值，该值指示用户是否选择保留策略。</span><span class="sxs-lookup"><span data-stu-id="1d70c-104">The **OptedInto** element specifies a Boolean value that indicates whether the user opted in to the retention policy.</span></span> 
  
```XML
<OptedInto>true | false</OptedInto>
```

 <span data-ttu-id="1d70c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1d70c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d70c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1d70c-106">Attributes and elements</span></span>

<span data-ttu-id="1d70c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1d70c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d70c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1d70c-108">Attributes</span></span>

<span data-ttu-id="1d70c-109">无。</span><span class="sxs-lookup"><span data-stu-id="1d70c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d70c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1d70c-110">Child elements</span></span>

<span data-ttu-id="1d70c-111">无。</span><span class="sxs-lookup"><span data-stu-id="1d70c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1d70c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1d70c-112">Parent elements</span></span>

[<span data-ttu-id="1d70c-113">Get-retentionpolicytag</span><span class="sxs-lookup"><span data-stu-id="1d70c-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="1d70c-114">文本值</span><span class="sxs-lookup"><span data-stu-id="1d70c-114">Text value</span></span>

<span data-ttu-id="1d70c-115">如果**OptedInto**元素的文本值为**true** ，则指示用户选择保留策略。</span><span class="sxs-lookup"><span data-stu-id="1d70c-115">A text value of **true** for the **OptedInto** element indicates that the user opted in to the retention policy.</span></span> <span data-ttu-id="1d70c-116">**如果值为 false** ，则表示用户未选择保留策略。</span><span class="sxs-lookup"><span data-stu-id="1d70c-116">A value of **false** indicates that the user did not opt into the retention policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1d70c-117">备注</span><span class="sxs-lookup"><span data-stu-id="1d70c-117">Remarks</span></span>

<span data-ttu-id="1d70c-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1d70c-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1d70c-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1d70c-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d70c-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="1d70c-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d70c-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="1d70c-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d70c-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="1d70c-122">Schema name</span></span>  <br/> |<span data-ttu-id="1d70c-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="1d70c-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d70c-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="1d70c-124">Validation file</span></span>  <br/> |<span data-ttu-id="1d70c-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1d70c-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d70c-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="1d70c-126">Can be empty</span></span>  <br/> ||
   

