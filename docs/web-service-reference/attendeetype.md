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
description: AttendeeType 元素表示在 Email （EmailAddressType）元素中标识的与会者的类型。 此元素用于会议建议的请求中。
ms.openlocfilehash: 104b9f38cc891310ecb47c0b47837a912ced6ab7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462295"
---
# <a name="attendeetype"></a><span data-ttu-id="a090d-104">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="a090d-104">AttendeeType</span></span>

<span data-ttu-id="a090d-105">**AttendeeType**元素表示在[Email （EmailAddressType）](email-emailaddresstype.md)元素中标识的与会者的类型。</span><span class="sxs-lookup"><span data-stu-id="a090d-105">The **AttendeeType** element represents the type of attendee that is identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="a090d-106">此元素用于会议建议的请求中。</span><span class="sxs-lookup"><span data-stu-id="a090d-106">This element is used in requests for meeting suggestions.</span></span> 
  
- [<span data-ttu-id="a090d-107">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="a090d-107">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="a090d-108">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="a090d-108">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="a090d-109">MailboxData</span><span class="sxs-lookup"><span data-stu-id="a090d-109">MailboxData</span></span>](mailboxdata.md)
  
- [<span data-ttu-id="a090d-110">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="a090d-110">AttendeeType</span></span>](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 <span data-ttu-id="a090d-111">**MeetingAttendeeType**</span><span class="sxs-lookup"><span data-stu-id="a090d-111">**MeetingAttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a090d-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a090d-112">Attributes and elements</span></span>

<span data-ttu-id="a090d-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a090d-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a090d-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="a090d-114">Attributes</span></span>

<span data-ttu-id="a090d-115">无。</span><span class="sxs-lookup"><span data-stu-id="a090d-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a090d-116">子元素</span><span class="sxs-lookup"><span data-stu-id="a090d-116">Child elements</span></span>

<span data-ttu-id="a090d-117">无。</span><span class="sxs-lookup"><span data-stu-id="a090d-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a090d-118">父元素</span><span class="sxs-lookup"><span data-stu-id="a090d-118">Parent elements</span></span>

|<span data-ttu-id="a090d-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="a090d-119">**Element**</span></span>|<span data-ttu-id="a090d-120">**描述**</span><span class="sxs-lookup"><span data-stu-id="a090d-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a090d-121">MailboxData</span><span class="sxs-lookup"><span data-stu-id="a090d-121">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="a090d-122">代表单个邮箱用户以及有关邮箱用户要返回的数据类型的选项。</span><span class="sxs-lookup"><span data-stu-id="a090d-122">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="a090d-123">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="a090d-123">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a090d-124">文本值</span><span class="sxs-lookup"><span data-stu-id="a090d-124">Text value</span></span>

<span data-ttu-id="a090d-125">此元素需要一个文本值。</span><span class="sxs-lookup"><span data-stu-id="a090d-125">A text value is required for this element.</span></span> <span data-ttu-id="a090d-126">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="a090d-126">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="a090d-127">**值**</span><span class="sxs-lookup"><span data-stu-id="a090d-127">**Value**</span></span>|<span data-ttu-id="a090d-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="a090d-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a090d-129">Organizer</span><span class="sxs-lookup"><span data-stu-id="a090d-129">Organizer</span></span>  <br/> |<span data-ttu-id="a090d-130">创建日历项目的邮箱用户和与会者。</span><span class="sxs-lookup"><span data-stu-id="a090d-130">The mailbox user and attendee who created the calendar item.</span></span>  <br/> |
|<span data-ttu-id="a090d-131">必需</span><span class="sxs-lookup"><span data-stu-id="a090d-131">Required</span></span>  <br/> |<span data-ttu-id="a090d-132">会议所必需的与会者的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="a090d-132">A mailbox user who is a required attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="a090d-133">可选</span><span class="sxs-lookup"><span data-stu-id="a090d-133">Optional</span></span>  <br/> |<span data-ttu-id="a090d-134">作为会议的可选与会者的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="a090d-134">A mailbox user who is an optional attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="a090d-135">房间</span><span class="sxs-lookup"><span data-stu-id="a090d-135">Room</span></span>  <br/> |<span data-ttu-id="a090d-136">表示用于会议的会议室资源的邮箱实体。</span><span class="sxs-lookup"><span data-stu-id="a090d-136">A mailbox entity that represents a room resource used for the meeting.</span></span>  <br/> |
|<span data-ttu-id="a090d-137">Resource</span><span class="sxs-lookup"><span data-stu-id="a090d-137">Resource</span></span>  <br/> |<span data-ttu-id="a090d-138">安排在会议中使用的一种资源，如电视或投影仪。</span><span class="sxs-lookup"><span data-stu-id="a090d-138">A resource such as a TV or projector that is scheduled for use in the meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a090d-139">备注</span><span class="sxs-lookup"><span data-stu-id="a090d-139">Remarks</span></span>

<span data-ttu-id="a090d-140">此元素是[MailboxData](mailboxdata.md)元素的必需子元素。</span><span class="sxs-lookup"><span data-stu-id="a090d-140">This element is a required child element of the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="a090d-141">此元素只能在[MailboxData](mailboxdata.md)元素中出现一次。</span><span class="sxs-lookup"><span data-stu-id="a090d-141">This element can only occur once in the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="a090d-142">描述此元素的架构位于运行 MicrosoftExchange Server 2007 且安装了客户端访问服务器角色的计算机的/EWS/目录中。</span><span class="sxs-lookup"><span data-stu-id="a090d-142">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a090d-143">AttendeeType 架构类型用于表示与会者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="a090d-143">The AttendeeType schema type is used to represent attendees to a calendar item.</span></span> <span data-ttu-id="a090d-144">请勿将此元素与 AttendeeType 架构类型的元素混淆。</span><span class="sxs-lookup"><span data-stu-id="a090d-144">Do not confuse this element with elements of the AttendeeType schema type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a090d-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="a090d-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a090d-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="a090d-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a090d-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="a090d-147">Schema Name</span></span>  <br/> |<span data-ttu-id="a090d-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="a090d-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="a090d-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="a090d-149">Validation File</span></span>  <br/> |<span data-ttu-id="a090d-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a090d-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a090d-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="a090d-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="a090d-152">False</span><span class="sxs-lookup"><span data-stu-id="a090d-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a090d-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a090d-153">See also</span></span>

- [<span data-ttu-id="a090d-154">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="a090d-154">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="a090d-155">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="a090d-155">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="a090d-156">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="a090d-156">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

