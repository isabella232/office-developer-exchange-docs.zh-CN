---
title: FreeBusyResponseArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyResponseArray
api_type:
- schema
ms.assetid: 5592a37e-cf4b-4643-8a2a-fa58c40345b9
description: FreeBusyResponseArray 元素包含请求的用户的可用性信息和响应状态。
ms.openlocfilehash: b45938c19b76a377fca125fb6a19f9d712718db6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457807"
---
# <a name="freebusyresponsearray"></a><span data-ttu-id="56349-103">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="56349-103">FreeBusyResponseArray</span></span>

<span data-ttu-id="56349-104">**FreeBusyResponseArray**元素包含请求的用户的可用性信息和响应状态。</span><span class="sxs-lookup"><span data-stu-id="56349-104">The **FreeBusyResponseArray** element contains the requested users' availability information and the response status.</span></span> 
  
[<span data-ttu-id="56349-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="56349-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="56349-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="56349-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
```xml
<FreeBusyResponseArray>
   <FreeBusyResponse>...</FreeBusyResponse>
</FreeBusyResponseArray>
```

 <span data-ttu-id="56349-107">**ArrayOfFreeBusyResponse**</span><span class="sxs-lookup"><span data-stu-id="56349-107">**ArrayOfFreeBusyResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="56349-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="56349-108">Attributes and elements</span></span>

<span data-ttu-id="56349-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="56349-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56349-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="56349-110">Attributes</span></span>

<span data-ttu-id="56349-111">无。</span><span class="sxs-lookup"><span data-stu-id="56349-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="56349-112">子元素</span><span class="sxs-lookup"><span data-stu-id="56349-112">Child elements</span></span>

|<span data-ttu-id="56349-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="56349-113">**Element**</span></span>|<span data-ttu-id="56349-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="56349-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56349-115">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="56349-115">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="56349-116">包含单个邮箱用户的忙/闲信息和响应状态。</span><span class="sxs-lookup"><span data-stu-id="56349-116">Contains the free/busy information for a single mailbox user and the response status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="56349-117">父元素</span><span class="sxs-lookup"><span data-stu-id="56349-117">Parent elements</span></span>

|<span data-ttu-id="56349-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="56349-118">**Element**</span></span>|<span data-ttu-id="56349-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="56349-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56349-120">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="56349-120">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="56349-121">包含用于定义用户可用性信息或建议的会议时间信息的属性。</span><span class="sxs-lookup"><span data-stu-id="56349-121">Contains the properties that define user availability information or suggested meeting time information.</span></span>  <br/> <span data-ttu-id="56349-122">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="56349-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56349-123">备注</span><span class="sxs-lookup"><span data-stu-id="56349-123">Remarks</span></span>

<span data-ttu-id="56349-124">如果不请求忙/闲信息，则 GetUserAvailability 响应中不包含此元素。</span><span class="sxs-lookup"><span data-stu-id="56349-124">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="56349-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="56349-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="56349-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="56349-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56349-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="56349-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="56349-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="56349-128">Schema Name</span></span>  <br/> |<span data-ttu-id="56349-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="56349-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="56349-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="56349-130">Validation File</span></span>  <br/> |<span data-ttu-id="56349-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="56349-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="56349-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="56349-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="56349-133">False</span><span class="sxs-lookup"><span data-stu-id="56349-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56349-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="56349-134">See also</span></span>



[<span data-ttu-id="56349-135">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="56349-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="56349-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="56349-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="56349-137">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="56349-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

