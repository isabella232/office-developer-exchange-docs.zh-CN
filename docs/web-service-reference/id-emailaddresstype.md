---
title: Id (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Id
api_type:
- schema
ms.assetid: 3e1e37b5-5469-4447-ad1f-c2c6d4e0482f
description: Id 元素标识在 Exchange server 组织内的会议室。
ms.openlocfilehash: 5cd62f6f4e5912d2ecccda352be15c6a3b24e06c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825847"
---
# <a name="id-emailaddresstype"></a><span data-ttu-id="aec1d-103">Id (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="aec1d-103">Id (EmailAddressType)</span></span>

<span data-ttu-id="aec1d-104">**Id**元素标识在 Exchange server 组织内的会议室。</span><span class="sxs-lookup"><span data-stu-id="aec1d-104">The **Id** element identifies a meeting room within the Exchange server organization.</span></span> 
  
[<span data-ttu-id="aec1d-105">聊天室</span><span class="sxs-lookup"><span data-stu-id="aec1d-105">Room</span></span>](room.md)
  
[<span data-ttu-id="aec1d-106">Id (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="aec1d-106">Id (EmailAddressType)</span></span>](id-emailaddresstype.md)
  
```xml
<Id>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Id>
```

 <span data-ttu-id="aec1d-107">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="aec1d-107">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aec1d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aec1d-108">Attributes and elements</span></span>

<span data-ttu-id="aec1d-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aec1d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aec1d-110">属性</span><span class="sxs-lookup"><span data-stu-id="aec1d-110">Attributes</span></span>

<span data-ttu-id="aec1d-111">无。</span><span class="sxs-lookup"><span data-stu-id="aec1d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aec1d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="aec1d-112">Child elements</span></span>

|<span data-ttu-id="aec1d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="aec1d-113">**Element**</span></span>|<span data-ttu-id="aec1d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="aec1d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aec1d-115">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="aec1d-115">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="aec1d-116">定义会议室的名称。</span><span class="sxs-lookup"><span data-stu-id="aec1d-116">Defines the name of the meeting room.</span></span> <span data-ttu-id="aec1d-117">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="aec1d-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="aec1d-118">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="aec1d-118">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="aec1d-119">定义会议室的简单邮件传输协议 (SMTP) 的地址。</span><span class="sxs-lookup"><span data-stu-id="aec1d-119">Defines the Simple Mail Transfer Protocol (SMTP) address of a meeting room.</span></span> <span data-ttu-id="aec1d-120">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="aec1d-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="aec1d-121">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="aec1d-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="aec1d-p103">定义用于邮箱路由。默认值为 SMTP。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="aec1d-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="aec1d-125">MailboxType</span><span class="sxs-lookup"><span data-stu-id="aec1d-125">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="aec1d-p104">定义邮箱用户的邮箱类型。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="aec1d-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="aec1d-128">ItemId</span><span class="sxs-lookup"><span data-stu-id="aec1d-128">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="aec1d-p105">定义用户联系人文件夹收件人的联系人或私人通讯组列表的项标识符。此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="aec1d-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aec1d-131">父元素</span><span class="sxs-lookup"><span data-stu-id="aec1d-131">Parent elements</span></span>

|<span data-ttu-id="aec1d-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="aec1d-132">**Element**</span></span>|<span data-ttu-id="aec1d-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="aec1d-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aec1d-134">聊天室</span><span class="sxs-lookup"><span data-stu-id="aec1d-134">Room</span></span>](room.md) <br/> |<span data-ttu-id="aec1d-135">Exchange server 组织中定义会议室。</span><span class="sxs-lookup"><span data-stu-id="aec1d-135">Defines a meeting room in the Exchange server organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aec1d-136">备注</span><span class="sxs-lookup"><span data-stu-id="aec1d-136">Remarks</span></span>

<span data-ttu-id="aec1d-137">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 目录中。</span><span class="sxs-lookup"><span data-stu-id="aec1d-137">The schema that describes this element is located in the EWS directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aec1d-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="aec1d-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aec1d-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="aec1d-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aec1d-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="aec1d-140">Schema Name</span></span>  <br/> |<span data-ttu-id="aec1d-141">类型架构</span><span class="sxs-lookup"><span data-stu-id="aec1d-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="aec1d-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="aec1d-142">Validation File</span></span>  <br/> |<span data-ttu-id="aec1d-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aec1d-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aec1d-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="aec1d-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="aec1d-145">False</span><span class="sxs-lookup"><span data-stu-id="aec1d-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aec1d-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aec1d-146">See also</span></span>



[<span data-ttu-id="aec1d-147">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="aec1d-147">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="aec1d-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="aec1d-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

