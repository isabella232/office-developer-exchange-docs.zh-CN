---
title: GlobalIconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d28ed70-4cfe-46e4-8d15-593c6e355bcf
description: GlobalIconIndex 元素标识会话中所有项目的全局图标索引。
ms.openlocfilehash: 9900a80136a1a7eaae4634afd31568679f6dba1b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459459"
---
# <a name="globaliconindex"></a><span data-ttu-id="6a226-103">GlobalIconIndex</span><span class="sxs-lookup"><span data-stu-id="6a226-103">GlobalIconIndex</span></span>

<span data-ttu-id="6a226-104">**GlobalIconIndex**元素标识会话中所有项目的全局图标索引。</span><span class="sxs-lookup"><span data-stu-id="6a226-104">The **GlobalIconIndex** element identifies the global icon index for all items in a conversation.</span></span> 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MaillrmForwarded | MaillrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 <span data-ttu-id="6a226-105">**IconIndexType**</span><span class="sxs-lookup"><span data-stu-id="6a226-105">**IconIndexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a226-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6a226-106">Attributes and elements</span></span>

<span data-ttu-id="6a226-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6a226-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a226-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6a226-108">Attributes</span></span>

<span data-ttu-id="6a226-109">无。</span><span class="sxs-lookup"><span data-stu-id="6a226-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a226-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6a226-110">Child elements</span></span>

<span data-ttu-id="6a226-111">无。</span><span class="sxs-lookup"><span data-stu-id="6a226-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6a226-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6a226-112">Parent elements</span></span>

<span data-ttu-id="6a226-113">[对话（ConversationType）](conversation-conversationtype.md)  | [项](item.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)  | [邮件](message-ex15websvcsotherref.md)  | [CalendarItem](calendaritem.md)  | [PostItem](postitem.md)  | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="6a226-113">[Conversation (ConversationType)](conversation-conversationtype.md) | [Item](item.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Message](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="6a226-114">文本值</span><span class="sxs-lookup"><span data-stu-id="6a226-114">Text value</span></span>

<span data-ttu-id="6a226-115">下表包含**GlobalIconIndex**元素的可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="6a226-115">The following table contains the possible text values for the **GlobalIconIndex** element.</span></span> 
  
|<span data-ttu-id="6a226-116">**值**</span><span class="sxs-lookup"><span data-stu-id="6a226-116">**Value**</span></span>|<span data-ttu-id="6a226-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6a226-117">**Description**</span></span>|
|:-----|:-----|
|||
|<span data-ttu-id="6a226-118">默认</span><span class="sxs-lookup"><span data-stu-id="6a226-118">Default</span></span>  <br/> |<span data-ttu-id="6a226-119">指定默认图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-119">Specifies the default icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-120">PostItem</span><span class="sxs-lookup"><span data-stu-id="6a226-120">PostItem</span></span>  <br/> |<span data-ttu-id="6a226-121">指定公告项的图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-121">Specifies the icon for a post item.</span></span>  <br/> |
|<span data-ttu-id="6a226-122">MailRead</span><span class="sxs-lookup"><span data-stu-id="6a226-122">MailRead</span></span>  <br/> |<span data-ttu-id="6a226-123">指定邮件读取图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-123">Specifies the mail read icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-124">MailUnread</span><span class="sxs-lookup"><span data-stu-id="6a226-124">MailUnread</span></span>  <br/> |<span data-ttu-id="6a226-125">指定 "未读邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-125">Specifies the unread mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-126">MailReplied</span><span class="sxs-lookup"><span data-stu-id="6a226-126">MailReplied</span></span>  <br/> |<span data-ttu-id="6a226-127">指定 "答复邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-127">Specifies the replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-128">MailForwarded</span><span class="sxs-lookup"><span data-stu-id="6a226-128">MailForwarded</span></span>  <br/> |<span data-ttu-id="6a226-129">指定转发的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-129">Specifies the forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-130">MailEncrypted</span><span class="sxs-lookup"><span data-stu-id="6a226-130">MailEncrypted</span></span>  <br/> |<span data-ttu-id="6a226-131">指定加密的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-131">Specifies the encrypted mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-132">MailSmimeSigned</span><span class="sxs-lookup"><span data-stu-id="6a226-132">MailSmimeSigned</span></span>  <br/> |<span data-ttu-id="6a226-133">指定 "安全/多用途 Internet 邮件扩展（S/MIME）" "签名邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-133">Specifies the Secure/Multipurpose Internet Mail Extensions (S/MIME) signed mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-134">MailEncryptedReplied</span><span class="sxs-lookup"><span data-stu-id="6a226-134">MailEncryptedReplied</span></span>  <br/> |<span data-ttu-id="6a226-135">指定已加密答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-135">Specifies the encrypted replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-136">MailSmimeSignedReplied</span><span class="sxs-lookup"><span data-stu-id="6a226-136">MailSmimeSignedReplied</span></span>  <br/> |<span data-ttu-id="6a226-137">指定 S/MIME 签名答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-137">Specifies the S/MIME signed replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-138">MailEncryptedForwarded</span><span class="sxs-lookup"><span data-stu-id="6a226-138">MailEncryptedForwarded</span></span>  <br/> |<span data-ttu-id="6a226-139">指定加密的转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-139">Specifies the encrypted forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-140">MailSmimeSignedForwarded</span><span class="sxs-lookup"><span data-stu-id="6a226-140">MailSmimeSignedForwarded</span></span>  <br/> |<span data-ttu-id="6a226-141">指定 S/MIME 签名的已转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-141">Specifies the S/MIME signed forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-142">MailEncryptedRead</span><span class="sxs-lookup"><span data-stu-id="6a226-142">MailEncryptedRead</span></span>  <br/> |<span data-ttu-id="6a226-143">指定加密的 "已读邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-143">Specifies the encrypted read mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-144">MailSmimeSignedRead</span><span class="sxs-lookup"><span data-stu-id="6a226-144">MailSmimeSignedRead</span></span>  <br/> |<span data-ttu-id="6a226-145">指定 S/MIME 签名的阅读邮件图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-145">Specifies the S/MIME signed read mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-146">MailIrm</span><span class="sxs-lookup"><span data-stu-id="6a226-146">MailIrm</span></span>  <br/> |<span data-ttu-id="6a226-147">指定信息权限管理（IRM）保护的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-147">Specifies the Information Rights Management (IRM)-protected mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-148">MailIrmForwarded</span><span class="sxs-lookup"><span data-stu-id="6a226-148">MailIrmForwarded</span></span>  <br/> |<span data-ttu-id="6a226-149">指定受 IRM 保护的转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-149">Specifies the IRM-protected forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-150">MailIrmReplied</span><span class="sxs-lookup"><span data-stu-id="6a226-150">MailIrmReplied</span></span>  <br/> |<span data-ttu-id="6a226-151">指定受 IRM 保护的 "已答复邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-151">Specifies the IRM-protected replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-152">SmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="6a226-152">SmsSubmitted</span></span>  <br/> |<span data-ttu-id="6a226-153">指定用于短信服务（SMS）路由的邮件提交的图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-153">Specifies the icon for mail submitted for Short Message Service (SMS) routing.</span></span>  <br/> |
|<span data-ttu-id="6a226-154">SmsRoutedToDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="6a226-154">SmsRoutedToDeliveryPoint</span></span>  <br/> |<span data-ttu-id="6a226-155">指定用于将 SMS 路由到外部传递点的图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-155">Specifies the icon for SMS routing to an external delivery point.</span></span>  <br/> |
|<span data-ttu-id="6a226-156">SmsRoutedToExternalMessagingSystem</span><span class="sxs-lookup"><span data-stu-id="6a226-156">SmsRoutedToExternalMessagingSystem</span></span>  <br/> |<span data-ttu-id="6a226-157">指定用于将 SMS 路由到外部邮件系统的图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-157">Specifies the icon for SMS routing to an external messaging system.</span></span>  <br/> |
|<span data-ttu-id="6a226-158">SmsDelivered</span><span class="sxs-lookup"><span data-stu-id="6a226-158">SmsDelivered</span></span>  <br/> |<span data-ttu-id="6a226-159">指定 "发送短信邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-159">Specifies the SMS delivered mail icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-160">OutlookDefaultForContacts</span><span class="sxs-lookup"><span data-stu-id="6a226-160">OutlookDefaultForContacts</span></span>  <br/> |<span data-ttu-id="6a226-161">指定联系人的默认图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-161">Specifies the default icon for contacts.</span></span>  <br/> |
|<span data-ttu-id="6a226-162">AppointmentItem</span><span class="sxs-lookup"><span data-stu-id="6a226-162">AppointmentItem</span></span>  <br/> |<span data-ttu-id="6a226-163">指定约会项图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-163">Specifies the appointment item icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-164">AppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="6a226-164">AppointmentRecur</span></span>  <br/> |<span data-ttu-id="6a226-165">指定定期约会图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-165">Specifies the recurring appointment icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-166">AppointmentMeet</span><span class="sxs-lookup"><span data-stu-id="6a226-166">AppointmentMeet</span></span>  <br/> |<span data-ttu-id="6a226-167">指定会议图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-167">Specifies the meeting icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-168">AppointmentMeetRecur</span><span class="sxs-lookup"><span data-stu-id="6a226-168">AppointmentMeetRecur</span></span>  <br/> |<span data-ttu-id="6a226-169">指定定期会议图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-169">Specifies the recurring meeting icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-170">AppointmentMeetNY</span><span class="sxs-lookup"><span data-stu-id="6a226-170">AppointmentMeetNY</span></span>  <br/> |<span data-ttu-id="6a226-171">指定对会议的暂定响应的图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-171">Specifies the icon for a tentative response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="6a226-172">AppointmentMeetYes</span><span class="sxs-lookup"><span data-stu-id="6a226-172">AppointmentMeetYes</span></span>  <br/> |<span data-ttu-id="6a226-173">指定 "接受会议" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-173">Specifies the meeting acceptance icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-174">AppointmentMeetNo</span><span class="sxs-lookup"><span data-stu-id="6a226-174">AppointmentMeetNo</span></span>  <br/> |<span data-ttu-id="6a226-175">指定 "已拒绝会议" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-175">Specifies the meeting declined icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-176">AppointmentMeetMaybe</span><span class="sxs-lookup"><span data-stu-id="6a226-176">AppointmentMeetMaybe</span></span>  <br/> |<span data-ttu-id="6a226-177">指定可能响应会议的图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-177">Specifies the icon for a maybe response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="6a226-178">AppointmentMeetCancel</span><span class="sxs-lookup"><span data-stu-id="6a226-178">AppointmentMeetCancel</span></span>  <br/> |<span data-ttu-id="6a226-179">指定会议取消图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-179">Specifies the meeting cancel icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-180">AppointmentMeetInfo</span><span class="sxs-lookup"><span data-stu-id="6a226-180">AppointmentMeetInfo</span></span>  <br/> |<span data-ttu-id="6a226-181">指定 "会议信息" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-181">Specifies the meeting information icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-182">TaskItem</span><span class="sxs-lookup"><span data-stu-id="6a226-182">TaskItem</span></span>  <br/> |<span data-ttu-id="6a226-183">指定任务项图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-183">Specifies the task item icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-184">TaskRecur</span><span class="sxs-lookup"><span data-stu-id="6a226-184">TaskRecur</span></span>  <br/> |<span data-ttu-id="6a226-185">指定定期任务图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-185">Specifies the recurring task icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-186">TaskOwned</span><span class="sxs-lookup"><span data-stu-id="6a226-186">TaskOwned</span></span>  <br/> |<span data-ttu-id="6a226-187">指定任务拥有的图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-187">Specifies the task owned icon.</span></span>  <br/> |
|<span data-ttu-id="6a226-188">TaskDelegated</span><span class="sxs-lookup"><span data-stu-id="6a226-188">TaskDelegated</span></span>  <br/> |<span data-ttu-id="6a226-189">指定 "任务委派" 图标。</span><span class="sxs-lookup"><span data-stu-id="6a226-189">Specifies the task delegated icon.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a226-190">备注</span><span class="sxs-lookup"><span data-stu-id="6a226-190">Remarks</span></span>

<span data-ttu-id="6a226-191">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6a226-191">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6a226-192">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6a226-192">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a226-193">元素信息</span><span class="sxs-lookup"><span data-stu-id="6a226-193">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a226-194">命名空间</span><span class="sxs-lookup"><span data-stu-id="6a226-194">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6a226-195">架构名称</span><span class="sxs-lookup"><span data-stu-id="6a226-195">Schema name</span></span>  <br/> |<span data-ttu-id="6a226-196">类型架构</span><span class="sxs-lookup"><span data-stu-id="6a226-196">Types schema</span></span>  <br/> |
|<span data-ttu-id="6a226-197">验证文件</span><span class="sxs-lookup"><span data-stu-id="6a226-197">Validation file</span></span>  <br/> |<span data-ttu-id="6a226-198">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6a226-198">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6a226-199">可以为空</span><span class="sxs-lookup"><span data-stu-id="6a226-199">Can be empty</span></span>  <br/> |<span data-ttu-id="6a226-200">false</span><span class="sxs-lookup"><span data-stu-id="6a226-200">false</span></span>  <br/> |
   

