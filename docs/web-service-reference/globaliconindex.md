---
title: GlobalIconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d28ed70-4cfe-46e4-8d15-593c6e355bcf
description: GlobalIconIndex 元素标识会话中的所有项目的全局图标索引。
ms.openlocfilehash: e8d78bfcfc0e57df9230db86e080d1ee29878094
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825727"
---
# <a name="globaliconindex"></a><span data-ttu-id="1316c-103">GlobalIconIndex</span><span class="sxs-lookup"><span data-stu-id="1316c-103">GlobalIconIndex</span></span>

<span data-ttu-id="1316c-104">**GlobalIconIndex**元素标识会话中的所有项目的全局图标索引。</span><span class="sxs-lookup"><span data-stu-id="1316c-104">The **GlobalIconIndex** element identifies the global icon index for all items in a conversation.</span></span> 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MaillrmForwarded | MaillrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 <span data-ttu-id="1316c-105">**IconIndexType**</span><span class="sxs-lookup"><span data-stu-id="1316c-105">**IconIndexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1316c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1316c-106">Attributes and elements</span></span>

<span data-ttu-id="1316c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1316c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1316c-108">属性</span><span class="sxs-lookup"><span data-stu-id="1316c-108">Attributes</span></span>

<span data-ttu-id="1316c-109">无。</span><span class="sxs-lookup"><span data-stu-id="1316c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1316c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1316c-110">Child elements</span></span>

<span data-ttu-id="1316c-111">无。</span><span class="sxs-lookup"><span data-stu-id="1316c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1316c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1316c-112">Parent elements</span></span>

<span data-ttu-id="1316c-113">[对话 (ConversationType)](conversation-conversationtype.md) | [项](item.md) | [联系人](contact.md) | [DistributionList](distributionlist.md) | [消息](message-ex15websvcsotherref.md) | [日历项目](calendaritem.md) | [PostItem](postitem.md) | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="1316c-113">[Conversation (ConversationType)](conversation-conversationtype.md) | [Item](item.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Message](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="1316c-114">文本值</span><span class="sxs-lookup"><span data-stu-id="1316c-114">Text value</span></span>

<span data-ttu-id="1316c-115">下表包含**GlobalIconIndex**元素的可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="1316c-115">The following table contains the possible text values for the **GlobalIconIndex** element.</span></span> 
  
|<span data-ttu-id="1316c-116">**值**</span><span class="sxs-lookup"><span data-stu-id="1316c-116">**Value**</span></span>|<span data-ttu-id="1316c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="1316c-117">**Description**</span></span>|
|:-----|:-----|
|||
|<span data-ttu-id="1316c-118">默认</span><span class="sxs-lookup"><span data-stu-id="1316c-118">Default</span></span>  <br/> |<span data-ttu-id="1316c-119">指定的默认图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-119">Specifies the default icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-120">PostItem</span><span class="sxs-lookup"><span data-stu-id="1316c-120">PostItem</span></span>  <br/> |<span data-ttu-id="1316c-121">指定一个公告项目的图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-121">Specifies the icon for a post item.</span></span>  <br/> |
|<span data-ttu-id="1316c-122">MailRead</span><span class="sxs-lookup"><span data-stu-id="1316c-122">MailRead</span></span>  <br/> |<span data-ttu-id="1316c-123">指定邮件读取图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-123">Specifies the mail read icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-124">MailUnread</span><span class="sxs-lookup"><span data-stu-id="1316c-124">MailUnread</span></span>  <br/> |<span data-ttu-id="1316c-125">指定未读的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-125">Specifies the unread mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-126">MailReplied</span><span class="sxs-lookup"><span data-stu-id="1316c-126">MailReplied</span></span>  <br/> |<span data-ttu-id="1316c-127">指定答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-127">Specifies the replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-128">MailForwarded</span><span class="sxs-lookup"><span data-stu-id="1316c-128">MailForwarded</span></span>  <br/> |<span data-ttu-id="1316c-129">指定的转发的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-129">Specifies the forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-130">MailEncrypted</span><span class="sxs-lookup"><span data-stu-id="1316c-130">MailEncrypted</span></span>  <br/> |<span data-ttu-id="1316c-131">指定加密的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-131">Specifies the encrypted mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-132">MailSmimeSigned</span><span class="sxs-lookup"><span data-stu-id="1316c-132">MailSmimeSigned</span></span>  <br/> |<span data-ttu-id="1316c-133">指定安全/多用途 Internet 邮件扩展 (S/MIME) 签名的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-133">Specifies the Secure/Multipurpose Internet Mail Extensions (S/MIME) signed mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-134">MailEncryptedReplied</span><span class="sxs-lookup"><span data-stu-id="1316c-134">MailEncryptedReplied</span></span>  <br/> |<span data-ttu-id="1316c-135">指定加密答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-135">Specifies the encrypted replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-136">MailSmimeSignedReplied</span><span class="sxs-lookup"><span data-stu-id="1316c-136">MailSmimeSignedReplied</span></span>  <br/> |<span data-ttu-id="1316c-137">指定 S/MIME 签名答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-137">Specifies the S/MIME signed replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-138">MailEncryptedForwarded</span><span class="sxs-lookup"><span data-stu-id="1316c-138">MailEncryptedForwarded</span></span>  <br/> |<span data-ttu-id="1316c-139">指定的转发的邮件加密的图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-139">Specifies the encrypted forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-140">MailSmimeSignedForwarded</span><span class="sxs-lookup"><span data-stu-id="1316c-140">MailSmimeSignedForwarded</span></span>  <br/> |<span data-ttu-id="1316c-141">指定签名的 S/MIME 转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-141">Specifies the S/MIME signed forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-142">MailEncryptedRead</span><span class="sxs-lookup"><span data-stu-id="1316c-142">MailEncryptedRead</span></span>  <br/> |<span data-ttu-id="1316c-143">指定读取的加密的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-143">Specifies the encrypted read mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-144">MailSmimeSignedRead</span><span class="sxs-lookup"><span data-stu-id="1316c-144">MailSmimeSignedRead</span></span>  <br/> |<span data-ttu-id="1316c-145">指定签名的 S/MIME 读取邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-145">Specifies the S/MIME signed read mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-146">MailIrm</span><span class="sxs-lookup"><span data-stu-id="1316c-146">MailIrm</span></span>  <br/> |<span data-ttu-id="1316c-147">指定受信息权限管理 IRM 保护的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-147">Specifies the Information Rights Management (IRM)-protected mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-148">MailIrmForwarded</span><span class="sxs-lookup"><span data-stu-id="1316c-148">MailIrmForwarded</span></span>  <br/> |<span data-ttu-id="1316c-149">指定受 IRM 保护转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-149">Specifies the IRM-protected forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-150">MailIrmReplied</span><span class="sxs-lookup"><span data-stu-id="1316c-150">MailIrmReplied</span></span>  <br/> |<span data-ttu-id="1316c-151">指定受 IRM 保护答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-151">Specifies the IRM-protected replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-152">SmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="1316c-152">SmsSubmitted</span></span>  <br/> |<span data-ttu-id="1316c-153">指定短信服务 (SMS) 传送所提交的邮件的图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-153">Specifies the icon for mail submitted for Short Message Service (SMS) routing.</span></span>  <br/> |
|<span data-ttu-id="1316c-154">SmsRoutedToDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="1316c-154">SmsRoutedToDeliveryPoint</span></span>  <br/> |<span data-ttu-id="1316c-155">指定 SMS 传送到一个外部传递点的图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-155">Specifies the icon for SMS routing to an external delivery point.</span></span>  <br/> |
|<span data-ttu-id="1316c-156">SmsRoutedToExternalMessagingSystem</span><span class="sxs-lookup"><span data-stu-id="1316c-156">SmsRoutedToExternalMessagingSystem</span></span>  <br/> |<span data-ttu-id="1316c-157">指定 SMS 路由到外部邮件系统的图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-157">Specifies the icon for SMS routing to an external messaging system.</span></span>  <br/> |
|<span data-ttu-id="1316c-158">SmsDelivered</span><span class="sxs-lookup"><span data-stu-id="1316c-158">SmsDelivered</span></span>  <br/> |<span data-ttu-id="1316c-159">指定 SMS 发送的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-159">Specifies the SMS delivered mail icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-160">OutlookDefaultForContacts</span><span class="sxs-lookup"><span data-stu-id="1316c-160">OutlookDefaultForContacts</span></span>  <br/> |<span data-ttu-id="1316c-161">指定联系人的默认图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-161">Specifies the default icon for contacts.</span></span>  <br/> |
|<span data-ttu-id="1316c-162">AppointmentItem</span><span class="sxs-lookup"><span data-stu-id="1316c-162">AppointmentItem</span></span>  <br/> |<span data-ttu-id="1316c-163">指定约会项目图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-163">Specifies the appointment item icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-164">AppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="1316c-164">AppointmentRecur</span></span>  <br/> |<span data-ttu-id="1316c-165">指定的定期约会图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-165">Specifies the recurring appointment icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-166">AppointmentMeet</span><span class="sxs-lookup"><span data-stu-id="1316c-166">AppointmentMeet</span></span>  <br/> |<span data-ttu-id="1316c-167">指定会议图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-167">Specifies the meeting icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-168">AppointmentMeetRecur</span><span class="sxs-lookup"><span data-stu-id="1316c-168">AppointmentMeetRecur</span></span>  <br/> |<span data-ttu-id="1316c-169">指定定期会议图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-169">Specifies the recurring meeting icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-170">AppointmentMeetNY</span><span class="sxs-lookup"><span data-stu-id="1316c-170">AppointmentMeetNY</span></span>  <br/> |<span data-ttu-id="1316c-171">指定对会议的暂定响应的图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-171">Specifies the icon for a tentative response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="1316c-172">AppointmentMeetYes</span><span class="sxs-lookup"><span data-stu-id="1316c-172">AppointmentMeetYes</span></span>  <br/> |<span data-ttu-id="1316c-173">指定会议验收图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-173">Specifies the meeting acceptance icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-174">AppointmentMeetNo</span><span class="sxs-lookup"><span data-stu-id="1316c-174">AppointmentMeetNo</span></span>  <br/> |<span data-ttu-id="1316c-175">指定会议拒绝的图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-175">Specifies the meeting declined icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-176">AppointmentMeetMaybe</span><span class="sxs-lookup"><span data-stu-id="1316c-176">AppointmentMeetMaybe</span></span>  <br/> |<span data-ttu-id="1316c-177">指定对会议的也许响应的图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-177">Specifies the icon for a maybe response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="1316c-178">AppointmentMeetCancel</span><span class="sxs-lookup"><span data-stu-id="1316c-178">AppointmentMeetCancel</span></span>  <br/> |<span data-ttu-id="1316c-179">指定会议取消图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-179">Specifies the meeting cancel icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-180">AppointmentMeetInfo</span><span class="sxs-lookup"><span data-stu-id="1316c-180">AppointmentMeetInfo</span></span>  <br/> |<span data-ttu-id="1316c-181">指定会议信息图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-181">Specifies the meeting information icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-182">TaskItem</span><span class="sxs-lookup"><span data-stu-id="1316c-182">TaskItem</span></span>  <br/> |<span data-ttu-id="1316c-183">指定任务项目图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-183">Specifies the task item icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-184">TaskRecur</span><span class="sxs-lookup"><span data-stu-id="1316c-184">TaskRecur</span></span>  <br/> |<span data-ttu-id="1316c-185">指定定期任务图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-185">Specifies the recurring task icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-186">TaskOwned</span><span class="sxs-lookup"><span data-stu-id="1316c-186">TaskOwned</span></span>  <br/> |<span data-ttu-id="1316c-187">指定拥有图标的任务。</span><span class="sxs-lookup"><span data-stu-id="1316c-187">Specifies the task owned icon.</span></span>  <br/> |
|<span data-ttu-id="1316c-188">TaskDelegated</span><span class="sxs-lookup"><span data-stu-id="1316c-188">TaskDelegated</span></span>  <br/> |<span data-ttu-id="1316c-189">指定的任务委派的图标。</span><span class="sxs-lookup"><span data-stu-id="1316c-189">Specifies the task delegated icon.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1316c-190">备注</span><span class="sxs-lookup"><span data-stu-id="1316c-190">Remarks</span></span>

<span data-ttu-id="1316c-191">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1316c-191">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1316c-192">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1316c-192">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1316c-193">元素信息</span><span class="sxs-lookup"><span data-stu-id="1316c-193">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1316c-194">命名空间</span><span class="sxs-lookup"><span data-stu-id="1316c-194">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1316c-195">架构名称</span><span class="sxs-lookup"><span data-stu-id="1316c-195">Schema name</span></span>  <br/> |<span data-ttu-id="1316c-196">类型架构</span><span class="sxs-lookup"><span data-stu-id="1316c-196">Types schema</span></span>  <br/> |
|<span data-ttu-id="1316c-197">验证文件</span><span class="sxs-lookup"><span data-stu-id="1316c-197">Validation file</span></span>  <br/> |<span data-ttu-id="1316c-198">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1316c-198">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1316c-199">可以为空</span><span class="sxs-lookup"><span data-stu-id="1316c-199">Can be empty</span></span>  <br/> |<span data-ttu-id="1316c-200">false</span><span class="sxs-lookup"><span data-stu-id="1316c-200">false</span></span>  <br/> |
   
