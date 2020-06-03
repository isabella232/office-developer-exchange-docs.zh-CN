---
title: GoodThreshold
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GoodThreshold
api_type:
- schema
ms.assetid: 68f607f5-7271-46a6-8ffc-91878185a683
description: GoodThreshold 元素指定必须处于打开状态的与会者的百分比，以使时间段的时间段处于限定状态以作为一个合理的建议会议时间。
ms.openlocfilehash: 34ea433ad7315d61df8cf8e22bae1166d3210af3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457310"
---
# <a name="goodthreshold"></a><span data-ttu-id="6180f-103">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="6180f-103">GoodThreshold</span></span>

<span data-ttu-id="6180f-104">**GoodThreshold**元素指定必须处于打开状态的与会者的百分比，以使时间段的时间段处于限定状态以作为一个合理的建议会议时间。</span><span class="sxs-lookup"><span data-stu-id="6180f-104">The **GoodThreshold** element specifies the percentage of attendees that must have the time period open in order for the time period to qualify as a Good suggested meeting time.</span></span> 
  
[<span data-ttu-id="6180f-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="6180f-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="6180f-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="6180f-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="6180f-107">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="6180f-107">GoodThreshold</span></span>](goodthreshold.md)
  
```xml
<GoodThreshold>...</GoodThreshold>
```

 <span data-ttu-id="6180f-108">**int**</span><span class="sxs-lookup"><span data-stu-id="6180f-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6180f-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6180f-109">Attributes and elements</span></span>

<span data-ttu-id="6180f-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6180f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6180f-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="6180f-111">Attributes</span></span>

<span data-ttu-id="6180f-112">无。</span><span class="sxs-lookup"><span data-stu-id="6180f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6180f-113">子元素</span><span class="sxs-lookup"><span data-stu-id="6180f-113">Child elements</span></span>

<span data-ttu-id="6180f-114">无。</span><span class="sxs-lookup"><span data-stu-id="6180f-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6180f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6180f-115">Parent elements</span></span>

|<span data-ttu-id="6180f-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6180f-116">**Element**</span></span>|<span data-ttu-id="6180f-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6180f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6180f-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="6180f-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="6180f-119">包含用于获取会议建议信息的选项。</span><span class="sxs-lookup"><span data-stu-id="6180f-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="6180f-120">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="6180f-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6180f-121">文本值</span><span class="sxs-lookup"><span data-stu-id="6180f-121">Text value</span></span>

<span data-ttu-id="6180f-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="6180f-122">A text value is required.</span></span> <span data-ttu-id="6180f-123">预期的整数值介于0到50之间。</span><span class="sxs-lookup"><span data-stu-id="6180f-123">The expected integer values are between 0 and 50.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6180f-124">备注</span><span class="sxs-lookup"><span data-stu-id="6180f-124">Remarks</span></span>

<span data-ttu-id="6180f-125">如果使用[SuggestionsViewOptions](suggestionsviewoptions.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="6180f-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> <span data-ttu-id="6180f-126">**GoodThreshold**元素还确定哪些会议被视为公平。</span><span class="sxs-lookup"><span data-stu-id="6180f-126">The **GoodThreshold** element also determines what meetings are considered Fair.</span></span> <span data-ttu-id="6180f-127">其冲突的与会者所占的百分比小于 "好" 阈值和高于50%，建议会议时间为 "公平"。</span><span class="sxs-lookup"><span data-stu-id="6180f-127">It the percentage of attendees with conflicts is less than the Good Threshold and higher than 50 percent, the suggested meeting time qualifies as Fair.</span></span> <span data-ttu-id="6180f-128">正常阈值加上50等于定义正常/公平阈值的百分比。</span><span class="sxs-lookup"><span data-stu-id="6180f-128">The Good Threshold plus 50 equals the percentage that defines the Good/Fair threshold.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6180f-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6180f-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6180f-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="6180f-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6180f-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="6180f-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6180f-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="6180f-132">Schema Name</span></span>  <br/> |<span data-ttu-id="6180f-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="6180f-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="6180f-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="6180f-134">Validation File</span></span>  <br/> |<span data-ttu-id="6180f-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6180f-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6180f-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="6180f-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="6180f-137">False</span><span class="sxs-lookup"><span data-stu-id="6180f-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6180f-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6180f-138">See also</span></span>



[<span data-ttu-id="6180f-139">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="6180f-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="6180f-140">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="6180f-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

