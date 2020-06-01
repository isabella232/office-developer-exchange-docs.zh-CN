---
title: SetOofStatus （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 9fc0ea9c-7a98-4fd7-a90c-cf5639c63a3a
description: SetOofStatus 元素定义一个请求，用于为发出请求的用户设置统一消息 "外出" （OOF）状态。
ms.openlocfilehash: 86e056a440e282cd444cfd405e452720b26b7456
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467065"
---
# <a name="setoofstatus-um-web-service"></a><span data-ttu-id="879e6-103">SetOofStatus （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="879e6-103">SetOofStatus (UM web service)</span></span>

<span data-ttu-id="879e6-104">**SetOofStatus**元素定义一个请求，用于为发出请求的用户设置统一消息 "外出" （OOF）状态。</span><span class="sxs-lookup"><span data-stu-id="879e6-104">The **SetOofStatus** element defines a request to set the Unified Messaging Out of Office (OOF) status for the user who makes the request.</span></span> 
  
[<span data-ttu-id="879e6-105">SetOofStatus （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="879e6-105">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 <span data-ttu-id="879e6-106">**类型**</span><span class="sxs-lookup"><span data-stu-id="879e6-106">**Type**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="879e6-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="879e6-107">Attributes and elements</span></span>

<span data-ttu-id="879e6-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="879e6-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="879e6-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="879e6-109">Attributes</span></span>

<span data-ttu-id="879e6-110">无。</span><span class="sxs-lookup"><span data-stu-id="879e6-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="879e6-111">子元素</span><span class="sxs-lookup"><span data-stu-id="879e6-111">Child elements</span></span>

|<span data-ttu-id="879e6-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="879e6-112">**Element**</span></span>|<span data-ttu-id="879e6-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="879e6-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="879e6-114">Status （UM web 服务-SetOofStatus）</span><span class="sxs-lookup"><span data-stu-id="879e6-114">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md) <br/> |<span data-ttu-id="879e6-115">定义要在[SetOofStatus 操作（UM web 服务）](setoofstatus-operation-um-web-service.md)请求中使用的值。</span><span class="sxs-lookup"><span data-stu-id="879e6-115">Defines a value to use in a [SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="879e6-116">父元素</span><span class="sxs-lookup"><span data-stu-id="879e6-116">Parent elements</span></span>

<span data-ttu-id="879e6-117">无。</span><span class="sxs-lookup"><span data-stu-id="879e6-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="879e6-118">文本值</span><span class="sxs-lookup"><span data-stu-id="879e6-118">Text value</span></span>

<span data-ttu-id="879e6-119">无。</span><span class="sxs-lookup"><span data-stu-id="879e6-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="879e6-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="879e6-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="879e6-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="879e6-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="879e6-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="879e6-122">Schema Name</span></span>  <br/> |<span data-ttu-id="879e6-123">邮件</span><span class="sxs-lookup"><span data-stu-id="879e6-123">Messages</span></span>  <br/> |
|<span data-ttu-id="879e6-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="879e6-124">Validation File</span></span>  <br/> |<span data-ttu-id="879e6-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="879e6-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="879e6-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="879e6-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="879e6-127">False</span><span class="sxs-lookup"><span data-stu-id="879e6-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="879e6-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="879e6-128">See also</span></span>



[<span data-ttu-id="879e6-129">SetOofStatus 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="879e6-129">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)
  
[<span data-ttu-id="879e6-130">Status （UM web 服务-SetOofStatus）</span><span class="sxs-lookup"><span data-stu-id="879e6-130">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)

