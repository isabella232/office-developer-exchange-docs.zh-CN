---
title: GetReminders
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 943c3d5d-7d29-4d70-932c-8a4fe44a0037
description: GetReminders 元素指定要获取提醒的请求。
ms.openlocfilehash: f4ecc858af2150bb3f88ebdf9ed541892f2fead1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754666"
---
# <a name="getreminders"></a><span data-ttu-id="9df82-103">GetReminders</span><span class="sxs-lookup"><span data-stu-id="9df82-103">GetReminders</span></span>

<span data-ttu-id="9df82-104">**GetReminders**元素指定要获取提醒的请求。</span><span class="sxs-lookup"><span data-stu-id="9df82-104">The **GetReminders** element specifies a request to get reminders.</span></span> 
  
```XML
<GetReminders>
   <BeginTime/>
   <EndTime/>
   <MaxItems/>
   <ReminderType/>
</GetReminders>

```

 <span data-ttu-id="9df82-105">**GetRemindersType**</span><span class="sxs-lookup"><span data-stu-id="9df82-105">**GetRemindersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9df82-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9df82-106">Attributes and elements</span></span>

<span data-ttu-id="9df82-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9df82-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9df82-108">属性</span><span class="sxs-lookup"><span data-stu-id="9df82-108">Attributes</span></span>

<span data-ttu-id="9df82-109">无。</span><span class="sxs-lookup"><span data-stu-id="9df82-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9df82-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9df82-110">Child elements</span></span>

<span data-ttu-id="9df82-111">[BeginTime](begintime.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [MaxItems](maxitems.md) | [ReminderType](remindertype.md)</span><span class="sxs-lookup"><span data-stu-id="9df82-111">[BeginTime](begintime.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [MaxItems](maxitems.md) | [ReminderType](remindertype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9df82-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9df82-112">Parent elements</span></span>

<span data-ttu-id="9df82-113">无。</span><span class="sxs-lookup"><span data-stu-id="9df82-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9df82-114">备注</span><span class="sxs-lookup"><span data-stu-id="9df82-114">Remarks</span></span>

<span data-ttu-id="9df82-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9df82-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9df82-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9df82-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9df82-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="9df82-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9df82-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="9df82-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9df82-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="9df82-119">Schema Name</span></span>  <br/> |<span data-ttu-id="9df82-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="9df82-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9df82-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="9df82-121">Validation File</span></span>  <br/> |<span data-ttu-id="9df82-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9df82-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9df82-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="9df82-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="9df82-124">True</span><span class="sxs-lookup"><span data-stu-id="9df82-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9df82-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9df82-125">See also</span></span>



- [<span data-ttu-id="9df82-126">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9df82-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

