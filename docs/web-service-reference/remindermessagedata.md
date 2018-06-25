---
title: ReminderMessageData
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04dd4987-baaf-4ebe-ae58-ad962c2f8fa1
description: ReminderMessageData 元素提醒消息中指定的数据。
ms.openlocfilehash: a1d01dd24030b047bd8ad025f3e1cebed0da8e29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827067"
---
# <a name="remindermessagedata"></a><span data-ttu-id="9a582-103">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="9a582-103">ReminderMessageData</span></span>

<span data-ttu-id="9a582-104">**ReminderMessageData**元素提醒消息中指定的数据。</span><span class="sxs-lookup"><span data-stu-id="9a582-104">The **ReminderMessageData** element specifies the data in a reminder message.</span></span> 
  
```XML
<ReminderMessageData>
   <ReminderText></ReminderText>
   <Location></Location>
   <StartTime></StartTime>
   <EndTime></EndTime>
   <AssociatedCalendarItemId></AssociatedCalendarItemId>
</ReminderMessageData>

```

 <span data-ttu-id="9a582-105">**ReminderMessageDataType**</span><span class="sxs-lookup"><span data-stu-id="9a582-105">**ReminderMessageDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a582-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9a582-106">Attributes and elements</span></span>

<span data-ttu-id="9a582-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9a582-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a582-108">属性</span><span class="sxs-lookup"><span data-stu-id="9a582-108">Attributes</span></span>

<span data-ttu-id="9a582-109">无。</span><span class="sxs-lookup"><span data-stu-id="9a582-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a582-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9a582-110">Child elements</span></span>

<span data-ttu-id="9a582-111">[ReminderText](remindertext.md) | [位置](location.md) | [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [AssociatedCalendarItemId](associatedcalendaritemid.md)</span><span class="sxs-lookup"><span data-stu-id="9a582-111">[ReminderText](remindertext.md) | [Location](location.md) | [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [AssociatedCalendarItemId](associatedcalendaritemid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9a582-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9a582-112">Parent elements</span></span>

[<span data-ttu-id="9a582-113">Message</span><span class="sxs-lookup"><span data-stu-id="9a582-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="9a582-114">备注</span><span class="sxs-lookup"><span data-stu-id="9a582-114">Remarks</span></span>

<span data-ttu-id="9a582-115">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9a582-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="9a582-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9a582-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="9a582-117">内部版本号 15.00.0913.09 开头的 Exchange 版本可作为**ReminderMessageData**元素的子元素包括**AssociatedCalendarItemId**元素。</span><span class="sxs-lookup"><span data-stu-id="9a582-117">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9a582-118">元素信息</span><span class="sxs-lookup"><span data-stu-id="9a582-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a582-119">命名空间</span><span class="sxs-lookup"><span data-stu-id="9a582-119">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9a582-120">架构名称</span><span class="sxs-lookup"><span data-stu-id="9a582-120">Schema Name</span></span>  <br/> |<span data-ttu-id="9a582-121">类型架构</span><span class="sxs-lookup"><span data-stu-id="9a582-121">Types schema</span></span>  <br/> |
|<span data-ttu-id="9a582-122">验证文件</span><span class="sxs-lookup"><span data-stu-id="9a582-122">Validation File</span></span>  <br/> |<span data-ttu-id="9a582-123">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9a582-123">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9a582-124">可以为空</span><span class="sxs-lookup"><span data-stu-id="9a582-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="9a582-125">True</span><span class="sxs-lookup"><span data-stu-id="9a582-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a582-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9a582-126">See also</span></span>



[<span data-ttu-id="9a582-127">Message</span><span class="sxs-lookup"><span data-stu-id="9a582-127">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="9a582-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9a582-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

