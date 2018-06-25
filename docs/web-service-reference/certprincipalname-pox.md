---
title: CertPrincipalName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: CertPrincipalName 元素指定需要使用 SSL 连接到 Microsoft Exchange Server 2007 组织的安全套接字层 (SSL) 证书主体名称。
ms.openlocfilehash: d2766b16a3e8a1bcd013de332d9c07f709fcf949
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753444"
---
# <a name="certprincipalname-pox"></a><span data-ttu-id="dfe8d-103">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="dfe8d-103">CertPrincipalName (POX)</span></span>

<span data-ttu-id="dfe8d-104">**CertPrincipalName**元素指定需要使用 SSL 连接到 Microsoft Exchange Server 2007 组织的安全套接字层 (SSL) 证书主体名称。</span><span class="sxs-lookup"><span data-stu-id="dfe8d-104">The **CertPrincipalName** element specifies the Secure Sockets Layer (SSL) certificate principal name that is required to connect to the Microsoft Exchange Server 2007 organization by using SSL.</span></span> 
  
[<span data-ttu-id="dfe8d-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="dfe8d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="dfe8d-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="dfe8d-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="dfe8d-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="dfe8d-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="dfe8d-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="dfe8d-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="dfe8d-109">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="dfe8d-109">CertPrincipalName (POX)</span></span>](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="dfe8d-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dfe8d-110">Attributes and elements</span></span>

<span data-ttu-id="dfe8d-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dfe8d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dfe8d-112">属性</span><span class="sxs-lookup"><span data-stu-id="dfe8d-112">Attributes</span></span>

<span data-ttu-id="dfe8d-113">无。</span><span class="sxs-lookup"><span data-stu-id="dfe8d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dfe8d-114">子元素</span><span class="sxs-lookup"><span data-stu-id="dfe8d-114">Child elements</span></span>

<span data-ttu-id="dfe8d-115">无。</span><span class="sxs-lookup"><span data-stu-id="dfe8d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dfe8d-116">父元素</span><span class="sxs-lookup"><span data-stu-id="dfe8d-116">Parent elements</span></span>

|<span data-ttu-id="dfe8d-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="dfe8d-117">**Element**</span></span>|<span data-ttu-id="dfe8d-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="dfe8d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfe8d-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="dfe8d-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="dfe8d-120">包含客户端连接到计算机上运行安装了客户端访问服务器角色的 Exchange 2007 的技术指标。</span><span class="sxs-lookup"><span data-stu-id="dfe8d-120">Contains the specifications for connecting a client to the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dfe8d-121">文本值</span><span class="sxs-lookup"><span data-stu-id="dfe8d-121">Text value</span></span>

<span data-ttu-id="dfe8d-122">文本值指定使用 SSL 连接到 Microsoft Exchange 组织所需的 SSL 证书主体名称。</span><span class="sxs-lookup"><span data-stu-id="dfe8d-122">The text value specifies the SSL certificate principal name that is required to connect to the Microsoft Exchange organization by using SSL.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfe8d-123">注解</span><span class="sxs-lookup"><span data-stu-id="dfe8d-123">Remarks</span></span>

<span data-ttu-id="dfe8d-124">如果未指定**CertPrincipalName**元素，则默认设置为 msstd:SERVER，其中的 SERVER 是[服务器 (POX)](server-pox.md)元素中指定的值。</span><span class="sxs-lookup"><span data-stu-id="dfe8d-124">If the **CertPrincipalName** element is not specified, the default is set to msstd:SERVER, where SERVER is the value that is specified in the [Server (POX)](server-pox.md) element.</span></span> <span data-ttu-id="dfe8d-125">例如，如果服务器指定为 example.com 和**CertPrincipalName**与开启[SSL (POX)](ssl-pox.md)保留为空，则**CertPrincipalName**的默认值将为 msstd:example.com。</span><span class="sxs-lookup"><span data-stu-id="dfe8d-125">For example, if SERVER is specified as example.com and **CertPrincipalName** is left blank with [SSL (POX)](ssl-pox.md) turned on, the default value of **CertPrincipalName** would be msstd:example.com.</span></span> 
  
<span data-ttu-id="dfe8d-126">如果**未**指定，Windows 将验证根据在 MSDN 上的[主体名称](http://go.microsoft.com/fwlink/?LinkId=93417)主题中找到的信息的证书主体名称。</span><span class="sxs-lookup"><span data-stu-id="dfe8d-126">If **none** is specified, Windows will validate the certificate principal name according to information found in the [Principal Names](http://go.microsoft.com/fwlink/?LinkId=93417) topic on MSDN.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfe8d-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dfe8d-127">See also</span></span>



[<span data-ttu-id="dfe8d-128">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="dfe8d-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

