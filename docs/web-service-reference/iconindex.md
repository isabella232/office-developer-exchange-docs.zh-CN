---
title: IconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92020822-2a86-4dfc-aee1-3067af4d4edf
description: IconIndex 元素标识项目或对话的图标索引。
ms.openlocfilehash: 0f932f5632422a8786e74500bf83cb1337f780c3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460783"
---
# <a name="iconindex"></a><span data-ttu-id="cfadc-103">IconIndex</span><span class="sxs-lookup"><span data-stu-id="cfadc-103">IconIndex</span></span>

<span data-ttu-id="cfadc-104">**IconIndex**元素标识项目或对话的图标索引。</span><span class="sxs-lookup"><span data-stu-id="cfadc-104">The **IconIndex** element identifies the icon index for an item or conversation.</span></span> 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MailIrmForwarded | MailIrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 <span data-ttu-id="cfadc-105">**IconIndexType**</span><span class="sxs-lookup"><span data-stu-id="cfadc-105">**IconIndexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cfadc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cfadc-106">Attributes and elements</span></span>

<span data-ttu-id="cfadc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cfadc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cfadc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cfadc-108">Attributes</span></span>

<span data-ttu-id="cfadc-109">无。</span><span class="sxs-lookup"><span data-stu-id="cfadc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cfadc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cfadc-110">Child elements</span></span>

<span data-ttu-id="cfadc-111">无。</span><span class="sxs-lookup"><span data-stu-id="cfadc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cfadc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cfadc-112">Parent elements</span></span>

<span data-ttu-id="cfadc-113">[对话（ConversationType）](conversation-conversationtype.md)  | [项](item.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)  | [邮件](message-ex15websvcsotherref.md)  | [CalendarItem](calendaritem.md)  | [PostItem](postitem.md)  | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="cfadc-113">[Conversation (ConversationType)](conversation-conversationtype.md) | [Item](item.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Message](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cfadc-114">文本值</span><span class="sxs-lookup"><span data-stu-id="cfadc-114">Text value</span></span>

<span data-ttu-id="cfadc-115">下表包含**IconIndex**元素的可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="cfadc-115">The following table contains the possible text values for the **IconIndex** element.</span></span> 
  
|<span data-ttu-id="cfadc-116">**值**</span><span class="sxs-lookup"><span data-stu-id="cfadc-116">**Value**</span></span>|<span data-ttu-id="cfadc-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="cfadc-117">**Description**</span></span>|
|:-----|:-----|
|||
|<span data-ttu-id="cfadc-118">默认</span><span class="sxs-lookup"><span data-stu-id="cfadc-118">Default</span></span>  <br/> |<span data-ttu-id="cfadc-119">指定默认图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-119">Specifies the default icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-120">PostItem</span><span class="sxs-lookup"><span data-stu-id="cfadc-120">PostItem</span></span>  <br/> |<span data-ttu-id="cfadc-121">指定公告项的图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-121">Specifies the icon for a post item.</span></span>  <br/> |
|<span data-ttu-id="cfadc-122">MailRead</span><span class="sxs-lookup"><span data-stu-id="cfadc-122">MailRead</span></span>  <br/> |<span data-ttu-id="cfadc-123">指定邮件读取图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-123">Specifies the mail read icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-124">MailUnread</span><span class="sxs-lookup"><span data-stu-id="cfadc-124">MailUnread</span></span>  <br/> |<span data-ttu-id="cfadc-125">指定 "未读邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-125">Specifies the unread mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-126">MailReplied</span><span class="sxs-lookup"><span data-stu-id="cfadc-126">MailReplied</span></span>  <br/> |<span data-ttu-id="cfadc-127">指定 "答复邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-127">Specifies the replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-128">MailForwarded</span><span class="sxs-lookup"><span data-stu-id="cfadc-128">MailForwarded</span></span>  <br/> |<span data-ttu-id="cfadc-129">指定转发的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-129">Specifies the forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-130">MailEncrypted</span><span class="sxs-lookup"><span data-stu-id="cfadc-130">MailEncrypted</span></span>  <br/> |<span data-ttu-id="cfadc-131">指定加密的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-131">Specifies the encrypted mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-132">MailSmimeSigned</span><span class="sxs-lookup"><span data-stu-id="cfadc-132">MailSmimeSigned</span></span>  <br/> |<span data-ttu-id="cfadc-133">指定 "安全/多用途 Internet 邮件扩展（S/MIME）" "签名邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-133">Specifies the Secure/Multipurpose Internet Mail Extensions (S/MIME) signed mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-134">MailEncryptedReplied</span><span class="sxs-lookup"><span data-stu-id="cfadc-134">MailEncryptedReplied</span></span>  <br/> |<span data-ttu-id="cfadc-135">指定已加密答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-135">Specifies the encrypted replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-136">MailSmimeSignedReplied</span><span class="sxs-lookup"><span data-stu-id="cfadc-136">MailSmimeSignedReplied</span></span>  <br/> |<span data-ttu-id="cfadc-137">指定 S/MIME 签名答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-137">Specifies the S/MIME signed replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-138">MailEncryptedForwarded</span><span class="sxs-lookup"><span data-stu-id="cfadc-138">MailEncryptedForwarded</span></span>  <br/> |<span data-ttu-id="cfadc-139">指定加密的转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-139">Specifies the encrypted forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-140">MailSmimeSignedForwarded</span><span class="sxs-lookup"><span data-stu-id="cfadc-140">MailSmimeSignedForwarded</span></span>  <br/> |<span data-ttu-id="cfadc-141">指定 S/MIME 签名的已转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-141">Specifies the S/MIME signed forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-142">MailEncryptedRead</span><span class="sxs-lookup"><span data-stu-id="cfadc-142">MailEncryptedRead</span></span>  <br/> |<span data-ttu-id="cfadc-143">指定加密的 "已读邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-143">Specifies the encrypted read mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-144">MailSmimeSignedRead</span><span class="sxs-lookup"><span data-stu-id="cfadc-144">MailSmimeSignedRead</span></span>  <br/> |<span data-ttu-id="cfadc-145">指定 S/MIME 签名的阅读邮件图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-145">Specifies the S/MIME signed read mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-146">MailIrm</span><span class="sxs-lookup"><span data-stu-id="cfadc-146">MailIrm</span></span>  <br/> |<span data-ttu-id="cfadc-147">指定信息权限管理（IRM）保护的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-147">Specifies the Information Rights Management (IRM)-protected mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-148">MailIrmForwarded</span><span class="sxs-lookup"><span data-stu-id="cfadc-148">MailIrmForwarded</span></span>  <br/> |<span data-ttu-id="cfadc-149">指定受 IRM 保护的转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-149">Specifies the IRM-protected forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-150">MailIrmReplied</span><span class="sxs-lookup"><span data-stu-id="cfadc-150">MailIrmReplied</span></span>  <br/> |<span data-ttu-id="cfadc-151">指定受 IRM 保护的 "已答复邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-151">Specifies the IRM-protected replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-152">SmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="cfadc-152">SmsSubmitted</span></span>  <br/> |<span data-ttu-id="cfadc-153">指定为短信服务（SMS）路由提交的图标邮件。</span><span class="sxs-lookup"><span data-stu-id="cfadc-153">Specifies the icon mail submitted for Short Message Service (SMS) routing.</span></span>  <br/> |
|<span data-ttu-id="cfadc-154">SmsRoutedToDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="cfadc-154">SmsRoutedToDeliveryPoint</span></span>  <br/> |<span data-ttu-id="cfadc-155">指定用于将 SMS 路由到外部传递点的图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-155">Specifies the icon for SMS routing to an external delivery point.</span></span>  <br/> |
|<span data-ttu-id="cfadc-156">SmsRoutedToExternalMessagingSystem</span><span class="sxs-lookup"><span data-stu-id="cfadc-156">SmsRoutedToExternalMessagingSystem</span></span>  <br/> |<span data-ttu-id="cfadc-157">指定用于将 SMS 路由到外部邮件系统的图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-157">Specifies the icon for SMS routing to an external messaging system.</span></span>  <br/> |
|<span data-ttu-id="cfadc-158">SmsDelivered</span><span class="sxs-lookup"><span data-stu-id="cfadc-158">SmsDelivered</span></span>  <br/> |<span data-ttu-id="cfadc-159">指定 "发送短信邮件" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-159">Specifies the SMS delivered mail icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-160">OutlookDefaultForContacts</span><span class="sxs-lookup"><span data-stu-id="cfadc-160">OutlookDefaultForContacts</span></span>  <br/> |<span data-ttu-id="cfadc-161">指定联系人的默认图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-161">Specifies the default icon for contacts.</span></span>  <br/> |
|<span data-ttu-id="cfadc-162">AppointmentItem</span><span class="sxs-lookup"><span data-stu-id="cfadc-162">AppointmentItem</span></span>  <br/> |<span data-ttu-id="cfadc-163">指定约会项图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-163">Specifies the appointment item icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-164">AppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="cfadc-164">AppointmentRecur</span></span>  <br/> |<span data-ttu-id="cfadc-165">指定定期约会图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-165">Specifies the recurring appointment icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-166">AppointmentMeet</span><span class="sxs-lookup"><span data-stu-id="cfadc-166">AppointmentMeet</span></span>  <br/> |<span data-ttu-id="cfadc-167">指定会议图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-167">Specifies the meeting icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-168">AppointmentMeetRecur</span><span class="sxs-lookup"><span data-stu-id="cfadc-168">AppointmentMeetRecur</span></span>  <br/> |<span data-ttu-id="cfadc-169">指定定期会议图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-169">Specifies the recurring meeting icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-170">AppointmentMeetNY</span><span class="sxs-lookup"><span data-stu-id="cfadc-170">AppointmentMeetNY</span></span>  <br/> |<span data-ttu-id="cfadc-171">指定对会议的暂定响应的图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-171">Specifies the icon for a tentative response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="cfadc-172">AppointmentMeetYes</span><span class="sxs-lookup"><span data-stu-id="cfadc-172">AppointmentMeetYes</span></span>  <br/> |<span data-ttu-id="cfadc-173">指定 "接受会议" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-173">Specifies the meeting acceptance icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-174">AppointmentMeetNo</span><span class="sxs-lookup"><span data-stu-id="cfadc-174">AppointmentMeetNo</span></span>  <br/> |<span data-ttu-id="cfadc-175">指定 "已拒绝会议" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-175">Specifies the meeting declined icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-176">AppointmentMeetMaybe</span><span class="sxs-lookup"><span data-stu-id="cfadc-176">AppointmentMeetMaybe</span></span>  <br/> |<span data-ttu-id="cfadc-177">指定可能响应会议的图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-177">Specifies the icon for a maybe response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="cfadc-178">AppointmentMeetCancel</span><span class="sxs-lookup"><span data-stu-id="cfadc-178">AppointmentMeetCancel</span></span>  <br/> |<span data-ttu-id="cfadc-179">指定会议取消图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-179">Specifies the meeting cancel icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-180">AppointmentMeetInfo</span><span class="sxs-lookup"><span data-stu-id="cfadc-180">AppointmentMeetInfo</span></span>  <br/> |<span data-ttu-id="cfadc-181">指定 "会议信息" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-181">Specifies the meeting information icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-182">TaskItem</span><span class="sxs-lookup"><span data-stu-id="cfadc-182">TaskItem</span></span>  <br/> |<span data-ttu-id="cfadc-183">指定任务项图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-183">Specifies the task item icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-184">TaskRecur</span><span class="sxs-lookup"><span data-stu-id="cfadc-184">TaskRecur</span></span>  <br/> |<span data-ttu-id="cfadc-185">指定定期任务图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-185">Specifies the recurring task icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-186">TaskOwned</span><span class="sxs-lookup"><span data-stu-id="cfadc-186">TaskOwned</span></span>  <br/> |<span data-ttu-id="cfadc-187">指定任务拥有的图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-187">Specifies the task owned icon.</span></span>  <br/> |
|<span data-ttu-id="cfadc-188">TaskDelegated</span><span class="sxs-lookup"><span data-stu-id="cfadc-188">TaskDelegated</span></span>  <br/> |<span data-ttu-id="cfadc-189">指定 "任务委派" 图标。</span><span class="sxs-lookup"><span data-stu-id="cfadc-189">Specifies the task delegated icon.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfadc-190">备注</span><span class="sxs-lookup"><span data-stu-id="cfadc-190">Remarks</span></span>

<span data-ttu-id="cfadc-191">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cfadc-191">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cfadc-192">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cfadc-192">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cfadc-193">元素信息</span><span class="sxs-lookup"><span data-stu-id="cfadc-193">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfadc-194">命名空间</span><span class="sxs-lookup"><span data-stu-id="cfadc-194">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cfadc-195">架构名称</span><span class="sxs-lookup"><span data-stu-id="cfadc-195">Schema name</span></span>  <br/> |<span data-ttu-id="cfadc-196">类型架构</span><span class="sxs-lookup"><span data-stu-id="cfadc-196">Types schema</span></span>  <br/> |
|<span data-ttu-id="cfadc-197">验证文件</span><span class="sxs-lookup"><span data-stu-id="cfadc-197">Validation file</span></span>  <br/> |<span data-ttu-id="cfadc-198">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cfadc-198">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cfadc-199">可以为空</span><span class="sxs-lookup"><span data-stu-id="cfadc-199">Can be empty</span></span>  <br/> |<span data-ttu-id="cfadc-200">false</span><span class="sxs-lookup"><span data-stu-id="cfadc-200">false</span></span>  <br/> |
   

