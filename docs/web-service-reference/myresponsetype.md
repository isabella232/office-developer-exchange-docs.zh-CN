---
title: MyResponseType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MyResponseType
api_type:
- schema
ms.assetid: 9741b71d-a310-4520-81d5-3787a1ee630f
description: MyResponseType 元素包含日历项目的状态或响应。
ms.openlocfilehash: 640b0595ac039cc3c119aa52aa6e791e5b695e87
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466624"
---
# <a name="myresponsetype"></a><span data-ttu-id="67224-103">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="67224-103">MyResponseType</span></span>

<span data-ttu-id="67224-104">**MyResponseType**元素包含日历项目的状态或响应。</span><span class="sxs-lookup"><span data-stu-id="67224-104">The **MyResponseType** element contains the status of or response to a calendar item.</span></span> 
  
```xml
<MyResponseType/>
```

 <span data-ttu-id="67224-105">**ResponseTypeType**</span><span class="sxs-lookup"><span data-stu-id="67224-105">**ResponseTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67224-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="67224-106">Attributes and elements</span></span>

<span data-ttu-id="67224-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="67224-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67224-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="67224-108">Attributes</span></span>

<span data-ttu-id="67224-109">无。</span><span class="sxs-lookup"><span data-stu-id="67224-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67224-110">子元素</span><span class="sxs-lookup"><span data-stu-id="67224-110">Child elements</span></span>

<span data-ttu-id="67224-111">无。</span><span class="sxs-lookup"><span data-stu-id="67224-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="67224-112">父元素</span><span class="sxs-lookup"><span data-stu-id="67224-112">Parent elements</span></span>

|<span data-ttu-id="67224-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="67224-113">**Element**</span></span>|<span data-ttu-id="67224-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="67224-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67224-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="67224-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="67224-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="67224-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="67224-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="67224-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="67224-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="67224-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="67224-119">文本值</span><span class="sxs-lookup"><span data-stu-id="67224-119">Text value</span></span>

<span data-ttu-id="67224-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="67224-120">A text value is required.</span></span> <span data-ttu-id="67224-121">以下是此元素的可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="67224-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="67224-122">未知</span><span class="sxs-lookup"><span data-stu-id="67224-122">Unknown</span></span>
    
- <span data-ttu-id="67224-123">Organizer</span><span class="sxs-lookup"><span data-stu-id="67224-123">Organizer</span></span>
    
- <span data-ttu-id="67224-124">暂</span><span class="sxs-lookup"><span data-stu-id="67224-124">Tentative</span></span>
    
- <span data-ttu-id="67224-125">接受</span><span class="sxs-lookup"><span data-stu-id="67224-125">Accept</span></span>
    
- <span data-ttu-id="67224-126">拒绝</span><span class="sxs-lookup"><span data-stu-id="67224-126">Decline</span></span>
    
- <span data-ttu-id="67224-127">NoResponseReceived</span><span class="sxs-lookup"><span data-stu-id="67224-127">NoResponseReceived</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67224-128">说明</span><span class="sxs-lookup"><span data-stu-id="67224-128">Remarks</span></span>

<span data-ttu-id="67224-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="67224-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67224-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="67224-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67224-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="67224-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="67224-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="67224-132">Schema name</span></span>  <br/> |<span data-ttu-id="67224-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="67224-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="67224-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="67224-134">Validation file</span></span>  <br/> |<span data-ttu-id="67224-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="67224-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="67224-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="67224-136">Can be empty</span></span>  <br/> |<span data-ttu-id="67224-137">False</span><span class="sxs-lookup"><span data-stu-id="67224-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67224-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67224-138">See also</span></span>



- [<span data-ttu-id="67224-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="67224-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

