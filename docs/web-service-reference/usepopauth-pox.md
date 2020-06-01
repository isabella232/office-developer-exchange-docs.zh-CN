---
title: UsePOPAuth （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 28f552d8-6bb8-49b4-a45c-b2053670f1cc
description: UsePOPAuth 元素指示为 POP3 帐户类型提供的身份验证信息是否也用于简单邮件传输协议（SMTP）。
ms.openlocfilehash: 8d5bfffaab31c382ad43915e18b8a7a2b2737c21
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466505"
---
# <a name="usepopauth-pox"></a><span data-ttu-id="c31fd-103">UsePOPAuth （POX）</span><span class="sxs-lookup"><span data-stu-id="c31fd-103">UsePOPAuth (POX)</span></span>

<span data-ttu-id="c31fd-104">**UsePOPAuth**元素指示为 POP3 帐户类型提供的身份验证信息是否也用于简单邮件传输协议（SMTP）。</span><span class="sxs-lookup"><span data-stu-id="c31fd-104">The **UsePOPAuth** element indicates whether the authentication information that is provided for a POP3 type of account is also used for Simple Mail Transfer Protocol (SMTP).</span></span> 
  
[<span data-ttu-id="c31fd-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="c31fd-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="c31fd-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="c31fd-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="c31fd-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="c31fd-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="c31fd-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="c31fd-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="c31fd-109">UsePOPAuth （POX）</span><span class="sxs-lookup"><span data-stu-id="c31fd-109">UsePOPAuth (POX)</span></span>](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c31fd-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c31fd-110">Attributes and elements</span></span>

<span data-ttu-id="c31fd-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c31fd-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c31fd-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="c31fd-112">Attributes</span></span>

<span data-ttu-id="c31fd-113">无。</span><span class="sxs-lookup"><span data-stu-id="c31fd-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c31fd-114">子元素</span><span class="sxs-lookup"><span data-stu-id="c31fd-114">Child elements</span></span>

<span data-ttu-id="c31fd-115">无。</span><span class="sxs-lookup"><span data-stu-id="c31fd-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c31fd-116">父元素</span><span class="sxs-lookup"><span data-stu-id="c31fd-116">Parent elements</span></span>

|<span data-ttu-id="c31fd-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="c31fd-117">**Element**</span></span>|<span data-ttu-id="c31fd-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="c31fd-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c31fd-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="c31fd-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="c31fd-120">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="c31fd-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c31fd-121">文本值</span><span class="sxs-lookup"><span data-stu-id="c31fd-121">Text value</span></span>

<span data-ttu-id="c31fd-122">Text 值指示为 POP3 帐户提供的身份验证信息是否也用于 SMTP。</span><span class="sxs-lookup"><span data-stu-id="c31fd-122">The text value indicates whether the authentication information that is provided for a POP3 type of account is also used for SMTP.</span></span> <span data-ttu-id="c31fd-123">可能的值为 **"开" 或 "** **关**"。</span><span class="sxs-lookup"><span data-stu-id="c31fd-123">The possible values are **on** and **off**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c31fd-124">备注</span><span class="sxs-lookup"><span data-stu-id="c31fd-124">Remarks</span></span>

<span data-ttu-id="c31fd-125">仅当[Type （POX）](type-pox.md)为 SMTP 时，才使用**UsePOPAuth**元素。</span><span class="sxs-lookup"><span data-stu-id="c31fd-125">The **UsePOPAuth** element is only used when [Type (POX)](type-pox.md) is SMTP.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c31fd-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c31fd-126">See also</span></span>



[<span data-ttu-id="c31fd-127">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="c31fd-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

