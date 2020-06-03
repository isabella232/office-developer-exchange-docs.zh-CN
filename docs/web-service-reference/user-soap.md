---
title: User （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6bc0031-bc1d-41bd-84e4-9074a5b77012
description: User 元素表示单个用户的标识。
ms.openlocfilehash: f151ffa8050a10cdbb4562471d815f8692596cc3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456344"
---
# <a name="user-soap"></a><span data-ttu-id="6c684-103">User （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c684-103">User (SOAP)</span></span>

<span data-ttu-id="6c684-104">**User**元素表示单个用户的标识。</span><span class="sxs-lookup"><span data-stu-id="6c684-104">The **User** element represents the identity of a single user.</span></span> 
  
```XML
<User>
    <LegacyDN/>
    <Mailbox/>
    <RequestedSettings/>
</User>
```

 <span data-ttu-id="6c684-105">**用户**</span><span class="sxs-lookup"><span data-stu-id="6c684-105">**User**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c684-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6c684-106">Attributes and elements</span></span>

<span data-ttu-id="6c684-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6c684-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c684-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6c684-108">Attributes</span></span>

<span data-ttu-id="6c684-109">无。</span><span class="sxs-lookup"><span data-stu-id="6c684-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c684-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6c684-110">Child elements</span></span>

|<span data-ttu-id="6c684-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c684-111">**Element**</span></span>|<span data-ttu-id="6c684-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c684-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c684-113">LegacyDN （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c684-113">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="6c684-114">表示备用邮箱旧版可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="6c684-114">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="6c684-115">邮箱（SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c684-115">Mailbox (SOAP)</span></span>](mailbox-soap.md) <br/> |<span data-ttu-id="6c684-116">包含要发现的用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="6c684-116">Contains the e-mail address of the user to be discovered.</span></span>  <br/> |
|[<span data-ttu-id="6c684-117">RequestedSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c684-117">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="6c684-118">包含所请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="6c684-118">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6c684-119">父元素</span><span class="sxs-lookup"><span data-stu-id="6c684-119">Parent elements</span></span>

|<span data-ttu-id="6c684-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c684-120">**Element**</span></span>|<span data-ttu-id="6c684-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c684-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c684-122">Users （SOAP）</span><span class="sxs-lookup"><span data-stu-id="6c684-122">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="6c684-123">表示**用户**元素的集合。</span><span class="sxs-lookup"><span data-stu-id="6c684-123">Represents a collection of **User** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6c684-124">文本值</span><span class="sxs-lookup"><span data-stu-id="6c684-124">Text value</span></span>

<span data-ttu-id="6c684-125">无。</span><span class="sxs-lookup"><span data-stu-id="6c684-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c684-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="6c684-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c684-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="6c684-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6c684-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="6c684-128">Schema Name</span></span>  <br/> |<span data-ttu-id="6c684-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="6c684-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6c684-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="6c684-130">Validation File</span></span>  <br/> |<span data-ttu-id="6c684-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6c684-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6c684-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="6c684-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c684-133">True</span><span class="sxs-lookup"><span data-stu-id="6c684-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c684-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c684-134">See also</span></span>



[<span data-ttu-id="6c684-135">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6c684-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="6c684-136">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6c684-136">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="6c684-137">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6c684-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

