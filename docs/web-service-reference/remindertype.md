---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: ReminderType 元素指定要返回的提醒的类型。
ms.openlocfilehash: 4ac20143bbfb29fb8f962515f2faba224b2f973f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465525"
---
# <a name="remindertype"></a><span data-ttu-id="24692-103">ReminderType</span><span class="sxs-lookup"><span data-stu-id="24692-103">ReminderType</span></span>

<span data-ttu-id="24692-104">**ReminderType**元素指定要返回的提醒的类型。</span><span class="sxs-lookup"><span data-stu-id="24692-104">The **ReminderType** element specifies the type of reminders to return.</span></span> 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 <span data-ttu-id="24692-105">**string**</span><span class="sxs-lookup"><span data-stu-id="24692-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24692-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="24692-106">Attributes and elements</span></span>

<span data-ttu-id="24692-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="24692-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24692-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="24692-108">Attributes</span></span>

<span data-ttu-id="24692-109">无。</span><span class="sxs-lookup"><span data-stu-id="24692-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24692-110">子元素</span><span class="sxs-lookup"><span data-stu-id="24692-110">Child elements</span></span>

<span data-ttu-id="24692-111">无。</span><span class="sxs-lookup"><span data-stu-id="24692-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="24692-112">父元素</span><span class="sxs-lookup"><span data-stu-id="24692-112">Parent elements</span></span>

[<span data-ttu-id="24692-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="24692-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="24692-114">文本值</span><span class="sxs-lookup"><span data-stu-id="24692-114">Text value</span></span>

<span data-ttu-id="24692-115">**ReminderType**元素的文本值是要返回的提醒类型，可以是 "**全部**"、"**当前**" 或 "**旧**"。</span><span class="sxs-lookup"><span data-stu-id="24692-115">The text value of the **ReminderType** element is the type of reminders to return, either **All**, **Current**, or **Old**.</span></span> <span data-ttu-id="24692-116">**All**是此元素的推荐值。</span><span class="sxs-lookup"><span data-stu-id="24692-116">**All** is the recommended value for this element.</span></span> <span data-ttu-id="24692-117">有关**ReminderType**元素与[BeginTime](begintime.md)和[EndTime](endtime-remindermessagedatatype.md)元素之间的关系的详细信息，请参阅[GetReminders operation](getreminders-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="24692-117">For more information about the relationship between the **ReminderType** element and the [BeginTime](begintime.md) and [EndTime](endtime-remindermessagedatatype.md) elements, see [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24692-118">备注</span><span class="sxs-lookup"><span data-stu-id="24692-118">Remarks</span></span>

<span data-ttu-id="24692-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="24692-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="24692-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="24692-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24692-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="24692-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24692-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="24692-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="24692-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="24692-123">Schema Name</span></span>  <br/> |<span data-ttu-id="24692-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="24692-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="24692-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="24692-125">Validation File</span></span>  <br/> |<span data-ttu-id="24692-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="24692-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="24692-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="24692-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="24692-128">False</span><span class="sxs-lookup"><span data-stu-id="24692-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24692-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="24692-129">See also</span></span>



[<span data-ttu-id="24692-130">GetReminders</span><span class="sxs-lookup"><span data-stu-id="24692-130">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="24692-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="24692-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

