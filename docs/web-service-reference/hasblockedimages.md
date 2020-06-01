---
title: HasBlockedImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddeb11db-797d-4939-91d5-3e44be5f0778
description: HasBlockedImages 元素指定一个布尔值，该值指示项目是否已阻止图像。
ms.openlocfilehash: 370ab4b12ae841815faa344b2fd3a6d3ddc16bcb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462792"
---
# <a name="hasblockedimages"></a><span data-ttu-id="72c9f-103">HasBlockedImages</span><span class="sxs-lookup"><span data-stu-id="72c9f-103">HasBlockedImages</span></span>

<span data-ttu-id="72c9f-104">**HasBlockedImages**元素指定一个布尔值，该值指示项目是否已阻止图像。</span><span class="sxs-lookup"><span data-stu-id="72c9f-104">The **HasBlockedImages** element specifies a Boolean value that indicates whether the item has blocked images.</span></span> 
  
```XML
<HasBlockedImages> true | false </HasBlockedImages>
```

 <span data-ttu-id="72c9f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="72c9f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="72c9f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="72c9f-106">Attributes and elements</span></span>

<span data-ttu-id="72c9f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="72c9f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72c9f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="72c9f-108">Attributes</span></span>

<span data-ttu-id="72c9f-109">无。</span><span class="sxs-lookup"><span data-stu-id="72c9f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="72c9f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="72c9f-110">Child elements</span></span>

<span data-ttu-id="72c9f-111">无。</span><span class="sxs-lookup"><span data-stu-id="72c9f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="72c9f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="72c9f-112">Parent elements</span></span>

|<span data-ttu-id="72c9f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="72c9f-113">**Element**</span></span>|<span data-ttu-id="72c9f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="72c9f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72c9f-115">Item</span><span class="sxs-lookup"><span data-stu-id="72c9f-115">Item</span></span>](item.md) <br/> |<span data-ttu-id="72c9f-116">表示 Exchange 存储中的一般项目。</span><span class="sxs-lookup"><span data-stu-id="72c9f-116">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="72c9f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="72c9f-117">Text value</span></span>

<span data-ttu-id="72c9f-118">如果**HasBlockedImages**元素的文本值为**true** ，则表示该项目具有阻止的图像。</span><span class="sxs-lookup"><span data-stu-id="72c9f-118">A text value of **true** for the **HasBlockedImages** element indicates that the item has blocked images.</span></span> <span data-ttu-id="72c9f-119">**如果值为 false** ，则表示项目没有任何被阻止的图像。</span><span class="sxs-lookup"><span data-stu-id="72c9f-119">A value of **false** indicates that the item does not have any blocked images.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="72c9f-120">备注</span><span class="sxs-lookup"><span data-stu-id="72c9f-120">Remarks</span></span>

<span data-ttu-id="72c9f-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="72c9f-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="72c9f-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="72c9f-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="72c9f-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="72c9f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72c9f-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="72c9f-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="72c9f-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="72c9f-125">Schema Name</span></span>  <br/> |<span data-ttu-id="72c9f-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="72c9f-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="72c9f-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="72c9f-127">Validation File</span></span>  <br/> |<span data-ttu-id="72c9f-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="72c9f-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="72c9f-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="72c9f-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="72c9f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="72c9f-130">See also</span></span>



- [<span data-ttu-id="72c9f-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="72c9f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

