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
description: MyResponseType 元素包含的状态或日历项目的响应。
ms.openlocfilehash: 3be900ed6d2932699e3e83a0bca2918c016eb689
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826497"
---
# <a name="myresponsetype"></a><span data-ttu-id="48d13-103">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="48d13-103">MyResponseType</span></span>

<span data-ttu-id="48d13-104">**MyResponseType**元素包含的状态或日历项目的响应。</span><span class="sxs-lookup"><span data-stu-id="48d13-104">The **MyResponseType** element contains the status of or response to a calendar item.</span></span> 
  
```xml
<MyResponseType/>
```

 <span data-ttu-id="48d13-105">**ResponseTypeType**</span><span class="sxs-lookup"><span data-stu-id="48d13-105">**ResponseTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48d13-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="48d13-106">Attributes and elements</span></span>

<span data-ttu-id="48d13-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="48d13-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48d13-108">属性</span><span class="sxs-lookup"><span data-stu-id="48d13-108">Attributes</span></span>

<span data-ttu-id="48d13-109">无。</span><span class="sxs-lookup"><span data-stu-id="48d13-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48d13-110">子元素</span><span class="sxs-lookup"><span data-stu-id="48d13-110">Child elements</span></span>

<span data-ttu-id="48d13-111">无。</span><span class="sxs-lookup"><span data-stu-id="48d13-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="48d13-112">父元素</span><span class="sxs-lookup"><span data-stu-id="48d13-112">Parent elements</span></span>

|<span data-ttu-id="48d13-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="48d13-113">**Element**</span></span>|<span data-ttu-id="48d13-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="48d13-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48d13-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="48d13-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="48d13-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="48d13-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="48d13-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="48d13-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="48d13-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="48d13-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="48d13-119">文本值</span><span class="sxs-lookup"><span data-stu-id="48d13-119">Text value</span></span>

<span data-ttu-id="48d13-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="48d13-120">A text value is required.</span></span> <span data-ttu-id="48d13-121">此元素的可能的文本值如下：</span><span class="sxs-lookup"><span data-stu-id="48d13-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="48d13-122">Unknown</span><span class="sxs-lookup"><span data-stu-id="48d13-122">Unknown</span></span>
    
- <span data-ttu-id="48d13-123">组织者</span><span class="sxs-lookup"><span data-stu-id="48d13-123">Organizer</span></span>
    
- <span data-ttu-id="48d13-124">暂定</span><span class="sxs-lookup"><span data-stu-id="48d13-124">Tentative</span></span>
    
- <span data-ttu-id="48d13-125">Accept</span><span class="sxs-lookup"><span data-stu-id="48d13-125">Accept</span></span>
    
- <span data-ttu-id="48d13-126">拒绝</span><span class="sxs-lookup"><span data-stu-id="48d13-126">Decline</span></span>
    
- <span data-ttu-id="48d13-127">NoResponseReceived</span><span class="sxs-lookup"><span data-stu-id="48d13-127">NoResponseReceived</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48d13-128">备注</span><span class="sxs-lookup"><span data-stu-id="48d13-128">Remarks</span></span>

<span data-ttu-id="48d13-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="48d13-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48d13-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="48d13-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48d13-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="48d13-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="48d13-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="48d13-132">Schema name</span></span>  <br/> |<span data-ttu-id="48d13-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="48d13-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="48d13-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="48d13-134">Validation file</span></span>  <br/> |<span data-ttu-id="48d13-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="48d13-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="48d13-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="48d13-136">Can be empty</span></span>  <br/> |<span data-ttu-id="48d13-137">False</span><span class="sxs-lookup"><span data-stu-id="48d13-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48d13-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="48d13-138">See also</span></span>



- [<span data-ttu-id="48d13-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="48d13-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

