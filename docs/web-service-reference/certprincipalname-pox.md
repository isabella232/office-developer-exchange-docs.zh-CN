---
title: CertPrincipalName （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: CertPrincipalName 元素指定使用 SSL 连接到 Microsoft Exchange Server 2007 组织所需的安全套接字层（SSL）证书主体名称。
ms.openlocfilehash: fb2a1c8577bce41945b669be56f2a94a2c4dca26
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463340"
---
# <a name="certprincipalname-pox"></a><span data-ttu-id="4b883-103">CertPrincipalName （POX）</span><span class="sxs-lookup"><span data-stu-id="4b883-103">CertPrincipalName (POX)</span></span>

<span data-ttu-id="4b883-104">**CertPrincipalName**元素指定使用 SSL 连接到 Microsoft Exchange Server 2007 组织所需的安全套接字层（SSL）证书主体名称。</span><span class="sxs-lookup"><span data-stu-id="4b883-104">The **CertPrincipalName** element specifies the Secure Sockets Layer (SSL) certificate principal name that is required to connect to the Microsoft Exchange Server 2007 organization by using SSL.</span></span> 
  
[<span data-ttu-id="4b883-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="4b883-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="4b883-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="4b883-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="4b883-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="4b883-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="4b883-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="4b883-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="4b883-109">CertPrincipalName （POX）</span><span class="sxs-lookup"><span data-stu-id="4b883-109">CertPrincipalName (POX)</span></span>](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="4b883-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4b883-110">Attributes and elements</span></span>

<span data-ttu-id="4b883-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4b883-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b883-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="4b883-112">Attributes</span></span>

<span data-ttu-id="4b883-113">无。</span><span class="sxs-lookup"><span data-stu-id="4b883-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b883-114">子元素</span><span class="sxs-lookup"><span data-stu-id="4b883-114">Child elements</span></span>

<span data-ttu-id="4b883-115">无。</span><span class="sxs-lookup"><span data-stu-id="4b883-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4b883-116">父元素</span><span class="sxs-lookup"><span data-stu-id="4b883-116">Parent elements</span></span>

|<span data-ttu-id="4b883-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="4b883-117">**Element**</span></span>|<span data-ttu-id="4b883-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b883-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b883-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="4b883-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="4b883-120">包含用于将客户端连接到运行 Exchange 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="4b883-120">Contains the specifications for connecting a client to the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4b883-121">文本值</span><span class="sxs-lookup"><span data-stu-id="4b883-121">Text value</span></span>

<span data-ttu-id="4b883-122">该文本值指定使用 SSL 连接到 Microsoft Exchange 组织所需的 SSL 证书主体名称。</span><span class="sxs-lookup"><span data-stu-id="4b883-122">The text value specifies the SSL certificate principal name that is required to connect to the Microsoft Exchange organization by using SSL.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4b883-123">备注</span><span class="sxs-lookup"><span data-stu-id="4b883-123">Remarks</span></span>

<span data-ttu-id="4b883-124">如果未指定**CertPrincipalName**元素，则默认设置为 MSSTD： server，其中的 server 是在[服务器（POX）](server-pox.md)元素中指定的值。</span><span class="sxs-lookup"><span data-stu-id="4b883-124">If the **CertPrincipalName** element is not specified, the default is set to msstd:SERVER, where SERVER is the value that is specified in the [Server (POX)](server-pox.md) element.</span></span> <span data-ttu-id="4b883-125">例如，如果将 SERVER 指定为 example.com，并将**CertPrincipalName**保留为空，并且[SSL （POX）](ssl-pox.md)打开，则**CertPrincipalName**的默认值为 msstd:example .com。</span><span class="sxs-lookup"><span data-stu-id="4b883-125">For example, if SERVER is specified as example.com and **CertPrincipalName** is left blank with [SSL (POX)](ssl-pox.md) turned on, the default value of **CertPrincipalName** would be msstd:example.com.</span></span> 
  
<span data-ttu-id="4b883-126">如果**未指定，则 Windows**将根据 MSDN 上的[主体名称](https://go.microsoft.com/fwlink/?LinkId=93417)主题中的信息来验证证书主体名称。</span><span class="sxs-lookup"><span data-stu-id="4b883-126">If **none** is specified, Windows will validate the certificate principal name according to information found in the [Principal Names](https://go.microsoft.com/fwlink/?LinkId=93417) topic on MSDN.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b883-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b883-127">See also</span></span>



[<span data-ttu-id="4b883-128">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="4b883-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

