---
title: FederatedDeliveryMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FederatedDeliveryMailbox
api_type:
- schema
ms.assetid: cd56bcc0-d24a-4e8b-87bd-999bf69234b7
description: FederatedDeliveryMailbox元素表示跨内部消息发送到该邮箱。
ms.openlocfilehash: d493ed81e82237b7257e8c469f4552d931b73aa6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461945"
---
# <a name="federateddeliverymailbox"></a><span data-ttu-id="9cdf7-103">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="9cdf7-103">FederatedDeliveryMailbox</span></span>

<span data-ttu-id="9cdf7-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **FederatedDeliveryMailbox**元素表示跨内部消息发送到该邮箱。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-104">The **FederatedDeliveryMailbox** element represents the mailbox to which a cross-premise message was sent.</span></span> 
  
```XML
<FederatedDeliveryMailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</FederatedDeliveryMailbox>
```

 <span data-ttu-id="9cdf7-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="9cdf7-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9cdf7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9cdf7-106">Attributes and elements</span></span>

<span data-ttu-id="9cdf7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9cdf7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9cdf7-108">Attributes</span></span>

<span data-ttu-id="9cdf7-109">无。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9cdf7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9cdf7-110">Child elements</span></span>

|<span data-ttu-id="9cdf7-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9cdf7-111">**Element**</span></span>|<span data-ttu-id="9cdf7-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9cdf7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9cdf7-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="9cdf7-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="9cdf7-p101">定义邮箱用户的名称。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-p101">Defines the name of the mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="9cdf7-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="9cdf7-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="9cdf7-p102">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="9cdf7-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="9cdf7-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="9cdf7-p103">定义用于邮箱路由。默认值为 SMTP。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="9cdf7-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="9cdf7-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="9cdf7-p104">定义邮箱用户的邮箱类型。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="9cdf7-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="9cdf7-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="9cdf7-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9cdf7-129">父元素</span><span class="sxs-lookup"><span data-stu-id="9cdf7-129">Parent elements</span></span>

|<span data-ttu-id="9cdf7-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="9cdf7-130">**Element**</span></span>|<span data-ttu-id="9cdf7-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="9cdf7-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9cdf7-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="9cdf7-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="9cdf7-133">包含要查找的邮件的类型的条件。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-133">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9cdf7-134">文本值</span><span class="sxs-lookup"><span data-stu-id="9cdf7-134">Text value</span></span>

<span data-ttu-id="9cdf7-135">无。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9cdf7-136">说明</span><span class="sxs-lookup"><span data-stu-id="9cdf7-136">Remarks</span></span>

<span data-ttu-id="9cdf7-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9cdf7-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9cdf7-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="9cdf7-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9cdf7-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="9cdf7-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9cdf7-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="9cdf7-140">Schema Name</span></span>  <br/> |<span data-ttu-id="9cdf7-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="9cdf7-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9cdf7-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="9cdf7-142">Validation File</span></span>  <br/> |<span data-ttu-id="9cdf7-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9cdf7-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9cdf7-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="9cdf7-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="9cdf7-145">False</span><span class="sxs-lookup"><span data-stu-id="9cdf7-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9cdf7-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9cdf7-146">See also</span></span>



- [<span data-ttu-id="9cdf7-147">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9cdf7-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

