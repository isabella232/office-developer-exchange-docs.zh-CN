---
title: User （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: User 元素提供用户特定的信息。
ms.openlocfilehash: 8f53319bcf34595305748adafc9aa1e25283611e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530216"
---
# <a name="user-pox"></a><span data-ttu-id="d4b20-103">User （POX）</span><span class="sxs-lookup"><span data-stu-id="d4b20-103">User (POX)</span></span>

<span data-ttu-id="d4b20-104">**User**元素提供用户特定的信息。</span><span class="sxs-lookup"><span data-stu-id="d4b20-104">The **User** element provides user-specific information.</span></span> 
  
[<span data-ttu-id="d4b20-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="d4b20-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="d4b20-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="d4b20-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="d4b20-107">User （POX）</span><span class="sxs-lookup"><span data-stu-id="d4b20-107">User (POX)</span></span>](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d4b20-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d4b20-108">Attributes and elements</span></span>

<span data-ttu-id="d4b20-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d4b20-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4b20-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="d4b20-110">Attributes</span></span>

<span data-ttu-id="d4b20-111">无。</span><span class="sxs-lookup"><span data-stu-id="d4b20-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4b20-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d4b20-112">Child elements</span></span>

|<span data-ttu-id="d4b20-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d4b20-113">**Element**</span></span>|<span data-ttu-id="d4b20-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d4b20-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4b20-115">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="d4b20-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="d4b20-116">表示用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="d4b20-116">Represents the user's display name.</span></span>  <br/> |
|[<span data-ttu-id="d4b20-117">LegacyDN （POX）</span><span class="sxs-lookup"><span data-stu-id="d4b20-117">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="d4b20-118">通过旧版可分辨名称标识用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="d4b20-118">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="d4b20-119">DeploymentId （POX）</span><span class="sxs-lookup"><span data-stu-id="d4b20-119">DeploymentId (POX)</span></span>](deploymentid-pox.md) <br/> |<span data-ttu-id="d4b20-120">唯一标识 Exchange 林。</span><span class="sxs-lookup"><span data-stu-id="d4b20-120">Uniquely identifies the Exchange forest.</span></span>  <br/> |
|[<span data-ttu-id="d4b20-121">AutoDiscoverSMTPAddress （POX）</span><span class="sxs-lookup"><span data-stu-id="d4b20-121">AutoDiscoverSMTPAddress (POX)</span></span>](autodiscoversmtpaddress-pox.md) <br/> |<span data-ttu-id="d4b20-122">包含用于自动发现过程的用户的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="d4b20-122">Contains the user's SMTP address that is used for the Autodiscover process.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d4b20-123">父元素</span><span class="sxs-lookup"><span data-stu-id="d4b20-123">Parent elements</span></span>

|<span data-ttu-id="d4b20-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="d4b20-124">**Element**</span></span>|<span data-ttu-id="d4b20-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="d4b20-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4b20-126">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="d4b20-126">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="d4b20-127">包含来自自动发现服务的响应。</span><span class="sxs-lookup"><span data-stu-id="d4b20-127">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4b20-128">备注</span><span class="sxs-lookup"><span data-stu-id="d4b20-128">Remarks</span></span>

<span data-ttu-id="d4b20-129">自动发现请求和响应必须是 UTF-8 编码的。</span><span class="sxs-lookup"><span data-stu-id="d4b20-129">Autodiscover requests and responses must be UTF-8 encoded.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d4b20-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d4b20-130">See also</span></span>



[<span data-ttu-id="d4b20-131">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="d4b20-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

