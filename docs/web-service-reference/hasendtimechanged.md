---
title: HasEndTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0eb444d-8e2e-478b-b785-2b9787ffb226
description: HasEndTimeChanged 元素指定会议的结束时间是否已更改。
ms.openlocfilehash: 15ad52c7b7581cce5ca96ba5ff4e8a1c130a02cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461784"
---
# <a name="hasendtimechanged"></a><span data-ttu-id="3402b-103">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="3402b-103">HasEndTimeChanged</span></span>

<span data-ttu-id="3402b-104">**HasEndTimeChanged**元素指定会议的结束时间是否已更改。</span><span class="sxs-lookup"><span data-stu-id="3402b-104">The **HasEndTimeChanged** element specifies whether the end time for a meeting has changed.</span></span> 
  
```XML
<HasEndTimeChanged>true | false</HasEndTimeChanged>
```

 <span data-ttu-id="3402b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3402b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3402b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3402b-106">Attributes and elements</span></span>

<span data-ttu-id="3402b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3402b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3402b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3402b-108">Attributes</span></span>

<span data-ttu-id="3402b-109">无。</span><span class="sxs-lookup"><span data-stu-id="3402b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3402b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3402b-110">Child elements</span></span>

<span data-ttu-id="3402b-111">无。</span><span class="sxs-lookup"><span data-stu-id="3402b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3402b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3402b-112">Parent elements</span></span>

|<span data-ttu-id="3402b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3402b-113">**Element**</span></span>|<span data-ttu-id="3402b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3402b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3402b-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="3402b-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="3402b-116">指定会议请求邮件的两个版本之间的变化。</span><span class="sxs-lookup"><span data-stu-id="3402b-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3402b-117">文本值</span><span class="sxs-lookup"><span data-stu-id="3402b-117">Text value</span></span>

<span data-ttu-id="3402b-118">如果**HasEndTimeChanged**元素的文本值为**true** ，则表示会议的结束时间已更改。</span><span class="sxs-lookup"><span data-stu-id="3402b-118">A text value of **true** for the **HasEndTimeChanged** element indicates that the end time of a meeting has changed.</span></span> <span data-ttu-id="3402b-119">**如果值为 false** ，则表示会议的结束时间未发生变化。</span><span class="sxs-lookup"><span data-stu-id="3402b-119">A value of **false** indicates that the end time of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3402b-120">备注</span><span class="sxs-lookup"><span data-stu-id="3402b-120">Remarks</span></span>

<span data-ttu-id="3402b-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3402b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3402b-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3402b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3402b-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="3402b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3402b-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="3402b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3402b-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="3402b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3402b-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="3402b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="3402b-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="3402b-127">Validation File</span></span>  <br/> |<span data-ttu-id="3402b-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="3402b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3402b-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="3402b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3402b-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3402b-130">See also</span></span>



- [<span data-ttu-id="3402b-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3402b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

