---
title: MaximumResultsByDay
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaximumResultsByDay
api_type:
- schema
ms.assetid: d581a12a-2b8e-4960-ae14-c8c4aa0b1849
description: MaximumResultsByDay 元素指定响应中返回的每一天的建议会议时间数。
ms.openlocfilehash: 46d5c35a83034b8b968901fbc4ee57d046b6c164
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468416"
---
# <a name="maximumresultsbyday"></a><span data-ttu-id="3b30d-103">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="3b30d-103">MaximumResultsByDay</span></span>

<span data-ttu-id="3b30d-104">**MaximumResultsByDay**元素指定响应中返回的每一天的建议会议时间数。</span><span class="sxs-lookup"><span data-stu-id="3b30d-104">The **MaximumResultsByDay** element specifies the number of suggested meeting times per a day returned in the response.</span></span> 
  
[<span data-ttu-id="3b30d-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="3b30d-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="3b30d-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="3b30d-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="3b30d-107">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="3b30d-107">MaximumResultsByDay</span></span>](maximumresultsbyday.md)
  
```xml
<MaximumResultsByDay>...</MaximumResultsByDay>
```

<span data-ttu-id="3b30d-108">**int**</span><span class="sxs-lookup"><span data-stu-id="3b30d-108">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3b30d-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3b30d-109">Attributes and elements</span></span>

<span data-ttu-id="3b30d-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3b30d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b30d-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="3b30d-111">Attributes</span></span>

<span data-ttu-id="3b30d-112">无。</span><span class="sxs-lookup"><span data-stu-id="3b30d-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b30d-113">子元素</span><span class="sxs-lookup"><span data-stu-id="3b30d-113">Child elements</span></span>

<span data-ttu-id="3b30d-114">无。</span><span class="sxs-lookup"><span data-stu-id="3b30d-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b30d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="3b30d-115">Parent elements</span></span>

|<span data-ttu-id="3b30d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="3b30d-116">**Element**</span></span>|<span data-ttu-id="3b30d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="3b30d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b30d-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="3b30d-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="3b30d-119">包含用于获取会议建议信息的选项。</span><span class="sxs-lookup"><span data-stu-id="3b30d-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="3b30d-120">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="3b30d-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3b30d-121">文本值</span><span class="sxs-lookup"><span data-stu-id="3b30d-121">Text value</span></span>

<span data-ttu-id="3b30d-p101">文本值是必需的。文本值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="3b30d-p101">A text value is required. The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b30d-124">说明</span><span class="sxs-lookup"><span data-stu-id="3b30d-124">Remarks</span></span>

<span data-ttu-id="3b30d-125">如果使用[SuggestionsViewOptions](suggestionsviewoptions.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="3b30d-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3b30d-126">描述此元素的架构位于运行 Microsoft® Exchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3b30d-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3b30d-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="3b30d-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b30d-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="3b30d-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b30d-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="3b30d-129">Schema Name</span></span>  <br/> |<span data-ttu-id="3b30d-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="3b30d-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b30d-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="3b30d-131">Validation File</span></span>  <br/> |<span data-ttu-id="3b30d-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b30d-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b30d-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="3b30d-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b30d-134">False</span><span class="sxs-lookup"><span data-stu-id="3b30d-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b30d-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3b30d-135">See also</span></span>

- [<span data-ttu-id="3b30d-136">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="3b30d-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="3b30d-137">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="3b30d-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

