---
title: EmailAddress （GetPersonaType）
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 052055b5-4630-40ed-9b24-9e7f4bf7ba1d
description: EmailAddress （GetPersonaType）元素指定与角色关联的电子邮件地址。
ms.openlocfilehash: b58f61202cd94ff282b21138b47b40887b38752a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463452"
---
# <a name="emailaddress-getpersonatype"></a><span data-ttu-id="6f242-103">EmailAddress （GetPersonaType）</span><span class="sxs-lookup"><span data-stu-id="6f242-103">EmailAddress (GetPersonaType)</span></span>

<span data-ttu-id="6f242-104">**EmailAddress （GetPersonaType）** 元素指定与角色关联的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="6f242-104">The **EmailAddress (GetPersonaType)** element specifies the email address associated with the persona.</span></span> 
  
```XML
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
    <OriginalDisplayName></OriginalDisplayName>
</EmailAddress>>
```

 <span data-ttu-id="6f242-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="6f242-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f242-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f242-106">Attributes and elements</span></span>

<span data-ttu-id="6f242-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f242-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f242-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6f242-108">Attributes</span></span>

<span data-ttu-id="6f242-109">无。</span><span class="sxs-lookup"><span data-stu-id="6f242-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f242-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6f242-110">Child elements</span></span>

<span data-ttu-id="6f242-111">[名称（字符串）](name-string.md)  | [EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)  | [RoutingType （EmailAddressType）](routingtype-emailaddresstype.md)  | [MailboxType](mailboxtype.md)  | [ItemId](itemid.md)  | [OriginalDisplayName](originaldisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="6f242-111">[Name (string)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f242-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6f242-112">Parent elements</span></span>

[<span data-ttu-id="6f242-113">GetPersona</span><span class="sxs-lookup"><span data-stu-id="6f242-113">GetPersona</span></span>](getpersona.md)
  
## <a name="remarks"></a><span data-ttu-id="6f242-114">说明</span><span class="sxs-lookup"><span data-stu-id="6f242-114">Remarks</span></span>

<span data-ttu-id="6f242-115">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6f242-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="6f242-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6f242-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f242-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f242-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f242-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f242-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6f242-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f242-119">Schema Name</span></span>  <br/> |<span data-ttu-id="6f242-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="6f242-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6f242-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f242-121">Validation File</span></span>  <br/> |<span data-ttu-id="6f242-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6f242-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6f242-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f242-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f242-124">True</span><span class="sxs-lookup"><span data-stu-id="6f242-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f242-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f242-125">See also</span></span>

- [<span data-ttu-id="6f242-126">GetPersona</span><span class="sxs-lookup"><span data-stu-id="6f242-126">GetPersona</span></span>](getpersona.md)
- [<span data-ttu-id="6f242-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6f242-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

