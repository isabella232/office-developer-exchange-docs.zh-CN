---
title: 用户 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: User 元素提供特定于用户的信息。
ms.openlocfilehash: 3f90ff0cc00170170c7304f2a19fe1d7abd9d1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838456"
---
# <a name="user-pox"></a><span data-ttu-id="0d9d9-103">用户 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d9d9-103">User (POX)</span></span>

<span data-ttu-id="0d9d9-104">**User**元素提供特定于用户的信息。</span><span class="sxs-lookup"><span data-stu-id="0d9d9-104">The **User** element provides user-specific information.</span></span> 
  
[<span data-ttu-id="0d9d9-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d9d9-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="0d9d9-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d9d9-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="0d9d9-107">用户 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d9d9-107">User (POX)</span></span>](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0d9d9-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0d9d9-108">Attributes and elements</span></span>

<span data-ttu-id="0d9d9-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0d9d9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d9d9-110">属性</span><span class="sxs-lookup"><span data-stu-id="0d9d9-110">Attributes</span></span>

<span data-ttu-id="0d9d9-111">无。</span><span class="sxs-lookup"><span data-stu-id="0d9d9-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d9d9-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0d9d9-112">Child elements</span></span>

|<span data-ttu-id="0d9d9-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0d9d9-113">**Element**</span></span>|<span data-ttu-id="0d9d9-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d9d9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d9d9-115">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="0d9d9-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="0d9d9-116">代表用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="0d9d9-116">Represents the user's display name.</span></span>  <br/> |
|[<span data-ttu-id="0d9d9-117">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="0d9d9-117">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="0d9d9-118">通过旧的可分辨名称标识用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="0d9d9-118">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="0d9d9-119">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="0d9d9-119">DeploymentId (POX)</span></span>](deploymentid-pox.md) <br/> |<span data-ttu-id="0d9d9-120">唯一标识 Exchange 林。</span><span class="sxs-lookup"><span data-stu-id="0d9d9-120">Uniquely identifies the Exchange forest.</span></span>  <br/> |
|[<span data-ttu-id="0d9d9-121">AutoDiscoverSMTPAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="0d9d9-121">AutoDiscoverSMTPAddress (POX)</span></span>](autodiscoversmtpaddress-pox.md) <br/> |<span data-ttu-id="0d9d9-122">包含用于自动发现过程的用户的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="0d9d9-122">Contains the user's SMTP address that is used for the Autodiscover process.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d9d9-123">父元素</span><span class="sxs-lookup"><span data-stu-id="0d9d9-123">Parent elements</span></span>

|<span data-ttu-id="0d9d9-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="0d9d9-124">**Element**</span></span>|<span data-ttu-id="0d9d9-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d9d9-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d9d9-126">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d9d9-126">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="0d9d9-127">包含来自自动发现服务的响应。</span><span class="sxs-lookup"><span data-stu-id="0d9d9-127">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d9d9-128">注解</span><span class="sxs-lookup"><span data-stu-id="0d9d9-128">Remarks</span></span>

<span data-ttu-id="0d9d9-129">自动发现请求和响应必须为 utf-8 编码。</span><span class="sxs-lookup"><span data-stu-id="0d9d9-129">Autodiscover requests and responses must be UTF-8 encoded.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d9d9-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0d9d9-130">See also</span></span>



[<span data-ttu-id="0d9d9-131">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="0d9d9-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

