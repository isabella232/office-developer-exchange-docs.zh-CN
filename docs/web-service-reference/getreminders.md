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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754666"
---
# <a name="getreminders"></a><span data-ttu-id="927c1-103">GetReminders</span><span class="sxs-lookup"><span data-stu-id="927c1-103">GetReminders</span></span>

<span data-ttu-id="927c1-104">**GetReminders**元素指定要获取提醒的请求。</span><span class="sxs-lookup"><span data-stu-id="927c1-104">The **GetReminders** element specifies a request to get reminders.</span></span> 
  
```XML
<GetReminders>
   <BeginTime/>
   <EndTime/>
   <MaxItems/>
   <ReminderType/>
</GetReminders>

```

 <span data-ttu-id="927c1-105">**GetRemindersType**</span><span class="sxs-lookup"><span data-stu-id="927c1-105">**GetRemindersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="927c1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="927c1-106">Attributes and elements</span></span>

<span data-ttu-id="927c1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="927c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="927c1-108">属性</span><span class="sxs-lookup"><span data-stu-id="927c1-108">Attributes</span></span>

<span data-ttu-id="927c1-109">无。</span><span class="sxs-lookup"><span data-stu-id="927c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="927c1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="927c1-110">Child elements</span></span>

<span data-ttu-id="927c1-111">[BeginTime](begintime.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [MaxItems](maxitems.md) | [ReminderType](remindertype.md)</span><span class="sxs-lookup"><span data-stu-id="927c1-111">[BeginTime](begintime.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [MaxItems](maxitems.md) | [ReminderType](remindertype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="927c1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="927c1-112">Parent elements</span></span>

<span data-ttu-id="927c1-113">无。</span><span class="sxs-lookup"><span data-stu-id="927c1-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="927c1-114">备注</span><span class="sxs-lookup"><span data-stu-id="927c1-114">Remarks</span></span>

<span data-ttu-id="927c1-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="927c1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="927c1-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="927c1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="927c1-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="927c1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="927c1-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="927c1-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="927c1-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="927c1-119">Schema Name</span></span>  <br/> |<span data-ttu-id="927c1-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="927c1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="927c1-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="927c1-121">Validation File</span></span>  <br/> |<span data-ttu-id="927c1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="927c1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="927c1-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="927c1-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="927c1-124">True</span><span class="sxs-lookup"><span data-stu-id="927c1-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="927c1-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="927c1-125">See also</span></span>



- [<span data-ttu-id="927c1-126">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="927c1-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

