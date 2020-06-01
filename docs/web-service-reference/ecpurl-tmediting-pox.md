---
title: EcpUrl-tmEditing （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: EcpUrl-tmEditing 元素指定一个可与 EcpUrl （POX）元素的值结合使用的部分 URL，以生成可用于编辑现有网站邮箱的 URL。
ms.openlocfilehash: 5d6c6b8e8f73d113cfde3570065435927ffbae05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463536"
---
# <a name="ecpurl-tmediting-pox"></a><span data-ttu-id="d655b-103">EcpUrl-tmEditing （POX）</span><span class="sxs-lookup"><span data-stu-id="d655b-103">EcpUrl-tmEditing (POX)</span></span>

<span data-ttu-id="d655b-104">**EcpUrl-tmEditing**元素指定一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于编辑现有网站邮箱的 url。</span><span class="sxs-lookup"><span data-stu-id="d655b-104">The **EcpUrl-tmEditing** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> 
  
[<span data-ttu-id="d655b-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="d655b-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="d655b-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="d655b-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="d655b-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="d655b-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="d655b-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="d655b-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="d655b-109">EcpUrl-tmEditing （POX）</span><span class="sxs-lookup"><span data-stu-id="d655b-109">EcpUrl-tmEditing (POX)</span></span>](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d655b-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d655b-110">Attributes and elements</span></span>

<span data-ttu-id="d655b-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d655b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d655b-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="d655b-112">Attributes</span></span>

<span data-ttu-id="d655b-113">无。</span><span class="sxs-lookup"><span data-stu-id="d655b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d655b-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d655b-114">Child elements</span></span>

<span data-ttu-id="d655b-115">无。</span><span class="sxs-lookup"><span data-stu-id="d655b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d655b-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d655b-116">Parent elements</span></span>

|<span data-ttu-id="d655b-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="d655b-117">**Element**</span></span>|<span data-ttu-id="d655b-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d655b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d655b-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="d655b-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d655b-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="d655b-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d655b-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d655b-121">Text value</span></span>

<span data-ttu-id="d655b-122">Text 值表示一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于编辑现有网站邮箱的 URL。</span><span class="sxs-lookup"><span data-stu-id="d655b-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> <span data-ttu-id="d655b-123">**EcpUrl-tmEditing**元素的值包含在 "<" 和 ">" 字符中包含的参数，这些参数由客户端替换，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="d655b-123">The value of the **EcpUrl-tmEditing** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="d655b-124">**参数**</span><span class="sxs-lookup"><span data-stu-id="d655b-124">**Parameter**</span></span>|<span data-ttu-id="d655b-125">**替换为**</span><span class="sxs-lookup"><span data-stu-id="d655b-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d655b-126">_Id_</span><span class="sxs-lookup"><span data-stu-id="d655b-126">_Id_</span></span> <br/> |<span data-ttu-id="d655b-127">网站邮箱的 SMTP 电子邮件地址或 X500 可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="d655b-127">The SMTP email address or the X500 distinguished name of the site mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d655b-128">备注</span><span class="sxs-lookup"><span data-stu-id="d655b-128">Remarks</span></span>

<span data-ttu-id="d655b-129">**EcpUrl-tmEditing**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="d655b-129">The **EcpUrl-tmEditing** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d655b-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d655b-130">See also</span></span>



[<span data-ttu-id="d655b-131">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="d655b-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

