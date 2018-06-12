---
title: ExternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: ExternalUrl 元素包含使用 MAPI/HTTP 协议客户端连接到通讯簿服务器或从用户的组织外部的用户的邮箱的 URL。
ms.openlocfilehash: 603e2109e7b3c98acdd4cbc13df81ed9717630ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754280"
---
# <a name="externalurl-pox"></a><span data-ttu-id="41a64-103">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="41a64-103">ExternalUrl (POX)</span></span>

<span data-ttu-id="41a64-104">**ExternalUrl**元素包含使用 MAPI/HTTP 协议客户端连接到通讯簿服务器或从用户的组织外部的用户的邮箱的 URL。</span><span class="sxs-lookup"><span data-stu-id="41a64-104">The **ExternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from outside the user's organization by using the MAPI/HTTP protocol.</span></span> 
  
```XML
<ExternalUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="41a64-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41a64-105">Attributes and elements</span></span>

<span data-ttu-id="41a64-106">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41a64-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41a64-107">属性</span><span class="sxs-lookup"><span data-stu-id="41a64-107">Attributes</span></span>

<span data-ttu-id="41a64-108">无。</span><span class="sxs-lookup"><span data-stu-id="41a64-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41a64-109">子元素</span><span class="sxs-lookup"><span data-stu-id="41a64-109">Child elements</span></span>

<span data-ttu-id="41a64-110">无。</span><span class="sxs-lookup"><span data-stu-id="41a64-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="41a64-111">父元素</span><span class="sxs-lookup"><span data-stu-id="41a64-111">Parent elements</span></span>

|<span data-ttu-id="41a64-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="41a64-112">**Element**</span></span>|<span data-ttu-id="41a64-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="41a64-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41a64-114">通讯簿 (POX)</span><span class="sxs-lookup"><span data-stu-id="41a64-114">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="41a64-115">包含使用 MAPI/HTTP 协议客户端连接到通讯簿服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="41a64-115">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="41a64-116">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="41a64-116">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="41a64-117">包含使用 MAPI/HTTP 协议来连接到用户邮箱的客户端的规范。</span><span class="sxs-lookup"><span data-stu-id="41a64-117">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41a64-118">文本值</span><span class="sxs-lookup"><span data-stu-id="41a64-118">Text value</span></span>

<span data-ttu-id="41a64-119">文本值表示可用于访问通讯簿服务器或从用户的组织外部的用户的邮箱的 URL。</span><span class="sxs-lookup"><span data-stu-id="41a64-119">The text value represents a URL that can be used to access an address book server or user's mailbox from outside the user's organization.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41a64-120">备注</span><span class="sxs-lookup"><span data-stu-id="41a64-120">Remarks</span></span>

<span data-ttu-id="41a64-121">**ExternalUrl**元素中可能存在一个响应，其中具有与**Type**属性值为"mapiHttp"[协议 (POX)](protocol-pox.md)元素。</span><span class="sxs-lookup"><span data-stu-id="41a64-121">The **ExternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="41a64-122">**ExternalUrl**元素是可用于实现 MAPI/HTTP 协议和目标 Exchange Online、 Exchange Online 作为 Office 365 的一部分的客户端和 Exchange 开头的本地版本构建 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="41a64-122">The **ExternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41a64-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41a64-123">See also</span></span>



[<span data-ttu-id="41a64-124">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="41a64-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
