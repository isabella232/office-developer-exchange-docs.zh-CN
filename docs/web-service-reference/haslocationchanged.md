---
title: HasLocationChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fd465b4-6070-4cd0-9ac3-ed9d2bfd5951
description: HasLocationChanged 元素指定会议的 location 属性是否已更改。
ms.openlocfilehash: dbb811b93149be0bb43fbb2f579a5086a396e401
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825804"
---
# <a name="haslocationchanged"></a><span data-ttu-id="43d16-103">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="43d16-103">HasLocationChanged</span></span>

<span data-ttu-id="43d16-104">**HasLocationChanged**元素指定会议的 location 属性是否已更改。</span><span class="sxs-lookup"><span data-stu-id="43d16-104">The **HasLocationChanged** element specifies whether the location property of a meeting has changed.</span></span> 
  
```XML
<HasLocationChanged> true | false </HasLocationChanged>
```

 <span data-ttu-id="43d16-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="43d16-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43d16-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="43d16-106">Attributes and elements</span></span>

<span data-ttu-id="43d16-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="43d16-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43d16-108">属性</span><span class="sxs-lookup"><span data-stu-id="43d16-108">Attributes</span></span>

<span data-ttu-id="43d16-109">无。</span><span class="sxs-lookup"><span data-stu-id="43d16-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43d16-110">子元素</span><span class="sxs-lookup"><span data-stu-id="43d16-110">Child elements</span></span>

<span data-ttu-id="43d16-111">无。</span><span class="sxs-lookup"><span data-stu-id="43d16-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43d16-112">父元素</span><span class="sxs-lookup"><span data-stu-id="43d16-112">Parent elements</span></span>

|<span data-ttu-id="43d16-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="43d16-113">**Element**</span></span>|<span data-ttu-id="43d16-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="43d16-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43d16-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="43d16-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="43d16-116">指定会议的两种版本之间的更改请求消息。</span><span class="sxs-lookup"><span data-stu-id="43d16-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="43d16-117">文本值</span><span class="sxs-lookup"><span data-stu-id="43d16-117">Text value</span></span>

<span data-ttu-id="43d16-118">文本值为**true**的**HasLocationChanged**元素指示会议的 location 属性已更改。</span><span class="sxs-lookup"><span data-stu-id="43d16-118">A text value of **true** for the **HasLocationChanged** element indicates that the location property of a meeting has changed.</span></span> <span data-ttu-id="43d16-119">值**false**指示会议的 location 属性未更改。</span><span class="sxs-lookup"><span data-stu-id="43d16-119">A value **false** indicates that the location property of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="43d16-120">备注</span><span class="sxs-lookup"><span data-stu-id="43d16-120">Remarks</span></span>

<span data-ttu-id="43d16-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="43d16-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="43d16-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="43d16-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43d16-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="43d16-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43d16-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="43d16-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43d16-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="43d16-125">Schema Name</span></span>  <br/> |<span data-ttu-id="43d16-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="43d16-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="43d16-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="43d16-127">Validation File</span></span>  <br/> |<span data-ttu-id="43d16-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="43d16-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="43d16-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="43d16-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="43d16-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43d16-130">See also</span></span>



- [<span data-ttu-id="43d16-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="43d16-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

