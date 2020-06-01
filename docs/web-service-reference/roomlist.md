---
title: RoomList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoomList
api_type:
- schema
ms.assetid: cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2
description: RoomList 元素表示标识会议室列表的电子邮件地址。
ms.openlocfilehash: 0444475cb9fffbb89ba2861096baee0c7e645995
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460517"
---
# <a name="roomlist"></a><span data-ttu-id="8385c-103">RoomList</span><span class="sxs-lookup"><span data-stu-id="8385c-103">RoomList</span></span>

<span data-ttu-id="8385c-104">**RoomList**元素表示标识会议室列表的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="8385c-104">The **RoomList** element represents an e-mail address that identifies a list of meeting rooms.</span></span> 
  
[<span data-ttu-id="8385c-105">GetRooms</span><span class="sxs-lookup"><span data-stu-id="8385c-105">GetRooms</span></span>](getrooms.md)
  
[<span data-ttu-id="8385c-106">RoomList</span><span class="sxs-lookup"><span data-stu-id="8385c-106">RoomList</span></span>](roomlist.md)
  
```XML
<RoomList>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RoomList>
```

 <span data-ttu-id="8385c-107">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="8385c-107">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8385c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8385c-108">Attributes and elements</span></span>

<span data-ttu-id="8385c-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8385c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8385c-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="8385c-110">Attributes</span></span>

<span data-ttu-id="8385c-111">无。</span><span class="sxs-lookup"><span data-stu-id="8385c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8385c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="8385c-112">Child elements</span></span>

|<span data-ttu-id="8385c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8385c-113">**Element**</span></span>|<span data-ttu-id="8385c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8385c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8385c-115">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="8385c-115">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="8385c-116">定义会议室列表的显示名称。</span><span class="sxs-lookup"><span data-stu-id="8385c-116">Defines the display name of the room list.</span></span> <span data-ttu-id="8385c-117">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="8385c-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8385c-118">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="8385c-118">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="8385c-119">定义会议室列表的简单邮件传输协议（SMTP）地址。</span><span class="sxs-lookup"><span data-stu-id="8385c-119">Defines the Simple Mail Transfer Protocol (SMTP) address of a room list.</span></span> <span data-ttu-id="8385c-120">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="8385c-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8385c-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="8385c-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="8385c-p103">定义用于邮箱路由。默认值为 SMTP。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8385c-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8385c-125">MailboxType</span><span class="sxs-lookup"><span data-stu-id="8385c-125">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="8385c-p104">定义邮箱用户的邮箱类型。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8385c-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8385c-128">ItemId</span><span class="sxs-lookup"><span data-stu-id="8385c-128">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="8385c-p105">定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8385c-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8385c-131">父元素</span><span class="sxs-lookup"><span data-stu-id="8385c-131">Parent elements</span></span>

|<span data-ttu-id="8385c-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="8385c-132">**Element**</span></span>|<span data-ttu-id="8385c-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="8385c-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8385c-134">GetRooms</span><span class="sxs-lookup"><span data-stu-id="8385c-134">GetRooms</span></span>](getrooms.md) <br/> |<span data-ttu-id="8385c-135">请求中的根元素，用于获取特定聊天室列表中的聊天室列表。</span><span class="sxs-lookup"><span data-stu-id="8385c-135">The root element in a request to get a list of rooms within a particular room list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8385c-136">文本值</span><span class="sxs-lookup"><span data-stu-id="8385c-136">Text value</span></span>

<span data-ttu-id="8385c-137">无。</span><span class="sxs-lookup"><span data-stu-id="8385c-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8385c-138">说明</span><span class="sxs-lookup"><span data-stu-id="8385c-138">Remarks</span></span>

<span data-ttu-id="8385c-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8385c-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8385c-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="8385c-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8385c-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="8385c-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8385c-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="8385c-142">Schema Name</span></span>  <br/> |<span data-ttu-id="8385c-143">消息架构</span><span class="sxs-lookup"><span data-stu-id="8385c-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8385c-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="8385c-144">Validation File</span></span>  <br/> |<span data-ttu-id="8385c-145">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8385c-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8385c-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="8385c-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="8385c-147">False</span><span class="sxs-lookup"><span data-stu-id="8385c-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8385c-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8385c-148">See also</span></span>



[<span data-ttu-id="8385c-149">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="8385c-149">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="8385c-150">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8385c-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

