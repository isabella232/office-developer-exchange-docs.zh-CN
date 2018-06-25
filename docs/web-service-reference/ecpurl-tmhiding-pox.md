---
title: EcpUrl tmHiding (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b9ae15b-3ac1-45ac-85ba-38c7231fe508
description: EcpUrl tmHiding 元素指定可以结合使用 EcpUrl (POX) 元素的值生成一个 URL，可用来取消订阅的站点邮箱用户的部分 URL。
ms.openlocfilehash: 461e9780dbd657ba0ba8b9ce9ea4fe902cba9698
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754016"
---
# <a name="ecpurl-tmhiding-pox"></a><span data-ttu-id="dedee-103">EcpUrl tmHiding (POX)</span><span class="sxs-lookup"><span data-stu-id="dedee-103">EcpUrl-tmHiding (POX)</span></span>

<span data-ttu-id="dedee-104">**EcpUrl tmHiding**元素指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用来取消订阅的站点邮箱用户的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="dedee-104">The **EcpUrl-tmHiding** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to unsubscribe the user from a site mailbox.</span></span> 
  
[<span data-ttu-id="dedee-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="dedee-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="dedee-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="dedee-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="dedee-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="dedee-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="dedee-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="dedee-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="dedee-109">EcpUrl tmHiding (POX)</span><span class="sxs-lookup"><span data-stu-id="dedee-109">EcpUrl-tmHiding (POX)</span></span>](ecpurl-tmhiding-pox.md)
  
```XML
<EcpUrl-tmHiding/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="dedee-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dedee-110">Attributes and elements</span></span>

<span data-ttu-id="dedee-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dedee-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dedee-112">属性</span><span class="sxs-lookup"><span data-stu-id="dedee-112">Attributes</span></span>

<span data-ttu-id="dedee-113">无。</span><span class="sxs-lookup"><span data-stu-id="dedee-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dedee-114">子元素</span><span class="sxs-lookup"><span data-stu-id="dedee-114">Child elements</span></span>

<span data-ttu-id="dedee-115">无。</span><span class="sxs-lookup"><span data-stu-id="dedee-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dedee-116">父元素</span><span class="sxs-lookup"><span data-stu-id="dedee-116">Parent elements</span></span>

|<span data-ttu-id="dedee-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="dedee-117">**Element**</span></span>|<span data-ttu-id="dedee-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="dedee-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dedee-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="dedee-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="dedee-120">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="dedee-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dedee-121">文本值</span><span class="sxs-lookup"><span data-stu-id="dedee-121">Text value</span></span>

<span data-ttu-id="dedee-122">文本值表示可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用来取消订阅的站点邮箱用户的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="dedee-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to unsubscribe the user from a site mailbox.</span></span> <span data-ttu-id="dedee-123">**EcpUrl tmHiding**元素的值包含参数中包含 < 和 > 下表中所示，客户端会替换的字符。</span><span class="sxs-lookup"><span data-stu-id="dedee-123">The value of the **EcpUrl-tmHiding** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="dedee-124">**参数**</span><span class="sxs-lookup"><span data-stu-id="dedee-124">**Parameter**</span></span>|<span data-ttu-id="dedee-125">**用替代**</span><span class="sxs-lookup"><span data-stu-id="dedee-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dedee-126">
  _Id_</span><span class="sxs-lookup"><span data-stu-id="dedee-126">_Id_</span></span> <br/> |<span data-ttu-id="dedee-127">SMTP 电子邮件地址或 X500 可分辨名称的站点邮箱。</span><span class="sxs-lookup"><span data-stu-id="dedee-127">The SMTP email address or the X500 distinguished name of the site mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dedee-128">注解</span><span class="sxs-lookup"><span data-stu-id="dedee-128">Remarks</span></span>

<span data-ttu-id="dedee-129">**EcpUrl tmHiding**元素是**协议**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="dedee-129">The **EcpUrl-tmHiding** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dedee-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dedee-130">See also</span></span>



[<span data-ttu-id="dedee-131">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="dedee-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

