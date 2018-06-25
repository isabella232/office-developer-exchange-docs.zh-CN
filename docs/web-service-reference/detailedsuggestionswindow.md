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
description: DetailedSuggestionsWindow 元素标识查询建议的会议时间有关的详细信息的时间跨度。
ms.openlocfilehash: 8a3af0178d0c96b50f4dd641716a9f7a7be8f7a2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753850"
---
# <a name="detailedsuggestionswindow"></a><span data-ttu-id="3b1aa-103">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="3b1aa-103">DetailedSuggestionsWindow</span></span>

<span data-ttu-id="3b1aa-104">**DetailedSuggestionsWindow**元素标识查询建议的会议时间有关的详细信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="3b1aa-104">The **DetailedSuggestionsWindow** element identifies the time span that is queried for detailed information about suggested meeting times.</span></span> 
  
- [<span data-ttu-id="3b1aa-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="3b1aa-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) 
- [<span data-ttu-id="3b1aa-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="3b1aa-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) 
- [<span data-ttu-id="3b1aa-107">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="3b1aa-107">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md)
  
```xml
<DetailedSuggestionsWindow>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
</DetailedSuggestionsWindow>
```

 <span data-ttu-id="3b1aa-108">**持续时间**</span><span class="sxs-lookup"><span data-stu-id="3b1aa-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b1aa-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3b1aa-109">Attributes and elements</span></span>

<span data-ttu-id="3b1aa-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3b1aa-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b1aa-111">属性</span><span class="sxs-lookup"><span data-stu-id="3b1aa-111">Attributes</span></span>

<span data-ttu-id="3b1aa-112">无。</span><span class="sxs-lookup"><span data-stu-id="3b1aa-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b1aa-113">子元素</span><span class="sxs-lookup"><span data-stu-id="3b1aa-113">Child elements</span></span>

|<span data-ttu-id="3b1aa-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="3b1aa-114">**Element**</span></span>|<span data-ttu-id="3b1aa-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="3b1aa-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b1aa-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="3b1aa-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="3b1aa-117">表示查询建议的会议时间的详细信息的时间跨度的开头。</span><span class="sxs-lookup"><span data-stu-id="3b1aa-117">Represents the start of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="3b1aa-118">结束时间</span><span class="sxs-lookup"><span data-stu-id="3b1aa-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="3b1aa-119">表示查询建议的会议时间的详细信息的时间跨度的末尾。</span><span class="sxs-lookup"><span data-stu-id="3b1aa-119">Represents the end of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3b1aa-120">父元素</span><span class="sxs-lookup"><span data-stu-id="3b1aa-120">Parent elements</span></span>

|<span data-ttu-id="3b1aa-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="3b1aa-121">**Element**</span></span>|<span data-ttu-id="3b1aa-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="3b1aa-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b1aa-123">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="3b1aa-123">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="3b1aa-124">包含选项的获取会议建议信息。</span><span class="sxs-lookup"><span data-stu-id="3b1aa-124">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="3b1aa-125">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="3b1aa-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b1aa-126">注解</span><span class="sxs-lookup"><span data-stu-id="3b1aa-126">Remarks</span></span>

<span data-ttu-id="3b1aa-127">此元素不是必需的。</span><span class="sxs-lookup"><span data-stu-id="3b1aa-127">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3b1aa-128">描述此元素的架构位于运行 MicrosoftExchange Server 2007 的安装了客户端访问服务器角色的计算机的 /EWS/ 目录中。</span><span class="sxs-lookup"><span data-stu-id="3b1aa-128">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3b1aa-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="3b1aa-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b1aa-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="3b1aa-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b1aa-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="3b1aa-131">Schema Name</span></span>  <br/> |<span data-ttu-id="3b1aa-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="3b1aa-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b1aa-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="3b1aa-133">Validation File</span></span>  <br/> |<span data-ttu-id="3b1aa-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b1aa-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b1aa-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="3b1aa-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b1aa-136">False</span><span class="sxs-lookup"><span data-stu-id="3b1aa-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b1aa-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3b1aa-137">See also</span></span>

- [<span data-ttu-id="3b1aa-138">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="3b1aa-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="3b1aa-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="3b1aa-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

