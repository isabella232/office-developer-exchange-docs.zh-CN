---
title: ReminderMessageData
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04dd4987-baaf-4ebe-ae58-ad962c2f8fa1
description: ReminderMessageData 元素指定提醒邮件中的数据。
ms.openlocfilehash: f2632062cd02581c426f7dbfa2a33d53e5594d72
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458549"
---
# <a name="remindermessagedata"></a><span data-ttu-id="7912b-103">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="7912b-103">ReminderMessageData</span></span>

<span data-ttu-id="7912b-104">**ReminderMessageData**元素指定提醒邮件中的数据。</span><span class="sxs-lookup"><span data-stu-id="7912b-104">The **ReminderMessageData** element specifies the data in a reminder message.</span></span> 
  
```XML
<ReminderMessageData>
   <ReminderText></ReminderText>
   <Location></Location>
   <StartTime></StartTime>
   <EndTime></EndTime>
   <AssociatedCalendarItemId></AssociatedCalendarItemId>
</ReminderMessageData>

```

 <span data-ttu-id="7912b-105">**ReminderMessageDataType**</span><span class="sxs-lookup"><span data-stu-id="7912b-105">**ReminderMessageDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7912b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7912b-106">Attributes and elements</span></span>

<span data-ttu-id="7912b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7912b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7912b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7912b-108">Attributes</span></span>

<span data-ttu-id="7912b-109">无。</span><span class="sxs-lookup"><span data-stu-id="7912b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7912b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7912b-110">Child elements</span></span>

<span data-ttu-id="7912b-111">[ReminderText](remindertext.md)  | [位置](location.md)  | [StartTime （ReminderMessageDataType）](starttime-remindermessagedatatype.md)  | [EndTime （ReminderMessageDataType）](endtime-remindermessagedatatype.md)  | [AssociatedCalendarItemId](associatedcalendaritemid.md)</span><span class="sxs-lookup"><span data-stu-id="7912b-111">[ReminderText](remindertext.md) | [Location](location.md) | [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [AssociatedCalendarItemId](associatedcalendaritemid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7912b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7912b-112">Parent elements</span></span>

[<span data-ttu-id="7912b-113">邮件</span><span class="sxs-lookup"><span data-stu-id="7912b-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="7912b-114">说明</span><span class="sxs-lookup"><span data-stu-id="7912b-114">Remarks</span></span>

<span data-ttu-id="7912b-115">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7912b-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="7912b-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7912b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="7912b-117">从内部版本号15.00.0913.09 开始的 Exchange 版本可以将**AssociatedCalendarItemId**元素作为**ReminderMessageData**元素的子元素包括在内。</span><span class="sxs-lookup"><span data-stu-id="7912b-117">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7912b-118">元素信息</span><span class="sxs-lookup"><span data-stu-id="7912b-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7912b-119">命名空间</span><span class="sxs-lookup"><span data-stu-id="7912b-119">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7912b-120">架构名称</span><span class="sxs-lookup"><span data-stu-id="7912b-120">Schema Name</span></span>  <br/> |<span data-ttu-id="7912b-121">类型架构</span><span class="sxs-lookup"><span data-stu-id="7912b-121">Types schema</span></span>  <br/> |
|<span data-ttu-id="7912b-122">验证文件</span><span class="sxs-lookup"><span data-stu-id="7912b-122">Validation File</span></span>  <br/> |<span data-ttu-id="7912b-123">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7912b-123">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7912b-124">可以为空</span><span class="sxs-lookup"><span data-stu-id="7912b-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="7912b-125">True</span><span class="sxs-lookup"><span data-stu-id="7912b-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7912b-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7912b-126">See also</span></span>



[<span data-ttu-id="7912b-127">邮件</span><span class="sxs-lookup"><span data-stu-id="7912b-127">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="7912b-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7912b-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

