---
title: 用户回音 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: 用户回音元素均表示为单个用户 GetUserSettings 请求的响应。
ms.openlocfilehash: 6fcd82e06916df5acdd317cb44161c1b69e58574
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2018
ms.locfileid: "19838484"
---
# <a name="userresponse-soap"></a><span data-ttu-id="ec2ba-103">用户回音 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ec2ba-103">UserResponse (SOAP)</span></span>

<span data-ttu-id="ec2ba-104">**用户回音**元素均表示为单个用户 GetUserSettings 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-104">The **UserResponse** element represents a response to a GetUserSettings request for an individual user.</span></span> 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 <span data-ttu-id="ec2ba-105">**用户回音**</span><span class="sxs-lookup"><span data-stu-id="ec2ba-105">**UserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec2ba-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ec2ba-106">Attributes and elements</span></span>

<span data-ttu-id="ec2ba-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec2ba-108">属性</span><span class="sxs-lookup"><span data-stu-id="ec2ba-108">Attributes</span></span>

<span data-ttu-id="ec2ba-109">无。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec2ba-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ec2ba-110">Child elements</span></span>

|<span data-ttu-id="ec2ba-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ec2ba-111">**Element**</span></span>|<span data-ttu-id="ec2ba-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ec2ba-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec2ba-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ec2ba-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="ec2ba-114">代表由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="ec2ba-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ec2ba-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="ec2ba-116">代表相关联的自动发现服务返回的错误代码的邮件。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="ec2ba-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ec2ba-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="ec2ba-118">包含目标的重定向 URL 或电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-118">Contains the target of the redirection URL or email address.</span></span>  <br/> |
|[<span data-ttu-id="ec2ba-119">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ec2ba-119">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="ec2ba-120">表示不会返回的设置的信息的集合。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-120">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="ec2ba-121">用户设置 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ec2ba-121">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="ec2ba-122">用户请求的设置。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-122">The requested settings for the user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec2ba-123">父元素</span><span class="sxs-lookup"><span data-stu-id="ec2ba-123">Parent elements</span></span>

|<span data-ttu-id="ec2ba-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="ec2ba-124">**Element**</span></span>|<span data-ttu-id="ec2ba-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="ec2ba-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec2ba-126">ArrayOfUserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ec2ba-126">ArrayOfUserResponse (SOAP)</span></span>](arrayofuserresponse-soap.md) <br/> |<span data-ttu-id="ec2ba-127">包含一组用户响应的数目。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-127">Contains an array of user responses.</span></span>  <br/> |
|[<span data-ttu-id="ec2ba-128">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ec2ba-128">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="ec2ba-129">包含为每个请求的用户的配置设置。</span><span class="sxs-lookup"><span data-stu-id="ec2ba-129">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="ec2ba-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="ec2ba-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec2ba-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="ec2ba-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ec2ba-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="ec2ba-132">Schema Name</span></span>  <br/> |<span data-ttu-id="ec2ba-133">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="ec2ba-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ec2ba-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="ec2ba-134">Validation File</span></span>  <br/> |<span data-ttu-id="ec2ba-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ec2ba-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec2ba-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="ec2ba-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec2ba-137">True</span><span class="sxs-lookup"><span data-stu-id="ec2ba-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec2ba-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ec2ba-138">See also</span></span>



[<span data-ttu-id="ec2ba-139">SOAP Exchange 2013 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="ec2ba-139">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

