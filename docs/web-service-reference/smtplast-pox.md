---
title: SMTPLast (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f1aa8bd9-c6ac-41ac-8d2d-56fb20006005
description: SMTPLast 元素指定的简单邮件传输协议 (SMTP) 服务器是否要求使用 SMTP 服务器发送电子邮件之前下载的电子邮件。
ms.openlocfilehash: 5359f20b33855f4ef48566058bc46bd618e3b2ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827505"
---
# <a name="smtplast-pox"></a><span data-ttu-id="3d823-103">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="3d823-103">SMTPLast (POX)</span></span>

<span data-ttu-id="3d823-104">**SMTPLast**元素指定的简单邮件传输协议 (SMTP) 服务器是否要求使用 SMTP 服务器发送电子邮件之前下载的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="3d823-104">The **SMTPLast** element specifies whether the Simple Mail Transfer Protocol (SMTP) server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> 
  
- [<span data-ttu-id="3d823-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="3d823-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="3d823-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="3d823-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="3d823-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="3d823-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="3d823-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="3d823-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="3d823-109">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="3d823-109">SMTPLast (POX)</span></span>](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="3d823-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3d823-110">Attributes and elements</span></span>

<span data-ttu-id="3d823-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3d823-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d823-112">属性</span><span class="sxs-lookup"><span data-stu-id="3d823-112">Attributes</span></span>

<span data-ttu-id="3d823-113">无。</span><span class="sxs-lookup"><span data-stu-id="3d823-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3d823-114">子元素</span><span class="sxs-lookup"><span data-stu-id="3d823-114">Child elements</span></span>

<span data-ttu-id="3d823-115">无。</span><span class="sxs-lookup"><span data-stu-id="3d823-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3d823-116">父元素</span><span class="sxs-lookup"><span data-stu-id="3d823-116">Parent elements</span></span>

|<span data-ttu-id="3d823-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="3d823-117">**Element**</span></span>|<span data-ttu-id="3d823-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="3d823-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d823-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="3d823-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="3d823-120">包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="3d823-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3d823-121">文本值</span><span class="sxs-lookup"><span data-stu-id="3d823-121">Text value</span></span>

<span data-ttu-id="3d823-122">文本值指定 SMTP 服务器是否要求使用 SMTP 服务器发送电子邮件之前下载的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="3d823-122">The text value specifies whether the SMTP server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> <span data-ttu-id="3d823-123">可能的值为**在**打开和**关闭**。</span><span class="sxs-lookup"><span data-stu-id="3d823-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="3d823-124">默认值已**关闭**。</span><span class="sxs-lookup"><span data-stu-id="3d823-124">The default value is **off**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3d823-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3d823-125">See also</span></span>

- [<span data-ttu-id="3d823-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="3d823-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

