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
ms.openlocfilehash: 4a9250455f8de3ede25f2b5ba9433690137ca1d3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754293"
---
# <a name="federateddeliverymailbox"></a><span data-ttu-id="1bb0f-103">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="1bb0f-103">FederatedDeliveryMailbox</span></span>

<span data-ttu-id="1bb0f-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **FederatedDeliveryMailbox**元素表示跨内部消息发送到该邮箱。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-104">The **FederatedDeliveryMailbox** element represents the mailbox to which a cross-premise message was sent.</span></span> 
  
```XML
<FederatedDeliveryMailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</FederatedDeliveryMailbox>
```

 <span data-ttu-id="1bb0f-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="1bb0f-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1bb0f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1bb0f-106">Attributes and elements</span></span>

<span data-ttu-id="1bb0f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1bb0f-108">属性</span><span class="sxs-lookup"><span data-stu-id="1bb0f-108">Attributes</span></span>

<span data-ttu-id="1bb0f-109">无。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1bb0f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1bb0f-110">Child elements</span></span>

|<span data-ttu-id="1bb0f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1bb0f-111">**Element**</span></span>|<span data-ttu-id="1bb0f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1bb0f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bb0f-113">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="1bb0f-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="1bb0f-p101">定义邮箱用户的名称。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-p101">Defines the name of the mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1bb0f-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="1bb0f-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="1bb0f-p102">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1bb0f-119">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="1bb0f-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="1bb0f-p103">定义用于邮箱路由。默认值为 SMTP。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1bb0f-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="1bb0f-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="1bb0f-p104">定义邮箱用户的邮箱类型。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1bb0f-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="1bb0f-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="1bb0f-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1bb0f-129">父元素</span><span class="sxs-lookup"><span data-stu-id="1bb0f-129">Parent elements</span></span>

|<span data-ttu-id="1bb0f-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="1bb0f-130">**Element**</span></span>|<span data-ttu-id="1bb0f-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="1bb0f-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bb0f-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1bb0f-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="1bb0f-133">包含要查找的邮件的类型的条件。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-133">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1bb0f-134">文本值</span><span class="sxs-lookup"><span data-stu-id="1bb0f-134">Text value</span></span>

<span data-ttu-id="1bb0f-135">无。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1bb0f-136">备注</span><span class="sxs-lookup"><span data-stu-id="1bb0f-136">Remarks</span></span>

<span data-ttu-id="1bb0f-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1bb0f-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1bb0f-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="1bb0f-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bb0f-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="1bb0f-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1bb0f-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="1bb0f-140">Schema Name</span></span>  <br/> |<span data-ttu-id="1bb0f-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="1bb0f-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1bb0f-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="1bb0f-142">Validation File</span></span>  <br/> |<span data-ttu-id="1bb0f-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1bb0f-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1bb0f-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="1bb0f-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="1bb0f-145">False</span><span class="sxs-lookup"><span data-stu-id="1bb0f-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bb0f-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1bb0f-146">See also</span></span>



- [<span data-ttu-id="1bb0f-147">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1bb0f-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

