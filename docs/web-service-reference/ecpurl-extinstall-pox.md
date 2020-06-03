---
title: EcpUrl-extinstall （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f81807e6-93de-4e47-afee-1e1ae6a85054
description: EcpUrl-extinstall 元素指定一个部分 URL，该 URL 可以与 EcpUrl （POX）元素的值结合使用，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 URL。
ms.openlocfilehash: 889e0ca3bdcdce4b557fe066db2918fde4abaa9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461301"
---
# <a name="ecpurl-extinstall-pox"></a><span data-ttu-id="bd6cd-103">EcpUrl-extinstall （POX）</span><span class="sxs-lookup"><span data-stu-id="bd6cd-103">EcpUrl-extinstall (POX)</span></span>

<span data-ttu-id="bd6cd-104">**EcpUrl-extinstall**元素指定一个部分 url，该 url 可以与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 url。</span><span class="sxs-lookup"><span data-stu-id="bd6cd-104">The **EcpUrl-extinstall** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the mail apps currently installed in the user's mailbox.</span></span> 
  
[<span data-ttu-id="bd6cd-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="bd6cd-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="bd6cd-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="bd6cd-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="bd6cd-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="bd6cd-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="bd6cd-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="bd6cd-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="bd6cd-109">EcpUrl-extinstall （POX）</span><span class="sxs-lookup"><span data-stu-id="bd6cd-109">EcpUrl-extinstall (POX)</span></span>](ecpurl-extinstall-pox.md)
  
```XML
<EcpUrl-extinstall/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bd6cd-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bd6cd-110">Attributes and elements</span></span>

<span data-ttu-id="bd6cd-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bd6cd-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd6cd-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="bd6cd-112">Attributes</span></span>

<span data-ttu-id="bd6cd-113">无。</span><span class="sxs-lookup"><span data-stu-id="bd6cd-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd6cd-114">子元素</span><span class="sxs-lookup"><span data-stu-id="bd6cd-114">Child elements</span></span>

<span data-ttu-id="bd6cd-115">无。</span><span class="sxs-lookup"><span data-stu-id="bd6cd-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bd6cd-116">父元素</span><span class="sxs-lookup"><span data-stu-id="bd6cd-116">Parent elements</span></span>

|<span data-ttu-id="bd6cd-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="bd6cd-117">**Element**</span></span>|<span data-ttu-id="bd6cd-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="bd6cd-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd6cd-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="bd6cd-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="bd6cd-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="bd6cd-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bd6cd-121">文本值</span><span class="sxs-lookup"><span data-stu-id="bd6cd-121">Text value</span></span>

<span data-ttu-id="bd6cd-122">Text 值代表可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 url。</span><span class="sxs-lookup"><span data-stu-id="bd6cd-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the mail apps currently installed in the user's mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bd6cd-123">备注</span><span class="sxs-lookup"><span data-stu-id="bd6cd-123">Remarks</span></span>

<span data-ttu-id="bd6cd-124">**EcpUrl-extinstall**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="bd6cd-124">The **EcpUrl-extinstall** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd6cd-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bd6cd-125">See also</span></span>



[<span data-ttu-id="bd6cd-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="bd6cd-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

