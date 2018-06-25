---
title: 内部 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 69c22546-ebd6-4a03-b0b4-bbac72ec5551
description: 内部元素包含客户端可以使用连接到从 Exchange 组织的网络内的 Url 的集合。
ms.openlocfilehash: 0dc5b679af98b52f15ef3b40181c2d97f102f373
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825946"
---
# <a name="internal-pox"></a><span data-ttu-id="b055e-103">内部 (POX)</span><span class="sxs-lookup"><span data-stu-id="b055e-103">Internal (POX)</span></span>

<span data-ttu-id="b055e-104">**内部**元素包含客户端可以使用连接到从 Exchange 组织的网络内的 Url 的集合。</span><span class="sxs-lookup"><span data-stu-id="b055e-104">The **Internal** element contains the collection of URLs that a client can use to connect to Exchange from inside the organization's network.</span></span> 
  
[<span data-ttu-id="b055e-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="b055e-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="b055e-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="b055e-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="b055e-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="b055e-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="b055e-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="b055e-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="b055e-109">内部 (POX)</span><span class="sxs-lookup"><span data-stu-id="b055e-109">Internal (POX)</span></span>](internal-pox.md)
  
```xml
<Internal>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</Internal>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b055e-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b055e-110">Attributes and elements</span></span>

<span data-ttu-id="b055e-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b055e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b055e-112">属性</span><span class="sxs-lookup"><span data-stu-id="b055e-112">Attributes</span></span>

<span data-ttu-id="b055e-113">无。</span><span class="sxs-lookup"><span data-stu-id="b055e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b055e-114">子元素</span><span class="sxs-lookup"><span data-stu-id="b055e-114">Child elements</span></span>

|<span data-ttu-id="b055e-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="b055e-115">**Element**</span></span>|<span data-ttu-id="b055e-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="b055e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b055e-117">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="b055e-117">OWAUrl (POX)</span></span>](owaurl-pox.md) <br/> |<span data-ttu-id="b055e-118">介绍 URL 并用于访问特定的正在运行 Microsoft Exchange Server 的计算机的身份验证架构了客户端访问服务器角色安装承载 Outlook Web Access。</span><span class="sxs-lookup"><span data-stu-id="b055e-118">Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.</span></span>  <br/> |
|[<span data-ttu-id="b055e-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="b055e-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="b055e-120">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="b055e-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> <span data-ttu-id="b055e-121">此**协议**元素具有仅两个子元素： 指定的连接协议，[类型 (POX)](type-pox.md)元素和[ASUrl (POX)](asurl-pox.md)元素，指定的 EWS 终结点的可用性 web 服务。</span><span class="sxs-lookup"><span data-stu-id="b055e-121">This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b055e-122">父元素</span><span class="sxs-lookup"><span data-stu-id="b055e-122">Parent elements</span></span>

|<span data-ttu-id="b055e-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="b055e-123">**Element**</span></span>|<span data-ttu-id="b055e-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="b055e-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b055e-125">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="b055e-125">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="b055e-126">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="b055e-126">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b055e-127">注解</span><span class="sxs-lookup"><span data-stu-id="b055e-127">Remarks</span></span>

<span data-ttu-id="b055e-128">**内部**元素是**协议**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="b055e-128">The **Internal** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b055e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b055e-129">See also</span></span>



[<span data-ttu-id="b055e-130">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="b055e-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

