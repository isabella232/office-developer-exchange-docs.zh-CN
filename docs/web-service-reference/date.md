---
title: 日期
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Date
api_type:
- schema
ms.assetid: 2f6bc090-fff4-45b1-8d7e-8fd6e060cce2
description: Date 元素表示包含建议的会议时间的日期。
ms.openlocfilehash: 98dc9d6c599222c819b2c9ed1bacd05758ae1655
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753737"
---
# <a name="date"></a><span data-ttu-id="f05ac-103">日期</span><span class="sxs-lookup"><span data-stu-id="f05ac-103">Date</span></span>

<span data-ttu-id="f05ac-104">**Date**元素表示包含建议的会议时间的日期。</span><span class="sxs-lookup"><span data-stu-id="f05ac-104">The **Date** element represents the date that contains the suggested meeting times.</span></span> 
  
- [<span data-ttu-id="f05ac-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f05ac-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) 
- [<span data-ttu-id="f05ac-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="f05ac-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="f05ac-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="f05ac-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="f05ac-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="f05ac-108">SuggestionDayResult</span></span>](suggestiondayresult.md)  
- [<span data-ttu-id="f05ac-109">日期</span><span class="sxs-lookup"><span data-stu-id="f05ac-109">Date</span></span>](date.md)
  
```xml
<Date>...</Date>
```

<span data-ttu-id="f05ac-110">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="f05ac-110">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f05ac-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f05ac-111">Attributes and elements</span></span>

<span data-ttu-id="f05ac-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f05ac-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f05ac-113">属性</span><span class="sxs-lookup"><span data-stu-id="f05ac-113">Attributes</span></span>

<span data-ttu-id="f05ac-114">无。</span><span class="sxs-lookup"><span data-stu-id="f05ac-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f05ac-115">子元素</span><span class="sxs-lookup"><span data-stu-id="f05ac-115">Child elements</span></span>

<span data-ttu-id="f05ac-116">无。</span><span class="sxs-lookup"><span data-stu-id="f05ac-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f05ac-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f05ac-117">Parent elements</span></span>

|<span data-ttu-id="f05ac-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="f05ac-118">**Element**</span></span>|<span data-ttu-id="f05ac-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="f05ac-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f05ac-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="f05ac-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="f05ac-121">表示一天包含建议的会议的时间。</span><span class="sxs-lookup"><span data-stu-id="f05ac-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="f05ac-122">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="f05ac-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f05ac-123">文本值</span><span class="sxs-lookup"><span data-stu-id="f05ac-123">Text value</span></span>

<span data-ttu-id="f05ac-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="f05ac-124">A text value is required.</span></span> <span data-ttu-id="f05ac-125">查看格式的日期时间基元数据类型的万维网联合会 (W3C) 架构数据类型建议。</span><span class="sxs-lookup"><span data-stu-id="f05ac-125">Review the World Wide Web Consortium (W3C) schema datatype recommendations for the format of the dateTime primitive datatype.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f05ac-126">备注</span><span class="sxs-lookup"><span data-stu-id="f05ac-126">Remarks</span></span>

<span data-ttu-id="f05ac-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f05ac-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f05ac-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="f05ac-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f05ac-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="f05ac-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f05ac-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="f05ac-130">Schema Name</span></span>  <br/> |<span data-ttu-id="f05ac-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="f05ac-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="f05ac-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="f05ac-132">Validation File</span></span>  <br/> |<span data-ttu-id="f05ac-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f05ac-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f05ac-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="f05ac-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="f05ac-135">False</span><span class="sxs-lookup"><span data-stu-id="f05ac-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f05ac-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f05ac-136">See also</span></span>

- [<span data-ttu-id="f05ac-137">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="f05ac-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="f05ac-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f05ac-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="f05ac-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="f05ac-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

