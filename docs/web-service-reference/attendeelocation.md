---
title: AttendeeLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1344a087-88ea-472a-bebf-9b45245592fb
description: AttendeeLocation 元素指定与会者的日历项目的位置。
ms.openlocfilehash: 4670f1fa59fec4cf1e2b35a1380f6205677ce5af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753284"
---
# <a name="attendeelocation"></a><span data-ttu-id="1971c-103">AttendeeLocation</span><span class="sxs-lookup"><span data-stu-id="1971c-103">AttendeeLocation</span></span>

<span data-ttu-id="1971c-104">**AttendeeLocation**元素指定与会者的日历项目的位置。</span><span class="sxs-lookup"><span data-stu-id="1971c-104">The **AttendeeLocation** element specifies the location of an attendee for a calendar item.</span></span> 
  
```XML
<AttendeeLocation></AttendeeLocation>
```

 <span data-ttu-id="1971c-105">**将**</span><span class="sxs-lookup"><span data-stu-id="1971c-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1971c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1971c-106">Attributes and elements</span></span>

<span data-ttu-id="1971c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1971c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1971c-108">属性</span><span class="sxs-lookup"><span data-stu-id="1971c-108">Attributes</span></span>

<span data-ttu-id="1971c-109">无。</span><span class="sxs-lookup"><span data-stu-id="1971c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1971c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1971c-110">Child elements</span></span>

<span data-ttu-id="1971c-111">无。</span><span class="sxs-lookup"><span data-stu-id="1971c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1971c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1971c-112">Parent elements</span></span>

|<span data-ttu-id="1971c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1971c-113">**Element**</span></span>|<span data-ttu-id="1971c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1971c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1971c-115">LocationBasedStateDefinition</span><span class="sxs-lookup"><span data-stu-id="1971c-115">LocationBasedStateDefinition</span></span>](locationbasedstatedefinition.md) <br/> |<span data-ttu-id="1971c-116">基于位置时，请指定的状态。</span><span class="sxs-lookup"><span data-stu-id="1971c-116">Specifies the state when it is based on location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1971c-117">文本值</span><span class="sxs-lookup"><span data-stu-id="1971c-117">Text value</span></span>

<span data-ttu-id="1971c-118">AttendeeLocation 元素的文本值是选的与会者位置。</span><span class="sxs-lookup"><span data-stu-id="1971c-118">The text value of the AttendeeLocation element is the attendess location.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1971c-119">备注</span><span class="sxs-lookup"><span data-stu-id="1971c-119">Remarks</span></span>

<span data-ttu-id="1971c-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1971c-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1971c-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1971c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1971c-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="1971c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1971c-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="1971c-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1971c-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="1971c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="1971c-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="1971c-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="1971c-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="1971c-126">Validation File</span></span>  <br/> |<span data-ttu-id="1971c-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="1971c-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1971c-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="1971c-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1971c-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1971c-129">See also</span></span>

- [<span data-ttu-id="1971c-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1971c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

