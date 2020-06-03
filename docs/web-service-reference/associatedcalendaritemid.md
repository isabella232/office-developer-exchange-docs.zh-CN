---
title: AssociatedCalendarItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AssociatedCalendarItemId
api_type:
- schema
ms.assetid: 5b29898c-ea59-4e6a-914c-c011ec754032
description: AssociatedCalendarItemId 元素表示与 MeetingMessage、MeetingRequest、MeetingResponse、MeetingCancellation 或 ReminderMessageData 相关联的日历项目。
ms.openlocfilehash: 816372c38243ba0fe5a7606c264dd1c5107350f2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460881"
---
# <a name="associatedcalendaritemid"></a><span data-ttu-id="dc83f-103">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="dc83f-103">AssociatedCalendarItemId</span></span>

<span data-ttu-id="dc83f-104">**AssociatedCalendarItemId**元素表示与[MeetingMessage](meetingmessage.md)、 [MeetingRequest](meetingrequest.md)、 [MeetingResponse](meetingresponse.md)、 [MeetingCancellation](meetingcancellation.md)或[ReminderMessageData](remindermessagedata.md)相关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="dc83f-104">The **AssociatedCalendarItemId** element represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md), or [ReminderMessageData](remindermessagedata.md).</span></span>
  
```XML
<AssociatedCalendarItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="dc83f-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="dc83f-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc83f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc83f-106">Attributes and elements</span></span>

<span data-ttu-id="dc83f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc83f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc83f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dc83f-108">Attributes</span></span>

|<span data-ttu-id="dc83f-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="dc83f-109">**Attribute**</span></span>|<span data-ttu-id="dc83f-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc83f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc83f-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="dc83f-111">**Id**</span></span> <br/> |<span data-ttu-id="dc83f-112">标识与会议关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="dc83f-112">Identifies the calendar item that is associated with meeting.</span></span>  <br/> |
|<span data-ttu-id="dc83f-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="dc83f-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="dc83f-114">标识与会议相关联的日历项目的特定版本。</span><span class="sxs-lookup"><span data-stu-id="dc83f-114">Identifies a specific version of the calendar item that is associated with a meeting.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dc83f-115">子元素</span><span class="sxs-lookup"><span data-stu-id="dc83f-115">Child elements</span></span>

<span data-ttu-id="dc83f-116">无。</span><span class="sxs-lookup"><span data-stu-id="dc83f-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc83f-117">父元素</span><span class="sxs-lookup"><span data-stu-id="dc83f-117">Parent elements</span></span>

<span data-ttu-id="dc83f-118">[MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [MeetingCancellation](meetingcancellation.md)  | [ReminderMessageData](remindermessagedata.md)</span><span class="sxs-lookup"><span data-stu-id="dc83f-118">[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc83f-119">备注</span><span class="sxs-lookup"><span data-stu-id="dc83f-119">Remarks</span></span>

<span data-ttu-id="dc83f-120">从内部版本号15.00.0913.09 开始的 Exchange 版本可以将**AssociatedCalendarItemId**元素作为**ReminderMessageData**元素的子元素包括在内。</span><span class="sxs-lookup"><span data-stu-id="dc83f-120">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
<span data-ttu-id="dc83f-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dc83f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc83f-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="dc83f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc83f-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="dc83f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc83f-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="dc83f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="dc83f-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="dc83f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc83f-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="dc83f-126">Validation File</span></span>  <br/> |<span data-ttu-id="dc83f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc83f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc83f-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="dc83f-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc83f-129">False</span><span class="sxs-lookup"><span data-stu-id="dc83f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc83f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc83f-130">See also</span></span>

- [<span data-ttu-id="dc83f-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dc83f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

