---
title: Mailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: befc70fd-51cb-4258-884c-80c9050f0e82
description: Mailbox 元素标识启用了邮件的 Active Directory 对象。
ms.openlocfilehash: 284c3ff6f9fece57611169a4ec41eeaa273c6ad3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468199"
---
# <a name="mailbox"></a><span data-ttu-id="269d8-103">邮箱</span><span class="sxs-lookup"><span data-stu-id="269d8-103">Mailbox</span></span>

<span data-ttu-id="269d8-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Mailbox** 元素标识启用了邮件的 Active Directory 对象。</span><span class="sxs-lookup"><span data-stu-id="269d8-104">The **Mailbox** element identifies a mail-enabled Active Directory object.</span></span> 
  
```XML
<Mailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Mailbox>
```

<span data-ttu-id="269d8-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="269d8-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="269d8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="269d8-106">Attributes and elements</span></span>

<span data-ttu-id="269d8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="269d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="269d8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="269d8-108">Attributes</span></span>

<span data-ttu-id="269d8-109">无。</span><span class="sxs-lookup"><span data-stu-id="269d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="269d8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="269d8-110">Child elements</span></span>

|<span data-ttu-id="269d8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="269d8-111">**Element**</span></span>|<span data-ttu-id="269d8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="269d8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="269d8-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="269d8-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="269d8-p101">定义邮箱用户的名称。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="269d8-p101">Defines the name of the mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="269d8-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="269d8-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="269d8-p102">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="269d8-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="269d8-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="269d8-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="269d8-p103">定义用于邮箱路由。默认值为 SMTP。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="269d8-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="269d8-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="269d8-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="269d8-p104">定义邮箱用户的邮箱类型。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="269d8-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="269d8-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="269d8-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="269d8-p105">定义用户联系人文件夹收件人的联系人或私人通讯组列表的项标识符。此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="269d8-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="269d8-129">父元素</span><span class="sxs-lookup"><span data-stu-id="269d8-129">Parent elements</span></span>

|<span data-ttu-id="269d8-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="269d8-130">**Element**</span></span>|<span data-ttu-id="269d8-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="269d8-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="269d8-132">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="269d8-132">ExpandDL</span></span>](expanddl.md) <br/> |<span data-ttu-id="269d8-133">定义展开通讯组列表的请求。</span><span class="sxs-lookup"><span data-stu-id="269d8-133">Defines a request to expand a distribution list.</span></span> <br/> <br/> <span data-ttu-id="269d8-134">下面是此元素的 XPath 表达式： ` /ExpandDL `</span><span class="sxs-lookup"><span data-stu-id="269d8-134">The following is the XPath expression to this element: ` /ExpandDL `</span></span> <br/> |
|[<span data-ttu-id="269d8-135">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="269d8-135">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="269d8-136">包含项目的收件人数组。</span><span class="sxs-lookup"><span data-stu-id="269d8-136">Contains an array of recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="269d8-137">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="269d8-137">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="269d8-138">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="269d8-138">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="269d8-139">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="269d8-139">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="269d8-140">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="269d8-140">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="269d8-141">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="269d8-141">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="269d8-142">标识副本应发送到的电子邮件地址数组。</span><span class="sxs-lookup"><span data-stu-id="269d8-142">Identifies an array of e-mail addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="269d8-143">发件人</span><span class="sxs-lookup"><span data-stu-id="269d8-143">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="269d8-144">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="269d8-144">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="269d8-145">发件人</span><span class="sxs-lookup"><span data-stu-id="269d8-145">From</span></span>](from.md) <br/> |<span data-ttu-id="269d8-146">表示邮件发件人的地址。</span><span class="sxs-lookup"><span data-stu-id="269d8-146">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="269d8-147">Organizer</span><span class="sxs-lookup"><span data-stu-id="269d8-147">Organizer</span></span>](organizer.md) <br/> |<span data-ttu-id="269d8-148">表示会议的组织者。</span><span class="sxs-lookup"><span data-stu-id="269d8-148">Represents the organizer of a meeting.</span></span>  <br/> |
|[<span data-ttu-id="269d8-149">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="269d8-149">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> | <span data-ttu-id="269d8-150">标识默认的 Microsoft Exchange Server 2007 文件夹。</span><span class="sxs-lookup"><span data-stu-id="269d8-150">Identifies default Microsoft Exchange Server 2007 folders.</span></span>  <br/><br/>  <span data-ttu-id="269d8-151">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="269d8-151">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/CreateItem/ParentFolderId/DistinguishedFolderId` <br/>  `/CreateFolder/ParentFolderId/DistinguishedFolderId` <br/> |
|[<span data-ttu-id="269d8-152">解决方法</span><span class="sxs-lookup"><span data-stu-id="269d8-152">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="269d8-153">包含单个已解析的实体。</span><span class="sxs-lookup"><span data-stu-id="269d8-153">Contains a single resolved entity.</span></span>  <br/> |
|[<span data-ttu-id="269d8-154">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="269d8-154">DLExpansion</span></span>](dlexpansion.md) <br/> |<span data-ttu-id="269d8-155">包含通讯组列表包含的邮箱数组。</span><span class="sxs-lookup"><span data-stu-id="269d8-155">Contains an array of mailboxes that are contained in a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="269d8-156">参与者</span><span class="sxs-lookup"><span data-stu-id="269d8-156">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="269d8-157">表示日历项的与会者和资源。</span><span class="sxs-lookup"><span data-stu-id="269d8-157">Represents attendees and resources for a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="269d8-158">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="269d8-158">CreateManagedFolder</span></span>](createmanagedfolder.md) <br/> |<span data-ttu-id="269d8-159">定义请求以将托管文件夹添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="269d8-159">Defines a request to add managed folders to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="269d8-160">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="269d8-160">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="269d8-161">定义请求以将代理人添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="269d8-161">Defines a request to add delegates to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="269d8-162">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="269d8-162">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="269d8-163">定义请求以获取有关委派给邮箱的信息。</span><span class="sxs-lookup"><span data-stu-id="269d8-163">Defines a request to get information about delegates to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="269d8-164">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="269d8-164">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="269d8-165">定义请求以从邮箱删除代理人。</span><span class="sxs-lookup"><span data-stu-id="269d8-165">Defines a request to remove delegates from a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="269d8-166">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="269d8-166">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="269d8-167">定义请求以更新邮箱中的代理人。</span><span class="sxs-lookup"><span data-stu-id="269d8-167">Defines a request to update delegates in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="269d8-168">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="269d8-168">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="269d8-169">描述委派访问方案中的代理人。</span><span class="sxs-lookup"><span data-stu-id="269d8-169">Describes the delegate in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="269d8-170">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="269d8-170">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="269d8-171">描述委派访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="269d8-171">Describes the principal in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="269d8-172">Member</span><span class="sxs-lookup"><span data-stu-id="269d8-172">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="269d8-173">表示一个通讯组列表的成员。</span><span class="sxs-lookup"><span data-stu-id="269d8-173">Represents a member of a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="269d8-174">文本值</span><span class="sxs-lookup"><span data-stu-id="269d8-174">Text value</span></span>

<span data-ttu-id="269d8-175">无。</span><span class="sxs-lookup"><span data-stu-id="269d8-175">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="269d8-176">说明</span><span class="sxs-lookup"><span data-stu-id="269d8-176">Remarks</span></span>

<span data-ttu-id="269d8-177">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) 和 [ItemId](itemid.md) 元素识别邮箱或通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="269d8-177">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) and [ItemId](itemid.md) elements identify a mailbox or distribution list.</span></span> 

<span data-ttu-id="269d8-178">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) 元素通过 SMTP 地址识别邮箱或通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="269d8-178">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element identifies a mailbox or distribution list by SMTP address.</span></span> 

<span data-ttu-id="269d8-179">[ItemId](itemid.md) 元素通过与特定邮箱相关联的项标识符识别邮箱。</span><span class="sxs-lookup"><span data-stu-id="269d8-179">The [ItemId](itemid.md) element identifies a mailbox by an item identifier, which is associated with a particular mailbox.</span></span> 

<span data-ttu-id="269d8-180">无法使用 [ItemId](itemid.md) 元素向公共联系人文件夹中的通讯组列表或联系人发送邮件。</span><span class="sxs-lookup"><span data-stu-id="269d8-180">The [ItemId](itemid.md) element cannot be used for sending a message to a distribution list or a contact in a public contacts folder.</span></span> <span data-ttu-id="269d8-181">在尝试向联系人公共文件夹中的通讯组列表或联系人发送邮件时，如果在 CreateItem、UpdateItem 或 SendItem 操作中使用此元素则会引发错误。</span><span class="sxs-lookup"><span data-stu-id="269d8-181">An error will be thrown if this is used in a CreateItem, UpdateItem, or SendItem operation when an attempt is made to send a message to a distribution list or contact in a contacts public folder.</span></span> <span data-ttu-id="269d8-182">使用 ExpandDL 操作获取 SMTP 地址，然后通过使用 [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) 元素发送邮件，而不是使用 [ItemId](itemid.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="269d8-182">Use the ExpandDL operation to get the SMTP address and then send the message by using the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element instead of the [ItemId](itemid.md) element.</span></span> 
  
<span data-ttu-id="269d8-183">另一个元素 [邮箱 (可用性)](mailbox-availability.md) 为可用性操作提供信息。</span><span class="sxs-lookup"><span data-stu-id="269d8-183">Another element, [Mailbox (Availability)](mailbox-availability.md), provides information for availability operations.</span></span> 
  
<span data-ttu-id="269d8-184">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="269d8-184">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="269d8-185">元素信息</span><span class="sxs-lookup"><span data-stu-id="269d8-185">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="269d8-186">命名空间</span><span class="sxs-lookup"><span data-stu-id="269d8-186">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="269d8-187">架构名称</span><span class="sxs-lookup"><span data-stu-id="269d8-187">Schema Name</span></span>  <br/> |<span data-ttu-id="269d8-188">类型架构</span><span class="sxs-lookup"><span data-stu-id="269d8-188">Types schema</span></span>  <br/> |
|<span data-ttu-id="269d8-189">验证文件</span><span class="sxs-lookup"><span data-stu-id="269d8-189">Validation File</span></span>  <br/> |<span data-ttu-id="269d8-190">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="269d8-190">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="269d8-191">可以为空</span><span class="sxs-lookup"><span data-stu-id="269d8-191">Can be Empty</span></span>  <br/> |<span data-ttu-id="269d8-192">False</span><span class="sxs-lookup"><span data-stu-id="269d8-192">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="269d8-193">另请参阅</span><span class="sxs-lookup"><span data-stu-id="269d8-193">See also</span></span>

- [<span data-ttu-id="269d8-194">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="269d8-194">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

