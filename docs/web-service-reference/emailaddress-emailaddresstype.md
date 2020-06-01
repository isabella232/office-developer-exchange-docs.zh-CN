---
title: EmailAddress （EmailAddressType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: EmailAddress 元素指定网站邮箱或关联角色的完全解析的 SMTP 地址。
ms.openlocfilehash: 8b04b75e91cc16be7f88c9a0ac08c5e36855056e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463459"
---
# <a name="emailaddress-emailaddresstype"></a><span data-ttu-id="f6b1e-103">EmailAddress （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="f6b1e-103">EmailAddress (EmailAddressType)</span></span>

<span data-ttu-id="f6b1e-104">**EmailAddress**元素指定网站邮箱或关联角色的完全解析的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-104">The **EmailAddress** element specifies the fully resolved SMTP address for the site mailbox or the associated persona.</span></span> 
  
```xml
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
</EmailAddress>
```

 <span data-ttu-id="f6b1e-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="f6b1e-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f6b1e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f6b1e-106">Attributes and elements</span></span>

<span data-ttu-id="f6b1e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6b1e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f6b1e-108">Attributes</span></span>

<span data-ttu-id="f6b1e-109">无。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6b1e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f6b1e-110">Child elements</span></span>

|<span data-ttu-id="f6b1e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f6b1e-111">**Element**</span></span>|<span data-ttu-id="f6b1e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f6b1e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6b1e-113">名称（字符串）</span><span class="sxs-lookup"><span data-stu-id="f6b1e-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="f6b1e-114">指定一个搜索精简程序名称或密钥或电子邮件用户的名称。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="f6b1e-115">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="f6b1e-115">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="f6b1e-116">定义邮箱用户的主 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-116">Defines the primary SMTP address of a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="f6b1e-117">RoutingType （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="f6b1e-117">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md) <br/> |<span data-ttu-id="f6b1e-118">指定电子邮件地址的路由类型。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-118">Specifies the routing type of an email address.</span></span>  <br/> |
|[<span data-ttu-id="f6b1e-119">MailboxType</span><span class="sxs-lookup"><span data-stu-id="f6b1e-119">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="f6b1e-120">代表电子邮件地址所代表的邮箱类型。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-120">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="f6b1e-121">ItemId</span><span class="sxs-lookup"><span data-stu-id="f6b1e-121">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f6b1e-122">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-122">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f6b1e-123">父元素</span><span class="sxs-lookup"><span data-stu-id="f6b1e-123">Parent elements</span></span>

|<span data-ttu-id="f6b1e-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="f6b1e-124">**Element**</span></span>|<span data-ttu-id="f6b1e-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="f6b1e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6b1e-126">角色</span><span class="sxs-lookup"><span data-stu-id="f6b1e-126">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="f6b1e-127">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-127">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f6b1e-128">文本值</span><span class="sxs-lookup"><span data-stu-id="f6b1e-128">Text value</span></span>

<span data-ttu-id="f6b1e-129">无。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6b1e-130">说明</span><span class="sxs-lookup"><span data-stu-id="f6b1e-130">Remarks</span></span>

<span data-ttu-id="f6b1e-131">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-131">This element is optional.</span></span>
  
<span data-ttu-id="f6b1e-132">**EmailAddress**元素适用于面向 exchange Online 的客户端和从 exchange 2013 开始的 Microsoft Exchange Server 版本。</span><span class="sxs-lookup"><span data-stu-id="f6b1e-132">The **EmailAddress** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f6b1e-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="f6b1e-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6b1e-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="f6b1e-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f6b1e-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="f6b1e-135">Schema Name</span></span>  <br/> |<span data-ttu-id="f6b1e-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="f6b1e-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="f6b1e-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="f6b1e-137">Validation File</span></span>  <br/> |<span data-ttu-id="f6b1e-138">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="f6b1e-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f6b1e-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="f6b1e-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f6b1e-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f6b1e-140">See also</span></span>

- [<span data-ttu-id="f6b1e-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f6b1e-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

