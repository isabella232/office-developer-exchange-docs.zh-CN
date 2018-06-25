---
title: EcpUrl tmEditing (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: EcpUrl tmEditing 元素指定可以结合使用 EcpUrl (POX) 元素的值生成一个 URL，可用于编辑现有的网站邮箱的部分 URL。
ms.openlocfilehash: 29b27ffe9ef3c18a3b6471ca4a42956a43a5aaa6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754014"
---
# <a name="ecpurl-tmediting-pox"></a><span data-ttu-id="d81f7-103">EcpUrl tmEditing (POX)</span><span class="sxs-lookup"><span data-stu-id="d81f7-103">EcpUrl-tmEditing (POX)</span></span>

<span data-ttu-id="d81f7-104">**EcpUrl tmEditing**元素指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于编辑现有的网站邮箱的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="d81f7-104">The **EcpUrl-tmEditing** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> 
  
[<span data-ttu-id="d81f7-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="d81f7-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="d81f7-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="d81f7-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="d81f7-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="d81f7-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="d81f7-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="d81f7-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="d81f7-109">EcpUrl tmEditing (POX)</span><span class="sxs-lookup"><span data-stu-id="d81f7-109">EcpUrl-tmEditing (POX)</span></span>](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d81f7-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d81f7-110">Attributes and elements</span></span>

<span data-ttu-id="d81f7-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d81f7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d81f7-112">属性</span><span class="sxs-lookup"><span data-stu-id="d81f7-112">Attributes</span></span>

<span data-ttu-id="d81f7-113">无。</span><span class="sxs-lookup"><span data-stu-id="d81f7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d81f7-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d81f7-114">Child elements</span></span>

<span data-ttu-id="d81f7-115">无。</span><span class="sxs-lookup"><span data-stu-id="d81f7-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d81f7-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d81f7-116">Parent elements</span></span>

|<span data-ttu-id="d81f7-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="d81f7-117">**Element**</span></span>|<span data-ttu-id="d81f7-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d81f7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d81f7-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="d81f7-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d81f7-120">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="d81f7-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d81f7-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d81f7-121">Text value</span></span>

<span data-ttu-id="d81f7-122">文本值表示可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于编辑现有的网站邮箱的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="d81f7-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> <span data-ttu-id="d81f7-123">**EcpUrl tmEditing**元素的值包含参数中包含 < 和 > 下表中所示，客户端会替换的字符。</span><span class="sxs-lookup"><span data-stu-id="d81f7-123">The value of the **EcpUrl-tmEditing** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="d81f7-124">**参数**</span><span class="sxs-lookup"><span data-stu-id="d81f7-124">**Parameter**</span></span>|<span data-ttu-id="d81f7-125">**用替代**</span><span class="sxs-lookup"><span data-stu-id="d81f7-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d81f7-126">
  _Id_</span><span class="sxs-lookup"><span data-stu-id="d81f7-126">_Id_</span></span> <br/> |<span data-ttu-id="d81f7-127">SMTP 电子邮件地址或 X500 可分辨名称的站点邮箱。</span><span class="sxs-lookup"><span data-stu-id="d81f7-127">The SMTP email address or the X500 distinguished name of the site mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d81f7-128">注解</span><span class="sxs-lookup"><span data-stu-id="d81f7-128">Remarks</span></span>

<span data-ttu-id="d81f7-129">**EcpUrl tmEditing**元素是**协议**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="d81f7-129">The **EcpUrl-tmEditing** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d81f7-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d81f7-130">See also</span></span>



[<span data-ttu-id="d81f7-131">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="d81f7-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

