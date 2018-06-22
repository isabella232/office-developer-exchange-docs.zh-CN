---
title: AlternateMailbox (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d913a70d-5a85-4b6e-becc-2fb9334b6088
description: AlternateMailbox 元素均表示一个备用的邮箱。
ms.openlocfilehash: 8eb53e4846ad55916e2c5876606c00c0f2e371ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2018
ms.locfileid: "19753193"
---
# <a name="alternatemailbox-soap"></a><span data-ttu-id="e3331-103">AlternateMailbox (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3331-103">AlternateMailbox (SOAP)</span></span>

<span data-ttu-id="e3331-104">**AlternateMailbox**元素均表示一个备用的邮箱。</span><span class="sxs-lookup"><span data-stu-id="e3331-104">The **AlternateMailbox** element represents an alternate mailbox.</span></span> 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 <span data-ttu-id="e3331-105">**AlternateMailbox**</span><span class="sxs-lookup"><span data-stu-id="e3331-105">**AlternateMailbox**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3331-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e3331-106">Attributes and elements</span></span>

<span data-ttu-id="e3331-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e3331-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3331-108">属性</span><span class="sxs-lookup"><span data-stu-id="e3331-108">Attributes</span></span>

<span data-ttu-id="e3331-109">无。</span><span class="sxs-lookup"><span data-stu-id="e3331-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3331-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e3331-110">Child elements</span></span>

|<span data-ttu-id="e3331-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e3331-111">**Element**</span></span>|<span data-ttu-id="e3331-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3331-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3331-113">类型 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3331-113">Type (SOAP)</span></span>](type-soap.md) <br/> |<span data-ttu-id="e3331-114">表示的备用邮箱类型。</span><span class="sxs-lookup"><span data-stu-id="e3331-114">Represents the alternate mailbox type.</span></span>  <br/> |
|[<span data-ttu-id="e3331-115">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3331-115">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="e3331-116">代表备用邮箱的显示名称。</span><span class="sxs-lookup"><span data-stu-id="e3331-116">Represents the alternate mailbox display name.</span></span>  <br/> |
|[<span data-ttu-id="e3331-117">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3331-117">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="e3331-118">代表旧的备用邮箱的可分辨的名称。</span><span class="sxs-lookup"><span data-stu-id="e3331-118">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="e3331-119">服务器 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3331-119">Server (SOAP)</span></span>](server-soap.md) <br/> |<span data-ttu-id="e3331-120">代表备用的邮箱服务器。</span><span class="sxs-lookup"><span data-stu-id="e3331-120">Represents the alternate mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="e3331-121">SmtpAddress (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3331-121">SmtpAddress (SOAP)</span></span>](smtpaddress-soap.md) <br/> |<span data-ttu-id="e3331-122">代表备用邮箱的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="e3331-122">Represents the alternate mailbox SMTP address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e3331-123">父元素</span><span class="sxs-lookup"><span data-stu-id="e3331-123">Parent elements</span></span>

|<span data-ttu-id="e3331-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="e3331-124">**Element**</span></span>|<span data-ttu-id="e3331-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3331-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3331-126">AlternateMailboxes (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3331-126">AlternateMailboxes (SOAP)</span></span>](alternatemailboxes-soap.md) <br/> |<span data-ttu-id="e3331-127">表示备用邮箱的集合。</span><span class="sxs-lookup"><span data-stu-id="e3331-127">Represents a collection of alternate mailboxes.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3331-128">文本值</span><span class="sxs-lookup"><span data-stu-id="e3331-128">Text value</span></span>

<span data-ttu-id="e3331-129">无。</span><span class="sxs-lookup"><span data-stu-id="e3331-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3331-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="e3331-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3331-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="e3331-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e3331-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="e3331-132">Schema Name</span></span>  <br/> |<span data-ttu-id="e3331-133">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="e3331-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e3331-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="e3331-134">Validation File</span></span>  <br/> |<span data-ttu-id="e3331-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e3331-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3331-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="e3331-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3331-137">True</span><span class="sxs-lookup"><span data-stu-id="e3331-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3331-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3331-138">See also</span></span>

- [<span data-ttu-id="e3331-139">AlternateMailboxCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3331-139">AlternateMailboxCollectionSetting (SOAP)</span></span>](alternatemailboxcollectionsetting-soap.md)
