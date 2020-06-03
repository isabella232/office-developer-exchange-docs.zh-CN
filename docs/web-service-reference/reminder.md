---
title: 提醒
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54dd748a-23a5-4ea2-88f2-b74c68a3c48f
description: "\"提醒\" 元素指定任务或日历项目的提醒。"
ms.openlocfilehash: 71e54d920a169b8060d22bb7d7d294208c344c2e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457485"
---
# <a name="reminder"></a><span data-ttu-id="14630-103">提醒</span><span class="sxs-lookup"><span data-stu-id="14630-103">Reminder</span></span>

<span data-ttu-id="14630-104">"**提醒**" 元素指定任务或日历项目的提醒。</span><span class="sxs-lookup"><span data-stu-id="14630-104">The **Reminder** element specifies a reminder for a task or a calendar item.</span></span> 
  
```XML
<Reminder>
   <Subject></Subject>
   <Location></Location>
   <ReminderTime></ReminderTime>
   <StartDate></StartDate>
   <EndDate></EndDate>
   <ItemId></ItemId>
   <RecurringMasterItemId></RecurringMasterItemId>
   <ReminderGroup></ReminderGroup>
   <UID></UID>
</Reminder>

```

 <span data-ttu-id="14630-105">**ReminderType**</span><span class="sxs-lookup"><span data-stu-id="14630-105">**ReminderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14630-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="14630-106">Attributes and elements</span></span>

<span data-ttu-id="14630-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="14630-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14630-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="14630-108">Attributes</span></span>

<span data-ttu-id="14630-109">无。</span><span class="sxs-lookup"><span data-stu-id="14630-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14630-110">子元素</span><span class="sxs-lookup"><span data-stu-id="14630-110">Child elements</span></span>

<span data-ttu-id="14630-111">[主题](subject.md)  | [位置](location.md)  | [ReminderTime](remindertime.md)  | [起始日期](startdate.md)  | [结束日期（ReminderType）](enddate-remindertype.md)  | [ItemId](itemid.md)  | [RecurringMasterItemId （ItemIdType）](recurringmasteritemid-itemidtype.md)  | [ReminderGroup](remindergroup.md)  | [UID](uid.md)</span><span class="sxs-lookup"><span data-stu-id="14630-111">[Subject](subject.md) | [Location](location.md) | [ReminderTime](remindertime.md) | [StartDate](startdate.md) | [EndDate (ReminderType)](enddate-remindertype.md) | [ItemId](itemid.md) | [RecurringMasterItemId (ItemIdType)](recurringmasteritemid-itemidtype.md) | [ReminderGroup](remindergroup.md) | [UID](uid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="14630-112">父元素</span><span class="sxs-lookup"><span data-stu-id="14630-112">Parent elements</span></span>

[<span data-ttu-id="14630-113">提醒</span><span class="sxs-lookup"><span data-stu-id="14630-113">Reminders</span></span>](reminders.md)
  
## <a name="remarks"></a><span data-ttu-id="14630-114">备注</span><span class="sxs-lookup"><span data-stu-id="14630-114">Remarks</span></span>

<span data-ttu-id="14630-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="14630-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="14630-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="14630-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14630-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="14630-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14630-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="14630-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="14630-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="14630-119">Schema Name</span></span>  <br/> |<span data-ttu-id="14630-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="14630-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="14630-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="14630-121">Validation File</span></span>  <br/> |<span data-ttu-id="14630-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="14630-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="14630-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="14630-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="14630-124">False</span><span class="sxs-lookup"><span data-stu-id="14630-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14630-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="14630-125">See also</span></span>



[<span data-ttu-id="14630-126">提醒</span><span class="sxs-lookup"><span data-stu-id="14630-126">Reminders</span></span>](reminders.md)


- [<span data-ttu-id="14630-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="14630-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

