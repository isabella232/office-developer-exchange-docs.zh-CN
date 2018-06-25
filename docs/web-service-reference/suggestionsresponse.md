---
title: SuggestionsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsResponse
api_type:
- schema
ms.assetid: d25ca143-f80c-4458-b669-346fda29a5a7
description: SuggestionsResponse 元素包含请求的会议建议的响应状态信息和建议数据。
ms.openlocfilehash: 614b58a1df8e340c6be468ccddd3b37537d32591
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838162"
---
# <a name="suggestionsresponse"></a><span data-ttu-id="4a7d2-103">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="4a7d2-103">SuggestionsResponse</span></span>

<span data-ttu-id="4a7d2-104">**SuggestionsResponse**元素包含请求的会议建议的响应状态信息和建议数据。</span><span class="sxs-lookup"><span data-stu-id="4a7d2-104">The **SuggestionsResponse** element contains response status information and suggestion data for requested meeting suggestions.</span></span> 
  
[<span data-ttu-id="4a7d2-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="4a7d2-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="4a7d2-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="4a7d2-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
```xml
<SuggestionsResponse>
   <ResponseMessage>...</ResponseMessage>
   <SuggestionDayResultArray>...</SuggestionDayResultArray>
</SuggestionsResponse>
```

 <span data-ttu-id="4a7d2-107">**SuggestionsResponseType**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-107">**SuggestionsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4a7d2-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4a7d2-108">Attributes and elements</span></span>

<span data-ttu-id="4a7d2-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4a7d2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a7d2-110">属性</span><span class="sxs-lookup"><span data-stu-id="4a7d2-110">Attributes</span></span>

<span data-ttu-id="4a7d2-111">无。</span><span class="sxs-lookup"><span data-stu-id="4a7d2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4a7d2-112">子元素</span><span class="sxs-lookup"><span data-stu-id="4a7d2-112">Child elements</span></span>

|<span data-ttu-id="4a7d2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-113">**Element**</span></span>|<span data-ttu-id="4a7d2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a7d2-115">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4a7d2-115">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="4a7d2-116">提供有关的响应状态的描述性信息。</span><span class="sxs-lookup"><span data-stu-id="4a7d2-116">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="4a7d2-117">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="4a7d2-117">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="4a7d2-118">包含数组的会议建议组织的日期。</span><span class="sxs-lookup"><span data-stu-id="4a7d2-118">Contains an array of meeting suggestions organized by date.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4a7d2-119">父元素</span><span class="sxs-lookup"><span data-stu-id="4a7d2-119">Parent elements</span></span>

|<span data-ttu-id="4a7d2-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-120">**Element**</span></span>|<span data-ttu-id="4a7d2-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a7d2-122">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="4a7d2-122">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="4a7d2-123">包含请求的用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="4a7d2-123">Contains the requested users' availability information.</span></span>  <br/> <span data-ttu-id="4a7d2-124">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="4a7d2-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a7d2-125">注解</span><span class="sxs-lookup"><span data-stu-id="4a7d2-125">Remarks</span></span>

<span data-ttu-id="4a7d2-126">此元素，则[SuggestionsViewOptions](suggestionsviewoptions.md)未设置 GetUserAvailability 请求消息中不包含在 GetUserAvailability 响应。</span><span class="sxs-lookup"><span data-stu-id="4a7d2-126">This element is not included in a GetUserAvailability response if [SuggestionsViewOptions](suggestionsviewoptions.md) is not set in the GetUserAvailability request message.</span></span> 
  
<span data-ttu-id="4a7d2-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4a7d2-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a7d2-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="4a7d2-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a7d2-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="4a7d2-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4a7d2-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="4a7d2-130">Schema Name</span></span>  <br/> |<span data-ttu-id="4a7d2-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="4a7d2-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4a7d2-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="4a7d2-132">Validation File</span></span>  <br/> |<span data-ttu-id="4a7d2-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4a7d2-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4a7d2-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="4a7d2-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="4a7d2-135">False</span><span class="sxs-lookup"><span data-stu-id="4a7d2-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a7d2-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4a7d2-136">See also</span></span>



[<span data-ttu-id="4a7d2-137">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="4a7d2-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="4a7d2-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="4a7d2-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="4a7d2-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="4a7d2-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

