---
title: GetUserSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 832a9211-d2d5-4a49-bcb3-1dc6dc3904ed
description: GetUserSettingsRequest 元素表示可以检索指定的设置为一个或多个用户的请求。
ms.openlocfilehash: dc22570144a6947dc6e7042326c7416422680cc1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825702"
---
# <a name="getusersettingsrequest-soap"></a><span data-ttu-id="52e3c-103">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52e3c-103">GetUserSettingsRequest (SOAP)</span></span>

<span data-ttu-id="52e3c-104">**GetUserSettingsRequest**元素表示可以检索指定的设置为一个或多个用户的请求。</span><span class="sxs-lookup"><span data-stu-id="52e3c-104">The **GetUserSettingsRequest** element represents a request to retrieve specified settings for one or more users.</span></span> 
  
```XML
<GetUserSettingsRequest>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetUserSettingsRequest>
```

 <span data-ttu-id="52e3c-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="52e3c-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52e3c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52e3c-106">Attributes and elements</span></span>

<span data-ttu-id="52e3c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52e3c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52e3c-108">属性</span><span class="sxs-lookup"><span data-stu-id="52e3c-108">Attributes</span></span>

<span data-ttu-id="52e3c-109">无。</span><span class="sxs-lookup"><span data-stu-id="52e3c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52e3c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="52e3c-110">Child elements</span></span>

|<span data-ttu-id="52e3c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="52e3c-111">**Element**</span></span>|<span data-ttu-id="52e3c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="52e3c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52e3c-113">用户 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52e3c-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="52e3c-114">代表电子邮件地址设置应为其检索用户的集合。</span><span class="sxs-lookup"><span data-stu-id="52e3c-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="52e3c-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52e3c-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="52e3c-116">包含请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="52e3c-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="52e3c-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52e3c-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="52e3c-118">指定提供程序希望使用的特定服务器版本。</span><span class="sxs-lookup"><span data-stu-id="52e3c-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52e3c-119">父元素</span><span class="sxs-lookup"><span data-stu-id="52e3c-119">Parent elements</span></span>

<span data-ttu-id="52e3c-120">无。</span><span class="sxs-lookup"><span data-stu-id="52e3c-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="52e3c-121">文本值</span><span class="sxs-lookup"><span data-stu-id="52e3c-121">Text value</span></span>

<span data-ttu-id="52e3c-122">无。</span><span class="sxs-lookup"><span data-stu-id="52e3c-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52e3c-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="52e3c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52e3c-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="52e3c-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="52e3c-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="52e3c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="52e3c-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="52e3c-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="52e3c-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="52e3c-127">Validation File</span></span>  <br/> |<span data-ttu-id="52e3c-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="52e3c-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52e3c-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="52e3c-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="52e3c-130">True</span><span class="sxs-lookup"><span data-stu-id="52e3c-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52e3c-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52e3c-131">See also</span></span>



[<span data-ttu-id="52e3c-132">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52e3c-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

