---
title: 用户 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4e051617-4eea-47d0-871a-ea1f17a0f711
description: Users 元素表示的设置应为其检索用户的电子邮件地址的集合。
ms.openlocfilehash: d7655f0020a315dcb32adbbc58610ca0e630c1fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838488"
---
# <a name="users-soap"></a><span data-ttu-id="2e36d-103">用户 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2e36d-103">Users (SOAP)</span></span>

<span data-ttu-id="2e36d-104">**Users**元素表示的设置应为其检索用户的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="2e36d-104">The **Users** element represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span> 
  
```XML
<Users>
   <User/>
</Users>
```

 <span data-ttu-id="2e36d-105">**用户**</span><span class="sxs-lookup"><span data-stu-id="2e36d-105">**Users**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e36d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2e36d-106">Attributes and elements</span></span>

<span data-ttu-id="2e36d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2e36d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e36d-108">属性</span><span class="sxs-lookup"><span data-stu-id="2e36d-108">Attributes</span></span>

<span data-ttu-id="2e36d-109">无。</span><span class="sxs-lookup"><span data-stu-id="2e36d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e36d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2e36d-110">Child elements</span></span>

|<span data-ttu-id="2e36d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2e36d-111">**Element**</span></span>|<span data-ttu-id="2e36d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e36d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e36d-113">用户 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2e36d-113">User (SOAP)</span></span>](user-soap.md) <br/> |<span data-ttu-id="2e36d-114">代表用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2e36d-114">Represents the e-mail address of a user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e36d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2e36d-115">Parent elements</span></span>

|<span data-ttu-id="2e36d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2e36d-116">**Element**</span></span>|<span data-ttu-id="2e36d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e36d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e36d-118">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2e36d-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="2e36d-119">表示检索指定的设置为一个或多个用户的请求。</span><span class="sxs-lookup"><span data-stu-id="2e36d-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="2e36d-120">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2e36d-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="2e36d-121">包含请求的配置设置和目标用户。</span><span class="sxs-lookup"><span data-stu-id="2e36d-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2e36d-122">文本值</span><span class="sxs-lookup"><span data-stu-id="2e36d-122">Text value</span></span>

<span data-ttu-id="2e36d-123">无。</span><span class="sxs-lookup"><span data-stu-id="2e36d-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e36d-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="2e36d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e36d-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="2e36d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="2e36d-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="2e36d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="2e36d-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="2e36d-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="2e36d-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="2e36d-128">Validation File</span></span>  <br/> |<span data-ttu-id="2e36d-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2e36d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2e36d-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="2e36d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e36d-131">True</span><span class="sxs-lookup"><span data-stu-id="2e36d-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e36d-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2e36d-132">See also</span></span>



[<span data-ttu-id="2e36d-133">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2e36d-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

