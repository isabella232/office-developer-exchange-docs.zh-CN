---
title: PublicFolderInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: PublicFolderInformation 元素包含客户端可以使用发送发现用户的公用文件夹信息的自动发现请求的信息。
ms.openlocfilehash: bb4432a664024c3d1ccb17826948cfe7a1b58cdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826927"
---
# <a name="publicfolderinformation-pox"></a><span data-ttu-id="abf38-103">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="abf38-103">PublicFolderInformation (POX)</span></span>

<span data-ttu-id="abf38-104">**PublicFolderInformation**元素包含客户端可以使用发送发现用户的公用文件夹信息的自动发现请求的信息。</span><span class="sxs-lookup"><span data-stu-id="abf38-104">The **PublicFolderInformation** element contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span> 
  
[<span data-ttu-id="abf38-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="abf38-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="abf38-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="abf38-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="abf38-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="abf38-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="abf38-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="abf38-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="abf38-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="abf38-109">Attributes and elements</span></span>

<span data-ttu-id="abf38-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="abf38-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abf38-111">属性</span><span class="sxs-lookup"><span data-stu-id="abf38-111">Attributes</span></span>

<span data-ttu-id="abf38-112">无。</span><span class="sxs-lookup"><span data-stu-id="abf38-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="abf38-113">子元素</span><span class="sxs-lookup"><span data-stu-id="abf38-113">Child elements</span></span>

|<span data-ttu-id="abf38-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="abf38-114">**Element**</span></span>|<span data-ttu-id="abf38-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="abf38-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abf38-116">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="abf38-116">SmtpAddress (POX)</span></span>](smtpaddress-pox.md) <br/> |<span data-ttu-id="abf38-117">包含分配给公用文件夹消息存储为用户配置的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="abf38-117">Contains the SMTP address assigned to the public folder message store configured for the user.</span></span> <span data-ttu-id="abf38-118">此 SMTP 地址可以自动发现请求的[电子邮件地址 (POX)](emailaddress-pox.md)元素中，用于发现公用文件夹设置。</span><span class="sxs-lookup"><span data-stu-id="abf38-118">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="abf38-119">父元素</span><span class="sxs-lookup"><span data-stu-id="abf38-119">Parent elements</span></span>

|<span data-ttu-id="abf38-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="abf38-120">**Element**</span></span>|<span data-ttu-id="abf38-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="abf38-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abf38-122">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="abf38-122">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="abf38-123">指定用户帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="abf38-123">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abf38-124">备注</span><span class="sxs-lookup"><span data-stu-id="abf38-124">Remarks</span></span>

<span data-ttu-id="abf38-125">**PublicFolderInformation**元素是**帐户**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="abf38-125">The **PublicFolderInformation** element is an optional child element of the **Account** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="abf38-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="abf38-126">See also</span></span>



[<span data-ttu-id="abf38-127">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="abf38-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

