---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: EmailAddress 元素指定站点邮箱或相关联的角色的完全解析的 SMTP 地址。
ms.openlocfilehash: c31a37fc0dbdcc2b501b82346a17a0a3b4775556
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754042"
---
# <a name="emailaddress-emailaddresstype"></a><span data-ttu-id="84880-103">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="84880-103">EmailAddress (EmailAddressType)</span></span>

<span data-ttu-id="84880-104">**EmailAddress**元素指定站点邮箱或相关联的角色的完全解析的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="84880-104">The **EmailAddress** element specifies the fully resolved SMTP address for the site mailbox or the associated persona.</span></span> 
  
```xml
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
</EmailAddress>
```

 <span data-ttu-id="84880-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="84880-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84880-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="84880-106">Attributes and elements</span></span>

<span data-ttu-id="84880-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="84880-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84880-108">属性</span><span class="sxs-lookup"><span data-stu-id="84880-108">Attributes</span></span>

<span data-ttu-id="84880-109">无。</span><span class="sxs-lookup"><span data-stu-id="84880-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84880-110">子元素</span><span class="sxs-lookup"><span data-stu-id="84880-110">Child elements</span></span>

|<span data-ttu-id="84880-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="84880-111">**Element**</span></span>|<span data-ttu-id="84880-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="84880-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84880-113">名称 （字符串）</span><span class="sxs-lookup"><span data-stu-id="84880-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="84880-114">指定搜索精简条件名称或键或电子邮件用户的名称。</span><span class="sxs-lookup"><span data-stu-id="84880-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="84880-115">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="84880-115">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="84880-116">定义邮箱用户的主 SMTP 的地址。</span><span class="sxs-lookup"><span data-stu-id="84880-116">Defines the primary SMTP address of a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="84880-117">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="84880-117">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md) <br/> |<span data-ttu-id="84880-118">指定传送的电子邮件地址类型。</span><span class="sxs-lookup"><span data-stu-id="84880-118">Specifies the routing type of an email address.</span></span>  <br/> |
|[<span data-ttu-id="84880-119">MailboxType</span><span class="sxs-lookup"><span data-stu-id="84880-119">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="84880-120">表示由的电子邮件地址的邮箱的类型。</span><span class="sxs-lookup"><span data-stu-id="84880-120">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="84880-121">ItemId</span><span class="sxs-lookup"><span data-stu-id="84880-121">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="84880-122">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="84880-122">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84880-123">父元素</span><span class="sxs-lookup"><span data-stu-id="84880-123">Parent elements</span></span>

|<span data-ttu-id="84880-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="84880-124">**Element**</span></span>|<span data-ttu-id="84880-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="84880-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84880-126">角色</span><span class="sxs-lookup"><span data-stu-id="84880-126">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="84880-127">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="84880-127">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="84880-128">文本值</span><span class="sxs-lookup"><span data-stu-id="84880-128">Text value</span></span>

<span data-ttu-id="84880-129">无。</span><span class="sxs-lookup"><span data-stu-id="84880-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84880-130">备注</span><span class="sxs-lookup"><span data-stu-id="84880-130">Remarks</span></span>

<span data-ttu-id="84880-131">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="84880-131">This element is optional.</span></span>
  
<span data-ttu-id="84880-132">适用于 Exchange Online 和版本的开头 Exchange 2013 的 Microsoft Exchange Server 的目标设定的客户端的**EmailAddress**元素。</span><span class="sxs-lookup"><span data-stu-id="84880-132">The **EmailAddress** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="84880-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="84880-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84880-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="84880-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84880-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="84880-135">Schema Name</span></span>  <br/> |<span data-ttu-id="84880-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="84880-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="84880-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="84880-137">Validation File</span></span>  <br/> |<span data-ttu-id="84880-138">types.xsd</span><span class="sxs-lookup"><span data-stu-id="84880-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="84880-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="84880-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="84880-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84880-140">See also</span></span>

- [<span data-ttu-id="84880-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="84880-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

