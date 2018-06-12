---
title: IconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92020822-2a86-4dfc-aee1-3067af4d4edf
description: IconIndex 元素标识的图标索引的项目或会话。
ms.openlocfilehash: 8ada9da2df1cf128009c9b153736b434925f1a3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825848"
---
# <a name="iconindex"></a><span data-ttu-id="f5b29-103">IconIndex</span><span class="sxs-lookup"><span data-stu-id="f5b29-103">IconIndex</span></span>

<span data-ttu-id="f5b29-104">**IconIndex**元素标识的图标索引的项目或会话。</span><span class="sxs-lookup"><span data-stu-id="f5b29-104">The **IconIndex** element identifies the icon index for an item or conversation.</span></span> 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MailIrmForwarded | MailIrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 <span data-ttu-id="f5b29-105">**IconIndexType**</span><span class="sxs-lookup"><span data-stu-id="f5b29-105">**IconIndexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f5b29-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f5b29-106">Attributes and elements</span></span>

<span data-ttu-id="f5b29-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f5b29-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5b29-108">属性</span><span class="sxs-lookup"><span data-stu-id="f5b29-108">Attributes</span></span>

<span data-ttu-id="f5b29-109">无。</span><span class="sxs-lookup"><span data-stu-id="f5b29-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f5b29-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f5b29-110">Child elements</span></span>

<span data-ttu-id="f5b29-111">无。</span><span class="sxs-lookup"><span data-stu-id="f5b29-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f5b29-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f5b29-112">Parent elements</span></span>

<span data-ttu-id="f5b29-113">[对话 (ConversationType)](conversation-conversationtype.md) | [项](item.md) | [联系人](contact.md) | [DistributionList](distributionlist.md) | [消息](message-ex15websvcsotherref.md) | [日历项目](calendaritem.md) | [PostItem](postitem.md) | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="f5b29-113">[Conversation (ConversationType)](conversation-conversationtype.md) | [Item](item.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Message](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f5b29-114">文本值</span><span class="sxs-lookup"><span data-stu-id="f5b29-114">Text value</span></span>

<span data-ttu-id="f5b29-115">下表包含**IconIndex**元素的可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="f5b29-115">The following table contains the possible text values for the **IconIndex** element.</span></span> 
  
|<span data-ttu-id="f5b29-116">**值**</span><span class="sxs-lookup"><span data-stu-id="f5b29-116">**Value**</span></span>|<span data-ttu-id="f5b29-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5b29-117">**Description**</span></span>|
|:-----|:-----|
|||
|<span data-ttu-id="f5b29-118">默认</span><span class="sxs-lookup"><span data-stu-id="f5b29-118">Default</span></span>  <br/> |<span data-ttu-id="f5b29-119">指定的默认图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-119">Specifies the default icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-120">PostItem</span><span class="sxs-lookup"><span data-stu-id="f5b29-120">PostItem</span></span>  <br/> |<span data-ttu-id="f5b29-121">指定一个公告项目的图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-121">Specifies the icon for a post item.</span></span>  <br/> |
|<span data-ttu-id="f5b29-122">MailRead</span><span class="sxs-lookup"><span data-stu-id="f5b29-122">MailRead</span></span>  <br/> |<span data-ttu-id="f5b29-123">指定邮件读取图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-123">Specifies the mail read icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-124">MailUnread</span><span class="sxs-lookup"><span data-stu-id="f5b29-124">MailUnread</span></span>  <br/> |<span data-ttu-id="f5b29-125">指定未读的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-125">Specifies the unread mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-126">MailReplied</span><span class="sxs-lookup"><span data-stu-id="f5b29-126">MailReplied</span></span>  <br/> |<span data-ttu-id="f5b29-127">指定答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-127">Specifies the replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-128">MailForwarded</span><span class="sxs-lookup"><span data-stu-id="f5b29-128">MailForwarded</span></span>  <br/> |<span data-ttu-id="f5b29-129">指定的转发的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-129">Specifies the forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-130">MailEncrypted</span><span class="sxs-lookup"><span data-stu-id="f5b29-130">MailEncrypted</span></span>  <br/> |<span data-ttu-id="f5b29-131">指定加密的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-131">Specifies the encrypted mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-132">MailSmimeSigned</span><span class="sxs-lookup"><span data-stu-id="f5b29-132">MailSmimeSigned</span></span>  <br/> |<span data-ttu-id="f5b29-133">指定安全/多用途 Internet 邮件扩展 (S/MIME) 签名的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-133">Specifies the Secure/Multipurpose Internet Mail Extensions (S/MIME) signed mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-134">MailEncryptedReplied</span><span class="sxs-lookup"><span data-stu-id="f5b29-134">MailEncryptedReplied</span></span>  <br/> |<span data-ttu-id="f5b29-135">指定加密答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-135">Specifies the encrypted replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-136">MailSmimeSignedReplied</span><span class="sxs-lookup"><span data-stu-id="f5b29-136">MailSmimeSignedReplied</span></span>  <br/> |<span data-ttu-id="f5b29-137">指定 S/MIME 签名答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-137">Specifies the S/MIME signed replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-138">MailEncryptedForwarded</span><span class="sxs-lookup"><span data-stu-id="f5b29-138">MailEncryptedForwarded</span></span>  <br/> |<span data-ttu-id="f5b29-139">指定的转发的邮件加密的图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-139">Specifies the encrypted forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-140">MailSmimeSignedForwarded</span><span class="sxs-lookup"><span data-stu-id="f5b29-140">MailSmimeSignedForwarded</span></span>  <br/> |<span data-ttu-id="f5b29-141">指定签名的 S/MIME 转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-141">Specifies the S/MIME signed forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-142">MailEncryptedRead</span><span class="sxs-lookup"><span data-stu-id="f5b29-142">MailEncryptedRead</span></span>  <br/> |<span data-ttu-id="f5b29-143">指定读取的加密的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-143">Specifies the encrypted read mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-144">MailSmimeSignedRead</span><span class="sxs-lookup"><span data-stu-id="f5b29-144">MailSmimeSignedRead</span></span>  <br/> |<span data-ttu-id="f5b29-145">指定签名的 S/MIME 读取邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-145">Specifies the S/MIME signed read mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-146">MailIrm</span><span class="sxs-lookup"><span data-stu-id="f5b29-146">MailIrm</span></span>  <br/> |<span data-ttu-id="f5b29-147">指定受信息权限管理 IRM 保护的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-147">Specifies the Information Rights Management (IRM)-protected mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-148">MailIrmForwarded</span><span class="sxs-lookup"><span data-stu-id="f5b29-148">MailIrmForwarded</span></span>  <br/> |<span data-ttu-id="f5b29-149">指定受 IRM 保护转发邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-149">Specifies the IRM-protected forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-150">MailIrmReplied</span><span class="sxs-lookup"><span data-stu-id="f5b29-150">MailIrmReplied</span></span>  <br/> |<span data-ttu-id="f5b29-151">指定受 IRM 保护答复邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-151">Specifies the IRM-protected replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-152">SmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="f5b29-152">SmsSubmitted</span></span>  <br/> |<span data-ttu-id="f5b29-153">指定短信服务 (SMS) 传送所提交的图标邮件。</span><span class="sxs-lookup"><span data-stu-id="f5b29-153">Specifies the icon mail submitted for Short Message Service (SMS) routing.</span></span>  <br/> |
|<span data-ttu-id="f5b29-154">SmsRoutedToDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="f5b29-154">SmsRoutedToDeliveryPoint</span></span>  <br/> |<span data-ttu-id="f5b29-155">指定 SMS 传送到一个外部传递点的图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-155">Specifies the icon for SMS routing to an external delivery point.</span></span>  <br/> |
|<span data-ttu-id="f5b29-156">SmsRoutedToExternalMessagingSystem</span><span class="sxs-lookup"><span data-stu-id="f5b29-156">SmsRoutedToExternalMessagingSystem</span></span>  <br/> |<span data-ttu-id="f5b29-157">指定 SMS 路由到外部邮件系统的图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-157">Specifies the icon for SMS routing to an external messaging system.</span></span>  <br/> |
|<span data-ttu-id="f5b29-158">SmsDelivered</span><span class="sxs-lookup"><span data-stu-id="f5b29-158">SmsDelivered</span></span>  <br/> |<span data-ttu-id="f5b29-159">指定 SMS 发送的邮件图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-159">Specifies the SMS delivered mail icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-160">OutlookDefaultForContacts</span><span class="sxs-lookup"><span data-stu-id="f5b29-160">OutlookDefaultForContacts</span></span>  <br/> |<span data-ttu-id="f5b29-161">指定联系人的默认图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-161">Specifies the default icon for contacts.</span></span>  <br/> |
|<span data-ttu-id="f5b29-162">AppointmentItem</span><span class="sxs-lookup"><span data-stu-id="f5b29-162">AppointmentItem</span></span>  <br/> |<span data-ttu-id="f5b29-163">指定约会项目图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-163">Specifies the appointment item icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-164">AppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="f5b29-164">AppointmentRecur</span></span>  <br/> |<span data-ttu-id="f5b29-165">指定的定期约会图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-165">Specifies the recurring appointment icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-166">AppointmentMeet</span><span class="sxs-lookup"><span data-stu-id="f5b29-166">AppointmentMeet</span></span>  <br/> |<span data-ttu-id="f5b29-167">指定会议图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-167">Specifies the meeting icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-168">AppointmentMeetRecur</span><span class="sxs-lookup"><span data-stu-id="f5b29-168">AppointmentMeetRecur</span></span>  <br/> |<span data-ttu-id="f5b29-169">指定定期会议图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-169">Specifies the recurring meeting icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-170">AppointmentMeetNY</span><span class="sxs-lookup"><span data-stu-id="f5b29-170">AppointmentMeetNY</span></span>  <br/> |<span data-ttu-id="f5b29-171">指定对会议的暂定响应的图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-171">Specifies the icon for a tentative response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="f5b29-172">AppointmentMeetYes</span><span class="sxs-lookup"><span data-stu-id="f5b29-172">AppointmentMeetYes</span></span>  <br/> |<span data-ttu-id="f5b29-173">指定会议验收图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-173">Specifies the meeting acceptance icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-174">AppointmentMeetNo</span><span class="sxs-lookup"><span data-stu-id="f5b29-174">AppointmentMeetNo</span></span>  <br/> |<span data-ttu-id="f5b29-175">指定会议拒绝的图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-175">Specifies the meeting declined icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-176">AppointmentMeetMaybe</span><span class="sxs-lookup"><span data-stu-id="f5b29-176">AppointmentMeetMaybe</span></span>  <br/> |<span data-ttu-id="f5b29-177">指定对会议的也许响应的图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-177">Specifies the icon for a maybe response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="f5b29-178">AppointmentMeetCancel</span><span class="sxs-lookup"><span data-stu-id="f5b29-178">AppointmentMeetCancel</span></span>  <br/> |<span data-ttu-id="f5b29-179">指定会议取消图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-179">Specifies the meeting cancel icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-180">AppointmentMeetInfo</span><span class="sxs-lookup"><span data-stu-id="f5b29-180">AppointmentMeetInfo</span></span>  <br/> |<span data-ttu-id="f5b29-181">指定会议信息图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-181">Specifies the meeting information icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-182">TaskItem</span><span class="sxs-lookup"><span data-stu-id="f5b29-182">TaskItem</span></span>  <br/> |<span data-ttu-id="f5b29-183">指定任务项目图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-183">Specifies the task item icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-184">TaskRecur</span><span class="sxs-lookup"><span data-stu-id="f5b29-184">TaskRecur</span></span>  <br/> |<span data-ttu-id="f5b29-185">指定定期任务图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-185">Specifies the recurring task icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-186">TaskOwned</span><span class="sxs-lookup"><span data-stu-id="f5b29-186">TaskOwned</span></span>  <br/> |<span data-ttu-id="f5b29-187">指定拥有图标的任务。</span><span class="sxs-lookup"><span data-stu-id="f5b29-187">Specifies the task owned icon.</span></span>  <br/> |
|<span data-ttu-id="f5b29-188">TaskDelegated</span><span class="sxs-lookup"><span data-stu-id="f5b29-188">TaskDelegated</span></span>  <br/> |<span data-ttu-id="f5b29-189">指定的任务委派的图标。</span><span class="sxs-lookup"><span data-stu-id="f5b29-189">Specifies the task delegated icon.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5b29-190">备注</span><span class="sxs-lookup"><span data-stu-id="f5b29-190">Remarks</span></span>

<span data-ttu-id="f5b29-191">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f5b29-191">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f5b29-192">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f5b29-192">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f5b29-193">元素信息</span><span class="sxs-lookup"><span data-stu-id="f5b29-193">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5b29-194">命名空间</span><span class="sxs-lookup"><span data-stu-id="f5b29-194">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f5b29-195">架构名称</span><span class="sxs-lookup"><span data-stu-id="f5b29-195">Schema name</span></span>  <br/> |<span data-ttu-id="f5b29-196">类型架构</span><span class="sxs-lookup"><span data-stu-id="f5b29-196">Types schema</span></span>  <br/> |
|<span data-ttu-id="f5b29-197">验证文件</span><span class="sxs-lookup"><span data-stu-id="f5b29-197">Validation file</span></span>  <br/> |<span data-ttu-id="f5b29-198">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f5b29-198">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f5b29-199">可以为空</span><span class="sxs-lookup"><span data-stu-id="f5b29-199">Can be empty</span></span>  <br/> |<span data-ttu-id="f5b29-200">false</span><span class="sxs-lookup"><span data-stu-id="f5b29-200">false</span></span>  <br/> |
   
