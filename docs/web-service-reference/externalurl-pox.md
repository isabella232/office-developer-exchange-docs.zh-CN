---
title: ExternalUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: ExternalUrl 元素包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器或用户邮箱外部的 URL。
ms.openlocfilehash: 94265051be68ed06d1dab8d46dd4ce29d8694c93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457954"
---
# <a name="externalurl-pox"></a><span data-ttu-id="0538a-103">ExternalUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="0538a-103">ExternalUrl (POX)</span></span>

<span data-ttu-id="0538a-104">**ExternalUrl**元素包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器或用户邮箱外部的 URL。</span><span class="sxs-lookup"><span data-stu-id="0538a-104">The **ExternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from outside the user's organization by using the MAPI/HTTP protocol.</span></span> 
  
```XML
<ExternalUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0538a-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0538a-105">Attributes and elements</span></span>

<span data-ttu-id="0538a-106">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0538a-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0538a-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="0538a-107">Attributes</span></span>

<span data-ttu-id="0538a-108">无。</span><span class="sxs-lookup"><span data-stu-id="0538a-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0538a-109">子元素</span><span class="sxs-lookup"><span data-stu-id="0538a-109">Child elements</span></span>

<span data-ttu-id="0538a-110">无。</span><span class="sxs-lookup"><span data-stu-id="0538a-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0538a-111">父元素</span><span class="sxs-lookup"><span data-stu-id="0538a-111">Parent elements</span></span>

|<span data-ttu-id="0538a-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="0538a-112">**Element**</span></span>|<span data-ttu-id="0538a-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="0538a-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0538a-114">AddressBook （POX）</span><span class="sxs-lookup"><span data-stu-id="0538a-114">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="0538a-115">包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="0538a-115">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="0538a-116">MailStore （POX）</span><span class="sxs-lookup"><span data-stu-id="0538a-116">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="0538a-117">包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。</span><span class="sxs-lookup"><span data-stu-id="0538a-117">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0538a-118">文本值</span><span class="sxs-lookup"><span data-stu-id="0538a-118">Text value</span></span>

<span data-ttu-id="0538a-119">文本值表示可用于从用户组织外部访问通讯簿服务器或用户邮箱的 URL。</span><span class="sxs-lookup"><span data-stu-id="0538a-119">The text value represents a URL that can be used to access an address book server or user's mailbox from outside the user's organization.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0538a-120">备注</span><span class="sxs-lookup"><span data-stu-id="0538a-120">Remarks</span></span>

<span data-ttu-id="0538a-121">**ExternalUrl**元素可以出现在具有**Type**属性值为 "mapi" 的[Protocol （POX）](protocol-pox.md)元素的响应中。</span><span class="sxs-lookup"><span data-stu-id="0538a-121">The **ExternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="0538a-122">**ExternalUrl**元素可用于实现 MAPI/HTTP 协议和目标 exchange online 的客户端、exchange online （作为 Office 365 的一部分）和 exchange online 版本（从 build 15.00.0847.032 （exchange SERVER 2013 SP1）开始。</span><span class="sxs-lookup"><span data-stu-id="0538a-122">The **ExternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0538a-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0538a-123">See also</span></span>



[<span data-ttu-id="0538a-124">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="0538a-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

