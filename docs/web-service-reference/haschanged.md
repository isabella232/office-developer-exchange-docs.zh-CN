---
title: HasChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: HasChanged 元素指示用户的照片是否已更改。
ms.openlocfilehash: d777220f55d33cde548d8257cf249b57481a43f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462785"
---
# <a name="haschanged"></a><span data-ttu-id="a712e-103">HasChanged</span><span class="sxs-lookup"><span data-stu-id="a712e-103">HasChanged</span></span>

<span data-ttu-id="a712e-104">**HasChanged**元素指示用户的照片是否已更改。</span><span class="sxs-lookup"><span data-stu-id="a712e-104">The **HasChanged** element indicates whether a user's photo has changed.</span></span> 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="a712e-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a712e-105">Attributes and elements</span></span>

<span data-ttu-id="a712e-106">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a712e-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a712e-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="a712e-107">Attributes</span></span>

<span data-ttu-id="a712e-108">无。</span><span class="sxs-lookup"><span data-stu-id="a712e-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a712e-109">子元素</span><span class="sxs-lookup"><span data-stu-id="a712e-109">Child elements</span></span>

<span data-ttu-id="a712e-110">无。</span><span class="sxs-lookup"><span data-stu-id="a712e-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a712e-111">父元素</span><span class="sxs-lookup"><span data-stu-id="a712e-111">Parent elements</span></span>

[<span data-ttu-id="a712e-112">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="a712e-112">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
  
## <a name="text-value"></a><span data-ttu-id="a712e-113">文本值</span><span class="sxs-lookup"><span data-stu-id="a712e-113">Text value</span></span>

<span data-ttu-id="a712e-114">如果**HasChanged**元素的文本值为**true** ，则表示自上次返回后照片已发生更改。</span><span class="sxs-lookup"><span data-stu-id="a712e-114">A text value of **true** for the **HasChanged** element indicates that the photo has changed since the last time it was returned.</span></span> <span data-ttu-id="a712e-115">**如果值为 false** ，则表示照片自上次返回后未发生更改。</span><span class="sxs-lookup"><span data-stu-id="a712e-115">A value of **false** indicates that the photo has not changed since the last time it was returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a712e-116">备注</span><span class="sxs-lookup"><span data-stu-id="a712e-116">Remarks</span></span>

<span data-ttu-id="a712e-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a712e-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a712e-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a712e-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a712e-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="a712e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a712e-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="a712e-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a712e-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="a712e-121">Schema name</span></span>  <br/> |<span data-ttu-id="a712e-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="a712e-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="a712e-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="a712e-123">Validation file</span></span>  <br/> |<span data-ttu-id="a712e-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a712e-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a712e-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="a712e-125">Can be empty</span></span>  <br/> ||
   

