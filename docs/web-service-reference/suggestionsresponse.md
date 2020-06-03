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
ms.openlocfilehash: cba344f3f97777580c2cc6d296f110f20b550063
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466652"
---
# <a name="suggestionsresponse"></a><span data-ttu-id="c585e-103">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="c585e-103">SuggestionsResponse</span></span>

<span data-ttu-id="c585e-104">**SuggestionsResponse**元素包含请求的会议建议的响应状态信息和建议数据。</span><span class="sxs-lookup"><span data-stu-id="c585e-104">The **SuggestionsResponse** element contains response status information and suggestion data for requested meeting suggestions.</span></span> 
  
[<span data-ttu-id="c585e-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c585e-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="c585e-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="c585e-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
```xml
<SuggestionsResponse>
   <ResponseMessage>...</ResponseMessage>
   <SuggestionDayResultArray>...</SuggestionDayResultArray>
</SuggestionsResponse>
```

 <span data-ttu-id="c585e-107">**SuggestionsResponseType**</span><span class="sxs-lookup"><span data-stu-id="c585e-107">**SuggestionsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c585e-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c585e-108">Attributes and elements</span></span>

<span data-ttu-id="c585e-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c585e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c585e-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="c585e-110">Attributes</span></span>

<span data-ttu-id="c585e-111">无。</span><span class="sxs-lookup"><span data-stu-id="c585e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c585e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="c585e-112">Child elements</span></span>

|<span data-ttu-id="c585e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c585e-113">**Element**</span></span>|<span data-ttu-id="c585e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c585e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c585e-115">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c585e-115">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="c585e-116">提供有关响应状态的描述性信息。</span><span class="sxs-lookup"><span data-stu-id="c585e-116">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="c585e-117">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="c585e-117">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="c585e-118">包含按日期组织的会议建议的数组。</span><span class="sxs-lookup"><span data-stu-id="c585e-118">Contains an array of meeting suggestions organized by date.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c585e-119">父元素</span><span class="sxs-lookup"><span data-stu-id="c585e-119">Parent elements</span></span>

|<span data-ttu-id="c585e-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="c585e-120">**Element**</span></span>|<span data-ttu-id="c585e-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="c585e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c585e-122">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c585e-122">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="c585e-123">包含请求的用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="c585e-123">Contains the requested users' availability information.</span></span>  <br/> <span data-ttu-id="c585e-124">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="c585e-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c585e-125">备注</span><span class="sxs-lookup"><span data-stu-id="c585e-125">Remarks</span></span>

<span data-ttu-id="c585e-126">如果 GetUserAvailability 请求消息中未设置[SuggestionsViewOptions](suggestionsviewoptions.md) ，则此元素不包含在 GetUserAvailability 响应中。</span><span class="sxs-lookup"><span data-stu-id="c585e-126">This element is not included in a GetUserAvailability response if [SuggestionsViewOptions](suggestionsviewoptions.md) is not set in the GetUserAvailability request message.</span></span> 
  
<span data-ttu-id="c585e-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c585e-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c585e-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="c585e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c585e-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="c585e-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c585e-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="c585e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="c585e-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="c585e-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c585e-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="c585e-132">Validation File</span></span>  <br/> |<span data-ttu-id="c585e-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c585e-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c585e-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="c585e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="c585e-135">False</span><span class="sxs-lookup"><span data-stu-id="c585e-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c585e-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c585e-136">See also</span></span>



[<span data-ttu-id="c585e-137">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="c585e-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="c585e-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c585e-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="c585e-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="c585e-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

