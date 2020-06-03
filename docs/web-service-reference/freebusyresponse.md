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
ms.openlocfilehash: 45a3e12756f3cbf29b76b442f7103abc5fb9a833
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461924"
---
# <a name="freebusyresponse"></a><span data-ttu-id="92aa7-103">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="92aa7-103">FreeBusyResponse</span></span>

<span data-ttu-id="92aa7-104">**FreeBusyResponse**元素包含单个邮箱用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="92aa7-104">The **FreeBusyResponse** element contains the free/busy information for a single mailbox user.</span></span> 
  
[<span data-ttu-id="92aa7-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="92aa7-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="92aa7-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="92aa7-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="92aa7-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="92aa7-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
```xml
<FreeBusyResponse>
   <ResponseMessage>...</ResponseMessage>
   <FreeBusyView>...</FreeBusyView>
</FreeBusyResponse>
```

 <span data-ttu-id="92aa7-108">**FreeBusyResponseType**</span><span class="sxs-lookup"><span data-stu-id="92aa7-108">**FreeBusyResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="92aa7-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="92aa7-109">Attributes and elements</span></span>

<span data-ttu-id="92aa7-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="92aa7-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92aa7-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="92aa7-111">Attributes</span></span>

<span data-ttu-id="92aa7-112">无。</span><span class="sxs-lookup"><span data-stu-id="92aa7-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92aa7-113">子元素</span><span class="sxs-lookup"><span data-stu-id="92aa7-113">Child elements</span></span>

|<span data-ttu-id="92aa7-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="92aa7-114">**Element**</span></span>|<span data-ttu-id="92aa7-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="92aa7-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92aa7-116">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="92aa7-116">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="92aa7-117">提供有关响应状态的描述性信息。</span><span class="sxs-lookup"><span data-stu-id="92aa7-117">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="92aa7-118">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="92aa7-118">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="92aa7-119">包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="92aa7-119">Contains availability information for a specific user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="92aa7-120">父元素</span><span class="sxs-lookup"><span data-stu-id="92aa7-120">Parent elements</span></span>

|<span data-ttu-id="92aa7-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="92aa7-121">**Element**</span></span>|<span data-ttu-id="92aa7-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="92aa7-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92aa7-123">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="92aa7-123">FreeBusyResponseArray</span></span>](freebusyresponsearray.md) <br/> |<span data-ttu-id="92aa7-124">包含请求的用户的可用性信息和响应状态。</span><span class="sxs-lookup"><span data-stu-id="92aa7-124">Contains the requested users' availability information and the response status.</span></span>  <br/> <span data-ttu-id="92aa7-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="92aa7-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92aa7-126">备注</span><span class="sxs-lookup"><span data-stu-id="92aa7-126">Remarks</span></span>

<span data-ttu-id="92aa7-127">如果不请求忙/闲信息，则 GetUserAvailability 响应中不包含此元素。</span><span class="sxs-lookup"><span data-stu-id="92aa7-127">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="92aa7-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="92aa7-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92aa7-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="92aa7-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92aa7-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="92aa7-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="92aa7-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="92aa7-131">Schema Name</span></span>  <br/> |<span data-ttu-id="92aa7-132">消息架构</span><span class="sxs-lookup"><span data-stu-id="92aa7-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="92aa7-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="92aa7-133">Validation File</span></span>  <br/> |<span data-ttu-id="92aa7-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="92aa7-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="92aa7-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="92aa7-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="92aa7-136">False</span><span class="sxs-lookup"><span data-stu-id="92aa7-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92aa7-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="92aa7-137">See also</span></span>



[<span data-ttu-id="92aa7-138">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="92aa7-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="92aa7-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="92aa7-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="92aa7-140">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="92aa7-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

