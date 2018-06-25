---
title: HasEndTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0eb444d-8e2e-478b-b785-2b9787ffb226
description: HasEndTimeChanged 元素指定是否已更改为会议的结束时间。
ms.openlocfilehash: 046bb302d6f7052c6f1757ce393583b305311e2f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825805"
---
# <a name="hasendtimechanged"></a><span data-ttu-id="e819a-103">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="e819a-103">HasEndTimeChanged</span></span>

<span data-ttu-id="e819a-104">**HasEndTimeChanged**元素指定是否已更改为会议的结束时间。</span><span class="sxs-lookup"><span data-stu-id="e819a-104">The **HasEndTimeChanged** element specifies whether the end time for a meeting has changed.</span></span> 
  
```XML
<HasEndTimeChanged>true | false</HasEndTimeChanged>
```

 <span data-ttu-id="e819a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e819a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e819a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e819a-106">Attributes and elements</span></span>

<span data-ttu-id="e819a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e819a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e819a-108">属性</span><span class="sxs-lookup"><span data-stu-id="e819a-108">Attributes</span></span>

<span data-ttu-id="e819a-109">无。</span><span class="sxs-lookup"><span data-stu-id="e819a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e819a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e819a-110">Child elements</span></span>

<span data-ttu-id="e819a-111">无。</span><span class="sxs-lookup"><span data-stu-id="e819a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e819a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e819a-112">Parent elements</span></span>

|<span data-ttu-id="e819a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e819a-113">**Element**</span></span>|<span data-ttu-id="e819a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e819a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e819a-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="e819a-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="e819a-116">指定会议的两种版本之间的更改请求消息。</span><span class="sxs-lookup"><span data-stu-id="e819a-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e819a-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e819a-117">Text value</span></span>

<span data-ttu-id="e819a-118">文本值为**true**的**HasEndTimeChanged**元素指示会议的结束时间已更改。</span><span class="sxs-lookup"><span data-stu-id="e819a-118">A text value of **true** for the **HasEndTimeChanged** element indicates that the end time of a meeting has changed.</span></span> <span data-ttu-id="e819a-119">如果值为**false**指示会议的结束时间未更改。</span><span class="sxs-lookup"><span data-stu-id="e819a-119">A value of **false** indicates that the end time of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e819a-120">备注</span><span class="sxs-lookup"><span data-stu-id="e819a-120">Remarks</span></span>

<span data-ttu-id="e819a-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e819a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e819a-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e819a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e819a-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="e819a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e819a-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="e819a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e819a-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="e819a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e819a-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="e819a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="e819a-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="e819a-127">Validation File</span></span>  <br/> |<span data-ttu-id="e819a-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="e819a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e819a-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="e819a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e819a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e819a-130">See also</span></span>



- [<span data-ttu-id="e819a-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e819a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

