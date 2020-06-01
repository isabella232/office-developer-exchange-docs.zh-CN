---
title: MeetingRequestWasSent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestWasSent
api_type:
- schema
ms.assetid: 9192400a-8eef-4147-9f94-aa8ea91b41d8
description: MeetingRequestWasSent 元素指示是否已将会议请求发送到请求的与会者。
ms.openlocfilehash: d5005eb86d5f8d2f438a69e634f0617c2311d720
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465763"
---
# <a name="meetingrequestwassent"></a><span data-ttu-id="a228d-103">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="a228d-103">MeetingRequestWasSent</span></span>

<span data-ttu-id="a228d-104">**MeetingRequestWasSent**元素指示是否已将会议请求发送到请求的与会者。</span><span class="sxs-lookup"><span data-stu-id="a228d-104">The **MeetingRequestWasSent** element indicates whether a meeting request has been sent to requested attendees.</span></span> 
  
```xml
<MeetingRequestWasSent/>
```

 <span data-ttu-id="a228d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a228d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a228d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a228d-106">Attributes and elements</span></span>

<span data-ttu-id="a228d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a228d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a228d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a228d-108">Attributes</span></span>

<span data-ttu-id="a228d-109">无。</span><span class="sxs-lookup"><span data-stu-id="a228d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a228d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a228d-110">Child elements</span></span>

<span data-ttu-id="a228d-111">无。</span><span class="sxs-lookup"><span data-stu-id="a228d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a228d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a228d-112">Parent elements</span></span>

|<span data-ttu-id="a228d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a228d-113">**Element**</span></span>|<span data-ttu-id="a228d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a228d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a228d-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a228d-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a228d-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="a228d-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a228d-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a228d-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a228d-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="a228d-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a228d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="a228d-119">Text value</span></span>

<span data-ttu-id="a228d-120">如果包含此元素，则需要一个表示布尔值的文本值。</span><span class="sxs-lookup"><span data-stu-id="a228d-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="a228d-121">**如果值为 true，则**表示会议请求已发送。</span><span class="sxs-lookup"><span data-stu-id="a228d-121">A value of **true** indicates that a meeting request was sent.</span></span> <span data-ttu-id="a228d-122">**如果值为 false** ，则表示尚未发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="a228d-122">A value of **false** indicates that a meeting request has not been sent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a228d-123">说明</span><span class="sxs-lookup"><span data-stu-id="a228d-123">Remarks</span></span>

<span data-ttu-id="a228d-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a228d-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a228d-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="a228d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a228d-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="a228d-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a228d-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="a228d-127">Schema name</span></span>  <br/> |<span data-ttu-id="a228d-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="a228d-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="a228d-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="a228d-129">Validation file</span></span>  <br/> |<span data-ttu-id="a228d-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a228d-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a228d-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="a228d-131">Can be empty</span></span>  <br/> |<span data-ttu-id="a228d-132">False</span><span class="sxs-lookup"><span data-stu-id="a228d-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a228d-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a228d-133">See also</span></span>



- [<span data-ttu-id="a228d-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a228d-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

