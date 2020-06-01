---
title: UserResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: UserResponse 元素表示对单个用户的 GetUserSettings 请求的响应。
ms.openlocfilehash: 73848cb19d9c859e07216f354965ac4051d0d20c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468899"
---
# <a name="userresponse-soap"></a><span data-ttu-id="d5b7b-103">UserResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d5b7b-103">UserResponse (SOAP)</span></span>

<span data-ttu-id="d5b7b-104">**UserResponse**元素表示对单个用户的 GetUserSettings 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-104">The **UserResponse** element represents a response to a GetUserSettings request for an individual user.</span></span> 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 <span data-ttu-id="d5b7b-105">**UserResponse**</span><span class="sxs-lookup"><span data-stu-id="d5b7b-105">**UserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5b7b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d5b7b-106">Attributes and elements</span></span>

<span data-ttu-id="d5b7b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5b7b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d5b7b-108">Attributes</span></span>

<span data-ttu-id="d5b7b-109">无。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5b7b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d5b7b-110">Child elements</span></span>

|<span data-ttu-id="d5b7b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d5b7b-111">**Element**</span></span>|<span data-ttu-id="d5b7b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d5b7b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5b7b-113">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d5b7b-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="d5b7b-114">表示自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="d5b7b-115">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d5b7b-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="d5b7b-116">表示与自动发现服务返回的错误代码相关联的消息。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="d5b7b-117">RedirectTarget （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d5b7b-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="d5b7b-118">包含重定向 URL 或电子邮件地址的目标。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-118">Contains the target of the redirection URL or email address.</span></span>  <br/> |
|[<span data-ttu-id="d5b7b-119">UserSettingErrors （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d5b7b-119">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="d5b7b-120">表示有关无法返回的设置的信息的集合。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-120">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="d5b7b-121">UserSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d5b7b-121">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="d5b7b-122">用户的请求设置。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-122">The requested settings for the user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5b7b-123">父元素</span><span class="sxs-lookup"><span data-stu-id="d5b7b-123">Parent elements</span></span>

|<span data-ttu-id="d5b7b-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="d5b7b-124">**Element**</span></span>|<span data-ttu-id="d5b7b-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="d5b7b-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5b7b-126">ArrayOfUserResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d5b7b-126">ArrayOfUserResponse (SOAP)</span></span>](arrayofuserresponse-soap.md) <br/> |<span data-ttu-id="d5b7b-127">包含用户响应的数组。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-127">Contains an array of user responses.</span></span>  <br/> |
|[<span data-ttu-id="d5b7b-128">UserResponses （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d5b7b-128">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="d5b7b-129">包含每个请求的用户的配置设置。</span><span class="sxs-lookup"><span data-stu-id="d5b7b-129">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="d5b7b-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="d5b7b-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5b7b-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="d5b7b-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d5b7b-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="d5b7b-132">Schema Name</span></span>  <br/> |<span data-ttu-id="d5b7b-133">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="d5b7b-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d5b7b-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="d5b7b-134">Validation File</span></span>  <br/> |<span data-ttu-id="d5b7b-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d5b7b-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d5b7b-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="d5b7b-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5b7b-137">True</span><span class="sxs-lookup"><span data-stu-id="d5b7b-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5b7b-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d5b7b-138">See also</span></span>



[<span data-ttu-id="d5b7b-139">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="d5b7b-139">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

