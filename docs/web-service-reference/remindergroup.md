---
title: ReminderGroup
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: ReminderGroup 元素指定提醒是用于日历项目还是任务。
ms.openlocfilehash: be6f4a7d7e9d495ed7b42ed40c60f016468e8c2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529866"
---
# <a name="remindergroup"></a><span data-ttu-id="b5d48-103">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="b5d48-103">ReminderGroup</span></span>

<span data-ttu-id="b5d48-104">**ReminderGroup**元素指定提醒是用于日历项目还是任务。</span><span class="sxs-lookup"><span data-stu-id="b5d48-104">The **ReminderGroup** element specifies whether the reminder is for a calendar item or a task.</span></span> 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 <span data-ttu-id="b5d48-105">**ReminderGroupType**</span><span class="sxs-lookup"><span data-stu-id="b5d48-105">**ReminderGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5d48-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b5d48-106">Attributes and elements</span></span>

<span data-ttu-id="b5d48-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b5d48-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5d48-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b5d48-108">Attributes</span></span>

<span data-ttu-id="b5d48-109">无。</span><span class="sxs-lookup"><span data-stu-id="b5d48-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5d48-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b5d48-110">Child elements</span></span>

<span data-ttu-id="b5d48-111">无。</span><span class="sxs-lookup"><span data-stu-id="b5d48-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b5d48-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b5d48-112">Parent elements</span></span>

[<span data-ttu-id="b5d48-113">提醒</span><span class="sxs-lookup"><span data-stu-id="b5d48-113">Reminder</span></span>](reminder.md)
  
## <a name="text-value"></a><span data-ttu-id="b5d48-114">文本值</span><span class="sxs-lookup"><span data-stu-id="b5d48-114">Text value</span></span>

<span data-ttu-id="b5d48-115">**ReminderGroup**元素的文本值是提醒的组类型。</span><span class="sxs-lookup"><span data-stu-id="b5d48-115">The text value of the **ReminderGroup** element is the group type of the reminder.</span></span> <span data-ttu-id="b5d48-116">**Calendar**的文本值指定 "日历" 项目的提醒。</span><span class="sxs-lookup"><span data-stu-id="b5d48-116">The text value of **Calendar** specifies that the reminder is for a calendar item.</span></span> <span data-ttu-id="b5d48-117">**任务**的文本值指定该提醒针对的是任务项。</span><span class="sxs-lookup"><span data-stu-id="b5d48-117">The text value of **Task** specifies that the reminder is for a task item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b5d48-118">备注</span><span class="sxs-lookup"><span data-stu-id="b5d48-118">Remarks</span></span>

<span data-ttu-id="b5d48-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b5d48-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b5d48-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b5d48-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5d48-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="b5d48-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5d48-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="b5d48-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b5d48-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="b5d48-123">Schema Name</span></span>  <br/> |<span data-ttu-id="b5d48-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="b5d48-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="b5d48-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="b5d48-125">Validation File</span></span>  <br/> |<span data-ttu-id="b5d48-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b5d48-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b5d48-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="b5d48-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="b5d48-128">False</span><span class="sxs-lookup"><span data-stu-id="b5d48-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5d48-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b5d48-129">See also</span></span>



[<span data-ttu-id="b5d48-130">提醒</span><span class="sxs-lookup"><span data-stu-id="b5d48-130">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="b5d48-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b5d48-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

