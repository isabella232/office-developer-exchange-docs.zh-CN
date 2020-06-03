---
title: UserResponses （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a48766df-4cc8-47c2-a8c1-826daec94e5a
description: UserResponses 元素包含每个请求的用户的配置设置。
ms.openlocfilehash: db2bab16334b90395d29dc03353dce05b0e45357
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526744"
---
# <a name="userresponses-soap"></a><span data-ttu-id="e850f-103">UserResponses （SOAP）</span><span class="sxs-lookup"><span data-stu-id="e850f-103">UserResponses (SOAP)</span></span>

<span data-ttu-id="e850f-104">**UserResponses**元素包含每个请求的用户的配置设置。</span><span class="sxs-lookup"><span data-stu-id="e850f-104">The **UserResponses** element contains the configuration settings for each requested user.</span></span> 
  
```XML
<UserResponses>
   <UserResponse/>
</UserResponses>
```

 <span data-ttu-id="e850f-105">**ArrayOfUserResponse**</span><span class="sxs-lookup"><span data-stu-id="e850f-105">**ArrayOfUserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e850f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e850f-106">Attributes and elements</span></span>

<span data-ttu-id="e850f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e850f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e850f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e850f-108">Attributes</span></span>

<span data-ttu-id="e850f-109">无。</span><span class="sxs-lookup"><span data-stu-id="e850f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e850f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e850f-110">Child elements</span></span>

|<span data-ttu-id="e850f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e850f-111">**Element**</span></span>|<span data-ttu-id="e850f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e850f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e850f-113">UserResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="e850f-113">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="e850f-114">表示对单个用户的[GetUserSettings 操作（SOAP）](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="e850f-114">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e850f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="e850f-115">Parent elements</span></span>

|<span data-ttu-id="e850f-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="e850f-116">**Element**</span></span>|<span data-ttu-id="e850f-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="e850f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e850f-118">响应（SOAP）</span><span class="sxs-lookup"><span data-stu-id="e850f-118">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="e850f-119">包含对[GetUserSettings 操作（SOAP）](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="e850f-119">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="e850f-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="e850f-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e850f-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="e850f-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e850f-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="e850f-122">Schema Name</span></span>  <br/> |<span data-ttu-id="e850f-123">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="e850f-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e850f-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="e850f-124">Validation File</span></span>  <br/> |<span data-ttu-id="e850f-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e850f-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e850f-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="e850f-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="e850f-127">True</span><span class="sxs-lookup"><span data-stu-id="e850f-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e850f-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e850f-128">See also</span></span>



[<span data-ttu-id="e850f-129">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e850f-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

