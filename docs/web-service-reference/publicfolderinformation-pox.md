---
title: PublicFolderInformation （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: PublicFolderInformation 元素包含的信息可供客户端用来发送自动发现请求，以发现用户的公用文件夹信息。
ms.openlocfilehash: e044a1feddfaeb4eb93c289c617dde9adc66f332
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457716"
---
# <a name="publicfolderinformation-pox"></a><span data-ttu-id="79053-103">PublicFolderInformation （POX）</span><span class="sxs-lookup"><span data-stu-id="79053-103">PublicFolderInformation (POX)</span></span>

<span data-ttu-id="79053-104">**PublicFolderInformation**元素包含的信息可供客户端用来发送自动发现请求，以发现用户的公用文件夹信息。</span><span class="sxs-lookup"><span data-stu-id="79053-104">The **PublicFolderInformation** element contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span> 
  
[<span data-ttu-id="79053-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="79053-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="79053-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="79053-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="79053-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="79053-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="79053-108">PublicFolderInformation （POX）</span><span class="sxs-lookup"><span data-stu-id="79053-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="79053-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="79053-109">Attributes and elements</span></span>

<span data-ttu-id="79053-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="79053-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79053-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="79053-111">Attributes</span></span>

<span data-ttu-id="79053-112">无。</span><span class="sxs-lookup"><span data-stu-id="79053-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="79053-113">子元素</span><span class="sxs-lookup"><span data-stu-id="79053-113">Child elements</span></span>

|<span data-ttu-id="79053-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="79053-114">**Element**</span></span>|<span data-ttu-id="79053-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="79053-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79053-116">SmtpAddress （POX）</span><span class="sxs-lookup"><span data-stu-id="79053-116">SmtpAddress (POX)</span></span>](smtpaddress-pox.md) <br/> |<span data-ttu-id="79053-117">包含分配给为用户配置的公用文件夹邮件存储的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="79053-117">Contains the SMTP address assigned to the public folder message store configured for the user.</span></span> <span data-ttu-id="79053-118">此 SMTP 地址可在自动发现请求的[EMailAddress （POX）](emailaddress-pox.md)元素中使用，以发现公用文件夹设置。</span><span class="sxs-lookup"><span data-stu-id="79053-118">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="79053-119">父元素</span><span class="sxs-lookup"><span data-stu-id="79053-119">Parent elements</span></span>

|<span data-ttu-id="79053-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="79053-120">**Element**</span></span>|<span data-ttu-id="79053-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="79053-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79053-122">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="79053-122">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="79053-123">指定用户的帐户设置。</span><span class="sxs-lookup"><span data-stu-id="79053-123">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79053-124">备注</span><span class="sxs-lookup"><span data-stu-id="79053-124">Remarks</span></span>

<span data-ttu-id="79053-125">**PublicFolderInformation**元素是**Account**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="79053-125">The **PublicFolderInformation** element is an optional child element of the **Account** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79053-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79053-126">See also</span></span>



[<span data-ttu-id="79053-127">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="79053-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

