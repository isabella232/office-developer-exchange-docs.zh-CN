---
title: SmtpAddress （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: SmtpAddress 元素包含分配给为用户配置的公用文件夹邮件存储的 SMTP 地址。
ms.openlocfilehash: 48703a11fb056967c6c76073c2e928d5f6efa264
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468640"
---
# <a name="smtpaddress-pox"></a><span data-ttu-id="366fc-103">SmtpAddress （POX）</span><span class="sxs-lookup"><span data-stu-id="366fc-103">SmtpAddress (POX)</span></span>

<span data-ttu-id="366fc-104">**SmtpAddress**元素包含分配给为用户配置的公用文件夹邮件存储的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="366fc-104">The **SmtpAddress** element contains the SMTP address assigned to the public folder message store configured for the user.</span></span> 
  
- [<span data-ttu-id="366fc-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="366fc-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="366fc-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="366fc-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="366fc-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="366fc-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="366fc-108">PublicFolderInformation （POX）</span><span class="sxs-lookup"><span data-stu-id="366fc-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
- [<span data-ttu-id="366fc-109">SmtpAddress （POX）</span><span class="sxs-lookup"><span data-stu-id="366fc-109">SmtpAddress (POX)</span></span>](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="366fc-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="366fc-110">Attributes and elements</span></span>

<span data-ttu-id="366fc-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="366fc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="366fc-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="366fc-112">Attributes</span></span>

<span data-ttu-id="366fc-113">无。</span><span class="sxs-lookup"><span data-stu-id="366fc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="366fc-114">子元素</span><span class="sxs-lookup"><span data-stu-id="366fc-114">Child elements</span></span>

<span data-ttu-id="366fc-115">无。</span><span class="sxs-lookup"><span data-stu-id="366fc-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="366fc-116">父元素</span><span class="sxs-lookup"><span data-stu-id="366fc-116">Parent elements</span></span>

|<span data-ttu-id="366fc-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="366fc-117">**Element**</span></span>|<span data-ttu-id="366fc-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="366fc-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="366fc-119">PublicFolderInformation （POX）</span><span class="sxs-lookup"><span data-stu-id="366fc-119">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="366fc-120">包含客户端可用于发送自动发现请求以发现用户公用文件夹信息的信息。</span><span class="sxs-lookup"><span data-stu-id="366fc-120">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="366fc-121">文本值</span><span class="sxs-lookup"><span data-stu-id="366fc-121">Text value</span></span>

<span data-ttu-id="366fc-122">Text 值表示分配给为用户配置的公用文件夹存储的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="366fc-122">The text value represents the SMTP address assigned to the public folder store configured for the user.</span></span> <span data-ttu-id="366fc-123">此 SMTP 地址可在自动发现请求的[EMailAddress （POX）](emailaddress-pox.md)元素中使用，以发现公用文件夹设置。</span><span class="sxs-lookup"><span data-stu-id="366fc-123">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="366fc-124">备注</span><span class="sxs-lookup"><span data-stu-id="366fc-124">Remarks</span></span>

<span data-ttu-id="366fc-125">**SmtpAddress**元素是**PublicFolderInformation**元素所需的子元素。</span><span class="sxs-lookup"><span data-stu-id="366fc-125">The **SmtpAddress** element is a required child element of the **PublicFolderInformation** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="366fc-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="366fc-126">See also</span></span>

- [<span data-ttu-id="366fc-127">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="366fc-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

