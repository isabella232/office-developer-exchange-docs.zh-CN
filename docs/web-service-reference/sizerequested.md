---
title: SizeRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e86f98b6-83b5-4530-80eb-dc5df42e2c62
description: SizeRequested 元素包含 GetUserPhoto 操作请求的照片大小。
ms.openlocfilehash: 2e79bbb158fa9a22cbd3ec08fcd6e60429e113b4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460454"
---
# <a name="sizerequested"></a><span data-ttu-id="ef3ee-103">SizeRequested</span><span class="sxs-lookup"><span data-stu-id="ef3ee-103">SizeRequested</span></span>

<span data-ttu-id="ef3ee-104">**SizeRequested**元素包含**GetUserPhoto**操作请求的照片大小。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-104">The **SizeRequested** element contains the requested photo size for a **GetUserPhoto** operation.</span></span> 
  
```XML
<SizeRequested>HR48x48 | HR64x64 | HR96X96 | HR120X120 | HR240X240 | HR360X360 | HR432X432 | HR504X504 | HR648X648</SizeRequested>
```

 <span data-ttu-id="ef3ee-105">**UserPhotoSizeType**</span><span class="sxs-lookup"><span data-stu-id="ef3ee-105">**UserPhotoSizeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef3ee-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ef3ee-106">Attributes and elements</span></span>

<span data-ttu-id="ef3ee-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef3ee-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ef3ee-108">Attributes</span></span>

<span data-ttu-id="ef3ee-109">无。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef3ee-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ef3ee-110">Child elements</span></span>

<span data-ttu-id="ef3ee-111">无。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef3ee-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ef3ee-112">Parent elements</span></span>

[<span data-ttu-id="ef3ee-113">GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="ef3ee-113">GetUserPhoto</span></span>](getuserphoto.md)
  
## <a name="text-value"></a><span data-ttu-id="ef3ee-114">文本值</span><span class="sxs-lookup"><span data-stu-id="ef3ee-114">Text value</span></span>

<span data-ttu-id="ef3ee-115">**SizeRequested**元素的文本值是从服务器返回的数字图像的请求照片大小。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-115">The text value of the **SizeRequested** element is the requested photo size of a digital image returned from the server.</span></span> <span data-ttu-id="ef3ee-116">下表标识了**SizeRequested**元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-116">The following table identifies the text values for the **SizeRequested** element.</span></span> 
  
|<span data-ttu-id="ef3ee-117">**值**</span><span class="sxs-lookup"><span data-stu-id="ef3ee-117">**Value**</span></span>|<span data-ttu-id="ef3ee-118">**含义**</span><span class="sxs-lookup"><span data-stu-id="ef3ee-118">**Meaning**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef3ee-119">HR48x48</span><span class="sxs-lookup"><span data-stu-id="ef3ee-119">HR48x48</span></span>  <br/> |<span data-ttu-id="ef3ee-120">图像的高度为48像素，宽度为48像素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-120">The image is 48 pixels high and 48 pixels wide.</span></span>  <br/> |
|<span data-ttu-id="ef3ee-121">HR64x64</span><span class="sxs-lookup"><span data-stu-id="ef3ee-121">HR64x64</span></span>  <br/> |<span data-ttu-id="ef3ee-122">图像的高度为64像素，宽度为64像素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-122">The image is 64 pixels high and 64 pixels wide.</span></span>  <br/> |
|<span data-ttu-id="ef3ee-123">HR96x96</span><span class="sxs-lookup"><span data-stu-id="ef3ee-123">HR96x96</span></span>  <br/> |<span data-ttu-id="ef3ee-124">图像的高度为96像素，宽度为96像素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-124">The image is 96 pixels high and 96 pixels wide.</span></span>  <br/> |
|<span data-ttu-id="ef3ee-125">HR120x120</span><span class="sxs-lookup"><span data-stu-id="ef3ee-125">HR120x120</span></span>  <br/> |<span data-ttu-id="ef3ee-126">图像的高度为120像素，宽度为120像素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-126">The image is 120 pixels high and 120 pixels wide.</span></span>  <br/> |
|<span data-ttu-id="ef3ee-127">HR240x240</span><span class="sxs-lookup"><span data-stu-id="ef3ee-127">HR240x240</span></span>  <br/> |<span data-ttu-id="ef3ee-128">图像的高度为240像素，宽度为240像素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-128">The image is 240 pixels high and 240 pixels wide.</span></span>  <br/> |
|<span data-ttu-id="ef3ee-129">HR360x360</span><span class="sxs-lookup"><span data-stu-id="ef3ee-129">HR360x360</span></span>  <br/> |<span data-ttu-id="ef3ee-130">图像的高度为360像素，宽度为360像素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-130">The image is 360 pixels high and 360 pixels wide.</span></span>  <br/> |
|<span data-ttu-id="ef3ee-131">HR432x432</span><span class="sxs-lookup"><span data-stu-id="ef3ee-131">HR432x432</span></span>  <br/> |<span data-ttu-id="ef3ee-132">图像的高度为432像素，宽度为432像素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-132">The image is 432 pixels high and 432 pixels wide.</span></span>  <br/> |
|<span data-ttu-id="ef3ee-133">HR504x504</span><span class="sxs-lookup"><span data-stu-id="ef3ee-133">HR504x504</span></span>  <br/> |<span data-ttu-id="ef3ee-134">图像的高度为504像素，宽度为504像素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-134">The image is 504 pixels high and 504 pixels wide.</span></span>  <br/> |
|<span data-ttu-id="ef3ee-135">HR648x648</span><span class="sxs-lookup"><span data-stu-id="ef3ee-135">HR648x648</span></span>  <br/> |<span data-ttu-id="ef3ee-136">图像的高度为648像素，宽度为648像素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-136">The image is 648 pixels high and 648 pixels wide.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef3ee-137">备注</span><span class="sxs-lookup"><span data-stu-id="ef3ee-137">Remarks</span></span>

<span data-ttu-id="ef3ee-138">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-138">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ef3ee-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ef3ee-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef3ee-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="ef3ee-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef3ee-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="ef3ee-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef3ee-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="ef3ee-142">Schema name</span></span>  <br/> |<span data-ttu-id="ef3ee-143">消息架构</span><span class="sxs-lookup"><span data-stu-id="ef3ee-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef3ee-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="ef3ee-144">Validation file</span></span>  <br/> |<span data-ttu-id="ef3ee-145">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ef3ee-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef3ee-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="ef3ee-146">Can be empty</span></span>  <br/> ||
   

