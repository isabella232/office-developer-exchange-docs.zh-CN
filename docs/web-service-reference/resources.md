---
title: 资源
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Resources
api_type:
- schema
ms.assetid: a2133cf2-7c62-4f1c-b3aa-75f14d30dd74
description: Resources 元素表示会议的计划的资源。
ms.openlocfilehash: 31f358414e53f55b983f7633fc9c67b0ce3ab645
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827166"
---
# <a name="resources"></a><span data-ttu-id="23761-103">资源</span><span class="sxs-lookup"><span data-stu-id="23761-103">Resources</span></span>

<span data-ttu-id="23761-104">**Resources**元素表示会议的计划的资源。</span><span class="sxs-lookup"><span data-stu-id="23761-104">The **Resources** element represents a scheduled resource for a meeting.</span></span> 
  
```xml
<Resources>
   <Attendee/>
</Resources>
```

 <span data-ttu-id="23761-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="23761-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23761-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="23761-106">Attributes and elements</span></span>

<span data-ttu-id="23761-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="23761-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23761-108">属性</span><span class="sxs-lookup"><span data-stu-id="23761-108">Attributes</span></span>

<span data-ttu-id="23761-109">无。</span><span class="sxs-lookup"><span data-stu-id="23761-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23761-110">子元素</span><span class="sxs-lookup"><span data-stu-id="23761-110">Child elements</span></span>

|<span data-ttu-id="23761-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="23761-111">**Element**</span></span>|<span data-ttu-id="23761-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="23761-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23761-113">参与者</span><span class="sxs-lookup"><span data-stu-id="23761-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="23761-114">代表与会者和会议的资源。</span><span class="sxs-lookup"><span data-stu-id="23761-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23761-115">父元素</span><span class="sxs-lookup"><span data-stu-id="23761-115">Parent elements</span></span>

|<span data-ttu-id="23761-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="23761-116">**Element**</span></span>|<span data-ttu-id="23761-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="23761-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23761-118">日历项目</span><span class="sxs-lookup"><span data-stu-id="23761-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="23761-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="23761-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="23761-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="23761-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="23761-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="23761-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23761-122">备注</span><span class="sxs-lookup"><span data-stu-id="23761-122">Remarks</span></span>

<span data-ttu-id="23761-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="23761-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23761-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="23761-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23761-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="23761-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23761-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="23761-126">Schema name</span></span>  <br/> |<span data-ttu-id="23761-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="23761-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="23761-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="23761-128">Validation file</span></span>  <br/> |<span data-ttu-id="23761-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="23761-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="23761-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="23761-130">Can be empty</span></span>  <br/> |<span data-ttu-id="23761-131">False</span><span class="sxs-lookup"><span data-stu-id="23761-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23761-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="23761-132">See also</span></span>



- [<span data-ttu-id="23761-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="23761-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

