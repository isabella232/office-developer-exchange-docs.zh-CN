---
title: GetUserSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: e7cd470d-5861-41e7-9e66-73ef7a59700b
description: GetUserSettingsResponse 元素均表示 GetUserSettings 操作 (SOAP) 请求的响应。
ms.openlocfilehash: 24dbfb1582f628fd0130aa82ea5f1beedd31b156
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825705"
---
# <a name="getusersettingsresponse-soap"></a><span data-ttu-id="136ee-103">GetUserSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="136ee-103">GetUserSettingsResponse (SOAP)</span></span>

<span data-ttu-id="136ee-104">**GetUserSettingsResponse**元素均表示[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="136ee-104">The **GetUserSettingsResponse** element represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span> 
  
```XML
<GetUserSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</GetUserSettingsResponse>
```

 <span data-ttu-id="136ee-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="136ee-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="136ee-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="136ee-106">Attributes and elements</span></span>

<span data-ttu-id="136ee-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="136ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="136ee-108">属性</span><span class="sxs-lookup"><span data-stu-id="136ee-108">Attributes</span></span>

<span data-ttu-id="136ee-109">无。</span><span class="sxs-lookup"><span data-stu-id="136ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="136ee-110">子元素</span><span class="sxs-lookup"><span data-stu-id="136ee-110">Child elements</span></span>

|<span data-ttu-id="136ee-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="136ee-111">**Element**</span></span>|<span data-ttu-id="136ee-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="136ee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="136ee-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="136ee-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="136ee-114">代表由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="136ee-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="136ee-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="136ee-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="136ee-116">代表相关联的自动发现服务返回的错误代码的邮件。</span><span class="sxs-lookup"><span data-stu-id="136ee-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="136ee-117">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="136ee-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="136ee-118">包含为每个请求的用户的配置设置。</span><span class="sxs-lookup"><span data-stu-id="136ee-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="136ee-119">父元素</span><span class="sxs-lookup"><span data-stu-id="136ee-119">Parent elements</span></span>

<span data-ttu-id="136ee-120">无。</span><span class="sxs-lookup"><span data-stu-id="136ee-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="136ee-121">文本值</span><span class="sxs-lookup"><span data-stu-id="136ee-121">Text value</span></span>

<span data-ttu-id="136ee-122">无。</span><span class="sxs-lookup"><span data-stu-id="136ee-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="136ee-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="136ee-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="136ee-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="136ee-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="136ee-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="136ee-125">Schema Name</span></span>  <br/> |<span data-ttu-id="136ee-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="136ee-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="136ee-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="136ee-127">Validation File</span></span>  <br/> |<span data-ttu-id="136ee-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="136ee-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="136ee-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="136ee-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="136ee-130">True</span><span class="sxs-lookup"><span data-stu-id="136ee-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="136ee-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="136ee-131">See also</span></span>



[<span data-ttu-id="136ee-132">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="136ee-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

