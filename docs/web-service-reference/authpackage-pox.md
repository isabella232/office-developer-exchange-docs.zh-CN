---
title: AuthPackage （POX）
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: AuthPackage 元素指定在对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时使用的身份验证方案。
ms.openlocfilehash: 5317cf49d354a558417829e1d1b5b67cd6874309
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459102"
---
# <a name="authpackage-pox"></a><span data-ttu-id="2c2b2-103">AuthPackage （POX）</span><span class="sxs-lookup"><span data-stu-id="2c2b2-103">AuthPackage (POX)</span></span>

<span data-ttu-id="2c2b2-104">**AuthPackage**元素指定在对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时使用的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="2c2b2-104">The **AuthPackage** element specifies the authentication scheme that is used when authenticating against the Exchange server that has the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="2c2b2-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="2c2b2-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="2c2b2-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="2c2b2-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="2c2b2-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="2c2b2-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="2c2b2-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="2c2b2-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="2c2b2-109">AuthPackage （POX）</span><span class="sxs-lookup"><span data-stu-id="2c2b2-109">AuthPackage (POX)</span></span>](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2c2b2-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2c2b2-110">Attributes and elements</span></span>

<span data-ttu-id="2c2b2-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2c2b2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c2b2-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="2c2b2-112">Attributes</span></span>

<span data-ttu-id="2c2b2-113">无。</span><span class="sxs-lookup"><span data-stu-id="2c2b2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c2b2-114">子元素</span><span class="sxs-lookup"><span data-stu-id="2c2b2-114">Child elements</span></span>

<span data-ttu-id="2c2b2-115">无。</span><span class="sxs-lookup"><span data-stu-id="2c2b2-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c2b2-116">父元素</span><span class="sxs-lookup"><span data-stu-id="2c2b2-116">Parent elements</span></span>

|<span data-ttu-id="2c2b2-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="2c2b2-117">**Element**</span></span>|<span data-ttu-id="2c2b2-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="2c2b2-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c2b2-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="2c2b2-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="2c2b2-120">包含用于将客户端连接到客户端访问服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="2c2b2-120">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2c2b2-121">文本值</span><span class="sxs-lookup"><span data-stu-id="2c2b2-121">Text value</span></span>

<span data-ttu-id="2c2b2-122">文本值指定在对邮箱服务器进行身份验证时使用的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="2c2b2-122">The text value specifies the authentication scheme that is used when authenticating against the Mailbox server.</span></span> <span data-ttu-id="2c2b2-123">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="2c2b2-123">The following are the possible values:</span></span>
  
- <span data-ttu-id="2c2b2-124">vba</span><span class="sxs-lookup"><span data-stu-id="2c2b2-124">basic</span></span>
- <span data-ttu-id="2c2b2-125">kerb</span><span class="sxs-lookup"><span data-stu-id="2c2b2-125">kerb</span></span>
- <span data-ttu-id="2c2b2-126">kerbntlm</span><span class="sxs-lookup"><span data-stu-id="2c2b2-126">kerbntlm</span></span>
- <span data-ttu-id="2c2b2-127">ntlm</span><span class="sxs-lookup"><span data-stu-id="2c2b2-127">ntlm</span></span>
- <span data-ttu-id="2c2b2-128">证书</span><span class="sxs-lookup"><span data-stu-id="2c2b2-128">certificate</span></span>
- <span data-ttu-id="2c2b2-129">沟通</span><span class="sxs-lookup"><span data-stu-id="2c2b2-129">negotiate</span></span>
- <span data-ttu-id="2c2b2-130">nego2</span><span class="sxs-lookup"><span data-stu-id="2c2b2-130">nego2</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c2b2-131">备注</span><span class="sxs-lookup"><span data-stu-id="2c2b2-131">Remarks</span></span>

<span data-ttu-id="2c2b2-132">仅当[Type （POX）](type-pox.md)元素的 text 值为 EXCH 或 EXPR 时，才使用**AuthPackage**元素。</span><span class="sxs-lookup"><span data-stu-id="2c2b2-132">The **AuthPackage** element is only used when the [Type (POX)](type-pox.md) element has a text value of EXCH or EXPR.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="2c2b2-133">版本差异</span><span class="sxs-lookup"><span data-stu-id="2c2b2-133">Version differences</span></span>

<span data-ttu-id="2c2b2-134">如果将服务器配置为使用协商身份验证，并且客户端包含包含 "协商" 的[X-ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头，则从生成15.00.0995.014 开始的 Office 365、exchange Online 和本地版本将返回 "negotiate" 值。</span><span class="sxs-lookup"><span data-stu-id="2c2b2-134">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "negotiate" only if the server is configured to use Negotiate authentication and the client includes a [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "Negotiate".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c2b2-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c2b2-135">See also</span></span>

- [<span data-ttu-id="2c2b2-136">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="2c2b2-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

