---
title: AuthPackage (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: AuthPackage 元素指定针对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时使用的身份验证方案。
ms.openlocfilehash: 120ec00ac82166ae2002a8fbac0edf9a1e23afc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753294"
---
# <a name="authpackage-pox"></a><span data-ttu-id="f71c1-103">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="f71c1-103">AuthPackage (POX)</span></span>

<span data-ttu-id="f71c1-104">**AuthPackage**元素指定针对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时使用的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="f71c1-104">The **AuthPackage** element specifies the authentication scheme that is used when authenticating against the Exchange server that has the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="f71c1-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="f71c1-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="f71c1-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="f71c1-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="f71c1-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="f71c1-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="f71c1-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="f71c1-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="f71c1-109">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="f71c1-109">AuthPackage (POX)</span></span>](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f71c1-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f71c1-110">Attributes and elements</span></span>

<span data-ttu-id="f71c1-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f71c1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f71c1-112">属性</span><span class="sxs-lookup"><span data-stu-id="f71c1-112">Attributes</span></span>

<span data-ttu-id="f71c1-113">无。</span><span class="sxs-lookup"><span data-stu-id="f71c1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f71c1-114">子元素</span><span class="sxs-lookup"><span data-stu-id="f71c1-114">Child elements</span></span>

<span data-ttu-id="f71c1-115">无。</span><span class="sxs-lookup"><span data-stu-id="f71c1-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f71c1-116">父元素</span><span class="sxs-lookup"><span data-stu-id="f71c1-116">Parent elements</span></span>

|<span data-ttu-id="f71c1-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="f71c1-117">**Element**</span></span>|<span data-ttu-id="f71c1-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="f71c1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f71c1-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="f71c1-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="f71c1-120">包含客户端连接到客户端访问服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="f71c1-120">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f71c1-121">文本值</span><span class="sxs-lookup"><span data-stu-id="f71c1-121">Text value</span></span>

<span data-ttu-id="f71c1-122">文本值指定对邮箱服务器进行身份验证时使用的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="f71c1-122">The text value specifies the authentication scheme that is used when authenticating against the Mailbox server.</span></span> <span data-ttu-id="f71c1-123">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="f71c1-123">The following are the possible values:</span></span>
  
- <span data-ttu-id="f71c1-124">基本</span><span class="sxs-lookup"><span data-stu-id="f71c1-124">basic</span></span>
- <span data-ttu-id="f71c1-125">kerb</span><span class="sxs-lookup"><span data-stu-id="f71c1-125">kerb</span></span>
- <span data-ttu-id="f71c1-126">kerbntlm</span><span class="sxs-lookup"><span data-stu-id="f71c1-126">kerbntlm</span></span>
- <span data-ttu-id="f71c1-127">ntlm</span><span class="sxs-lookup"><span data-stu-id="f71c1-127">ntlm</span></span>
- <span data-ttu-id="f71c1-128">certificate</span><span class="sxs-lookup"><span data-stu-id="f71c1-128">certificate</span></span>
- <span data-ttu-id="f71c1-129">协商</span><span class="sxs-lookup"><span data-stu-id="f71c1-129">negotiate</span></span>
- <span data-ttu-id="f71c1-130">nego2</span><span class="sxs-lookup"><span data-stu-id="f71c1-130">nego2</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f71c1-131">注解</span><span class="sxs-lookup"><span data-stu-id="f71c1-131">Remarks</span></span>

<span data-ttu-id="f71c1-132">[类型 (POX)](type-pox.md)元素的文本值为 EXCH 或 EXPR 时才使用**AuthPackage**元素。</span><span class="sxs-lookup"><span data-stu-id="f71c1-132">The **AuthPackage** element is only used when the [Type (POX)](type-pox.md) element has a text value of EXCH or EXPR.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="f71c1-133">版本差异</span><span class="sxs-lookup"><span data-stu-id="f71c1-133">Version differences</span></span>

<span data-ttu-id="f71c1-134">Office 365 和 Exchange Online 中，在本地版本的 Exchange 开头构建 15.00.0995.014 返回的值为"协商"才将服务器配置为使用协商身份验证和客户端包括[X ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头的包含"协商"。</span><span class="sxs-lookup"><span data-stu-id="f71c1-134">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "negotiate" only if the server is configured to use Negotiate authentication and the client includes a [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "Negotiate".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f71c1-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f71c1-135">See also</span></span>

- [<span data-ttu-id="f71c1-136">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="f71c1-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

