---
title: 请求 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75696436-997e-49f1-a31b-eb9a8c3526f3
description: Request 元素包含请求的配置设置和目标用户。
ms.openlocfilehash: 4358713d19e763b75d2a43f147385026f43b1255
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44448987"
---
# <a name="request-soap"></a><span data-ttu-id="ad1cc-103">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad1cc-103">Request (SOAP)</span></span>

<span data-ttu-id="ad1cc-104">**Request**元素包含请求的配置设置和目标用户。</span><span class="sxs-lookup"><span data-stu-id="ad1cc-104">The **Request** element contains the requested configuration settings and the target users.</span></span> 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 <span data-ttu-id="ad1cc-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="ad1cc-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad1cc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ad1cc-106">Attributes and elements</span></span>

<span data-ttu-id="ad1cc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ad1cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad1cc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ad1cc-108">Attributes</span></span>

<span data-ttu-id="ad1cc-109">无。</span><span class="sxs-lookup"><span data-stu-id="ad1cc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad1cc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ad1cc-110">Child elements</span></span>

|<span data-ttu-id="ad1cc-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ad1cc-111">**Element**</span></span>|<span data-ttu-id="ad1cc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ad1cc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad1cc-113">Users （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ad1cc-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="ad1cc-114">表示应检索其设置的用户的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="ad1cc-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="ad1cc-115">RequestedSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ad1cc-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="ad1cc-116">包含所请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="ad1cc-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="ad1cc-117">RequestedVersion （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ad1cc-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="ad1cc-118">指定提供程序要使用的特定服务器版本。</span><span class="sxs-lookup"><span data-stu-id="ad1cc-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ad1cc-119">父元素</span><span class="sxs-lookup"><span data-stu-id="ad1cc-119">Parent elements</span></span>

|<span data-ttu-id="ad1cc-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="ad1cc-120">**Element**</span></span>|<span data-ttu-id="ad1cc-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="ad1cc-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad1cc-122">GetUserSettingsRequestMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ad1cc-122">GetUserSettingsRequestMessage (SOAP)</span></span>](getusersettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="ad1cc-123">表示[GetUserSettings 操作（SOAP）](getusersettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="ad1cc-123">Represents a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ad1cc-124">文本值</span><span class="sxs-lookup"><span data-stu-id="ad1cc-124">Text value</span></span>

<span data-ttu-id="ad1cc-125">无。</span><span class="sxs-lookup"><span data-stu-id="ad1cc-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad1cc-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="ad1cc-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad1cc-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="ad1cc-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ad1cc-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="ad1cc-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ad1cc-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="ad1cc-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ad1cc-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="ad1cc-130">Validation File</span></span>  <br/> |<span data-ttu-id="ad1cc-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ad1cc-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ad1cc-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="ad1cc-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad1cc-133">True</span><span class="sxs-lookup"><span data-stu-id="ad1cc-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad1cc-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ad1cc-134">See also</span></span>



[<span data-ttu-id="ad1cc-135">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad1cc-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

