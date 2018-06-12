---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: SmtpAddress 元素包含分配给公用文件夹消息存储为用户配置的 SMTP 地址。
ms.openlocfilehash: 43ebb328e31cdec11412e80b743d4d4393b7960a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827507"
---
# <a name="smtpaddress-pox"></a><span data-ttu-id="be437-103">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="be437-103">SmtpAddress (POX)</span></span>

<span data-ttu-id="be437-104">**SmtpAddress**元素包含分配给公用文件夹消息存储为用户配置的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="be437-104">The **SmtpAddress** element contains the SMTP address assigned to the public folder message store configured for the user.</span></span> 
  
- [<span data-ttu-id="be437-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="be437-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="be437-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="be437-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="be437-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="be437-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="be437-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="be437-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
- [<span data-ttu-id="be437-109">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="be437-109">SmtpAddress (POX)</span></span>](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="be437-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="be437-110">Attributes and elements</span></span>

<span data-ttu-id="be437-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="be437-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be437-112">属性</span><span class="sxs-lookup"><span data-stu-id="be437-112">Attributes</span></span>

<span data-ttu-id="be437-113">无。</span><span class="sxs-lookup"><span data-stu-id="be437-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be437-114">子元素</span><span class="sxs-lookup"><span data-stu-id="be437-114">Child elements</span></span>

<span data-ttu-id="be437-115">无。</span><span class="sxs-lookup"><span data-stu-id="be437-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="be437-116">父元素</span><span class="sxs-lookup"><span data-stu-id="be437-116">Parent elements</span></span>

|<span data-ttu-id="be437-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="be437-117">**Element**</span></span>|<span data-ttu-id="be437-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="be437-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be437-119">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="be437-119">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="be437-120">包含客户端可以使用发送发现用户的公用文件夹信息的自动发现请求的信息。</span><span class="sxs-lookup"><span data-stu-id="be437-120">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="be437-121">文本值</span><span class="sxs-lookup"><span data-stu-id="be437-121">Text value</span></span>

<span data-ttu-id="be437-122">文本值表示分配给公用文件夹存储为用户配置的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="be437-122">The text value represents the SMTP address assigned to the public folder store configured for the user.</span></span> <span data-ttu-id="be437-123">此 SMTP 地址可以自动发现请求的[电子邮件地址 (POX)](emailaddress-pox.md)元素中，用于发现公用文件夹设置。</span><span class="sxs-lookup"><span data-stu-id="be437-123">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="be437-124">备注</span><span class="sxs-lookup"><span data-stu-id="be437-124">Remarks</span></span>

<span data-ttu-id="be437-125">**SmtpAddress**元素是**PublicFolderInformation**元素的必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="be437-125">The **SmtpAddress** element is a required child element of the **PublicFolderInformation** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be437-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="be437-126">See also</span></span>

- [<span data-ttu-id="be437-127">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="be437-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

