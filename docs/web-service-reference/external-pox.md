---
title: 外部 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: 外部元素包含客户端可以使用连接到从 Exchange 组织的网络之外的 Url 的集合。
ms.openlocfilehash: 7f01fc29b5ce63b02de0a4a6e42887dcffbb4b82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754242"
---
# <a name="external-pox"></a><span data-ttu-id="572cc-103">外部 (POX)</span><span class="sxs-lookup"><span data-stu-id="572cc-103">External (POX)</span></span>

<span data-ttu-id="572cc-104">**外部**元素包含客户端可以使用连接到从 Exchange 组织的网络之外的 Url 的集合。</span><span class="sxs-lookup"><span data-stu-id="572cc-104">The **External** element contains a collection of URLs that a client can use to connect to Exchange from outside of the organization's network.</span></span> 
  
[<span data-ttu-id="572cc-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="572cc-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="572cc-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="572cc-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="572cc-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="572cc-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="572cc-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="572cc-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="572cc-109">外部 (POX)</span><span class="sxs-lookup"><span data-stu-id="572cc-109">External (POX)</span></span>](external-pox.md)
  
```XML
<External>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</External>

```

## <a name="attributes-and-elements"></a><span data-ttu-id="572cc-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="572cc-110">Attributes and elements</span></span>

<span data-ttu-id="572cc-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="572cc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="572cc-112">属性</span><span class="sxs-lookup"><span data-stu-id="572cc-112">Attributes</span></span>

<span data-ttu-id="572cc-113">无。</span><span class="sxs-lookup"><span data-stu-id="572cc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="572cc-114">子元素</span><span class="sxs-lookup"><span data-stu-id="572cc-114">Child elements</span></span>

|<span data-ttu-id="572cc-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="572cc-115">**Element**</span></span>|<span data-ttu-id="572cc-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="572cc-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="572cc-117">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="572cc-117">OWAUrl (POX)</span></span>](owaurl-pox.md) <br/> |<span data-ttu-id="572cc-118">介绍 URL 并用于访问特定的正在运行 Microsoft Exchange Server 的计算机的身份验证架构了客户端访问服务器角色安装承载 Outlook Web Access。</span><span class="sxs-lookup"><span data-stu-id="572cc-118">Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.</span></span>  <br/> |
|[<span data-ttu-id="572cc-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="572cc-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="572cc-120">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="572cc-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> <span data-ttu-id="572cc-121">此**协议**元素具有仅两个子元素： 指定的连接协议，[类型 (POX)](type-pox.md)元素和[ASUrl (POX)](asurl-pox.md)元素，指定的 EWS 终结点的可用性 web 服务。</span><span class="sxs-lookup"><span data-stu-id="572cc-121">This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="572cc-122">父元素</span><span class="sxs-lookup"><span data-stu-id="572cc-122">Parent elements</span></span>

|<span data-ttu-id="572cc-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="572cc-123">**Element**</span></span>|<span data-ttu-id="572cc-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="572cc-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="572cc-125">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="572cc-125">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="572cc-126">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="572cc-126">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="572cc-127">备注</span><span class="sxs-lookup"><span data-stu-id="572cc-127">Remarks</span></span>

<span data-ttu-id="572cc-128">**外部**元素是**协议**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="572cc-128">The **External** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="572cc-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="572cc-129">See also</span></span>



[<span data-ttu-id="572cc-130">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="572cc-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
