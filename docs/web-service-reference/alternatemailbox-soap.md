---
title: AlternateMailbox （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d913a70d-5a85-4b6e-becc-2fb9334b6088
description: AlternateMailbox 元素表示备用邮箱。
ms.openlocfilehash: 9019f85a373cc186cc9dadddceee3dc9d11b3854
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466155"
---
# <a name="alternatemailbox-soap"></a><span data-ttu-id="2f0a0-103">AlternateMailbox （SOAP）</span><span class="sxs-lookup"><span data-stu-id="2f0a0-103">AlternateMailbox (SOAP)</span></span>

<span data-ttu-id="2f0a0-104">**AlternateMailbox**元素表示备用邮箱。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-104">The **AlternateMailbox** element represents an alternate mailbox.</span></span> 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 <span data-ttu-id="2f0a0-105">**AlternateMailbox**</span><span class="sxs-lookup"><span data-stu-id="2f0a0-105">**AlternateMailbox**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f0a0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2f0a0-106">Attributes and elements</span></span>

<span data-ttu-id="2f0a0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f0a0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2f0a0-108">Attributes</span></span>

<span data-ttu-id="2f0a0-109">无。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f0a0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2f0a0-110">Child elements</span></span>

|<span data-ttu-id="2f0a0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f0a0-111">**Element**</span></span>|<span data-ttu-id="2f0a0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f0a0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f0a0-113">类型（SOAP）</span><span class="sxs-lookup"><span data-stu-id="2f0a0-113">Type (SOAP)</span></span>](type-soap.md) <br/> |<span data-ttu-id="2f0a0-114">代表备用邮箱类型。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-114">Represents the alternate mailbox type.</span></span>  <br/> |
|[<span data-ttu-id="2f0a0-115">DisplayName （SOAP）</span><span class="sxs-lookup"><span data-stu-id="2f0a0-115">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="2f0a0-116">表示备用邮箱的显示名称。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-116">Represents the alternate mailbox display name.</span></span>  <br/> |
|[<span data-ttu-id="2f0a0-117">LegacyDN （SOAP）</span><span class="sxs-lookup"><span data-stu-id="2f0a0-117">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="2f0a0-118">表示备用邮箱旧版可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-118">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="2f0a0-119">服务器（SOAP）</span><span class="sxs-lookup"><span data-stu-id="2f0a0-119">Server (SOAP)</span></span>](server-soap.md) <br/> |<span data-ttu-id="2f0a0-120">代表备用邮箱服务器。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-120">Represents the alternate mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="2f0a0-121">SmtpAddress （SOAP）</span><span class="sxs-lookup"><span data-stu-id="2f0a0-121">SmtpAddress (SOAP)</span></span>](smtpaddress-soap.md) <br/> |<span data-ttu-id="2f0a0-122">代表备用邮箱 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-122">Represents the alternate mailbox SMTP address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2f0a0-123">父元素</span><span class="sxs-lookup"><span data-stu-id="2f0a0-123">Parent elements</span></span>

|<span data-ttu-id="2f0a0-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f0a0-124">**Element**</span></span>|<span data-ttu-id="2f0a0-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f0a0-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f0a0-126">AlternateMailboxes （SOAP）</span><span class="sxs-lookup"><span data-stu-id="2f0a0-126">AlternateMailboxes (SOAP)</span></span>](alternatemailboxes-soap.md) <br/> |<span data-ttu-id="2f0a0-127">代表备用邮箱的集合。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-127">Represents a collection of alternate mailboxes.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2f0a0-128">文本值</span><span class="sxs-lookup"><span data-stu-id="2f0a0-128">Text value</span></span>

<span data-ttu-id="2f0a0-129">无。</span><span class="sxs-lookup"><span data-stu-id="2f0a0-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f0a0-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="2f0a0-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f0a0-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="2f0a0-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="2f0a0-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="2f0a0-132">Schema Name</span></span>  <br/> |<span data-ttu-id="2f0a0-133">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="2f0a0-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="2f0a0-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="2f0a0-134">Validation File</span></span>  <br/> |<span data-ttu-id="2f0a0-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2f0a0-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f0a0-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="2f0a0-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f0a0-137">True</span><span class="sxs-lookup"><span data-stu-id="2f0a0-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f0a0-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f0a0-138">See also</span></span>

- [<span data-ttu-id="2f0a0-139">AlternateMailboxCollectionSetting （SOAP）</span><span class="sxs-lookup"><span data-stu-id="2f0a0-139">AlternateMailboxCollectionSetting (SOAP)</span></span>](alternatemailboxcollectionsetting-soap.md)

