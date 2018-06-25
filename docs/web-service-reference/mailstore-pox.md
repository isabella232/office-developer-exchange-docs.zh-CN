---
title: MailStore (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: MailStore 元素包含客户端连接到用户的邮箱，使用 MAPI/HTTP 协议的规范。
ms.openlocfilehash: 4c82c7b61752cf7d91287a3968f6c642f4943855
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826301"
---
# <a name="mailstore-pox"></a><span data-ttu-id="0f37f-103">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="0f37f-103">MailStore (POX)</span></span>

<span data-ttu-id="0f37f-104">**MailStore**元素包含客户端连接到用户的邮箱，使用 MAPI/HTTP 协议的规范。</span><span class="sxs-lookup"><span data-stu-id="0f37f-104">The **MailStore** element contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="0f37f-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="0f37f-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="0f37f-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="0f37f-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="0f37f-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="0f37f-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="0f37f-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="0f37f-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="0f37f-109">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="0f37f-109">MailStore (POX)</span></span>](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0f37f-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0f37f-110">Attributes and elements</span></span>

<span data-ttu-id="0f37f-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0f37f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f37f-112">属性</span><span class="sxs-lookup"><span data-stu-id="0f37f-112">Attributes</span></span>

<span data-ttu-id="0f37f-113">无。</span><span class="sxs-lookup"><span data-stu-id="0f37f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0f37f-114">子元素</span><span class="sxs-lookup"><span data-stu-id="0f37f-114">Child elements</span></span>

|<span data-ttu-id="0f37f-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="0f37f-115">**Element**</span></span>|<span data-ttu-id="0f37f-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="0f37f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f37f-117">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="0f37f-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="0f37f-118">包含用于访问用户的邮箱从组织的网络外部通过 MAPI/HTTP 协议的 URL。</span><span class="sxs-lookup"><span data-stu-id="0f37f-118">Contains the URL that should be used to access the user's mailbox from outside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="0f37f-119">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="0f37f-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="0f37f-120">包含用于通过 MAPI/HTTP 协议访问从组织的网络内的用户的邮箱的 URL。</span><span class="sxs-lookup"><span data-stu-id="0f37f-120">Contains the URL that should be used to access the user's mailbox from inside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0f37f-121">父元素</span><span class="sxs-lookup"><span data-stu-id="0f37f-121">Parent elements</span></span>

|<span data-ttu-id="0f37f-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="0f37f-122">**Element**</span></span>|<span data-ttu-id="0f37f-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="0f37f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f37f-124">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="0f37f-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="0f37f-125">包含客户端连接到客户端访问服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="0f37f-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f37f-126">注解</span><span class="sxs-lookup"><span data-stu-id="0f37f-126">Remarks</span></span>

<span data-ttu-id="0f37f-127">与**Type**属性值为"mapiHttp"[协议 (POX)](protocol-pox.md)元素的响应中存在的**MailStore**元素。</span><span class="sxs-lookup"><span data-stu-id="0f37f-127">The **MailStore** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="0f37f-128">**MailStore**元素是可用于实现 MAPI/HTTP 协议和目标 Exchange Online、 Exchange Online 作为 Office 365 的一部分的客户端和 Exchange 开头的本地版本构建 15.00.0847.032 (Exchange Server 2013 SP1)。</span><span class="sxs-lookup"><span data-stu-id="0f37f-128">The **MailStore** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f37f-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0f37f-129">See also</span></span>



[<span data-ttu-id="0f37f-130">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="0f37f-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

