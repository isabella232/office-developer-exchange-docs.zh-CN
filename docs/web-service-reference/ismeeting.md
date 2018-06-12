---
title: IsMeeting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsMeeting
api_type:
- schema
ms.assetid: 6ce22f17-7a31-46c4-b643-0894d087e852
description: IsMeeting 元素指示日历项目是否会议或约会。
ms.openlocfilehash: bb1349a8690450882e6beac0ccd84a8d03272a7d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826051"
---
# <a name="ismeeting"></a><span data-ttu-id="fd67f-103">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="fd67f-103">IsMeeting</span></span>

<span data-ttu-id="fd67f-104">**IsMeeting**元素指示日历项目是否会议或约会。</span><span class="sxs-lookup"><span data-stu-id="fd67f-104">The **IsMeeting** element indicates whether the calendar item is a meeting or an appointment.</span></span> 
  
```xml
<IsMeeting/>
```

 <span data-ttu-id="fd67f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd67f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd67f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fd67f-106">Attributes and elements</span></span>

<span data-ttu-id="fd67f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fd67f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd67f-108">属性</span><span class="sxs-lookup"><span data-stu-id="fd67f-108">Attributes</span></span>

<span data-ttu-id="fd67f-109">无。</span><span class="sxs-lookup"><span data-stu-id="fd67f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd67f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fd67f-110">Child elements</span></span>

<span data-ttu-id="fd67f-111">无。</span><span class="sxs-lookup"><span data-stu-id="fd67f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fd67f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fd67f-112">Parent elements</span></span>

|<span data-ttu-id="fd67f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fd67f-113">**Element**</span></span>|<span data-ttu-id="fd67f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fd67f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd67f-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="fd67f-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fd67f-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="fd67f-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fd67f-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="fd67f-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="fd67f-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="fd67f-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fd67f-119">文本值</span><span class="sxs-lookup"><span data-stu-id="fd67f-119">Text value</span></span>

<span data-ttu-id="fd67f-120">如果此元素是包含，则需要一个文本值，它代表一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="fd67f-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="fd67f-121">值为**true**指示日历项目是一个会议。</span><span class="sxs-lookup"><span data-stu-id="fd67f-121">A value of **true** indicates that the calendar item is a meeting.</span></span> <span data-ttu-id="fd67f-122">如果值为**false**指示日历项目为约会。</span><span class="sxs-lookup"><span data-stu-id="fd67f-122">A value of **false** indicates that the calendar item is an appointment.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fd67f-123">备注</span><span class="sxs-lookup"><span data-stu-id="fd67f-123">Remarks</span></span>

<span data-ttu-id="fd67f-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fd67f-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd67f-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="fd67f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd67f-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="fd67f-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fd67f-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="fd67f-127">Schema name</span></span>  <br/> |<span data-ttu-id="fd67f-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="fd67f-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="fd67f-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="fd67f-129">Validation file</span></span>  <br/> |<span data-ttu-id="fd67f-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fd67f-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fd67f-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="fd67f-131">Can be empty</span></span>  <br/> |<span data-ttu-id="fd67f-132">False</span><span class="sxs-lookup"><span data-stu-id="fd67f-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd67f-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fd67f-133">See also</span></span>



- [<span data-ttu-id="fd67f-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fd67f-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

