---
title: IsOutOfDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsOutOfDate
api_type:
- schema
ms.assetid: 2b6005a6-56a9-4848-b998-32908c13e2e2
description: IsOutOfDate 元素指示会议消息、请求、响应或取消是否已过期。
ms.openlocfilehash: b50b021e48789ba63016582450404b5da3ff86e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466547"
---
# <a name="isoutofdate"></a><span data-ttu-id="3c2ef-103">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="3c2ef-103">IsOutOfDate</span></span>

<span data-ttu-id="3c2ef-104">**IsOutOfDate**元素指示会议消息、请求、响应或取消是否已过期。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-104">The **IsOutOfDate** element indicates whether a meeting message, request, response, or cancellation is out-of-date.</span></span> 
  
```xml
<IsOutOfDate/>
```

 <span data-ttu-id="3c2ef-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3c2ef-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c2ef-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3c2ef-106">Attributes and elements</span></span>

<span data-ttu-id="3c2ef-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c2ef-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3c2ef-108">Attributes</span></span>

<span data-ttu-id="3c2ef-109">无。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c2ef-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3c2ef-110">Child elements</span></span>

<span data-ttu-id="3c2ef-111">无。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3c2ef-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3c2ef-112">Parent elements</span></span>

|<span data-ttu-id="3c2ef-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3c2ef-113">**Element**</span></span>|<span data-ttu-id="3c2ef-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3c2ef-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c2ef-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="3c2ef-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="3c2ef-116">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3c2ef-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="3c2ef-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="3c2ef-118">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3c2ef-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3c2ef-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3c2ef-120">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3c2ef-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="3c2ef-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="3c2ef-122">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3c2ef-123">文本值</span><span class="sxs-lookup"><span data-stu-id="3c2ef-123">Text value</span></span>

<span data-ttu-id="3c2ef-124">如果文本值为**true** ，则表示会议项目已过期。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-124">A text value of **true** indicates that the meeting item is out-of-date.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3c2ef-125">说明</span><span class="sxs-lookup"><span data-stu-id="3c2ef-125">Remarks</span></span>

<span data-ttu-id="3c2ef-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3c2ef-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c2ef-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="3c2ef-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c2ef-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="3c2ef-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3c2ef-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="3c2ef-129">Schema Name</span></span>  <br/> |<span data-ttu-id="3c2ef-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="3c2ef-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="3c2ef-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="3c2ef-131">Validation File</span></span>  <br/> |<span data-ttu-id="3c2ef-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3c2ef-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3c2ef-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="3c2ef-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c2ef-134">False</span><span class="sxs-lookup"><span data-stu-id="3c2ef-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c2ef-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3c2ef-135">See also</span></span>



- [<span data-ttu-id="3c2ef-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3c2ef-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

