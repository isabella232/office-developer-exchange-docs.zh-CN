---
title: UserResponses (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a48766df-4cc8-47c2-a8c1-826daec94e5a
description: UserResponses 元素包含每个请求的用户的配置设置。
ms.openlocfilehash: bee7f3c9a95c1facfe0adc990516dfa323d9c8cf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838483"
---
# <a name="userresponses-soap"></a><span data-ttu-id="892c8-103">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="892c8-103">UserResponses (SOAP)</span></span>

<span data-ttu-id="892c8-104">**UserResponses**元素包含每个请求的用户的配置设置。</span><span class="sxs-lookup"><span data-stu-id="892c8-104">The **UserResponses** element contains the configuration settings for each requested user.</span></span> 
  
```XML
<UserResponses>
   <UserResponse/>
</UserResponses>
```

 <span data-ttu-id="892c8-105">**ArrayOfUserResponse**</span><span class="sxs-lookup"><span data-stu-id="892c8-105">**ArrayOfUserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="892c8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="892c8-106">Attributes and elements</span></span>

<span data-ttu-id="892c8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="892c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="892c8-108">属性</span><span class="sxs-lookup"><span data-stu-id="892c8-108">Attributes</span></span>

<span data-ttu-id="892c8-109">无。</span><span class="sxs-lookup"><span data-stu-id="892c8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="892c8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="892c8-110">Child elements</span></span>

|<span data-ttu-id="892c8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="892c8-111">**Element**</span></span>|<span data-ttu-id="892c8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="892c8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="892c8-113">用户回音 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="892c8-113">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="892c8-114">代表对单个用户[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="892c8-114">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="892c8-115">父元素</span><span class="sxs-lookup"><span data-stu-id="892c8-115">Parent elements</span></span>

|<span data-ttu-id="892c8-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="892c8-116">**Element**</span></span>|<span data-ttu-id="892c8-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="892c8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="892c8-118">响应 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="892c8-118">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="892c8-119">包含对[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="892c8-119">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="892c8-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="892c8-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="892c8-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="892c8-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="892c8-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="892c8-122">Schema Name</span></span>  <br/> |<span data-ttu-id="892c8-123">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="892c8-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="892c8-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="892c8-124">Validation File</span></span>  <br/> |<span data-ttu-id="892c8-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="892c8-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="892c8-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="892c8-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="892c8-127">True</span><span class="sxs-lookup"><span data-stu-id="892c8-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="892c8-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="892c8-128">See also</span></span>



[<span data-ttu-id="892c8-129">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="892c8-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

