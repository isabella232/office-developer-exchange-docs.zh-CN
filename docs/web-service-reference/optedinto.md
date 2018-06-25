---
title: OptedInto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 083a23d9-acc3-4c15-9d30-c20bf7e6808d
description: OptedInto 元素指定一个布尔值，该值指示是否用户选择加入的保留策略。
ms.openlocfilehash: 0d8fb2b07c6c98ba6973ab6efabe9c35d2d1ac12
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826657"
---
# <a name="optedinto"></a><span data-ttu-id="3b746-103">OptedInto</span><span class="sxs-lookup"><span data-stu-id="3b746-103">OptedInto</span></span>

<span data-ttu-id="3b746-104">**OptedInto**元素指定一个布尔值，该值指示是否用户选择加入的保留策略。</span><span class="sxs-lookup"><span data-stu-id="3b746-104">The **OptedInto** element specifies a Boolean value that indicates whether the user opted in to the retention policy.</span></span> 
  
```XML
<OptedInto>true | false</OptedInto>
```

 <span data-ttu-id="3b746-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3b746-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b746-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3b746-106">Attributes and elements</span></span>

<span data-ttu-id="3b746-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3b746-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b746-108">属性</span><span class="sxs-lookup"><span data-stu-id="3b746-108">Attributes</span></span>

<span data-ttu-id="3b746-109">无。</span><span class="sxs-lookup"><span data-stu-id="3b746-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b746-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3b746-110">Child elements</span></span>

<span data-ttu-id="3b746-111">无。</span><span class="sxs-lookup"><span data-stu-id="3b746-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b746-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3b746-112">Parent elements</span></span>

[<span data-ttu-id="3b746-113">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="3b746-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="3b746-114">文本值</span><span class="sxs-lookup"><span data-stu-id="3b746-114">Text value</span></span>

<span data-ttu-id="3b746-115">文本值为**true**的**OptedInto**元素表示，用户选择加入的保留策略。</span><span class="sxs-lookup"><span data-stu-id="3b746-115">A text value of **true** for the **OptedInto** element indicates that the user opted in to the retention policy.</span></span> <span data-ttu-id="3b746-116">如果值为**false**指示的用户未选择不使用保留策略。</span><span class="sxs-lookup"><span data-stu-id="3b746-116">A value of **false** indicates that the user did not opt into the retention policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b746-117">备注</span><span class="sxs-lookup"><span data-stu-id="3b746-117">Remarks</span></span>

<span data-ttu-id="3b746-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3b746-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3b746-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3b746-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b746-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="3b746-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b746-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="3b746-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b746-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="3b746-122">Schema name</span></span>  <br/> |<span data-ttu-id="3b746-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="3b746-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b746-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="3b746-124">Validation file</span></span>  <br/> |<span data-ttu-id="3b746-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b746-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b746-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="3b746-126">Can be empty</span></span>  <br/> ||
   

