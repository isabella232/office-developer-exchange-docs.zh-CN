---
title: FreeBusyResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyResponse
api_type:
- schema
ms.assetid: 3038d106-9ac9-4ac7-bb43-96c783edbef5
description: FreeBusyResponse 元素包含单个邮箱用户的忙/闲信息。
ms.openlocfilehash: 73e3972bb53d6bf59e5156098bad06bcde5f0155
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754423"
---
# <a name="freebusyresponse"></a><span data-ttu-id="7ba00-103">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="7ba00-103">FreeBusyResponse</span></span>

<span data-ttu-id="7ba00-104">**FreeBusyResponse**元素包含单个邮箱用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="7ba00-104">The **FreeBusyResponse** element contains the free/busy information for a single mailbox user.</span></span> 
  
[<span data-ttu-id="7ba00-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7ba00-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="7ba00-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="7ba00-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="7ba00-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="7ba00-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
```xml
<FreeBusyResponse>
   <ResponseMessage>...</ResponseMessage>
   <FreeBusyView>...</FreeBusyView>
</FreeBusyResponse>
```

 <span data-ttu-id="7ba00-108">**FreeBusyResponseType**</span><span class="sxs-lookup"><span data-stu-id="7ba00-108">**FreeBusyResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ba00-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7ba00-109">Attributes and elements</span></span>

<span data-ttu-id="7ba00-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7ba00-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ba00-111">属性</span><span class="sxs-lookup"><span data-stu-id="7ba00-111">Attributes</span></span>

<span data-ttu-id="7ba00-112">无。</span><span class="sxs-lookup"><span data-stu-id="7ba00-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ba00-113">子元素</span><span class="sxs-lookup"><span data-stu-id="7ba00-113">Child elements</span></span>

|<span data-ttu-id="7ba00-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ba00-114">**Element**</span></span>|<span data-ttu-id="7ba00-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ba00-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ba00-116">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7ba00-116">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="7ba00-117">提供有关的响应状态的描述性信息。</span><span class="sxs-lookup"><span data-stu-id="7ba00-117">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="7ba00-118">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="7ba00-118">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="7ba00-119">包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="7ba00-119">Contains availability information for a specific user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7ba00-120">父元素</span><span class="sxs-lookup"><span data-stu-id="7ba00-120">Parent elements</span></span>

|<span data-ttu-id="7ba00-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ba00-121">**Element**</span></span>|<span data-ttu-id="7ba00-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ba00-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ba00-123">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="7ba00-123">FreeBusyResponseArray</span></span>](freebusyresponsearray.md) <br/> |<span data-ttu-id="7ba00-124">包含请求的用户的可用性信息和响应状态。</span><span class="sxs-lookup"><span data-stu-id="7ba00-124">Contains the requested users' availability information and the response status.</span></span>  <br/> <span data-ttu-id="7ba00-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="7ba00-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ba00-126">注解</span><span class="sxs-lookup"><span data-stu-id="7ba00-126">Remarks</span></span>

<span data-ttu-id="7ba00-127">此元素，则不请求忙/闲信息不包含在 GetUserAvailability 响应。</span><span class="sxs-lookup"><span data-stu-id="7ba00-127">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="7ba00-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7ba00-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ba00-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="7ba00-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ba00-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="7ba00-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7ba00-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="7ba00-131">Schema Name</span></span>  <br/> |<span data-ttu-id="7ba00-132">消息架构</span><span class="sxs-lookup"><span data-stu-id="7ba00-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7ba00-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="7ba00-133">Validation File</span></span>  <br/> |<span data-ttu-id="7ba00-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7ba00-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7ba00-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="7ba00-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="7ba00-136">False</span><span class="sxs-lookup"><span data-stu-id="7ba00-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ba00-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ba00-137">See also</span></span>



[<span data-ttu-id="7ba00-138">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="7ba00-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="7ba00-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7ba00-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="7ba00-140">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="7ba00-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

