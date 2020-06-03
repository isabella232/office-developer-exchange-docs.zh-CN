---
title: EmwsUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: EmwsUrl 元素指定启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。
ms.openlocfilehash: 19e1078ae8d08513e85d75d87e960a910986f727
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530668"
---
# <a name="emwsurl-pox"></a><span data-ttu-id="2d6f5-103">EmwsUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="2d6f5-103">EmwsUrl (POX)</span></span>

<span data-ttu-id="2d6f5-104">**EmwsUrl**元素指定启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="2d6f5-104">The **EmwsUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
- [<span data-ttu-id="2d6f5-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="2d6f5-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="2d6f5-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="2d6f5-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="2d6f5-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="2d6f5-107">Account (POX)</span></span>](account-pox.md) 
- [<span data-ttu-id="2d6f5-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="2d6f5-108">Protocol (POX)</span></span>](protocol-pox.md) 
- [<span data-ttu-id="2d6f5-109">EmwsUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="2d6f5-109">EmwsUrl (POX)</span></span>](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2d6f5-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d6f5-110">Attributes and elements</span></span>

<span data-ttu-id="2d6f5-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d6f5-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d6f5-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="2d6f5-112">Attributes</span></span>

<span data-ttu-id="2d6f5-113">无。</span><span class="sxs-lookup"><span data-stu-id="2d6f5-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d6f5-114">子元素</span><span class="sxs-lookup"><span data-stu-id="2d6f5-114">Child elements</span></span>

<span data-ttu-id="2d6f5-115">无。</span><span class="sxs-lookup"><span data-stu-id="2d6f5-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d6f5-116">父元素</span><span class="sxs-lookup"><span data-stu-id="2d6f5-116">Parent elements</span></span>

|<span data-ttu-id="2d6f5-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d6f5-117">**Element**</span></span>|<span data-ttu-id="2d6f5-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d6f5-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d6f5-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="2d6f5-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="2d6f5-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="2d6f5-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2d6f5-121">文本值</span><span class="sxs-lookup"><span data-stu-id="2d6f5-121">Text value</span></span>

<span data-ttu-id="2d6f5-122">文本值表示用户的 EWS 终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="2d6f5-122">The text value represents the URL of the EWS endpoint for the user.</span></span> <span data-ttu-id="2d6f5-123">它等效于[mailbox.ewsurl （POX）](ewsurl-pox.md)元素。</span><span class="sxs-lookup"><span data-stu-id="2d6f5-123">It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d6f5-124">备注</span><span class="sxs-lookup"><span data-stu-id="2d6f5-124">Remarks</span></span>

<span data-ttu-id="2d6f5-125">**EmwsUrl**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="2d6f5-125">The **EmwsUrl** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d6f5-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d6f5-126">See also</span></span>

- [<span data-ttu-id="2d6f5-127">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="2d6f5-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

