---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: ReminderType 元素指定的提醒，以便在返回的类型。
ms.openlocfilehash: 11739d2068a1009b2840b2169e86b113151cbfa9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827077"
---
# <a name="remindertype"></a><span data-ttu-id="8b919-103">ReminderType</span><span class="sxs-lookup"><span data-stu-id="8b919-103">ReminderType</span></span>

<span data-ttu-id="8b919-104">**ReminderType**元素指定的提醒，以便在返回的类型。</span><span class="sxs-lookup"><span data-stu-id="8b919-104">The **ReminderType** element specifies the type of reminders to return.</span></span> 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 <span data-ttu-id="8b919-105">**string**</span><span class="sxs-lookup"><span data-stu-id="8b919-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8b919-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8b919-106">Attributes and elements</span></span>

<span data-ttu-id="8b919-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8b919-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b919-108">属性</span><span class="sxs-lookup"><span data-stu-id="8b919-108">Attributes</span></span>

<span data-ttu-id="8b919-109">无。</span><span class="sxs-lookup"><span data-stu-id="8b919-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8b919-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8b919-110">Child elements</span></span>

<span data-ttu-id="8b919-111">无。</span><span class="sxs-lookup"><span data-stu-id="8b919-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8b919-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8b919-112">Parent elements</span></span>

[<span data-ttu-id="8b919-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="8b919-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="8b919-114">文本值</span><span class="sxs-lookup"><span data-stu-id="8b919-114">Text value</span></span>

<span data-ttu-id="8b919-115">**ReminderType**元素的文本值的提醒，以便返回，**所有**、**当前**，或**旧**的类型。</span><span class="sxs-lookup"><span data-stu-id="8b919-115">The text value of the **ReminderType** element is the type of reminders to return, either **All**, **Current**, or **Old**.</span></span> <span data-ttu-id="8b919-116">**所有**是此元素的建议的值。</span><span class="sxs-lookup"><span data-stu-id="8b919-116">**All** is the recommended value for this element.</span></span> <span data-ttu-id="8b919-117">有关**ReminderType**元素和[BeginTime](begintime.md)和[EndTime](endtime-remindermessagedatatype.md)元素之间的关系的详细信息，请参阅[GetReminders 操作](getreminders-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="8b919-117">For more information about the relationship between the **ReminderType** element and the [BeginTime](begintime.md) and [EndTime](endtime-remindermessagedatatype.md) elements, see [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8b919-118">备注</span><span class="sxs-lookup"><span data-stu-id="8b919-118">Remarks</span></span>

<span data-ttu-id="8b919-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8b919-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8b919-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8b919-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b919-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="8b919-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b919-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="8b919-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8b919-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="8b919-123">Schema Name</span></span>  <br/> |<span data-ttu-id="8b919-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="8b919-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8b919-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="8b919-125">Validation File</span></span>  <br/> |<span data-ttu-id="8b919-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8b919-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8b919-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="8b919-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="8b919-128">False</span><span class="sxs-lookup"><span data-stu-id="8b919-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b919-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8b919-129">See also</span></span>



[<span data-ttu-id="8b919-130">GetReminders</span><span class="sxs-lookup"><span data-stu-id="8b919-130">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="8b919-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8b919-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

