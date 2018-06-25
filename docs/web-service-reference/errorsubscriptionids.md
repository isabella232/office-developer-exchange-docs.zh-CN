---
title: ErrorSubscriptionIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrorSubscriptionIds
api_type:
- schema
ms.assetid: e64e76ff-4d98-4082-9acc-a1114ae45f44
description: ErrorSubscriptionIds 元素包含无效的订阅 Id 的数组。
ms.openlocfilehash: 5cdbbeb1083754510f431bc092bb67dc0addecab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754160"
---
# <a name="errorsubscriptionids"></a><span data-ttu-id="b0d35-103">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="b0d35-103">ErrorSubscriptionIds</span></span>

<span data-ttu-id="b0d35-104">**ErrorSubscriptionIds**元素包含无效的订阅 Id 的数组。</span><span class="sxs-lookup"><span data-stu-id="b0d35-104">The **ErrorSubscriptionIds** element contains an array of invalid subscription IDs.</span></span> 
  
```xml
<ErrorSubscriptionIds>
   <SubscriptionId/>
</ErrorSubscriptionIds>
```

 <span data-ttu-id="b0d35-105">**NonEmptyArrayOfSubscriptionIdsType**</span><span class="sxs-lookup"><span data-stu-id="b0d35-105">**NonEmptyArrayOfSubscriptionIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0d35-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b0d35-106">Attributes and elements</span></span>

<span data-ttu-id="b0d35-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b0d35-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0d35-108">属性</span><span class="sxs-lookup"><span data-stu-id="b0d35-108">Attributes</span></span>

<span data-ttu-id="b0d35-109">无。</span><span class="sxs-lookup"><span data-stu-id="b0d35-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0d35-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b0d35-110">Child elements</span></span>

|<span data-ttu-id="b0d35-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0d35-111">**Element**</span></span>|<span data-ttu-id="b0d35-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0d35-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0d35-113">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="b0d35-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="b0d35-114">表示订阅的标识符。</span><span class="sxs-lookup"><span data-stu-id="b0d35-114">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b0d35-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b0d35-115">Parent elements</span></span>

|<span data-ttu-id="b0d35-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0d35-116">**Element**</span></span>|<span data-ttu-id="b0d35-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0d35-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0d35-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b0d35-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="b0d35-119">包含状态和的单个结果[GetStreamingEvents 操作](getstreamingevents-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="b0d35-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b0d35-120">文本值</span><span class="sxs-lookup"><span data-stu-id="b0d35-120">Text value</span></span>

<span data-ttu-id="b0d35-121">无。</span><span class="sxs-lookup"><span data-stu-id="b0d35-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0d35-122">备注</span><span class="sxs-lookup"><span data-stu-id="b0d35-122">Remarks</span></span>

<span data-ttu-id="b0d35-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b0d35-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0d35-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="b0d35-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0d35-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="b0d35-125">Namespace</span></span>  <br/> |<span data-ttu-id="b0d35-126">http://schemas.microsoft.com/exchange/services/2006/messages 和 http://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="b0d35-126">http://schemas.microsoft.com/exchange/services/2006/messages and http://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="b0d35-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="b0d35-127">Schema Name</span></span>  <br/> |<span data-ttu-id="b0d35-128">邮件架构;类型架构</span><span class="sxs-lookup"><span data-stu-id="b0d35-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="b0d35-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="b0d35-129">Validation File</span></span>  <br/> |<span data-ttu-id="b0d35-130">Messages.xsd;Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b0d35-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0d35-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="b0d35-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="b0d35-132">False</span><span class="sxs-lookup"><span data-stu-id="b0d35-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0d35-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b0d35-133">See also</span></span>



[<span data-ttu-id="b0d35-134">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="b0d35-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="b0d35-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b0d35-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

