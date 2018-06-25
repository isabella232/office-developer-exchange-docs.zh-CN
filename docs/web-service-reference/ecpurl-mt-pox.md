---
title: EcpUrl 黑 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: EcpUrl 黑元素指定可以结合使用 EcpUrl (POX) 元素的值生成一个 URL，可用于访问电子邮件跟踪已启用邮件的用户设置的部分 URL。
ms.openlocfilehash: 13954a4dab8e81f4ba75b3578e6ba7f67f4b8b96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754002"
---
# <a name="ecpurl-mt-pox"></a><span data-ttu-id="b88da-103">EcpUrl 黑 (POX)</span><span class="sxs-lookup"><span data-stu-id="b88da-103">EcpUrl-mt (POX)</span></span>

<span data-ttu-id="b88da-104">**EcpUrl 黑**元素指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问电子邮件跟踪已启用邮件的用户设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="b88da-104">The **EcpUrl-mt** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="b88da-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="b88da-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="b88da-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="b88da-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="b88da-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="b88da-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="b88da-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="b88da-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="b88da-109">EcpUrl 黑 (POX)</span><span class="sxs-lookup"><span data-stu-id="b88da-109">EcpUrl-mt (POX)</span></span>](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b88da-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b88da-110">Attributes and elements</span></span>

<span data-ttu-id="b88da-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b88da-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b88da-112">属性</span><span class="sxs-lookup"><span data-stu-id="b88da-112">Attributes</span></span>

<span data-ttu-id="b88da-113">无。</span><span class="sxs-lookup"><span data-stu-id="b88da-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b88da-114">子元素</span><span class="sxs-lookup"><span data-stu-id="b88da-114">Child elements</span></span>

<span data-ttu-id="b88da-115">无。</span><span class="sxs-lookup"><span data-stu-id="b88da-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b88da-116">父元素</span><span class="sxs-lookup"><span data-stu-id="b88da-116">Parent elements</span></span>

|<span data-ttu-id="b88da-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="b88da-117">**Element**</span></span>|<span data-ttu-id="b88da-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="b88da-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b88da-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="b88da-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="b88da-120">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="b88da-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b88da-121">文本值</span><span class="sxs-lookup"><span data-stu-id="b88da-121">Text value</span></span>

<span data-ttu-id="b88da-122">文本值表示可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问电子邮件跟踪的用户设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="b88da-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email tracking settings for the user.</span></span> <span data-ttu-id="b88da-123">**EcpUrl 黑**元素的值包含参数中包含 < 和 > 下表中所示，客户端会替换的字符。</span><span class="sxs-lookup"><span data-stu-id="b88da-123">The value of the **EcpUrl-mt** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="b88da-124">**参数**</span><span class="sxs-lookup"><span data-stu-id="b88da-124">**Parameter**</span></span>|<span data-ttu-id="b88da-125">**用替代**</span><span class="sxs-lookup"><span data-stu-id="b88da-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b88da-126">_IsOwa_</span><span class="sxs-lookup"><span data-stu-id="b88da-126">_IsOwa_</span></span> <br/> |<span data-ttu-id="b88da-127">n</span><span class="sxs-lookup"><span data-stu-id="b88da-127">n</span></span>  <br/> |
| <span data-ttu-id="b88da-128">_邮件 Id_</span><span class="sxs-lookup"><span data-stu-id="b88da-128">_MsgID_</span></span> <br/> |<span data-ttu-id="b88da-129">Internet 消息标识符的邮件跟踪所指定的邮件 ID 标头。</span><span class="sxs-lookup"><span data-stu-id="b88da-129">Internet message identifier of the message to be tracked as specified by the Message-ID header.</span></span>  <br/> |
| <span data-ttu-id="b88da-130">_Mbx_</span><span class="sxs-lookup"><span data-stu-id="b88da-130">_Mbx_</span></span> <br/> |<span data-ttu-id="b88da-131">邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="b88da-131">The SMTP address of the mailbox owner.</span></span>  <br/> |
| <span data-ttu-id="b88da-132">_发件人_</span><span class="sxs-lookup"><span data-stu-id="b88da-132">_Sender_</span></span> <br/> |<span data-ttu-id="b88da-133">发件人 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="b88da-133">The SMTP address of the message's sender.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b88da-134">注解</span><span class="sxs-lookup"><span data-stu-id="b88da-134">Remarks</span></span>

<span data-ttu-id="b88da-135">**EcpUrl 黑**元素是**协议**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="b88da-135">The **EcpUrl-mt** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b88da-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b88da-136">See also</span></span>



[<span data-ttu-id="b88da-137">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="b88da-137">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

