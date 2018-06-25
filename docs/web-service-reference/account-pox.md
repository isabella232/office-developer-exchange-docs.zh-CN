---
title: 帐户 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: 帐户元素指定的用户帐户设置，或包含错误响应。
ms.openlocfilehash: 88911aad41816f7cefbffef151e066fe5d4da192
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754263"
---
# <a name="account-pox"></a><span data-ttu-id="6fb48-103">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-103">Account (POX)</span></span>

<span data-ttu-id="6fb48-104">**帐户**元素指定的用户帐户设置，或包含错误响应。</span><span class="sxs-lookup"><span data-stu-id="6fb48-104">The **Account** element specifies account settings for the user or contains error responses.</span></span> 
  
- [<span data-ttu-id="6fb48-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="6fb48-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="6fb48-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-107">Account (POX)</span></span>](account-pox.md)
  
```XML
<Account>
   <AccountType/>
   <Action/>
   <MicrosoftOnline/>
   <RedirectURL/>
   <RedirectAddr/>
   <Image/>
   <ServiceHome/>
   <Protocol/>
   <PublicFolderInformation/>
</Account>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="6fb48-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6fb48-108">Attributes and elements</span></span>

<span data-ttu-id="6fb48-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6fb48-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6fb48-110">属性</span><span class="sxs-lookup"><span data-stu-id="6fb48-110">Attributes</span></span>

<span data-ttu-id="6fb48-111">无。</span><span class="sxs-lookup"><span data-stu-id="6fb48-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6fb48-112">子元素</span><span class="sxs-lookup"><span data-stu-id="6fb48-112">Child elements</span></span>

|<span data-ttu-id="6fb48-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6fb48-113">**Element**</span></span>|<span data-ttu-id="6fb48-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6fb48-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fb48-115">AccountType (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-115">AccountType (POX)</span></span>](accounttype-pox.md) <br/> |<span data-ttu-id="6fb48-116">表示的帐户类型。</span><span class="sxs-lookup"><span data-stu-id="6fb48-116">Represents the account type.</span></span>  <br/> |
|[<span data-ttu-id="6fb48-117">操作 (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-117">Action (POX)</span></span>](action-pox.md) <br/> |<span data-ttu-id="6fb48-118">提供用于确定是否需要返回用户配置信息的另一个自动发现请求的信息。</span><span class="sxs-lookup"><span data-stu-id="6fb48-118">Provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span>  <br/> |
|[<span data-ttu-id="6fb48-119">MicrosoftOnline (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-119">MicrosoftOnline (POX)</span></span>](microsoftonline-pox.md) <br/> |<span data-ttu-id="6fb48-120">包含一个值，指示是否在用户邮箱位于 Exchange Online 或 Exchange Online 作为 Office 365 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6fb48-120">Contains a value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.</span></span>  <br/> |
|[<span data-ttu-id="6fb48-121">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-121">RedirectUrl (POX)</span></span>](redirecturl-pox.md) <br/> |<span data-ttu-id="6fb48-122">包含正在运行了客户端访问服务器角色安装的用于获取自动发现设置的 Exchange Server 的计算机的 URL。</span><span class="sxs-lookup"><span data-stu-id="6fb48-122">Contains the URL of the computer that is running Exchange Server that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span>  <br/> |
|[<span data-ttu-id="6fb48-123">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-123">RedirectAddr (POX)</span></span>](redirectaddr-pox.md) <br/> |<span data-ttu-id="6fb48-124">指定应用于后续的自动发现请求的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="6fb48-124">Specifies the email address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|[<span data-ttu-id="6fb48-125">图像 (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-125">Image (POX)</span></span>](image-pox.md) <br/> |<span data-ttu-id="6fb48-126">包含用于打造品牌的配置体验的图像的路径。</span><span class="sxs-lookup"><span data-stu-id="6fb48-126">Contains the path of an image that is used to brand the configuration experience.</span></span>  <br/> |
|[<span data-ttu-id="6fb48-127">ServiceHome (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-127">ServiceHome (POX)</span></span>](servicehome-pox.md) <br/> |<span data-ttu-id="6fb48-128">包含主页上的 Internet 服务提供商 (ISP) 的 URL。</span><span class="sxs-lookup"><span data-stu-id="6fb48-128">Contains the URL of the home page of the Internet service provider (ISP).</span></span>  <br/> |
|[<span data-ttu-id="6fb48-129">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-129">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="6fb48-130">包含客户端连接到客户端访问服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="6fb48-130">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
|[<span data-ttu-id="6fb48-131">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-131">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="6fb48-132">包含客户端可以使用发送发现用户的公用文件夹信息的自动发现请求的信息。</span><span class="sxs-lookup"><span data-stu-id="6fb48-132">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
|[<span data-ttu-id="6fb48-133">错误 (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-133">Error (POX)</span></span>](error-pox.md) <br/> |<span data-ttu-id="6fb48-134">包含自动发现错误响应。</span><span class="sxs-lookup"><span data-stu-id="6fb48-134">Contains an Autodiscover error response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6fb48-135">父元素</span><span class="sxs-lookup"><span data-stu-id="6fb48-135">Parent elements</span></span>

|<span data-ttu-id="6fb48-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="6fb48-136">**Element**</span></span>|<span data-ttu-id="6fb48-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="6fb48-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fb48-138">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="6fb48-138">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="6fb48-139">包含来自自动发现服务的响应。</span><span class="sxs-lookup"><span data-stu-id="6fb48-139">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fb48-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6fb48-140">See also</span></span>

- [<span data-ttu-id="6fb48-141">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="6fb48-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

