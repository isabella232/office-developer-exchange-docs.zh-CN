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
description: 请求元素包含请求的配置设置和目标用户。
ms.openlocfilehash: dfea33786066dd7803d0fd061cbb87bb06d11531
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827125"
---
# <a name="request-soap"></a><span data-ttu-id="54ca1-103">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="54ca1-103">Request (SOAP)</span></span>

<span data-ttu-id="54ca1-104">**请求**元素包含请求的配置设置和目标用户。</span><span class="sxs-lookup"><span data-stu-id="54ca1-104">The **Request** element contains the requested configuration settings and the target users.</span></span> 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 <span data-ttu-id="54ca1-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="54ca1-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54ca1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="54ca1-106">Attributes and elements</span></span>

<span data-ttu-id="54ca1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="54ca1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54ca1-108">属性</span><span class="sxs-lookup"><span data-stu-id="54ca1-108">Attributes</span></span>

<span data-ttu-id="54ca1-109">无。</span><span class="sxs-lookup"><span data-stu-id="54ca1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54ca1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="54ca1-110">Child elements</span></span>

|<span data-ttu-id="54ca1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="54ca1-111">**Element**</span></span>|<span data-ttu-id="54ca1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="54ca1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54ca1-113">用户 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="54ca1-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="54ca1-114">代表电子邮件地址设置应为其检索用户的集合。</span><span class="sxs-lookup"><span data-stu-id="54ca1-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="54ca1-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="54ca1-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="54ca1-116">包含请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="54ca1-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="54ca1-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="54ca1-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="54ca1-118">指定提供程序希望使用的特定服务器版本。</span><span class="sxs-lookup"><span data-stu-id="54ca1-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="54ca1-119">父元素</span><span class="sxs-lookup"><span data-stu-id="54ca1-119">Parent elements</span></span>

|<span data-ttu-id="54ca1-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="54ca1-120">**Element**</span></span>|<span data-ttu-id="54ca1-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="54ca1-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54ca1-122">GetUserSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="54ca1-122">GetUserSettingsRequestMessage (SOAP)</span></span>](getusersettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="54ca1-123">代表[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="54ca1-123">Represents a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="54ca1-124">文本值</span><span class="sxs-lookup"><span data-stu-id="54ca1-124">Text value</span></span>

<span data-ttu-id="54ca1-125">无。</span><span class="sxs-lookup"><span data-stu-id="54ca1-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54ca1-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="54ca1-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54ca1-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="54ca1-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="54ca1-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="54ca1-128">Schema Name</span></span>  <br/> |<span data-ttu-id="54ca1-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="54ca1-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="54ca1-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="54ca1-130">Validation File</span></span>  <br/> |<span data-ttu-id="54ca1-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="54ca1-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="54ca1-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="54ca1-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="54ca1-133">True</span><span class="sxs-lookup"><span data-stu-id="54ca1-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54ca1-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="54ca1-134">See also</span></span>



[<span data-ttu-id="54ca1-135">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="54ca1-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

