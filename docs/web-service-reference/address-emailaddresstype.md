---
title: 地址 (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: 518641c8-7f6f-496c-86f9-341e7c1bb44c
description: Address 元素表示完全解析的电子邮件地址。
ms.openlocfilehash: 591bc675165ec80f69407bd8ee19d16c9ddff15a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464901"
---
# <a name="address-emailaddresstype"></a><span data-ttu-id="36bec-103">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="36bec-103">Address (EmailAddressType)</span></span>

<span data-ttu-id="36bec-104">**Address**元素表示完全解析的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="36bec-104">The **Address** element represents a fully resolved e-mail address.</span></span> 
  
```XML
<Address>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Address >
```

 <span data-ttu-id="36bec-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="36bec-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36bec-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="36bec-106">Attributes and elements</span></span>

<span data-ttu-id="36bec-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="36bec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36bec-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="36bec-108">Attributes</span></span>

<span data-ttu-id="36bec-109">无。</span><span class="sxs-lookup"><span data-stu-id="36bec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36bec-110">子元素</span><span class="sxs-lookup"><span data-stu-id="36bec-110">Child elements</span></span>

|<span data-ttu-id="36bec-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="36bec-111">**Element**</span></span>|<span data-ttu-id="36bec-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="36bec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36bec-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="36bec-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="36bec-p101">定义邮箱用户的名称。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="36bec-p101">Defines the name of the mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="36bec-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="36bec-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="36bec-p102">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="36bec-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="36bec-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="36bec-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="36bec-p103">定义用于邮箱路由。默认值为 SMTP。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="36bec-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="36bec-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="36bec-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="36bec-p104">定义邮箱用户的邮箱类型。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="36bec-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="36bec-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="36bec-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="36bec-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="36bec-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="36bec-129">父元素</span><span class="sxs-lookup"><span data-stu-id="36bec-129">Parent elements</span></span>

|<span data-ttu-id="36bec-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="36bec-130">**Element**</span></span>|<span data-ttu-id="36bec-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="36bec-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36bec-132">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="36bec-132">OriginalRecipients</span></span>](originalrecipients.md) <br/> |<span data-ttu-id="36bec-133">包含代表跟踪的邮件的原始收件人的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="36bec-133">Contains a collection of e-mail addresses that represent the original recipients of a tracked message.</span></span>  <br/> |
|[<span data-ttu-id="36bec-134">RoomLists</span><span class="sxs-lookup"><span data-stu-id="36bec-134">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="36bec-135">包含组织中的会议室列表。</span><span class="sxs-lookup"><span data-stu-id="36bec-135">Contains a list of meeting rooms in an organization.</span></span>  <br/> |
|[<span data-ttu-id="36bec-136">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="36bec-136">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="36bec-137">包含传入邮件必须发送到的电子邮件地址列表，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="36bec-137">Contains a list of e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36bec-138">文本值</span><span class="sxs-lookup"><span data-stu-id="36bec-138">Text value</span></span>

<span data-ttu-id="36bec-139">无。</span><span class="sxs-lookup"><span data-stu-id="36bec-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36bec-140">说明</span><span class="sxs-lookup"><span data-stu-id="36bec-140">Remarks</span></span>

<span data-ttu-id="36bec-141">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="36bec-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36bec-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="36bec-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36bec-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="36bec-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="36bec-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="36bec-144">Schema Name</span></span>  <br/> |<span data-ttu-id="36bec-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="36bec-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="36bec-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="36bec-146">Validation File</span></span>  <br/> |<span data-ttu-id="36bec-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="36bec-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="36bec-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="36bec-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="36bec-149">False</span><span class="sxs-lookup"><span data-stu-id="36bec-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36bec-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36bec-150">See also</span></span>

- [<span data-ttu-id="36bec-151">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="36bec-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md) 
- [<span data-ttu-id="36bec-152">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="36bec-152">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="36bec-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="36bec-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

