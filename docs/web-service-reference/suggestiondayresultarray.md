---
title: SuggestionDayResultArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionDayResultArray
api_type:
- schema
ms.assetid: eeba9eff-5eca-4002-b5a5-8fb794feaba1
description: SuggestionDayResultArray 元素包含一个会议建议按日期组织数组。
ms.openlocfilehash: c208104356606a5d9961461ad8743a772d2410d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838161"
---
# <a name="suggestiondayresultarray"></a><span data-ttu-id="020c1-103">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="020c1-103">SuggestionDayResultArray</span></span>

<span data-ttu-id="020c1-104">**SuggestionDayResultArray**元素包含一个会议建议按日期组织数组。</span><span class="sxs-lookup"><span data-stu-id="020c1-104">The **SuggestionDayResultArray** element contains an array of meeting suggestions organized by date.</span></span> 
  
[<span data-ttu-id="020c1-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="020c1-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="020c1-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="020c1-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="020c1-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="020c1-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
```xml
<SuggestionDayResultArray>
   <SuggestionDayResult>...</SuggestionDayResult>
</SuggestionDayResultArray>
```

 <span data-ttu-id="020c1-108">**ArrayOfSuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="020c1-108">**ArrayOfSuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="020c1-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="020c1-109">Attributes and elements</span></span>

<span data-ttu-id="020c1-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="020c1-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="020c1-111">属性</span><span class="sxs-lookup"><span data-stu-id="020c1-111">Attributes</span></span>

<span data-ttu-id="020c1-112">无。</span><span class="sxs-lookup"><span data-stu-id="020c1-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="020c1-113">子元素</span><span class="sxs-lookup"><span data-stu-id="020c1-113">Child elements</span></span>

|<span data-ttu-id="020c1-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="020c1-114">**Element**</span></span>|<span data-ttu-id="020c1-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="020c1-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="020c1-116">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="020c1-116">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="020c1-117">表示一天包含建议的会议的时间。</span><span class="sxs-lookup"><span data-stu-id="020c1-117">Represents a single day that contains suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="020c1-118">父元素</span><span class="sxs-lookup"><span data-stu-id="020c1-118">Parent elements</span></span>

|<span data-ttu-id="020c1-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="020c1-119">**Element**</span></span>|<span data-ttu-id="020c1-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="020c1-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="020c1-121">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="020c1-121">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="020c1-122">包含用于请求会议建议响应信息和建议的数据</span><span class="sxs-lookup"><span data-stu-id="020c1-122">Contains response information and suggestion data for requested meeting suggestions</span></span>  <br/> <span data-ttu-id="020c1-123">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="020c1-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="020c1-124">备注</span><span class="sxs-lookup"><span data-stu-id="020c1-124">Remarks</span></span>

<span data-ttu-id="020c1-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="020c1-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="020c1-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="020c1-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="020c1-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="020c1-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="020c1-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="020c1-128">Schema Name</span></span>  <br/> |<span data-ttu-id="020c1-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="020c1-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="020c1-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="020c1-130">Validation File</span></span>  <br/> |<span data-ttu-id="020c1-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="020c1-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="020c1-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="020c1-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="020c1-133">False</span><span class="sxs-lookup"><span data-stu-id="020c1-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="020c1-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="020c1-134">See also</span></span>



[<span data-ttu-id="020c1-135">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="020c1-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="020c1-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="020c1-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="020c1-137">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="020c1-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

