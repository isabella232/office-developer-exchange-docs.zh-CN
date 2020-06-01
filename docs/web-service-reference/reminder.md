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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457485"
---
# <a name="reminder"></a><span data-ttu-id="2b785-103">提醒</span><span class="sxs-lookup"><span data-stu-id="2b785-103">Reminder</span></span>

<span data-ttu-id="2b785-104">"**提醒**" 元素指定任务或日历项目的提醒。</span><span class="sxs-lookup"><span data-stu-id="2b785-104">The **Reminder** element specifies a reminder for a task or a calendar item.</span></span> 
  
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

 <span data-ttu-id="2b785-105">**ReminderType**</span><span class="sxs-lookup"><span data-stu-id="2b785-105">**ReminderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b785-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2b785-106">Attributes and elements</span></span>

<span data-ttu-id="2b785-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2b785-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b785-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2b785-108">Attributes</span></span>

<span data-ttu-id="2b785-109">无。</span><span class="sxs-lookup"><span data-stu-id="2b785-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b785-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2b785-110">Child elements</span></span>

<span data-ttu-id="2b785-111">[主题](subject.md)  | [位置](location.md)  | [ReminderTime](remindertime.md)  | [起始日期](startdate.md)  | [结束日期（ReminderType）](enddate-remindertype.md)  | [ItemId](itemid.md)  | [RecurringMasterItemId （ItemIdType）](recurringmasteritemid-itemidtype.md)  | [ReminderGroup](remindergroup.md)  | [UID](uid.md)</span><span class="sxs-lookup"><span data-stu-id="2b785-111">[Subject](subject.md) | [Location](location.md) | [ReminderTime](remindertime.md) | [StartDate](startdate.md) | [EndDate (ReminderType)](enddate-remindertype.md) | [ItemId](itemid.md) | [RecurringMasterItemId (ItemIdType)](recurringmasteritemid-itemidtype.md) | [ReminderGroup](remindergroup.md) | [UID](uid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2b785-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2b785-112">Parent elements</span></span>

[<span data-ttu-id="2b785-113">提醒</span><span class="sxs-lookup"><span data-stu-id="2b785-113">Reminders</span></span>](reminders.md)
  
## <a name="remarks"></a><span data-ttu-id="2b785-114">备注</span><span class="sxs-lookup"><span data-stu-id="2b785-114">Remarks</span></span>

<span data-ttu-id="2b785-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2b785-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2b785-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2b785-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b785-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="2b785-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b785-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="2b785-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2b785-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="2b785-119">Schema Name</span></span>  <br/> |<span data-ttu-id="2b785-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="2b785-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="2b785-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="2b785-121">Validation File</span></span>  <br/> |<span data-ttu-id="2b785-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2b785-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2b785-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="2b785-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b785-124">False</span><span class="sxs-lookup"><span data-stu-id="2b785-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b785-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2b785-125">See also</span></span>



[<span data-ttu-id="2b785-126">提醒</span><span class="sxs-lookup"><span data-stu-id="2b785-126">Reminders</span></span>](reminders.md)


- [<span data-ttu-id="2b785-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2b785-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

