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
description: MeetingRequestWasSent 元素指示是否已向请求与会者发送会议请求。
ms.openlocfilehash: 0a87b1d773997e08ab96726375e4c8ce010faaf7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826438"
---
# <a name="meetingrequestwassent"></a><span data-ttu-id="53eb2-103">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="53eb2-103">MeetingRequestWasSent</span></span>

<span data-ttu-id="53eb2-104">**MeetingRequestWasSent**元素指示是否已向请求与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="53eb2-104">The **MeetingRequestWasSent** element indicates whether a meeting request has been sent to requested attendees.</span></span> 
  
```xml
<MeetingRequestWasSent/>
```

 <span data-ttu-id="53eb2-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="53eb2-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53eb2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="53eb2-106">Attributes and elements</span></span>

<span data-ttu-id="53eb2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="53eb2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53eb2-108">属性</span><span class="sxs-lookup"><span data-stu-id="53eb2-108">Attributes</span></span>

<span data-ttu-id="53eb2-109">无。</span><span class="sxs-lookup"><span data-stu-id="53eb2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53eb2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="53eb2-110">Child elements</span></span>

<span data-ttu-id="53eb2-111">无。</span><span class="sxs-lookup"><span data-stu-id="53eb2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="53eb2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="53eb2-112">Parent elements</span></span>

|<span data-ttu-id="53eb2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="53eb2-113">**Element**</span></span>|<span data-ttu-id="53eb2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="53eb2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53eb2-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="53eb2-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="53eb2-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="53eb2-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="53eb2-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="53eb2-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="53eb2-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="53eb2-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="53eb2-119">文本值</span><span class="sxs-lookup"><span data-stu-id="53eb2-119">Text value</span></span>

<span data-ttu-id="53eb2-120">如果此元素是包含，则需要一个文本值，它代表一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="53eb2-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="53eb2-121">值为**true**表示发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="53eb2-121">A value of **true** indicates that a meeting request was sent.</span></span> <span data-ttu-id="53eb2-122">如果值为**false**指示尚未发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="53eb2-122">A value of **false** indicates that a meeting request has not been sent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="53eb2-123">备注</span><span class="sxs-lookup"><span data-stu-id="53eb2-123">Remarks</span></span>

<span data-ttu-id="53eb2-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="53eb2-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53eb2-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="53eb2-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53eb2-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="53eb2-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="53eb2-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="53eb2-127">Schema name</span></span>  <br/> |<span data-ttu-id="53eb2-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="53eb2-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="53eb2-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="53eb2-129">Validation file</span></span>  <br/> |<span data-ttu-id="53eb2-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="53eb2-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="53eb2-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="53eb2-131">Can be empty</span></span>  <br/> |<span data-ttu-id="53eb2-132">False</span><span class="sxs-lookup"><span data-stu-id="53eb2-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53eb2-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="53eb2-133">See also</span></span>



- [<span data-ttu-id="53eb2-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="53eb2-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

