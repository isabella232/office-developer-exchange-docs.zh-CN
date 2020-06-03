---
title: EwsPartnerUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ebae21c-3efa-4239-9b49-4a3a8871449b
description: EwsPartnerUrl 元素指定启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。
ms.openlocfilehash: a67eb17bb3db67a922c53ba5e37900ee0a9b956b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526107"
---
# <a name="ewspartnerurl-pox"></a><span data-ttu-id="08d23-103">EwsPartnerUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="08d23-103">EwsPartnerUrl (POX)</span></span>

<span data-ttu-id="08d23-104">**EwsPartnerUrl**元素指定启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="08d23-104">The **EwsPartnerUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="08d23-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="08d23-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="08d23-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="08d23-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="08d23-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="08d23-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="08d23-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="08d23-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="08d23-109">EwsPartnerUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="08d23-109">EwsPartnerUrl (POX)</span></span>](ewspartnerurl-pox.md)
  
```XML
<EwsPartnerUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="08d23-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="08d23-110">Attributes and elements</span></span>

<span data-ttu-id="08d23-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="08d23-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08d23-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="08d23-112">Attributes</span></span>

<span data-ttu-id="08d23-113">无。</span><span class="sxs-lookup"><span data-stu-id="08d23-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="08d23-114">子元素</span><span class="sxs-lookup"><span data-stu-id="08d23-114">Child elements</span></span>

<span data-ttu-id="08d23-115">无。</span><span class="sxs-lookup"><span data-stu-id="08d23-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="08d23-116">父元素</span><span class="sxs-lookup"><span data-stu-id="08d23-116">Parent elements</span></span>

|<span data-ttu-id="08d23-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="08d23-117">**Element**</span></span>|<span data-ttu-id="08d23-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="08d23-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08d23-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="08d23-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="08d23-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="08d23-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="08d23-121">文本值</span><span class="sxs-lookup"><span data-stu-id="08d23-121">Text value</span></span>

<span data-ttu-id="08d23-122">文本值表示用户的 EWS 终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="08d23-122">The text value represents the URL of the EWS endpoint for the user.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08d23-123">备注</span><span class="sxs-lookup"><span data-stu-id="08d23-123">Remarks</span></span>

<span data-ttu-id="08d23-124">**EwsPartnerUrl**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="08d23-124">The **EwsPartnerUrl** element is an optional child element of the **Protocol** element.</span></span> <span data-ttu-id="08d23-125">它等效于[mailbox.ewsurl （POX）](ewsurl-pox.md)元素。</span><span class="sxs-lookup"><span data-stu-id="08d23-125">It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08d23-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="08d23-126">See also</span></span>



[<span data-ttu-id="08d23-127">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="08d23-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

