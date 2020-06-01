---
title: 帐户（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: Account 元素指定用户的帐户设置或包含错误响应。
ms.openlocfilehash: ffd8ebe4b7bd9d4b3f6a9b42fc557ac6189a068d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462316"
---
# <a name="account-pox"></a><span data-ttu-id="80189-103">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="80189-103">Account (POX)</span></span>

<span data-ttu-id="80189-104">**Account**元素指定用户的帐户设置或包含错误响应。</span><span class="sxs-lookup"><span data-stu-id="80189-104">The **Account** element specifies account settings for the user or contains error responses.</span></span> 
  
- [<span data-ttu-id="80189-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="80189-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
- [<span data-ttu-id="80189-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="80189-106">Response (POX)</span></span>](response-pox.md)
- [<span data-ttu-id="80189-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="80189-107">Account (POX)</span></span>](account-pox.md)
  
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

<br/>

```XML
<Account> 
    <Error/> 
</Account>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="80189-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="80189-108">Attributes and elements</span></span>

<span data-ttu-id="80189-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="80189-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80189-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="80189-110">Attributes</span></span>

<span data-ttu-id="80189-111">无。</span><span class="sxs-lookup"><span data-stu-id="80189-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80189-112">子元素</span><span class="sxs-lookup"><span data-stu-id="80189-112">Child elements</span></span>

|<span data-ttu-id="80189-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="80189-113">**Element**</span></span>|<span data-ttu-id="80189-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="80189-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80189-115">AccountType （POX）</span><span class="sxs-lookup"><span data-stu-id="80189-115">AccountType (POX)</span></span>](accounttype-pox.md) <br/> |<span data-ttu-id="80189-116">代表帐户类型。</span><span class="sxs-lookup"><span data-stu-id="80189-116">Represents the account type.</span></span>  <br/> |
|[<span data-ttu-id="80189-117">Action （POX）</span><span class="sxs-lookup"><span data-stu-id="80189-117">Action (POX)</span></span>](action-pox.md) <br/> |<span data-ttu-id="80189-118">提供用于确定是否需要其他自动发现请求来返回用户配置信息的信息。</span><span class="sxs-lookup"><span data-stu-id="80189-118">Provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span>  <br/> |
|[<span data-ttu-id="80189-119">MicrosoftOnline （POX）</span><span class="sxs-lookup"><span data-stu-id="80189-119">MicrosoftOnline (POX)</span></span>](microsoftonline-pox.md) <br/> |<span data-ttu-id="80189-120">包含一个值，该值指示用户的邮箱是托管在 Exchange Online 中还是 Exchange Online 中作为 Office 365 的一部分承载。</span><span class="sxs-lookup"><span data-stu-id="80189-120">Contains a value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.</span></span>  <br/> |
|[<span data-ttu-id="80189-121">RedirectUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="80189-121">RedirectUrl (POX)</span></span>](redirecturl-pox.md) <br/> |<span data-ttu-id="80189-122">包含运行 Exchange Server 且安装了应用于获取自动发现设置的客户端访问服务器角色的计算机的 URL。</span><span class="sxs-lookup"><span data-stu-id="80189-122">Contains the URL of the computer that is running Exchange Server that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span>  <br/> |
|[<span data-ttu-id="80189-123">RedirectAddr （POX）</span><span class="sxs-lookup"><span data-stu-id="80189-123">RedirectAddr (POX)</span></span>](redirectaddr-pox.md) <br/> |<span data-ttu-id="80189-124">指定应用于后续自动发现请求的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="80189-124">Specifies the email address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|[<span data-ttu-id="80189-125">Image （POX）</span><span class="sxs-lookup"><span data-stu-id="80189-125">Image (POX)</span></span>](image-pox.md) <br/> |<span data-ttu-id="80189-126">包含用于标记配置体验的图像的路径。</span><span class="sxs-lookup"><span data-stu-id="80189-126">Contains the path of an image that is used to brand the configuration experience.</span></span>  <br/> |
|[<span data-ttu-id="80189-127">ServiceHome （POX）</span><span class="sxs-lookup"><span data-stu-id="80189-127">ServiceHome (POX)</span></span>](servicehome-pox.md) <br/> |<span data-ttu-id="80189-128">包含 Internet 服务提供商（ISP）主页的 URL。</span><span class="sxs-lookup"><span data-stu-id="80189-128">Contains the URL of the home page of the Internet service provider (ISP).</span></span>  <br/> |
|[<span data-ttu-id="80189-129">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="80189-129">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="80189-130">包含用于将客户端连接到客户端访问服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="80189-130">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
|[<span data-ttu-id="80189-131">PublicFolderInformation （POX）</span><span class="sxs-lookup"><span data-stu-id="80189-131">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="80189-132">包含客户端可用于发送自动发现请求以发现用户公用文件夹信息的信息。</span><span class="sxs-lookup"><span data-stu-id="80189-132">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
|[<span data-ttu-id="80189-133">错误（POX）</span><span class="sxs-lookup"><span data-stu-id="80189-133">Error (POX)</span></span>](error-pox.md) <br/> |<span data-ttu-id="80189-134">包含自动发现错误响应。</span><span class="sxs-lookup"><span data-stu-id="80189-134">Contains an Autodiscover error response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="80189-135">父元素</span><span class="sxs-lookup"><span data-stu-id="80189-135">Parent elements</span></span>

|<span data-ttu-id="80189-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="80189-136">**Element**</span></span>|<span data-ttu-id="80189-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="80189-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80189-138">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="80189-138">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="80189-139">包含来自自动发现服务的响应。</span><span class="sxs-lookup"><span data-stu-id="80189-139">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80189-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80189-140">See also</span></span>

- [<span data-ttu-id="80189-141">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="80189-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

