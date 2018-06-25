---
title: AttendeeType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: AttendeeType 元素表示与会者的电子邮件 (EmailAddressType) 元素中标识的类型。 此元素是请求中使用的会议建议。
ms.openlocfilehash: a08532ed78296102ee252c1e0c40beee7ca8ea5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753288"
---
# <a name="attendeetype"></a><span data-ttu-id="3f542-104">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="3f542-104">AttendeeType</span></span>

<span data-ttu-id="3f542-105">**AttendeeType**元素表示与会者的[电子邮件 (EmailAddressType)](email-emailaddresstype.md)元素中标识的类型。</span><span class="sxs-lookup"><span data-stu-id="3f542-105">The **AttendeeType** element represents the type of attendee that is identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="3f542-106">此元素是请求中使用的会议建议。</span><span class="sxs-lookup"><span data-stu-id="3f542-106">This element is used in requests for meeting suggestions.</span></span> 
  
- [<span data-ttu-id="3f542-107">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="3f542-107">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="3f542-108">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="3f542-108">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="3f542-109">MailboxData</span><span class="sxs-lookup"><span data-stu-id="3f542-109">MailboxData</span></span>](mailboxdata.md)
  
- [<span data-ttu-id="3f542-110">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="3f542-110">AttendeeType</span></span>](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 <span data-ttu-id="3f542-111">**MeetingAttendeeType**</span><span class="sxs-lookup"><span data-stu-id="3f542-111">**MeetingAttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f542-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3f542-112">Attributes and elements</span></span>

<span data-ttu-id="3f542-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3f542-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f542-114">属性</span><span class="sxs-lookup"><span data-stu-id="3f542-114">Attributes</span></span>

<span data-ttu-id="3f542-115">无。</span><span class="sxs-lookup"><span data-stu-id="3f542-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f542-116">子元素</span><span class="sxs-lookup"><span data-stu-id="3f542-116">Child elements</span></span>

<span data-ttu-id="3f542-117">无。</span><span class="sxs-lookup"><span data-stu-id="3f542-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3f542-118">父元素</span><span class="sxs-lookup"><span data-stu-id="3f542-118">Parent elements</span></span>

|<span data-ttu-id="3f542-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="3f542-119">**Element**</span></span>|<span data-ttu-id="3f542-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="3f542-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f542-121">MailboxData</span><span class="sxs-lookup"><span data-stu-id="3f542-121">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="3f542-122">代表单个邮箱用户和类型的数据的选项，将返回有关邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="3f542-122">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="3f542-123">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="3f542-123">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3f542-124">文本值</span><span class="sxs-lookup"><span data-stu-id="3f542-124">Text value</span></span>

<span data-ttu-id="3f542-125">需要为此元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="3f542-125">A text value is required for this element.</span></span> <span data-ttu-id="3f542-126">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="3f542-126">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="3f542-127">**值**</span><span class="sxs-lookup"><span data-stu-id="3f542-127">**Value**</span></span>|<span data-ttu-id="3f542-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="3f542-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f542-129">组织者</span><span class="sxs-lookup"><span data-stu-id="3f542-129">Organizer</span></span>  <br/> |<span data-ttu-id="3f542-130">邮箱用户和创建的日历项目的与会者。</span><span class="sxs-lookup"><span data-stu-id="3f542-130">The mailbox user and attendee who created the calendar item.</span></span>  <br/> |
|<span data-ttu-id="3f542-131">必需</span><span class="sxs-lookup"><span data-stu-id="3f542-131">Required</span></span>  <br/> |<span data-ttu-id="3f542-132">作为会议必需的与会者的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="3f542-132">A mailbox user who is a required attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="3f542-133">可选</span><span class="sxs-lookup"><span data-stu-id="3f542-133">Optional</span></span>  <br/> |<span data-ttu-id="3f542-134">作为会议可选与会者的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="3f542-134">A mailbox user who is an optional attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="3f542-135">聊天室</span><span class="sxs-lookup"><span data-stu-id="3f542-135">Room</span></span>  <br/> |<span data-ttu-id="3f542-136">表示用于会议的会议室资源邮箱实体。</span><span class="sxs-lookup"><span data-stu-id="3f542-136">A mailbox entity that represents a room resource used for the meeting.</span></span>  <br/> |
|<span data-ttu-id="3f542-137">资源</span><span class="sxs-lookup"><span data-stu-id="3f542-137">Resource</span></span>  <br/> |<span data-ttu-id="3f542-138">如 TV 或计划在会议中使用的投影仪资源。</span><span class="sxs-lookup"><span data-stu-id="3f542-138">A resource such as a TV or projector that is scheduled for use in the meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f542-139">注解</span><span class="sxs-lookup"><span data-stu-id="3f542-139">Remarks</span></span>

<span data-ttu-id="3f542-140">此元素是[MailboxData](mailboxdata.md)元素的必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="3f542-140">This element is a required child element of the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="3f542-141">此元素[MailboxData](mailboxdata.md)元素中只能出现一次。</span><span class="sxs-lookup"><span data-stu-id="3f542-141">This element can only occur once in the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="3f542-142">描述此元素的架构位于运行 MicrosoftExchange Server 2007 的安装了客户端访问服务器角色的计算机的 /EWS/ 目录中。</span><span class="sxs-lookup"><span data-stu-id="3f542-142">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3f542-143">AttendeeType 架构类型用于表示与会者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="3f542-143">The AttendeeType schema type is used to represent attendees to a calendar item.</span></span> <span data-ttu-id="3f542-144">请勿将此元素包含 AttendeeType 架构类型元素的混淆。</span><span class="sxs-lookup"><span data-stu-id="3f542-144">Do not confuse this element with elements of the AttendeeType schema type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3f542-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="3f542-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f542-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="3f542-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3f542-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="3f542-147">Schema Name</span></span>  <br/> |<span data-ttu-id="3f542-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="3f542-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="3f542-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="3f542-149">Validation File</span></span>  <br/> |<span data-ttu-id="3f542-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3f542-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3f542-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="3f542-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="3f542-152">False</span><span class="sxs-lookup"><span data-stu-id="3f542-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f542-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3f542-153">See also</span></span>

- [<span data-ttu-id="3f542-154">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="3f542-154">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="3f542-155">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="3f542-155">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="3f542-156">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="3f542-156">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

