---
title: 用户 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6bc0031-bc1d-41bd-84e4-9074a5b77012
description: User 元素表示单个用户的标识。
ms.openlocfilehash: a8dcb22f5c74a9622f978f34e48146115351fe82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838459"
---
# <a name="user-soap"></a><span data-ttu-id="04f57-103">用户 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04f57-103">User (SOAP)</span></span>

<span data-ttu-id="04f57-104">**User**元素表示单个用户的标识。</span><span class="sxs-lookup"><span data-stu-id="04f57-104">The **User** element represents the identity of a single user.</span></span> 
  
```XML
<User>
    <LegacyDN/>
    <Mailbox/>
    <RequestedSettings/>
</User>
```

 <span data-ttu-id="04f57-105">**User**</span><span class="sxs-lookup"><span data-stu-id="04f57-105">**User**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04f57-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="04f57-106">Attributes and elements</span></span>

<span data-ttu-id="04f57-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="04f57-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04f57-108">属性</span><span class="sxs-lookup"><span data-stu-id="04f57-108">Attributes</span></span>

<span data-ttu-id="04f57-109">无。</span><span class="sxs-lookup"><span data-stu-id="04f57-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04f57-110">子元素</span><span class="sxs-lookup"><span data-stu-id="04f57-110">Child elements</span></span>

|<span data-ttu-id="04f57-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="04f57-111">**Element**</span></span>|<span data-ttu-id="04f57-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="04f57-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04f57-113">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04f57-113">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="04f57-114">代表旧的备用邮箱的可分辨的名称。</span><span class="sxs-lookup"><span data-stu-id="04f57-114">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="04f57-115">邮箱 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04f57-115">Mailbox (SOAP)</span></span>](mailbox-soap.md) <br/> |<span data-ttu-id="04f57-116">包含用户发现的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="04f57-116">Contains the e-mail address of the user to be discovered.</span></span>  <br/> |
|[<span data-ttu-id="04f57-117">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04f57-117">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="04f57-118">包含请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="04f57-118">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="04f57-119">父元素</span><span class="sxs-lookup"><span data-stu-id="04f57-119">Parent elements</span></span>

|<span data-ttu-id="04f57-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="04f57-120">**Element**</span></span>|<span data-ttu-id="04f57-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="04f57-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04f57-122">用户 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04f57-122">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="04f57-123">代表**用户**元素的集合。</span><span class="sxs-lookup"><span data-stu-id="04f57-123">Represents a collection of **User** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="04f57-124">文本值</span><span class="sxs-lookup"><span data-stu-id="04f57-124">Text value</span></span>

<span data-ttu-id="04f57-125">无。</span><span class="sxs-lookup"><span data-stu-id="04f57-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04f57-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="04f57-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04f57-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="04f57-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="04f57-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="04f57-128">Schema Name</span></span>  <br/> |<span data-ttu-id="04f57-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="04f57-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="04f57-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="04f57-130">Validation File</span></span>  <br/> |<span data-ttu-id="04f57-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="04f57-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="04f57-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="04f57-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="04f57-133">True</span><span class="sxs-lookup"><span data-stu-id="04f57-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04f57-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04f57-134">See also</span></span>



[<span data-ttu-id="04f57-135">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04f57-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="04f57-136">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04f57-136">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="04f57-137">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04f57-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

