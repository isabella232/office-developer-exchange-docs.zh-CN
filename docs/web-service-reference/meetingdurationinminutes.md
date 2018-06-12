---
title: MeetingDurationInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingDurationInMinutes
api_type:
- schema
ms.assetid: bb86b275-9c29-4daf-8196-8d505b87a4f4
description: MeetingDurationInMinutes 元素指定会议建议的持续的时间。
ms.openlocfilehash: 2ff60b69fb352c2ac7316f1ca231bb04da67ead2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826433"
---
# <a name="meetingdurationinminutes"></a><span data-ttu-id="d9c19-103">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="d9c19-103">MeetingDurationInMinutes</span></span>

<span data-ttu-id="d9c19-104">**MeetingDurationInMinutes**元素指定会议建议的持续的时间。</span><span class="sxs-lookup"><span data-stu-id="d9c19-104">The **MeetingDurationInMinutes** element specifies the duration of the meeting to be suggested.</span></span> 
  
[<span data-ttu-id="d9c19-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="d9c19-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="d9c19-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="d9c19-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="d9c19-107">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="d9c19-107">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md)
  
```xml
<MeetingDurationInMinutes>...</MeetingDurationInMinutes>
```

 <span data-ttu-id="d9c19-108">**int**</span><span class="sxs-lookup"><span data-stu-id="d9c19-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9c19-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d9c19-109">Attributes and elements</span></span>

<span data-ttu-id="d9c19-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d9c19-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9c19-111">属性</span><span class="sxs-lookup"><span data-stu-id="d9c19-111">Attributes</span></span>

<span data-ttu-id="d9c19-112">无。</span><span class="sxs-lookup"><span data-stu-id="d9c19-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9c19-113">子元素</span><span class="sxs-lookup"><span data-stu-id="d9c19-113">Child elements</span></span>

<span data-ttu-id="d9c19-114">无。</span><span class="sxs-lookup"><span data-stu-id="d9c19-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d9c19-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d9c19-115">Parent elements</span></span>

|<span data-ttu-id="d9c19-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9c19-116">**Element**</span></span>|<span data-ttu-id="d9c19-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9c19-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9c19-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="d9c19-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="d9c19-119">包含选项的获取会议建议信息。</span><span class="sxs-lookup"><span data-stu-id="d9c19-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="d9c19-120">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="d9c19-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d9c19-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d9c19-121">Text value</span></span>

<span data-ttu-id="d9c19-p101">文本值是必需的。文本值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="d9c19-p101">A text value is required. The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9c19-124">备注</span><span class="sxs-lookup"><span data-stu-id="d9c19-124">Remarks</span></span>

<span data-ttu-id="d9c19-125">如果使用[SuggestionsViewOptions](suggestionsviewoptions.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="d9c19-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d9c19-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d9c19-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d9c19-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="d9c19-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9c19-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="d9c19-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d9c19-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="d9c19-129">Schema Name</span></span>  <br/> |<span data-ttu-id="d9c19-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="d9c19-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="d9c19-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="d9c19-131">Validation File</span></span>  <br/> |<span data-ttu-id="d9c19-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d9c19-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d9c19-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="d9c19-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9c19-134">False</span><span class="sxs-lookup"><span data-stu-id="d9c19-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9c19-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9c19-135">See also</span></span>



[<span data-ttu-id="d9c19-136">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="d9c19-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="d9c19-137">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="d9c19-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
