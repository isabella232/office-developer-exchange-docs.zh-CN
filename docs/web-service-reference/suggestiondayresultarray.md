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
description: SuggestionDayResultArray 元素包含按日期组织的会议建议的数组。
ms.openlocfilehash: 277d4cf71c31aba26cbff6f598eaa62769cae552
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457982"
---
# <a name="suggestiondayresultarray"></a><span data-ttu-id="72456-103">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="72456-103">SuggestionDayResultArray</span></span>

<span data-ttu-id="72456-104">**SuggestionDayResultArray**元素包含按日期组织的会议建议的数组。</span><span class="sxs-lookup"><span data-stu-id="72456-104">The **SuggestionDayResultArray** element contains an array of meeting suggestions organized by date.</span></span> 
  
[<span data-ttu-id="72456-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="72456-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="72456-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="72456-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="72456-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="72456-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
```xml
<SuggestionDayResultArray>
   <SuggestionDayResult>...</SuggestionDayResult>
</SuggestionDayResultArray>
```

 <span data-ttu-id="72456-108">**ArrayOfSuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="72456-108">**ArrayOfSuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="72456-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="72456-109">Attributes and elements</span></span>

<span data-ttu-id="72456-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="72456-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72456-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="72456-111">Attributes</span></span>

<span data-ttu-id="72456-112">无。</span><span class="sxs-lookup"><span data-stu-id="72456-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="72456-113">子元素</span><span class="sxs-lookup"><span data-stu-id="72456-113">Child elements</span></span>

|<span data-ttu-id="72456-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="72456-114">**Element**</span></span>|<span data-ttu-id="72456-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="72456-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72456-116">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="72456-116">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="72456-117">表示包含建议会议时间的一天。</span><span class="sxs-lookup"><span data-stu-id="72456-117">Represents a single day that contains suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="72456-118">父元素</span><span class="sxs-lookup"><span data-stu-id="72456-118">Parent elements</span></span>

|<span data-ttu-id="72456-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="72456-119">**Element**</span></span>|<span data-ttu-id="72456-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="72456-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72456-121">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="72456-121">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="72456-122">包含请求的会议建议的响应信息和建议数据</span><span class="sxs-lookup"><span data-stu-id="72456-122">Contains response information and suggestion data for requested meeting suggestions</span></span>  <br/> <span data-ttu-id="72456-123">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="72456-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72456-124">说明</span><span class="sxs-lookup"><span data-stu-id="72456-124">Remarks</span></span>

<span data-ttu-id="72456-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="72456-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="72456-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="72456-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72456-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="72456-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="72456-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="72456-128">Schema Name</span></span>  <br/> |<span data-ttu-id="72456-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="72456-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="72456-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="72456-130">Validation File</span></span>  <br/> |<span data-ttu-id="72456-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="72456-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="72456-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="72456-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="72456-133">False</span><span class="sxs-lookup"><span data-stu-id="72456-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72456-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="72456-134">See also</span></span>



[<span data-ttu-id="72456-135">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="72456-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="72456-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="72456-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="72456-137">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="72456-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

