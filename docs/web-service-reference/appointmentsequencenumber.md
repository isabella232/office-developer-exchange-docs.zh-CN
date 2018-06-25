---
title: AppointmentSequenceNumber
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppointmentSequenceNumber
api_type:
- schema
ms.assetid: eb4c48bd-f905-48dc-ae16-53a080b9b025
description: AppointmentSequenceNumber 元素指定约会的版本的序列号。
ms.openlocfilehash: bc186170ccca06669ea7d20cea06c542f9ce274a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753246"
---
# <a name="appointmentsequencenumber"></a><span data-ttu-id="0a919-103">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0a919-103">AppointmentSequenceNumber</span></span>

<span data-ttu-id="0a919-104">**AppointmentSequenceNumber**元素指定约会的版本的序列号。</span><span class="sxs-lookup"><span data-stu-id="0a919-104">The **AppointmentSequenceNumber** element specifies the sequence number of a version of an appointment.</span></span> 
  
```xml
<AppointmentSequenceNumber/>
```

 <span data-ttu-id="0a919-105">**int**</span><span class="sxs-lookup"><span data-stu-id="0a919-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a919-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0a919-106">Attributes and elements</span></span>

<span data-ttu-id="0a919-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0a919-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a919-108">属性</span><span class="sxs-lookup"><span data-stu-id="0a919-108">Attributes</span></span>

<span data-ttu-id="0a919-109">无。</span><span class="sxs-lookup"><span data-stu-id="0a919-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a919-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0a919-110">Child elements</span></span>

<span data-ttu-id="0a919-111">无。</span><span class="sxs-lookup"><span data-stu-id="0a919-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0a919-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0a919-112">Parent elements</span></span>

|<span data-ttu-id="0a919-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0a919-113">**Element**</span></span>|<span data-ttu-id="0a919-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a919-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a919-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="0a919-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="0a919-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="0a919-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="0a919-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0a919-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="0a919-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="0a919-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0a919-119">文本值</span><span class="sxs-lookup"><span data-stu-id="0a919-119">Text value</span></span>

<span data-ttu-id="0a919-120">文本值表示的版本号。</span><span class="sxs-lookup"><span data-stu-id="0a919-120">The text value represents a version number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a919-121">注解</span><span class="sxs-lookup"><span data-stu-id="0a919-121">Remarks</span></span>

<span data-ttu-id="0a919-122">该约会新信息进行更新时，将更新此值。</span><span class="sxs-lookup"><span data-stu-id="0a919-122">This value is updated when the appointment is updated with new information.</span></span> 
  
<span data-ttu-id="0a919-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0a919-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a919-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="0a919-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a919-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="0a919-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0a919-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="0a919-126">Schema Name</span></span>  <br/> |<span data-ttu-id="0a919-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="0a919-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="0a919-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="0a919-128">Validation File</span></span>  <br/> |<span data-ttu-id="0a919-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0a919-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0a919-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="0a919-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="0a919-131">False</span><span class="sxs-lookup"><span data-stu-id="0a919-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a919-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a919-132">See also</span></span>

- [<span data-ttu-id="0a919-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0a919-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

