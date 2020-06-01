---
title: IsOrganizer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a31ac268-5061-4272-a433-ffaea2fbcfa9
description: IsOrganizer 元素指定一个布尔值，该值指示此人是否为会议的组织者。
ms.openlocfilehash: 45b7a66068dc00f6e60b7380240bea6836282fd4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466561"
---
# <a name="isorganizer"></a><span data-ttu-id="b5e85-103">IsOrganizer</span><span class="sxs-lookup"><span data-stu-id="b5e85-103">IsOrganizer</span></span>

<span data-ttu-id="b5e85-104">**IsOrganizer**元素指定一个布尔值，该值指示此人是否为会议的组织者。</span><span class="sxs-lookup"><span data-stu-id="b5e85-104">The **IsOrganizer** element specifies a Boolean value that indicates whether this person is the organizer of the meeting.</span></span> 
  
```XML
<IsOrganizer>true | false</IsOrganizer>
```

 <span data-ttu-id="b5e85-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b5e85-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5e85-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b5e85-106">Attributes and elements</span></span>

<span data-ttu-id="b5e85-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b5e85-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5e85-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b5e85-108">Attributes</span></span>

<span data-ttu-id="b5e85-109">无。</span><span class="sxs-lookup"><span data-stu-id="b5e85-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5e85-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b5e85-110">Child elements</span></span>

<span data-ttu-id="b5e85-111">无。</span><span class="sxs-lookup"><span data-stu-id="b5e85-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b5e85-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b5e85-112">Parent elements</span></span>

|<span data-ttu-id="b5e85-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b5e85-113">**Element**</span></span>|<span data-ttu-id="b5e85-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b5e85-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5e85-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="b5e85-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b5e85-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="b5e85-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b5e85-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="b5e85-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="b5e85-118">表示会议邮件。</span><span class="sxs-lookup"><span data-stu-id="b5e85-118">Represents a meeting message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b5e85-119">文本值</span><span class="sxs-lookup"><span data-stu-id="b5e85-119">Text value</span></span>

<span data-ttu-id="b5e85-120">如果**IsOrganizer**元素的文本值为**true** ，则表示日历项目或会议邮件是由用户创建的。</span><span class="sxs-lookup"><span data-stu-id="b5e85-120">A text value of **true** for the **IsOrganizer** element indicates that the calendar item or meeting message was created by the user.</span></span> <span data-ttu-id="b5e85-121">**如果值为 false** ，则表示未 bv 用户创建日历项目或会议邮件。</span><span class="sxs-lookup"><span data-stu-id="b5e85-121">A value of **false** indicates that the calendar item or meeting message was not created bv the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b5e85-122">备注</span><span class="sxs-lookup"><span data-stu-id="b5e85-122">Remarks</span></span>

<span data-ttu-id="b5e85-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b5e85-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b5e85-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b5e85-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5e85-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="b5e85-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5e85-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="b5e85-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b5e85-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="b5e85-127">Schema Name</span></span>  <br/> |<span data-ttu-id="b5e85-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="b5e85-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="b5e85-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="b5e85-129">Validation File</span></span>  <br/> |<span data-ttu-id="b5e85-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="b5e85-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b5e85-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="b5e85-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b5e85-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b5e85-132">See also</span></span>



- [<span data-ttu-id="b5e85-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b5e85-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

