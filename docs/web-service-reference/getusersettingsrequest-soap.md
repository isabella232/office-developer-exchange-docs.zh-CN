---
title: GetUserSettingsRequest （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 832a9211-d2d5-4a49-bcb3-1dc6dc3904ed
description: GetUserSettingsRequest 元素表示一个请求，用于检索一个或多个用户的指定设置。
ms.openlocfilehash: 353facb5d0bbf922a23b33cbaf6f9d2e7d82bd6b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530160"
---
# <a name="getusersettingsrequest-soap"></a><span data-ttu-id="c21ad-103">GetUserSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="c21ad-103">GetUserSettingsRequest (SOAP)</span></span>

<span data-ttu-id="c21ad-104">**GetUserSettingsRequest**元素表示一个请求，用于检索一个或多个用户的指定设置。</span><span class="sxs-lookup"><span data-stu-id="c21ad-104">The **GetUserSettingsRequest** element represents a request to retrieve specified settings for one or more users.</span></span> 
  
```XML
<GetUserSettingsRequest>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetUserSettingsRequest>
```

 <span data-ttu-id="c21ad-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="c21ad-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c21ad-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c21ad-106">Attributes and elements</span></span>

<span data-ttu-id="c21ad-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c21ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c21ad-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c21ad-108">Attributes</span></span>

<span data-ttu-id="c21ad-109">无。</span><span class="sxs-lookup"><span data-stu-id="c21ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c21ad-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c21ad-110">Child elements</span></span>

|<span data-ttu-id="c21ad-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c21ad-111">**Element**</span></span>|<span data-ttu-id="c21ad-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c21ad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c21ad-113">Users （SOAP）</span><span class="sxs-lookup"><span data-stu-id="c21ad-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="c21ad-114">表示应检索其设置的用户的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="c21ad-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="c21ad-115">RequestedSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="c21ad-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="c21ad-116">包含所请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="c21ad-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="c21ad-117">RequestedVersion （SOAP）</span><span class="sxs-lookup"><span data-stu-id="c21ad-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="c21ad-118">指定提供程序要使用的特定服务器版本。</span><span class="sxs-lookup"><span data-stu-id="c21ad-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c21ad-119">父元素</span><span class="sxs-lookup"><span data-stu-id="c21ad-119">Parent elements</span></span>

<span data-ttu-id="c21ad-120">无。</span><span class="sxs-lookup"><span data-stu-id="c21ad-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c21ad-121">文本值</span><span class="sxs-lookup"><span data-stu-id="c21ad-121">Text value</span></span>

<span data-ttu-id="c21ad-122">无。</span><span class="sxs-lookup"><span data-stu-id="c21ad-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c21ad-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="c21ad-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c21ad-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="c21ad-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="c21ad-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="c21ad-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c21ad-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="c21ad-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="c21ad-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="c21ad-127">Validation File</span></span>  <br/> |<span data-ttu-id="c21ad-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c21ad-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c21ad-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="c21ad-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="c21ad-130">True</span><span class="sxs-lookup"><span data-stu-id="c21ad-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c21ad-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c21ad-131">See also</span></span>



[<span data-ttu-id="c21ad-132">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c21ad-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

