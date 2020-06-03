---
title: SMTPLast （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f1aa8bd9-c6ac-41ac-8d2d-56fb20006005
description: SMTPLast 元素指定简单邮件传输协议（SMTP）服务器是否要求先下载电子邮件，然后再使用 SMTP 服务器发送电子邮件。
ms.openlocfilehash: 7019da28ffa196a9abc8798aa75aff2756198da3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468430"
---
# <a name="smtplast-pox"></a><span data-ttu-id="7a1c4-103">SMTPLast （POX）</span><span class="sxs-lookup"><span data-stu-id="7a1c4-103">SMTPLast (POX)</span></span>

<span data-ttu-id="7a1c4-104">**SMTPLast**元素指定简单邮件传输协议（SMTP）服务器是否要求先下载电子邮件，然后再使用 SMTP 服务器发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="7a1c4-104">The **SMTPLast** element specifies whether the Simple Mail Transfer Protocol (SMTP) server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> 
  
- [<span data-ttu-id="7a1c4-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="7a1c4-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="7a1c4-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="7a1c4-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="7a1c4-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="7a1c4-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="7a1c4-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="7a1c4-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="7a1c4-109">SMTPLast （POX）</span><span class="sxs-lookup"><span data-stu-id="7a1c4-109">SMTPLast (POX)</span></span>](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="7a1c4-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7a1c4-110">Attributes and elements</span></span>

<span data-ttu-id="7a1c4-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a1c4-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a1c4-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="7a1c4-112">Attributes</span></span>

<span data-ttu-id="7a1c4-113">无。</span><span class="sxs-lookup"><span data-stu-id="7a1c4-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a1c4-114">子元素</span><span class="sxs-lookup"><span data-stu-id="7a1c4-114">Child elements</span></span>

<span data-ttu-id="7a1c4-115">无。</span><span class="sxs-lookup"><span data-stu-id="7a1c4-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7a1c4-116">父元素</span><span class="sxs-lookup"><span data-stu-id="7a1c4-116">Parent elements</span></span>

|<span data-ttu-id="7a1c4-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a1c4-117">**Element**</span></span>|<span data-ttu-id="7a1c4-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a1c4-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a1c4-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="7a1c4-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="7a1c4-120">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="7a1c4-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7a1c4-121">文本值</span><span class="sxs-lookup"><span data-stu-id="7a1c4-121">Text value</span></span>

<span data-ttu-id="7a1c4-122">该文本值指定 SMTP 服务器是否要求先下载电子邮件，然后再使用 SMTP 服务器发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="7a1c4-122">The text value specifies whether the SMTP server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> <span data-ttu-id="7a1c4-123">可能的值为 **"开" 或 "** **关**"。</span><span class="sxs-lookup"><span data-stu-id="7a1c4-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="7a1c4-124">默认值为**off**。</span><span class="sxs-lookup"><span data-stu-id="7a1c4-124">The default value is **off**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a1c4-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a1c4-125">See also</span></span>

- [<span data-ttu-id="7a1c4-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="7a1c4-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

