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
ms.openlocfilehash: a10f7e481b474501f33dba4c09060766568952b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465952"
---
# <a name="newremindertime"></a><span data-ttu-id="2789e-103">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="2789e-103">NewReminderTime</span></span>

<span data-ttu-id="2789e-104">**NewReminderTime**元素指定提醒的新时间。</span><span class="sxs-lookup"><span data-stu-id="2789e-104">The **NewReminderTime** element specifies a new time for a reminder.</span></span> 
  
```XML
<NewReminderTime/>
```

 <span data-ttu-id="2789e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="2789e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2789e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2789e-106">Attributes and elements</span></span>

<span data-ttu-id="2789e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2789e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2789e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2789e-108">Attributes</span></span>

<span data-ttu-id="2789e-109">无。</span><span class="sxs-lookup"><span data-stu-id="2789e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2789e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2789e-110">Child elements</span></span>

<span data-ttu-id="2789e-111">无。</span><span class="sxs-lookup"><span data-stu-id="2789e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2789e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2789e-112">Parent elements</span></span>

[<span data-ttu-id="2789e-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="2789e-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="2789e-114">文本值</span><span class="sxs-lookup"><span data-stu-id="2789e-114">Text value</span></span>

<span data-ttu-id="2789e-115">**NewReminderTime**元素的文本值是提醒的新时间。</span><span class="sxs-lookup"><span data-stu-id="2789e-115">The text value of the **NewReminderTime** element is a new time for the reminder.</span></span> <span data-ttu-id="2789e-116">当[ActionType](actiontype-reminderactiontype.md)元素设置为 "**暂停**" 时，将使用**NewReminderTime**元素，以便延迟提醒。</span><span class="sxs-lookup"><span data-stu-id="2789e-116">The **NewReminderTime** element is used when the [ActionType](actiontype-reminderactiontype.md) element is set to **Snooze**, in order to delay the reminder.</span></span> <span data-ttu-id="2789e-117">**NewReminderTime**的值必须大于[GetReminders 操作](getreminders-operation.md)返回的[ReminderTime](remindertime.md) 。</span><span class="sxs-lookup"><span data-stu-id="2789e-117">The value of the **NewReminderTime** must be greater than the [ReminderTime](remindertime.md) returned by the [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2789e-118">备注</span><span class="sxs-lookup"><span data-stu-id="2789e-118">Remarks</span></span>

<span data-ttu-id="2789e-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2789e-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2789e-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2789e-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2789e-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="2789e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2789e-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="2789e-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2789e-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="2789e-123">Schema Name</span></span>  <br/> |<span data-ttu-id="2789e-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="2789e-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="2789e-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="2789e-125">Validation File</span></span>  <br/> |<span data-ttu-id="2789e-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2789e-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2789e-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="2789e-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="2789e-128">False</span><span class="sxs-lookup"><span data-stu-id="2789e-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2789e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2789e-129">See also</span></span>



[<span data-ttu-id="2789e-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="2789e-130">ReminderItemAction</span></span>](reminderitemaction.md)


- [<span data-ttu-id="2789e-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2789e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

