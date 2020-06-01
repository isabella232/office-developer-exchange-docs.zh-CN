---
title: EcpUrl-mt （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: EcpUrl 元素指定一个部分 URL，该 URL 可以与 EcpUrl （POX）元素的值相结合，以生成可用于访问启用邮件的用户的电子邮件跟踪设置的 URL。
ms.openlocfilehash: 097811add5635bca14c659814652bca244a1398d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458710"
---
# <a name="ecpurl-mt-pox"></a><span data-ttu-id="b0ebe-103">EcpUrl-mt （POX）</span><span class="sxs-lookup"><span data-stu-id="b0ebe-103">EcpUrl-mt (POX)</span></span>

<span data-ttu-id="b0ebe-104">**EcpUrl**元素指定一个部分 url，该 url 可以与[EcpUrl （POX）](ecpurl-pox.md)元素的值相结合，以生成可用于访问启用邮件的用户的电子邮件跟踪设置的 url。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-104">The **EcpUrl-mt** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="b0ebe-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="b0ebe-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="b0ebe-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="b0ebe-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="b0ebe-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="b0ebe-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="b0ebe-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="b0ebe-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="b0ebe-109">EcpUrl-mt （POX）</span><span class="sxs-lookup"><span data-stu-id="b0ebe-109">EcpUrl-mt (POX)</span></span>](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b0ebe-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b0ebe-110">Attributes and elements</span></span>

<span data-ttu-id="b0ebe-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0ebe-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="b0ebe-112">Attributes</span></span>

<span data-ttu-id="b0ebe-113">无。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0ebe-114">子元素</span><span class="sxs-lookup"><span data-stu-id="b0ebe-114">Child elements</span></span>

<span data-ttu-id="b0ebe-115">无。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0ebe-116">父元素</span><span class="sxs-lookup"><span data-stu-id="b0ebe-116">Parent elements</span></span>

|<span data-ttu-id="b0ebe-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0ebe-117">**Element**</span></span>|<span data-ttu-id="b0ebe-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0ebe-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0ebe-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="b0ebe-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="b0ebe-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b0ebe-121">文本值</span><span class="sxs-lookup"><span data-stu-id="b0ebe-121">Text value</span></span>

<span data-ttu-id="b0ebe-122">Text 值表示一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于访问用户的电子邮件跟踪设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email tracking settings for the user.</span></span> <span data-ttu-id="b0ebe-123">**EcpUrl**元素的值包含在 "<" 和 ">" 字符中包含的参数，这些参数由客户端替代，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-123">The value of the **EcpUrl-mt** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="b0ebe-124">**参数**</span><span class="sxs-lookup"><span data-stu-id="b0ebe-124">**Parameter**</span></span>|<span data-ttu-id="b0ebe-125">**替换为**</span><span class="sxs-lookup"><span data-stu-id="b0ebe-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b0ebe-126">_IsOwa_</span><span class="sxs-lookup"><span data-stu-id="b0ebe-126">_IsOwa_</span></span> <br/> |<span data-ttu-id="b0ebe-127">n</span><span class="sxs-lookup"><span data-stu-id="b0ebe-127">n</span></span>  <br/> |
| <span data-ttu-id="b0ebe-128">_MsgID_</span><span class="sxs-lookup"><span data-stu-id="b0ebe-128">_MsgID_</span></span> <br/> |<span data-ttu-id="b0ebe-129">要跟踪的邮件的 Internet 邮件标识符（由邮件 ID 标头指定）。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-129">Internet message identifier of the message to be tracked as specified by the Message-ID header.</span></span>  <br/> |
| <span data-ttu-id="b0ebe-130">_Mbx_</span><span class="sxs-lookup"><span data-stu-id="b0ebe-130">_Mbx_</span></span> <br/> |<span data-ttu-id="b0ebe-131">邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-131">The SMTP address of the mailbox owner.</span></span>  <br/> |
| <span data-ttu-id="b0ebe-132">_Sender_</span><span class="sxs-lookup"><span data-stu-id="b0ebe-132">_Sender_</span></span> <br/> |<span data-ttu-id="b0ebe-133">邮件发件人的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-133">The SMTP address of the message's sender.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0ebe-134">备注</span><span class="sxs-lookup"><span data-stu-id="b0ebe-134">Remarks</span></span>

<span data-ttu-id="b0ebe-135">**EcpUrl-mt**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="b0ebe-135">The **EcpUrl-mt** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b0ebe-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b0ebe-136">See also</span></span>



[<span data-ttu-id="b0ebe-137">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="b0ebe-137">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

