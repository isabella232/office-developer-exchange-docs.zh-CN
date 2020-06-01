---
title: Status （UM web 服务-SetOofStatus）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 893bcff1-ccdc-493f-b366-ce8a68c813bd
description: Status 元素定义要在 SetOofStatus 操作（UM web 服务）请求中使用的值。
ms.openlocfilehash: 865152baf28c22578664e16db2dcd5f82a04af98
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459978"
---
# <a name="status-um-web-service---setoofstatus"></a><span data-ttu-id="85d58-103">Status （UM web 服务-SetOofStatus）</span><span class="sxs-lookup"><span data-stu-id="85d58-103">Status (UM web service - SetOofStatus)</span></span>

<span data-ttu-id="85d58-104">**Status**元素定义要在[SETOOFSTATUS 操作（UM web 服务）](setoofstatus-operation-um-web-service.md)请求中使用的值。</span><span class="sxs-lookup"><span data-stu-id="85d58-104">The **Status** element defines the value to use in a [SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="85d58-105">SetOofStatus （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="85d58-105">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="85d58-106">Status （UM web 服务-SetOofStatus）</span><span class="sxs-lookup"><span data-stu-id="85d58-106">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 <span data-ttu-id="85d58-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="85d58-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85d58-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="85d58-108">Attributes and elements</span></span>

<span data-ttu-id="85d58-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="85d58-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85d58-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="85d58-110">Attributes</span></span>

<span data-ttu-id="85d58-111">无。</span><span class="sxs-lookup"><span data-stu-id="85d58-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85d58-112">子元素</span><span class="sxs-lookup"><span data-stu-id="85d58-112">Child elements</span></span>

<span data-ttu-id="85d58-113">无。</span><span class="sxs-lookup"><span data-stu-id="85d58-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85d58-114">父元素</span><span class="sxs-lookup"><span data-stu-id="85d58-114">Parent elements</span></span>

|<span data-ttu-id="85d58-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="85d58-115">**Element**</span></span>|<span data-ttu-id="85d58-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="85d58-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85d58-117">SetOofStatus （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="85d58-117">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md) <br/> |<span data-ttu-id="85d58-118">定义一个请求，用于为发出请求的用户设置统一消息 "外出" （OOF）状态。</span><span class="sxs-lookup"><span data-stu-id="85d58-118">Defines a request to set the Unified Messaging Out of Office (OOF) status for the user who makes the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="85d58-119">文本值</span><span class="sxs-lookup"><span data-stu-id="85d58-119">Text value</span></span>

<span data-ttu-id="85d58-120">布尔值是必需的。</span><span class="sxs-lookup"><span data-stu-id="85d58-120">A Boolean value is required.</span></span> <span data-ttu-id="85d58-121">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="85d58-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="85d58-122">True</span><span class="sxs-lookup"><span data-stu-id="85d58-122">True</span></span>
    
- <span data-ttu-id="85d58-123">False</span><span class="sxs-lookup"><span data-stu-id="85d58-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="85d58-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="85d58-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85d58-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="85d58-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="85d58-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="85d58-126">Schema Name</span></span>  <br/> |<span data-ttu-id="85d58-127">邮件</span><span class="sxs-lookup"><span data-stu-id="85d58-127">Messages</span></span>  <br/> |
|<span data-ttu-id="85d58-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="85d58-128">Validation File</span></span>  <br/> |<span data-ttu-id="85d58-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="85d58-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="85d58-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="85d58-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="85d58-131">False</span><span class="sxs-lookup"><span data-stu-id="85d58-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85d58-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="85d58-132">See also</span></span>



[<span data-ttu-id="85d58-133">SetOofStatus 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="85d58-133">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)

