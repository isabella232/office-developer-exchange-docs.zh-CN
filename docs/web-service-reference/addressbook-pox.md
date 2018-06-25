---
title: 通讯簿 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: AddressBook 元素包含使用 MAPI/HTTP 协议客户端连接到通讯簿服务器的规范。
ms.openlocfilehash: c30f0ee7c36de7e63157d07d003a11187d661fd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753121"
---
# <a name="addressbook-pox"></a><span data-ttu-id="a10f6-103">通讯簿 (POX)</span><span class="sxs-lookup"><span data-stu-id="a10f6-103">AddressBook (POX)</span></span>

<span data-ttu-id="a10f6-104">**AddressBook**元素包含使用 MAPI/HTTP 协议客户端连接到通讯簿服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="a10f6-104">The **AddressBook** element contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="a10f6-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="a10f6-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="a10f6-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="a10f6-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="a10f6-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="a10f6-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="a10f6-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="a10f6-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="a10f6-109">通讯簿 (POX)</span><span class="sxs-lookup"><span data-stu-id="a10f6-109">AddressBook (POX)</span></span>](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a10f6-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a10f6-110">Attributes and elements</span></span>

<span data-ttu-id="a10f6-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a10f6-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a10f6-112">属性</span><span class="sxs-lookup"><span data-stu-id="a10f6-112">Attributes</span></span>

<span data-ttu-id="a10f6-113">无。</span><span class="sxs-lookup"><span data-stu-id="a10f6-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a10f6-114">子元素</span><span class="sxs-lookup"><span data-stu-id="a10f6-114">Child elements</span></span>

|<span data-ttu-id="a10f6-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="a10f6-115">**Element**</span></span>|<span data-ttu-id="a10f6-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="a10f6-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a10f6-117">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="a10f6-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="a10f6-118">包含用于访问通讯簿从组织的网络外部使用 MAPI/HTTP 协议的 URL。</span><span class="sxs-lookup"><span data-stu-id="a10f6-118">Contains the URL that should be used to access the address book from outside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="a10f6-119">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="a10f6-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="a10f6-120">包含用于访问通讯簿从组织的网络内使用的 MAPI/HTTP 协议的 URL。</span><span class="sxs-lookup"><span data-stu-id="a10f6-120">Contains the URL that should be used to access the address book from inside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a10f6-121">父元素</span><span class="sxs-lookup"><span data-stu-id="a10f6-121">Parent elements</span></span>

|<span data-ttu-id="a10f6-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="a10f6-122">**Element**</span></span>|<span data-ttu-id="a10f6-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="a10f6-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a10f6-124">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="a10f6-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="a10f6-125">包含客户端连接到客户端访问服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="a10f6-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a10f6-126">注解</span><span class="sxs-lookup"><span data-stu-id="a10f6-126">Remarks</span></span>

<span data-ttu-id="a10f6-127">**AddressBook**元素中不存在一个响应，其中具有与**Type**属性值为"mapiHttp"[协议 (POX)](protocol-pox.md)元素。</span><span class="sxs-lookup"><span data-stu-id="a10f6-127">The **AddressBook** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="a10f6-128">**AddressBook**元素是可用于实现 MAPI/HTTP 协议和目标 Exchange Online、 Exchange Online 作为 Office 365 的一部分的客户端和 Exchange 开头的本地版本构建 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="a10f6-128">The **AddressBook** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a10f6-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a10f6-129">See also</span></span>

- [<span data-ttu-id="a10f6-130">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="a10f6-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

