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
description: AppointmentSequenceNumber 元素指定约会的一个版本的序列号。
ms.openlocfilehash: daeea7a656c59923bcb6f2850539c7869d6eb181
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461658"
---
# <a name="appointmentsequencenumber"></a><span data-ttu-id="9511b-103">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="9511b-103">AppointmentSequenceNumber</span></span>

<span data-ttu-id="9511b-104">**AppointmentSequenceNumber**元素指定约会的一个版本的序列号。</span><span class="sxs-lookup"><span data-stu-id="9511b-104">The **AppointmentSequenceNumber** element specifies the sequence number of a version of an appointment.</span></span> 
  
```xml
<AppointmentSequenceNumber/>
```

 <span data-ttu-id="9511b-105">**int**</span><span class="sxs-lookup"><span data-stu-id="9511b-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9511b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9511b-106">Attributes and elements</span></span>

<span data-ttu-id="9511b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9511b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9511b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9511b-108">Attributes</span></span>

<span data-ttu-id="9511b-109">无。</span><span class="sxs-lookup"><span data-stu-id="9511b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9511b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9511b-110">Child elements</span></span>

<span data-ttu-id="9511b-111">无。</span><span class="sxs-lookup"><span data-stu-id="9511b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9511b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9511b-112">Parent elements</span></span>

|<span data-ttu-id="9511b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9511b-113">**Element**</span></span>|<span data-ttu-id="9511b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9511b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9511b-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="9511b-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="9511b-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="9511b-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="9511b-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="9511b-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="9511b-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="9511b-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9511b-119">文本值</span><span class="sxs-lookup"><span data-stu-id="9511b-119">Text value</span></span>

<span data-ttu-id="9511b-120">该文本值表示版本号。</span><span class="sxs-lookup"><span data-stu-id="9511b-120">The text value represents a version number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9511b-121">备注</span><span class="sxs-lookup"><span data-stu-id="9511b-121">Remarks</span></span>

<span data-ttu-id="9511b-122">在使用新信息更新约会时，将更新此值。</span><span class="sxs-lookup"><span data-stu-id="9511b-122">This value is updated when the appointment is updated with new information.</span></span> 
  
<span data-ttu-id="9511b-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9511b-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9511b-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="9511b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9511b-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="9511b-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9511b-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="9511b-126">Schema Name</span></span>  <br/> |<span data-ttu-id="9511b-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="9511b-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="9511b-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="9511b-128">Validation File</span></span>  <br/> |<span data-ttu-id="9511b-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9511b-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9511b-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="9511b-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="9511b-131">False</span><span class="sxs-lookup"><span data-stu-id="9511b-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9511b-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9511b-132">See also</span></span>

- [<span data-ttu-id="9511b-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9511b-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

