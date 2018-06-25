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
description: AssociatedCalendarItemId 元素均表示与 MeetingMessage、 MeetingRequest、 MeetingResponse、 MeetingCancellation 或 ReminderMessageData 相关联的日历项目。
ms.openlocfilehash: 4445da88d6fec42c1e02cd8de4d2e423485a4472
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753274"
---
# <a name="associatedcalendaritemid"></a><span data-ttu-id="8ffc4-103">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="8ffc4-103">AssociatedCalendarItemId</span></span>

<span data-ttu-id="8ffc4-104">**AssociatedCalendarItemId**元素均表示与[MeetingMessage](meetingmessage.md)、 [MeetingRequest](meetingrequest.md)、 [MeetingResponse](meetingresponse.md)、 [MeetingCancellation](meetingcancellation.md)或[ReminderMessageData](remindermessagedata.md)相关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="8ffc4-104">The **AssociatedCalendarItemId** element represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md), or [ReminderMessageData](remindermessagedata.md).</span></span>
  
```XML
<AssociatedCalendarItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="8ffc4-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="8ffc4-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ffc4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8ffc4-106">Attributes and elements</span></span>

<span data-ttu-id="8ffc4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8ffc4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ffc4-108">属性</span><span class="sxs-lookup"><span data-stu-id="8ffc4-108">Attributes</span></span>

|<span data-ttu-id="8ffc4-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="8ffc4-109">**Attribute**</span></span>|<span data-ttu-id="8ffc4-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="8ffc4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ffc4-111">
  **Id**</span><span class="sxs-lookup"><span data-stu-id="8ffc4-111">**Id**</span></span> <br/> |<span data-ttu-id="8ffc4-112">标识与会议相关联的日历项。</span><span class="sxs-lookup"><span data-stu-id="8ffc4-112">Identifies the calendar item that is associated with meeting.</span></span>  <br/> |
|<span data-ttu-id="8ffc4-113">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="8ffc4-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="8ffc4-114">标识与会议相关联的日历项目的特定版本。</span><span class="sxs-lookup"><span data-stu-id="8ffc4-114">Identifies a specific version of the calendar item that is associated with a meeting.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8ffc4-115">子元素</span><span class="sxs-lookup"><span data-stu-id="8ffc4-115">Child elements</span></span>

<span data-ttu-id="8ffc4-116">无。</span><span class="sxs-lookup"><span data-stu-id="8ffc4-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8ffc4-117">父元素</span><span class="sxs-lookup"><span data-stu-id="8ffc4-117">Parent elements</span></span>

<span data-ttu-id="8ffc4-118">[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)</span><span class="sxs-lookup"><span data-stu-id="8ffc4-118">[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ffc4-119">注解</span><span class="sxs-lookup"><span data-stu-id="8ffc4-119">Remarks</span></span>

<span data-ttu-id="8ffc4-120">内部版本号 15.00.0913.09 开头的 Exchange 版本可作为**ReminderMessageData**元素的子元素包括**AssociatedCalendarItemId**元素。</span><span class="sxs-lookup"><span data-stu-id="8ffc4-120">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
<span data-ttu-id="8ffc4-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8ffc4-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ffc4-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="8ffc4-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ffc4-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="8ffc4-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8ffc4-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="8ffc4-124">Schema Name</span></span>  <br/> |<span data-ttu-id="8ffc4-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="8ffc4-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="8ffc4-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="8ffc4-126">Validation File</span></span>  <br/> |<span data-ttu-id="8ffc4-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8ffc4-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8ffc4-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="8ffc4-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="8ffc4-129">False</span><span class="sxs-lookup"><span data-stu-id="8ffc4-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ffc4-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8ffc4-130">See also</span></span>

- [<span data-ttu-id="8ffc4-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8ffc4-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

