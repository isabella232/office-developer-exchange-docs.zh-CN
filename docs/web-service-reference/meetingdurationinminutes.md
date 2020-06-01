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
description: MeetingDurationInMinutes 元素指定要建议的会议持续时间。
ms.openlocfilehash: b41e234be40c2ad8b28047ae2e812edfd66af644
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467485"
---
# <a name="meetingdurationinminutes"></a><span data-ttu-id="4749e-103">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="4749e-103">MeetingDurationInMinutes</span></span>

<span data-ttu-id="4749e-104">**MeetingDurationInMinutes**元素指定要建议的会议持续时间。</span><span class="sxs-lookup"><span data-stu-id="4749e-104">The **MeetingDurationInMinutes** element specifies the duration of the meeting to be suggested.</span></span> 
  
[<span data-ttu-id="4749e-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="4749e-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="4749e-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="4749e-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="4749e-107">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="4749e-107">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md)
  
```xml
<MeetingDurationInMinutes>...</MeetingDurationInMinutes>
```

 <span data-ttu-id="4749e-108">**int**</span><span class="sxs-lookup"><span data-stu-id="4749e-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4749e-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4749e-109">Attributes and elements</span></span>

<span data-ttu-id="4749e-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4749e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4749e-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="4749e-111">Attributes</span></span>

<span data-ttu-id="4749e-112">无。</span><span class="sxs-lookup"><span data-stu-id="4749e-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4749e-113">子元素</span><span class="sxs-lookup"><span data-stu-id="4749e-113">Child elements</span></span>

<span data-ttu-id="4749e-114">无。</span><span class="sxs-lookup"><span data-stu-id="4749e-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4749e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4749e-115">Parent elements</span></span>

|<span data-ttu-id="4749e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="4749e-116">**Element**</span></span>|<span data-ttu-id="4749e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4749e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4749e-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="4749e-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="4749e-119">包含用于获取会议建议信息的选项。</span><span class="sxs-lookup"><span data-stu-id="4749e-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="4749e-120">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="4749e-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4749e-121">文本值</span><span class="sxs-lookup"><span data-stu-id="4749e-121">Text value</span></span>

<span data-ttu-id="4749e-p101">文本值是必需的。文本值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="4749e-p101">A text value is required. The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4749e-124">说明</span><span class="sxs-lookup"><span data-stu-id="4749e-124">Remarks</span></span>

<span data-ttu-id="4749e-125">如果使用[SuggestionsViewOptions](suggestionsviewoptions.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="4749e-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4749e-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4749e-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4749e-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="4749e-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4749e-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="4749e-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4749e-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="4749e-129">Schema Name</span></span>  <br/> |<span data-ttu-id="4749e-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="4749e-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="4749e-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="4749e-131">Validation File</span></span>  <br/> |<span data-ttu-id="4749e-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4749e-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4749e-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="4749e-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="4749e-134">False</span><span class="sxs-lookup"><span data-stu-id="4749e-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4749e-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4749e-135">See also</span></span>



[<span data-ttu-id="4749e-136">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="4749e-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="4749e-137">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="4749e-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

