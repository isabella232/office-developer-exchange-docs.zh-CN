---
title: Users （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4e051617-4eea-47d0-871a-ea1f17a0f711
description: Users 元素表示应检索其设置的用户的电子邮件地址的集合。
ms.openlocfilehash: 851447a2918e365b7c5d8812a61c9d425d26ffa2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461896"
---
# <a name="users-soap"></a><span data-ttu-id="f566b-103">Users （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f566b-103">Users (SOAP)</span></span>

<span data-ttu-id="f566b-104">**Users**元素表示应检索其设置的用户的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="f566b-104">The **Users** element represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span> 
  
```XML
<Users>
   <User/>
</Users>
```

 <span data-ttu-id="f566b-105">**用户**</span><span class="sxs-lookup"><span data-stu-id="f566b-105">**Users**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f566b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f566b-106">Attributes and elements</span></span>

<span data-ttu-id="f566b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f566b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f566b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f566b-108">Attributes</span></span>

<span data-ttu-id="f566b-109">无。</span><span class="sxs-lookup"><span data-stu-id="f566b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f566b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f566b-110">Child elements</span></span>

|<span data-ttu-id="f566b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f566b-111">**Element**</span></span>|<span data-ttu-id="f566b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f566b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f566b-113">User （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f566b-113">User (SOAP)</span></span>](user-soap.md) <br/> |<span data-ttu-id="f566b-114">表示用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f566b-114">Represents the e-mail address of a user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f566b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f566b-115">Parent elements</span></span>

|<span data-ttu-id="f566b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f566b-116">**Element**</span></span>|<span data-ttu-id="f566b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f566b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f566b-118">GetUserSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f566b-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="f566b-119">表示检索一个或多个用户的指定设置的请求。</span><span class="sxs-lookup"><span data-stu-id="f566b-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="f566b-120">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f566b-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="f566b-121">包含请求的配置设置和目标用户。</span><span class="sxs-lookup"><span data-stu-id="f566b-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f566b-122">文本值</span><span class="sxs-lookup"><span data-stu-id="f566b-122">Text value</span></span>

<span data-ttu-id="f566b-123">无。</span><span class="sxs-lookup"><span data-stu-id="f566b-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f566b-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="f566b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f566b-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="f566b-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f566b-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="f566b-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f566b-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="f566b-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f566b-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="f566b-128">Validation File</span></span>  <br/> |<span data-ttu-id="f566b-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f566b-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f566b-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="f566b-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f566b-131">True</span><span class="sxs-lookup"><span data-stu-id="f566b-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f566b-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f566b-132">See also</span></span>



[<span data-ttu-id="f566b-133">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f566b-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

