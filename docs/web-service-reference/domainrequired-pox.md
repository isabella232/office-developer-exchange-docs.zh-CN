---
title: DomainRequired （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: DomainRequired 元素指示是否需要域进行身份验证。
ms.openlocfilehash: 97d602c40b247f9a6650cc4440b53bf23c18482e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461322"
---
# <a name="domainrequired-pox"></a><span data-ttu-id="4d482-103">DomainRequired （POX）</span><span class="sxs-lookup"><span data-stu-id="4d482-103">DomainRequired (POX)</span></span>

<span data-ttu-id="4d482-104">**DomainRequired**元素指示是否需要域进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4d482-104">The **DomainRequired** element indicates whether the domain is required for authentication.</span></span> 
  
- [<span data-ttu-id="4d482-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="4d482-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="4d482-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="4d482-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="4d482-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="4d482-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="4d482-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="4d482-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="4d482-109">DomainRequired （POX）</span><span class="sxs-lookup"><span data-stu-id="4d482-109">DomainRequired (POX)</span></span>](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="4d482-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4d482-110">Attributes and elements</span></span>

<span data-ttu-id="4d482-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4d482-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d482-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="4d482-112">Attributes</span></span>

<span data-ttu-id="4d482-113">无。</span><span class="sxs-lookup"><span data-stu-id="4d482-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d482-114">子元素</span><span class="sxs-lookup"><span data-stu-id="4d482-114">Child elements</span></span>

<span data-ttu-id="4d482-115">无。</span><span class="sxs-lookup"><span data-stu-id="4d482-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4d482-116">父元素</span><span class="sxs-lookup"><span data-stu-id="4d482-116">Parent elements</span></span>

|<span data-ttu-id="4d482-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d482-117">**Element**</span></span>|<span data-ttu-id="4d482-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d482-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d482-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="4d482-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="4d482-120">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="4d482-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4d482-121">文本值</span><span class="sxs-lookup"><span data-stu-id="4d482-121">Text value</span></span>

<span data-ttu-id="4d482-122">Text 值指示是否需要域进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4d482-122">The text value indicates whether the domain is required for authentication.</span></span> <span data-ttu-id="4d482-123">可能的值为 **"开" 或 "** **关**"。</span><span class="sxs-lookup"><span data-stu-id="4d482-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="4d482-124">如果值为 **"开**"，则后续请求必须包含用户帐户的域。</span><span class="sxs-lookup"><span data-stu-id="4d482-124">If the value is **on**, the subsequent request must contain the domain of the user's account.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d482-125">备注</span><span class="sxs-lookup"><span data-stu-id="4d482-125">Remarks</span></span>

<span data-ttu-id="4d482-126">如果未在[person.loginname （POX）](loginname-pox.md)元素中指定域，或未指定**person.loginname**元素，则用户必须输入域，然后身份验证才能成功。</span><span class="sxs-lookup"><span data-stu-id="4d482-126">If the domain is not specified in the [LoginName (POX)](loginname-pox.md) element, or the **LoginName** element was not specified, the user must enter the domain before authentication will succeed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d482-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d482-127">See also</span></span>

- [<span data-ttu-id="4d482-128">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="4d482-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

