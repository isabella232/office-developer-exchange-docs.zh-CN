---
title: 外部（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: External 元素包含一个 Url 集合，客户端可以使用这些 Url 从组织的网络外部连接到 Exchange。
ms.openlocfilehash: 45d7e72c5a43c5c468c1edd303a5e5ea8c2cb62e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457968"
---
# <a name="external-pox"></a><span data-ttu-id="f5b78-103">外部（POX）</span><span class="sxs-lookup"><span data-stu-id="f5b78-103">External (POX)</span></span>

<span data-ttu-id="f5b78-104">**External**元素包含一个 url 集合，客户端可以使用这些 url 从组织的网络外部连接到 Exchange。</span><span class="sxs-lookup"><span data-stu-id="f5b78-104">The **External** element contains a collection of URLs that a client can use to connect to Exchange from outside of the organization's network.</span></span> 
  
[<span data-ttu-id="f5b78-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="f5b78-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="f5b78-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="f5b78-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="f5b78-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="f5b78-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="f5b78-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="f5b78-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="f5b78-109">外部（POX）</span><span class="sxs-lookup"><span data-stu-id="f5b78-109">External (POX)</span></span>](external-pox.md)
  
```XML
<External>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</External>

```

## <a name="attributes-and-elements"></a><span data-ttu-id="f5b78-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f5b78-110">Attributes and elements</span></span>

<span data-ttu-id="f5b78-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f5b78-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5b78-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="f5b78-112">Attributes</span></span>

<span data-ttu-id="f5b78-113">无。</span><span class="sxs-lookup"><span data-stu-id="f5b78-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f5b78-114">子元素</span><span class="sxs-lookup"><span data-stu-id="f5b78-114">Child elements</span></span>

|<span data-ttu-id="f5b78-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5b78-115">**Element**</span></span>|<span data-ttu-id="f5b78-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5b78-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5b78-117">OWAUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="f5b78-117">OWAUrl (POX)</span></span>](owaurl-pox.md) <br/> |<span data-ttu-id="f5b78-118">介绍用于访问运行 Microsoft Exchange Server 的特定计算机的 URL 和身份验证架构，该计算机安装了承载 Outlook Web Access 的客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="f5b78-118">Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.</span></span>  <br/> |
|[<span data-ttu-id="f5b78-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="f5b78-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="f5b78-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="f5b78-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> <span data-ttu-id="f5b78-121">此**协议**元素只有两个子元素：一个指定连接协议的[类型（POX）](type-pox.md)元素和一个[ASUrl （POX）](asurl-pox.md)元素，指定了可用性 web 服务的 EWS 终结点。</span><span class="sxs-lookup"><span data-stu-id="f5b78-121">This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f5b78-122">父元素</span><span class="sxs-lookup"><span data-stu-id="f5b78-122">Parent elements</span></span>

|<span data-ttu-id="f5b78-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5b78-123">**Element**</span></span>|<span data-ttu-id="f5b78-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5b78-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5b78-125">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="f5b78-125">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="f5b78-126">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="f5b78-126">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5b78-127">备注</span><span class="sxs-lookup"><span data-stu-id="f5b78-127">Remarks</span></span>

<span data-ttu-id="f5b78-128">**External**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="f5b78-128">The **External** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f5b78-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5b78-129">See also</span></span>



[<span data-ttu-id="f5b78-130">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="f5b78-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

