---
title: ActionType （ReminderActionType）
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: ActionType 元素指定要对提醒执行的操作。
ms.openlocfilehash: 5c62b2dd945b23a5ff2bb824385c45dbc617a5a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465056"
---
# <a name="actiontype-reminderactiontype"></a><span data-ttu-id="d1799-103">ActionType （ReminderActionType）</span><span class="sxs-lookup"><span data-stu-id="d1799-103">ActionType (ReminderActionType)</span></span>

<span data-ttu-id="d1799-104">**ActionType**元素指定要对提醒执行的操作。</span><span class="sxs-lookup"><span data-stu-id="d1799-104">The **ActionType** element specifies the action to take on the reminder.</span></span> 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 <span data-ttu-id="d1799-105">**ReminderActionType**</span><span class="sxs-lookup"><span data-stu-id="d1799-105">**ReminderActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1799-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d1799-106">Attributes and elements</span></span>

<span data-ttu-id="d1799-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d1799-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1799-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d1799-108">Attributes</span></span>

<span data-ttu-id="d1799-109">无。</span><span class="sxs-lookup"><span data-stu-id="d1799-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1799-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d1799-110">Child elements</span></span>

<span data-ttu-id="d1799-111">无。</span><span class="sxs-lookup"><span data-stu-id="d1799-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1799-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d1799-112">Parent elements</span></span>

[<span data-ttu-id="d1799-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="d1799-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="d1799-114">文本值</span><span class="sxs-lookup"><span data-stu-id="d1799-114">Text value</span></span>

<span data-ttu-id="d1799-115">**ActionType**元素的文本值指定要对提醒执行的操作。</span><span class="sxs-lookup"><span data-stu-id="d1799-115">The text value of the **ActionType** element specifies the action to take on the reminder.</span></span> <span data-ttu-id="d1799-116">"**取消**" 文本值表示应消除提醒。</span><span class="sxs-lookup"><span data-stu-id="d1799-116">The text value of **Dismiss** indicates the reminder should be dismissed.</span></span> <span data-ttu-id="d1799-117">"**推迟**" 的文本值表示提醒应延迟到[NewReminderTime](newremindertime.md)元素指定的时间。</span><span class="sxs-lookup"><span data-stu-id="d1799-117">The text value of **Snooze** indicates that the reminder should be delayed until the time specified by the [NewReminderTime](newremindertime.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d1799-118">备注</span><span class="sxs-lookup"><span data-stu-id="d1799-118">Remarks</span></span>

<span data-ttu-id="d1799-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d1799-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d1799-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d1799-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1799-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="d1799-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1799-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="d1799-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1799-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="d1799-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d1799-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="d1799-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1799-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="d1799-125">Validation File</span></span>  <br/> |<span data-ttu-id="d1799-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1799-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1799-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="d1799-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1799-128">False</span><span class="sxs-lookup"><span data-stu-id="d1799-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1799-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d1799-129">See also</span></span>

- [<span data-ttu-id="d1799-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="d1799-130">ReminderItemAction</span></span>](reminderitemaction.md)
- [<span data-ttu-id="d1799-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d1799-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

