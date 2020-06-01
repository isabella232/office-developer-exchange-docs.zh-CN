---
title: DetailedSuggestionsWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DetailedSuggestionsWindow
api_type:
- schema
ms.assetid: 7b348d63-6a7d-45f4-9562-5c42243d63a5
description: DetailedSuggestionsWindow 元素标识查询的时间跨度，以获取有关建议会议时间的详细信息。
ms.openlocfilehash: 45d582f2642c0e3d8f6330b09946230c8842618d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467842"
---
# <a name="detailedsuggestionswindow"></a><span data-ttu-id="ba81f-103">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="ba81f-103">DetailedSuggestionsWindow</span></span>

<span data-ttu-id="ba81f-104">**DetailedSuggestionsWindow**元素标识查询的时间跨度，以获取有关建议会议时间的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ba81f-104">The **DetailedSuggestionsWindow** element identifies the time span that is queried for detailed information about suggested meeting times.</span></span> 
  
- [<span data-ttu-id="ba81f-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="ba81f-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) 
- [<span data-ttu-id="ba81f-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="ba81f-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) 
- [<span data-ttu-id="ba81f-107">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="ba81f-107">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md)
  
```xml
<DetailedSuggestionsWindow>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
</DetailedSuggestionsWindow>
```

 <span data-ttu-id="ba81f-108">**Duration**</span><span class="sxs-lookup"><span data-stu-id="ba81f-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba81f-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ba81f-109">Attributes and elements</span></span>

<span data-ttu-id="ba81f-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ba81f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba81f-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="ba81f-111">Attributes</span></span>

<span data-ttu-id="ba81f-112">无。</span><span class="sxs-lookup"><span data-stu-id="ba81f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba81f-113">子元素</span><span class="sxs-lookup"><span data-stu-id="ba81f-113">Child elements</span></span>

|<span data-ttu-id="ba81f-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba81f-114">**Element**</span></span>|<span data-ttu-id="ba81f-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba81f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba81f-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="ba81f-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="ba81f-117">表示查询时间跨度的开始时间，以获取有关建议会议时间的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ba81f-117">Represents the start of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="ba81f-118">EndTime</span><span class="sxs-lookup"><span data-stu-id="ba81f-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="ba81f-119">表示查询时间跨度的结束时间，以获取有关建议会议时间的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ba81f-119">Represents the end of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba81f-120">父元素</span><span class="sxs-lookup"><span data-stu-id="ba81f-120">Parent elements</span></span>

|<span data-ttu-id="ba81f-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba81f-121">**Element**</span></span>|<span data-ttu-id="ba81f-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba81f-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba81f-123">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="ba81f-123">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="ba81f-124">包含用于获取会议建议信息的选项。</span><span class="sxs-lookup"><span data-stu-id="ba81f-124">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="ba81f-125">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="ba81f-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba81f-126">备注</span><span class="sxs-lookup"><span data-stu-id="ba81f-126">Remarks</span></span>

<span data-ttu-id="ba81f-127">此元素不是必需的。</span><span class="sxs-lookup"><span data-stu-id="ba81f-127">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ba81f-128">描述此元素的架构位于运行 MicrosoftExchange Server 2007 且安装了客户端访问服务器角色的计算机的/EWS/目录中。</span><span class="sxs-lookup"><span data-stu-id="ba81f-128">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ba81f-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="ba81f-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba81f-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="ba81f-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba81f-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="ba81f-131">Schema Name</span></span>  <br/> |<span data-ttu-id="ba81f-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="ba81f-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba81f-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="ba81f-133">Validation File</span></span>  <br/> |<span data-ttu-id="ba81f-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba81f-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba81f-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="ba81f-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba81f-136">False</span><span class="sxs-lookup"><span data-stu-id="ba81f-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba81f-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ba81f-137">See also</span></span>

- [<span data-ttu-id="ba81f-138">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="ba81f-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="ba81f-139">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="ba81f-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

