---
title: ActionType (ReminderActionType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: ActionType 元素指定要在提醒上执行的操作。
ms.openlocfilehash: 361259f733756995fae2c2c2390013a728e475a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753095"
---
# <a name="actiontype-reminderactiontype"></a><span data-ttu-id="e3773-103">ActionType (ReminderActionType)</span><span class="sxs-lookup"><span data-stu-id="e3773-103">ActionType (ReminderActionType)</span></span>

<span data-ttu-id="e3773-104">**ActionType**元素指定要在提醒上执行的操作。</span><span class="sxs-lookup"><span data-stu-id="e3773-104">The **ActionType** element specifies the action to take on the reminder.</span></span> 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 <span data-ttu-id="e3773-105">**ReminderActionType**</span><span class="sxs-lookup"><span data-stu-id="e3773-105">**ReminderActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3773-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e3773-106">Attributes and elements</span></span>

<span data-ttu-id="e3773-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e3773-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3773-108">属性</span><span class="sxs-lookup"><span data-stu-id="e3773-108">Attributes</span></span>

<span data-ttu-id="e3773-109">无。</span><span class="sxs-lookup"><span data-stu-id="e3773-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3773-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e3773-110">Child elements</span></span>

<span data-ttu-id="e3773-111">无。</span><span class="sxs-lookup"><span data-stu-id="e3773-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3773-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e3773-112">Parent elements</span></span>

[<span data-ttu-id="e3773-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="e3773-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="e3773-114">文本值</span><span class="sxs-lookup"><span data-stu-id="e3773-114">Text value</span></span>

<span data-ttu-id="e3773-115">**ActionType**元素的文本值指定要在提醒上执行的操作。</span><span class="sxs-lookup"><span data-stu-id="e3773-115">The text value of the **ActionType** element specifies the action to take on the reminder.</span></span> <span data-ttu-id="e3773-116">**Dismiss**的文本值指示应消除提醒。</span><span class="sxs-lookup"><span data-stu-id="e3773-116">The text value of **Dismiss** indicates the reminder should be dismissed.</span></span> <span data-ttu-id="e3773-117">**Snooze**的文本值指示提醒，应推迟到[NewReminderTime](newremindertime.md)元素所指定的时间。</span><span class="sxs-lookup"><span data-stu-id="e3773-117">The text value of **Snooze** indicates that the reminder should be delayed until the time specified by the [NewReminderTime](newremindertime.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e3773-118">备注</span><span class="sxs-lookup"><span data-stu-id="e3773-118">Remarks</span></span>

<span data-ttu-id="e3773-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e3773-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e3773-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e3773-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3773-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="e3773-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3773-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="e3773-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e3773-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="e3773-123">Schema Name</span></span>  <br/> |<span data-ttu-id="e3773-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="e3773-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="e3773-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="e3773-125">Validation File</span></span>  <br/> |<span data-ttu-id="e3773-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e3773-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e3773-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="e3773-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3773-128">False</span><span class="sxs-lookup"><span data-stu-id="e3773-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3773-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3773-129">See also</span></span>

- [<span data-ttu-id="e3773-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="e3773-130">ReminderItemAction</span></span>](reminderitemaction.md)
- [<span data-ttu-id="e3773-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e3773-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

