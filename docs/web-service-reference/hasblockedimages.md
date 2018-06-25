---
title: HasBlockedImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddeb11db-797d-4939-91d5-3e44be5f0778
description: HasBlockedImages 元素指定一个布尔值，指示项目是否已阻止图像。
ms.openlocfilehash: fbe9967c898016aeef27e3c86e8a1cf603bd87fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825795"
---
# <a name="hasblockedimages"></a><span data-ttu-id="fe05e-103">HasBlockedImages</span><span class="sxs-lookup"><span data-stu-id="fe05e-103">HasBlockedImages</span></span>

<span data-ttu-id="fe05e-104">**HasBlockedImages**元素指定一个布尔值，指示项目是否已阻止图像。</span><span class="sxs-lookup"><span data-stu-id="fe05e-104">The **HasBlockedImages** element specifies a Boolean value that indicates whether the item has blocked images.</span></span> 
  
```XML
<HasBlockedImages> true | false </HasBlockedImages>
```

 <span data-ttu-id="fe05e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe05e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe05e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fe05e-106">Attributes and elements</span></span>

<span data-ttu-id="fe05e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fe05e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe05e-108">属性</span><span class="sxs-lookup"><span data-stu-id="fe05e-108">Attributes</span></span>

<span data-ttu-id="fe05e-109">无。</span><span class="sxs-lookup"><span data-stu-id="fe05e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe05e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fe05e-110">Child elements</span></span>

<span data-ttu-id="fe05e-111">无。</span><span class="sxs-lookup"><span data-stu-id="fe05e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe05e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fe05e-112">Parent elements</span></span>

|<span data-ttu-id="fe05e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fe05e-113">**Element**</span></span>|<span data-ttu-id="fe05e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe05e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe05e-115">Item</span><span class="sxs-lookup"><span data-stu-id="fe05e-115">Item</span></span>](item.md) <br/> |<span data-ttu-id="fe05e-116">表示 Exchange 存储中的泛型项。</span><span class="sxs-lookup"><span data-stu-id="fe05e-116">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fe05e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="fe05e-117">Text value</span></span>

<span data-ttu-id="fe05e-118">文本值为**true**的**HasBlockedImages**元素表示该项目已阻止图像。</span><span class="sxs-lookup"><span data-stu-id="fe05e-118">A text value of **true** for the **HasBlockedImages** element indicates that the item has blocked images.</span></span> <span data-ttu-id="fe05e-119">如果值为**false**指示项目没有任何被阻止的图像。</span><span class="sxs-lookup"><span data-stu-id="fe05e-119">A value of **false** indicates that the item does not have any blocked images.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe05e-120">备注</span><span class="sxs-lookup"><span data-stu-id="fe05e-120">Remarks</span></span>

<span data-ttu-id="fe05e-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fe05e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fe05e-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fe05e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe05e-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="fe05e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe05e-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="fe05e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fe05e-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="fe05e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="fe05e-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="fe05e-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="fe05e-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="fe05e-127">Validation File</span></span>  <br/> |<span data-ttu-id="fe05e-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="fe05e-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fe05e-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="fe05e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fe05e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe05e-130">See also</span></span>



- [<span data-ttu-id="fe05e-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fe05e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

