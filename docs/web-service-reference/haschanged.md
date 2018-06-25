---
title: HasChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: HasChanged 元素指示是否已更改用户的照片。
ms.openlocfilehash: b0129e3d3acb43ada16a824e3d21706999d7053c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825802"
---
# <a name="haschanged"></a><span data-ttu-id="80a4b-103">HasChanged</span><span class="sxs-lookup"><span data-stu-id="80a4b-103">HasChanged</span></span>

<span data-ttu-id="80a4b-104">**HasChanged**元素指示是否已更改用户的照片。</span><span class="sxs-lookup"><span data-stu-id="80a4b-104">The **HasChanged** element indicates whether a user's photo has changed.</span></span> 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="80a4b-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="80a4b-105">Attributes and elements</span></span>

<span data-ttu-id="80a4b-106">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="80a4b-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80a4b-107">属性</span><span class="sxs-lookup"><span data-stu-id="80a4b-107">Attributes</span></span>

<span data-ttu-id="80a4b-108">无。</span><span class="sxs-lookup"><span data-stu-id="80a4b-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80a4b-109">子元素</span><span class="sxs-lookup"><span data-stu-id="80a4b-109">Child elements</span></span>

<span data-ttu-id="80a4b-110">无。</span><span class="sxs-lookup"><span data-stu-id="80a4b-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="80a4b-111">父元素</span><span class="sxs-lookup"><span data-stu-id="80a4b-111">Parent elements</span></span>

[<span data-ttu-id="80a4b-112">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="80a4b-112">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
  
## <a name="text-value"></a><span data-ttu-id="80a4b-113">文本值</span><span class="sxs-lookup"><span data-stu-id="80a4b-113">Text value</span></span>

<span data-ttu-id="80a4b-114">文本值为**true**的**HasChanged**元素指示照片已更改所返回的最后一次。</span><span class="sxs-lookup"><span data-stu-id="80a4b-114">A text value of **true** for the **HasChanged** element indicates that the photo has changed since the last time it was returned.</span></span> <span data-ttu-id="80a4b-115">如果值为**false**指示最后一次它返回未更改的照片。</span><span class="sxs-lookup"><span data-stu-id="80a4b-115">A value of **false** indicates that the photo has not changed since the last time it was returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="80a4b-116">备注</span><span class="sxs-lookup"><span data-stu-id="80a4b-116">Remarks</span></span>

<span data-ttu-id="80a4b-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="80a4b-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="80a4b-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="80a4b-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80a4b-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="80a4b-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80a4b-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="80a4b-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="80a4b-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="80a4b-121">Schema name</span></span>  <br/> |<span data-ttu-id="80a4b-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="80a4b-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="80a4b-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="80a4b-123">Validation file</span></span>  <br/> |<span data-ttu-id="80a4b-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="80a4b-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="80a4b-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="80a4b-125">Can be empty</span></span>  <br/> ||
   

