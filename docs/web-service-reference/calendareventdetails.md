---
title: CalendarEventDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: CalendarEventDetails 元素提供有关日历事件的其他信息。
ms.openlocfilehash: 3e1dbba00bce4a1fdc53f3330527764c516890ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459067"
---
# <a name="calendareventdetails"></a><span data-ttu-id="50dd6-103">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="50dd6-103">CalendarEventDetails</span></span>

<span data-ttu-id="50dd6-104">**CalendarEventDetails**元素提供有关日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="50dd6-104">The **CalendarEventDetails** element provides additional information about a calendar event.</span></span> 
  
[<span data-ttu-id="50dd6-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="50dd6-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="50dd6-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="50dd6-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="50dd6-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="50dd6-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="50dd6-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="50dd6-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="50dd6-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="50dd6-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="50dd6-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="50dd6-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="50dd6-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="50dd6-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
```xml
<CalendarEventDetails>
   <ID/>
   <Subject/>
   <Location/>
   <IsMeeting/>
   <IsRecurring/>
   <IsException/>
   <IsReminderSet/>
   <IsPrivate/>
</CalendarEventDetails>
```

 <span data-ttu-id="50dd6-112">**CalendarEventDetails**</span><span class="sxs-lookup"><span data-stu-id="50dd6-112">**CalendarEventDetails**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50dd6-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="50dd6-113">Attributes and elements</span></span>

<span data-ttu-id="50dd6-114">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="50dd6-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50dd6-115">Attributes</span><span class="sxs-lookup"><span data-stu-id="50dd6-115">Attributes</span></span>

<span data-ttu-id="50dd6-116">无。</span><span class="sxs-lookup"><span data-stu-id="50dd6-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50dd6-117">子元素</span><span class="sxs-lookup"><span data-stu-id="50dd6-117">Child elements</span></span>

|<span data-ttu-id="50dd6-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="50dd6-118">**Element**</span></span>|<span data-ttu-id="50dd6-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="50dd6-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50dd6-120">ID</span><span class="sxs-lookup"><span data-stu-id="50dd6-120">ID</span></span>](id.md) <br/> |<span data-ttu-id="50dd6-121">代表日历项目的条目 ID。</span><span class="sxs-lookup"><span data-stu-id="50dd6-121">Represents the entry ID of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="50dd6-122">Subject （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="50dd6-122">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md) <br/> |<span data-ttu-id="50dd6-123">代表 "日历" 项目的主题。</span><span class="sxs-lookup"><span data-stu-id="50dd6-123">Represents the subject of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="50dd6-124">Location （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="50dd6-124">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md) <br/> |<span data-ttu-id="50dd6-125">代表 "日历" 项目的 "位置" 字段。</span><span class="sxs-lookup"><span data-stu-id="50dd6-125">Represents the location field of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="50dd6-126">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="50dd6-126">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md) <br/> |<span data-ttu-id="50dd6-127">指示日历事件是否为会议或约会。</span><span class="sxs-lookup"><span data-stu-id="50dd6-127">Indicates whether the calendar event is a meeting or an appointment.</span></span>  <br/> |
|[<span data-ttu-id="50dd6-128">IsRecurring （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="50dd6-128">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md) <br/> |<span data-ttu-id="50dd6-129">指示日历事件是定期日历项目的实例还是单个日历项目。</span><span class="sxs-lookup"><span data-stu-id="50dd6-129">Indicates whether the calendar event is an instance of a recurring calendar item or a single calendar item.</span></span>  <br/> |
|[<span data-ttu-id="50dd6-130">IsException</span><span class="sxs-lookup"><span data-stu-id="50dd6-130">IsException</span></span>](isexception.md) <br/> |<span data-ttu-id="50dd6-131">指示定期日历项目的实例是否已从主控形状更改。</span><span class="sxs-lookup"><span data-stu-id="50dd6-131">Indicates whether an instance of a recurring calendar item is changed from the master.</span></span>  <br/> |
|[<span data-ttu-id="50dd6-132">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="50dd6-132">IsReminderSet</span></span>](isreminderset.md) <br/> |<span data-ttu-id="50dd6-133">指示是否已为日历事件设置提醒。</span><span class="sxs-lookup"><span data-stu-id="50dd6-133">Indicates whether a reminder has been set for the calendar event.</span></span>  <br/> |
|[<span data-ttu-id="50dd6-134">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="50dd6-134">IsPrivate</span></span>](isprivate.md) <br/> |<span data-ttu-id="50dd6-135">指示日历项目是否为私有。</span><span class="sxs-lookup"><span data-stu-id="50dd6-135">Indicates whether the calendar item is private.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="50dd6-136">父元素</span><span class="sxs-lookup"><span data-stu-id="50dd6-136">Parent elements</span></span>

|<span data-ttu-id="50dd6-137">**元素**</span><span class="sxs-lookup"><span data-stu-id="50dd6-137">**Element**</span></span>|<span data-ttu-id="50dd6-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="50dd6-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50dd6-139">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="50dd6-139">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="50dd6-140">代表唯一的日历项目事件。</span><span class="sxs-lookup"><span data-stu-id="50dd6-140">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="50dd6-141">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="50dd6-141">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50dd6-142">备注</span><span class="sxs-lookup"><span data-stu-id="50dd6-142">Remarks</span></span>

<span data-ttu-id="50dd6-143">所有子元素都按它们出现的顺序列出。</span><span class="sxs-lookup"><span data-stu-id="50dd6-143">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="50dd6-144">如果[IsPrivate](isprivate.md)元素为**true**，则不会在响应中返回[CalendarEventDetails](calendareventdetails.md)元素中的所有其他元素。</span><span class="sxs-lookup"><span data-stu-id="50dd6-144">If the [IsPrivate](isprivate.md) element is **true**, all the other elements in the [CalendarEventDetails](calendareventdetails.md) element are not returned in the response.</span></span> 
  
<span data-ttu-id="50dd6-145">除非呼叫者拥有对目标用户日历的读取访问权限，否则 GetUserAvailability 操作不会返回详细的呼叫者信息。</span><span class="sxs-lookup"><span data-stu-id="50dd6-145">The GetUserAvailability operation does not return detailed caller information unless the caller has read access on the target user's calendar.</span></span> <span data-ttu-id="50dd6-146">您可以使用 Exchange 命令行管理程序设置访问权限。</span><span class="sxs-lookup"><span data-stu-id="50dd6-146">You can set access permissions by using the Exchange Management Shell.</span></span>
  
<span data-ttu-id="50dd6-147">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="50dd6-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50dd6-148">元素信息</span><span class="sxs-lookup"><span data-stu-id="50dd6-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50dd6-149">命名空间</span><span class="sxs-lookup"><span data-stu-id="50dd6-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50dd6-150">架构名称</span><span class="sxs-lookup"><span data-stu-id="50dd6-150">Schema Name</span></span>  <br/> |<span data-ttu-id="50dd6-151">类型架构</span><span class="sxs-lookup"><span data-stu-id="50dd6-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="50dd6-152">验证文件</span><span class="sxs-lookup"><span data-stu-id="50dd6-152">Validation File</span></span>  <br/> |<span data-ttu-id="50dd6-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="50dd6-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="50dd6-154">可以为空</span><span class="sxs-lookup"><span data-stu-id="50dd6-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="50dd6-155">False</span><span class="sxs-lookup"><span data-stu-id="50dd6-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50dd6-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="50dd6-156">See also</span></span>



[<span data-ttu-id="50dd6-157">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="50dd6-157">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="50dd6-158">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="50dd6-158">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="50dd6-159">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="50dd6-159">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

