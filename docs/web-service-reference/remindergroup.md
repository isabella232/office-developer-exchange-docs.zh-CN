---
title: ReminderGroup
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: ReminderGroup 元素指定的日历项目或任务是否是提醒。
ms.openlocfilehash: d9d31cdab482d04149428021ad44cc742108053a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827060"
---
# <a name="remindergroup"></a><span data-ttu-id="c2b21-103">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="c2b21-103">ReminderGroup</span></span>

<span data-ttu-id="c2b21-104">**ReminderGroup**元素指定的日历项目或任务是否是提醒。</span><span class="sxs-lookup"><span data-stu-id="c2b21-104">The **ReminderGroup** element specifies whether the reminder is for a calendar item or a task.</span></span> 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 <span data-ttu-id="c2b21-105">**ReminderGroupType**</span><span class="sxs-lookup"><span data-stu-id="c2b21-105">**ReminderGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2b21-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c2b21-106">Attributes and elements</span></span>

<span data-ttu-id="c2b21-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c2b21-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2b21-108">属性</span><span class="sxs-lookup"><span data-stu-id="c2b21-108">Attributes</span></span>

<span data-ttu-id="c2b21-109">无。</span><span class="sxs-lookup"><span data-stu-id="c2b21-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2b21-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c2b21-110">Child elements</span></span>

<span data-ttu-id="c2b21-111">无。</span><span class="sxs-lookup"><span data-stu-id="c2b21-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c2b21-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c2b21-112">Parent elements</span></span>

[<span data-ttu-id="c2b21-113">提醒</span><span class="sxs-lookup"><span data-stu-id="c2b21-113">Reminder</span></span>](reminder.md)
  
## <a name="text-value"></a><span data-ttu-id="c2b21-114">文本值</span><span class="sxs-lookup"><span data-stu-id="c2b21-114">Text value</span></span>

<span data-ttu-id="c2b21-115">**ReminderGroup**元素的文本值是提醒的组类型。</span><span class="sxs-lookup"><span data-stu-id="c2b21-115">The text value of the **ReminderGroup** element is the group type of the reminder.</span></span> <span data-ttu-id="c2b21-116">**日历**的文本值指定提醒的日历项目。</span><span class="sxs-lookup"><span data-stu-id="c2b21-116">The text value of **Calendar** specifies that the reminder is for a calendar item.</span></span> <span data-ttu-id="c2b21-117">**任务**的文本值指定提醒目的为任务项。</span><span class="sxs-lookup"><span data-stu-id="c2b21-117">The text value of **Task** specifies that the reminder is for a task item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c2b21-118">备注</span><span class="sxs-lookup"><span data-stu-id="c2b21-118">Remarks</span></span>

<span data-ttu-id="c2b21-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c2b21-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c2b21-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c2b21-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2b21-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="c2b21-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2b21-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="c2b21-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c2b21-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="c2b21-123">Schema Name</span></span>  <br/> |<span data-ttu-id="c2b21-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="c2b21-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="c2b21-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="c2b21-125">Validation File</span></span>  <br/> |<span data-ttu-id="c2b21-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c2b21-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c2b21-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="c2b21-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="c2b21-128">False</span><span class="sxs-lookup"><span data-stu-id="c2b21-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2b21-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2b21-129">See also</span></span>



[<span data-ttu-id="c2b21-130">提醒</span><span class="sxs-lookup"><span data-stu-id="c2b21-130">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="c2b21-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c2b21-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

