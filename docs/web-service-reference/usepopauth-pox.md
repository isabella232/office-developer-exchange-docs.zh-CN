---
title: UsePOPAuth (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 28f552d8-6bb8-49b4-a45c-b2053670f1cc
description: UsePOPAuth 元素指示是否提供 POP3 类型的帐户的身份验证信息也使用的简单邮件传输协议 (SMTP)。
ms.openlocfilehash: be03568d697b1f5461d49dba388a1d3f1008a67e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838452"
---
# <a name="usepopauth-pox"></a><span data-ttu-id="0de07-103">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="0de07-103">UsePOPAuth (POX)</span></span>

<span data-ttu-id="0de07-104">**UsePOPAuth**元素指示是否提供 POP3 类型的帐户的身份验证信息也使用的简单邮件传输协议 (SMTP)。</span><span class="sxs-lookup"><span data-stu-id="0de07-104">The **UsePOPAuth** element indicates whether the authentication information that is provided for a POP3 type of account is also used for Simple Mail Transfer Protocol (SMTP).</span></span> 
  
[<span data-ttu-id="0de07-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="0de07-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="0de07-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="0de07-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="0de07-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="0de07-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="0de07-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="0de07-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="0de07-109">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="0de07-109">UsePOPAuth (POX)</span></span>](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0de07-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0de07-110">Attributes and elements</span></span>

<span data-ttu-id="0de07-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0de07-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0de07-112">属性</span><span class="sxs-lookup"><span data-stu-id="0de07-112">Attributes</span></span>

<span data-ttu-id="0de07-113">无。</span><span class="sxs-lookup"><span data-stu-id="0de07-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0de07-114">子元素</span><span class="sxs-lookup"><span data-stu-id="0de07-114">Child elements</span></span>

<span data-ttu-id="0de07-115">无。</span><span class="sxs-lookup"><span data-stu-id="0de07-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0de07-116">父元素</span><span class="sxs-lookup"><span data-stu-id="0de07-116">Parent elements</span></span>

|<span data-ttu-id="0de07-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="0de07-117">**Element**</span></span>|<span data-ttu-id="0de07-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="0de07-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0de07-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="0de07-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="0de07-120">包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="0de07-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0de07-121">文本值</span><span class="sxs-lookup"><span data-stu-id="0de07-121">Text value</span></span>

<span data-ttu-id="0de07-122">文本值指示是否为 SMTP 还使用 POP3 类型的帐户提供的身份验证信息。</span><span class="sxs-lookup"><span data-stu-id="0de07-122">The text value indicates whether the authentication information that is provided for a POP3 type of account is also used for SMTP.</span></span> <span data-ttu-id="0de07-123">可能的值为**在**打开和**关闭**。</span><span class="sxs-lookup"><span data-stu-id="0de07-123">The possible values are **on** and **off**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0de07-124">备注</span><span class="sxs-lookup"><span data-stu-id="0de07-124">Remarks</span></span>

<span data-ttu-id="0de07-125">SMTP[类型 (POX)](type-pox.md)时，仅使用**UsePOPAuth**元素。</span><span class="sxs-lookup"><span data-stu-id="0de07-125">The **UsePOPAuth** element is only used when [Type (POX)](type-pox.md) is SMTP.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0de07-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0de07-126">See also</span></span>



[<span data-ttu-id="0de07-127">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="0de07-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

