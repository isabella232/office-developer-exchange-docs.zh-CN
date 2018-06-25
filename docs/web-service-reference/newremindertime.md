---
title: NewReminderTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: NewReminderTime 元素指定提醒的新时间。
ms.openlocfilehash: 9f3f509942c673c916cc646cd9519240aef6ea06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826531"
---
# <a name="newremindertime"></a><span data-ttu-id="8e6ed-103">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="8e6ed-103">NewReminderTime</span></span>

<span data-ttu-id="8e6ed-104">**NewReminderTime**元素指定提醒的新时间。</span><span class="sxs-lookup"><span data-stu-id="8e6ed-104">The **NewReminderTime** element specifies a new time for a reminder.</span></span> 
  
```XML
<NewReminderTime/>
```

 <span data-ttu-id="8e6ed-105">**string**</span><span class="sxs-lookup"><span data-stu-id="8e6ed-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e6ed-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8e6ed-106">Attributes and elements</span></span>

<span data-ttu-id="8e6ed-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8e6ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e6ed-108">属性</span><span class="sxs-lookup"><span data-stu-id="8e6ed-108">Attributes</span></span>

<span data-ttu-id="8e6ed-109">无。</span><span class="sxs-lookup"><span data-stu-id="8e6ed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8e6ed-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8e6ed-110">Child elements</span></span>

<span data-ttu-id="8e6ed-111">无。</span><span class="sxs-lookup"><span data-stu-id="8e6ed-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8e6ed-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8e6ed-112">Parent elements</span></span>

[<span data-ttu-id="8e6ed-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="8e6ed-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="8e6ed-114">文本值</span><span class="sxs-lookup"><span data-stu-id="8e6ed-114">Text value</span></span>

<span data-ttu-id="8e6ed-115">**NewReminderTime**元素的文本值是提醒的新时间。</span><span class="sxs-lookup"><span data-stu-id="8e6ed-115">The text value of the **NewReminderTime** element is a new time for the reminder.</span></span> <span data-ttu-id="8e6ed-116">[ActionType](actiontype-reminderactiontype.md)元素设置为**Snooze**，以便提醒延迟时使用**NewReminderTime**元素。</span><span class="sxs-lookup"><span data-stu-id="8e6ed-116">The **NewReminderTime** element is used when the [ActionType](actiontype-reminderactiontype.md) element is set to **Snooze**, in order to delay the reminder.</span></span> <span data-ttu-id="8e6ed-117">**NewReminderTime**的值必须大于[ReminderTime](remindertime.md) [GetReminders 操作](getreminders-operation.md)返回。</span><span class="sxs-lookup"><span data-stu-id="8e6ed-117">The value of the **NewReminderTime** must be greater than the [ReminderTime](remindertime.md) returned by the [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e6ed-118">备注</span><span class="sxs-lookup"><span data-stu-id="8e6ed-118">Remarks</span></span>

<span data-ttu-id="8e6ed-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8e6ed-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8e6ed-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8e6ed-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e6ed-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="8e6ed-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e6ed-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="8e6ed-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8e6ed-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="8e6ed-123">Schema Name</span></span>  <br/> |<span data-ttu-id="8e6ed-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="8e6ed-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="8e6ed-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="8e6ed-125">Validation File</span></span>  <br/> |<span data-ttu-id="8e6ed-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8e6ed-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8e6ed-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="8e6ed-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="8e6ed-128">False</span><span class="sxs-lookup"><span data-stu-id="8e6ed-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e6ed-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8e6ed-129">See also</span></span>



[<span data-ttu-id="8e6ed-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="8e6ed-130">ReminderItemAction</span></span>](reminderitemaction.md)


- [<span data-ttu-id="8e6ed-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8e6ed-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

