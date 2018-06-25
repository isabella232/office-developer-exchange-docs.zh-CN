---
title: MaximumNonWorkHourResultsByDay
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaximumNonWorkHourResultsByDay
api_type:
- schema
ms.assetid: 9fb7314d-779c-4b1f-9d7c-b5cb092ed134
description: MaximumNonWorkHourResultsByDay 元素指定的会议时间每天的正常工作时间以外的建议结果数。
ms.openlocfilehash: f931dcaabda222e1579a0a4c0e0e6e49d88c6342
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826382"
---
# <a name="maximumnonworkhourresultsbyday"></a><span data-ttu-id="a9b58-103">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="a9b58-103">MaximumNonWorkHourResultsByDay</span></span>

<span data-ttu-id="a9b58-104">**MaximumNonWorkHourResultsByDay**元素指定的会议时间每天的正常工作时间以外的建议结果数。</span><span class="sxs-lookup"><span data-stu-id="a9b58-104">The **MaximumNonWorkHourResultsByDay** element specifies the number of suggested results for meeting times outside regular working hours per day.</span></span> 
  
[<span data-ttu-id="a9b58-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="a9b58-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="a9b58-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="a9b58-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="a9b58-107">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="a9b58-107">MaximumNonWorkHourResultsByDay</span></span>](maximumnonworkhourresultsbyday.md)
  
```xml
<MaximumNonWorkHourResultsByDay>...</MaximumNonWorkHourResultsByDay>
```

 <span data-ttu-id="a9b58-108">**int**</span><span class="sxs-lookup"><span data-stu-id="a9b58-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9b58-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a9b58-109">Attributes and elements</span></span>

<span data-ttu-id="a9b58-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a9b58-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9b58-111">属性</span><span class="sxs-lookup"><span data-stu-id="a9b58-111">Attributes</span></span>

<span data-ttu-id="a9b58-112">无。</span><span class="sxs-lookup"><span data-stu-id="a9b58-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9b58-113">子元素</span><span class="sxs-lookup"><span data-stu-id="a9b58-113">Child elements</span></span>

<span data-ttu-id="a9b58-114">无。</span><span class="sxs-lookup"><span data-stu-id="a9b58-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a9b58-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a9b58-115">Parent elements</span></span>

|<span data-ttu-id="a9b58-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a9b58-116">**Element**</span></span>|<span data-ttu-id="a9b58-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a9b58-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9b58-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="a9b58-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="a9b58-119">包含选项的获取会议建议信息。</span><span class="sxs-lookup"><span data-stu-id="a9b58-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="a9b58-120">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="a9b58-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9b58-121">文本值</span><span class="sxs-lookup"><span data-stu-id="a9b58-121">Text value</span></span>

<span data-ttu-id="a9b58-p101">文本值是必需的。文本值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="a9b58-p101">A text value is required. The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9b58-124">备注</span><span class="sxs-lookup"><span data-stu-id="a9b58-124">Remarks</span></span>

<span data-ttu-id="a9b58-125">如果使用[SuggestionsViewOptions](suggestionsviewoptions.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="a9b58-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a9b58-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a9b58-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a9b58-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="a9b58-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9b58-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="a9b58-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9b58-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="a9b58-129">Schema Name</span></span>  <br/> |<span data-ttu-id="a9b58-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="a9b58-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9b58-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="a9b58-131">Validation File</span></span>  <br/> |<span data-ttu-id="a9b58-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9b58-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9b58-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="a9b58-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9b58-134">False</span><span class="sxs-lookup"><span data-stu-id="a9b58-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9b58-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a9b58-135">See also</span></span>



[<span data-ttu-id="a9b58-136">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="a9b58-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="a9b58-137">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="a9b58-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

