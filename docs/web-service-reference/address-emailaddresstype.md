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
description: 地址元素均表示一个完全解析电子邮件地址。
ms.openlocfilehash: 2a2d409edcc3a04bf82c6da0080183becfc9b25b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753191"
---
# <a name="address-emailaddresstype"></a><span data-ttu-id="a557f-103">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="a557f-103">Address (EmailAddressType)</span></span>

<span data-ttu-id="a557f-104">**地址**元素均表示一个完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="a557f-104">The **Address** element represents a fully resolved e-mail address.</span></span> 
  
```XML
<Address>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Address >
```

 <span data-ttu-id="a557f-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="a557f-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a557f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a557f-106">Attributes and elements</span></span>

<span data-ttu-id="a557f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a557f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a557f-108">属性</span><span class="sxs-lookup"><span data-stu-id="a557f-108">Attributes</span></span>

<span data-ttu-id="a557f-109">无。</span><span class="sxs-lookup"><span data-stu-id="a557f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a557f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a557f-110">Child elements</span></span>

|<span data-ttu-id="a557f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a557f-111">**Element**</span></span>|<span data-ttu-id="a557f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a557f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a557f-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="a557f-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="a557f-p101">定义邮箱用户的名称。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="a557f-p101">Defines the name of the mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a557f-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="a557f-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="a557f-p102">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="a557f-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a557f-119">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="a557f-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="a557f-p103">定义用于邮箱路由。默认值为 SMTP。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="a557f-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a557f-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="a557f-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="a557f-p104">定义邮箱用户的邮箱类型。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="a557f-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a557f-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="a557f-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="a557f-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="a557f-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a557f-129">父元素</span><span class="sxs-lookup"><span data-stu-id="a557f-129">Parent elements</span></span>

|<span data-ttu-id="a557f-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="a557f-130">**Element**</span></span>|<span data-ttu-id="a557f-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="a557f-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a557f-132">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="a557f-132">OriginalRecipients</span></span>](originalrecipients.md) <br/> |<span data-ttu-id="a557f-133">包含表示跟踪邮件的原始收件人的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="a557f-133">Contains a collection of e-mail addresses that represent the original recipients of a tracked message.</span></span>  <br/> |
|[<span data-ttu-id="a557f-134">RoomLists</span><span class="sxs-lookup"><span data-stu-id="a557f-134">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="a557f-135">包含会议组织中的聊天室的列表。</span><span class="sxs-lookup"><span data-stu-id="a557f-135">Contains a list of meeting rooms in an organization.</span></span>  <br/> |
|[<span data-ttu-id="a557f-136">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="a557f-136">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="a557f-137">包含一组中的条件或例外的顺序应用发送给所需要的传入消息的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="a557f-137">Contains a list of e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a557f-138">文本值</span><span class="sxs-lookup"><span data-stu-id="a557f-138">Text value</span></span>

<span data-ttu-id="a557f-139">无。</span><span class="sxs-lookup"><span data-stu-id="a557f-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a557f-140">备注</span><span class="sxs-lookup"><span data-stu-id="a557f-140">Remarks</span></span>

<span data-ttu-id="a557f-141">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a557f-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a557f-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="a557f-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a557f-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="a557f-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a557f-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="a557f-144">Schema Name</span></span>  <br/> |<span data-ttu-id="a557f-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="a557f-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="a557f-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="a557f-146">Validation File</span></span>  <br/> |<span data-ttu-id="a557f-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a557f-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a557f-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="a557f-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="a557f-149">False</span><span class="sxs-lookup"><span data-stu-id="a557f-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a557f-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a557f-150">See also</span></span>

- [<span data-ttu-id="a557f-151">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="a557f-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md) 
- [<span data-ttu-id="a557f-152">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="a557f-152">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="a557f-153">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a557f-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

