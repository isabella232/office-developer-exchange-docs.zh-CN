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
description: ErrorSubscriptionIds 元素包含一个由无效订阅 Id 组成的数组。
ms.openlocfilehash: bdc5c86560800464d677a9043607bed3f7872e32
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526184"
---
# <a name="errorsubscriptionids"></a><span data-ttu-id="f1e1f-103">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="f1e1f-103">ErrorSubscriptionIds</span></span>

<span data-ttu-id="f1e1f-104">**ErrorSubscriptionIds**元素包含一个由无效订阅 id 组成的数组。</span><span class="sxs-lookup"><span data-stu-id="f1e1f-104">The **ErrorSubscriptionIds** element contains an array of invalid subscription IDs.</span></span> 
  
```xml
<ErrorSubscriptionIds>
   <SubscriptionId/>
</ErrorSubscriptionIds>
```

 <span data-ttu-id="f1e1f-105">**NonEmptyArrayOfSubscriptionIdsType**</span><span class="sxs-lookup"><span data-stu-id="f1e1f-105">**NonEmptyArrayOfSubscriptionIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1e1f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f1e1f-106">Attributes and elements</span></span>

<span data-ttu-id="f1e1f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f1e1f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1e1f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f1e1f-108">Attributes</span></span>

<span data-ttu-id="f1e1f-109">无。</span><span class="sxs-lookup"><span data-stu-id="f1e1f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1e1f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f1e1f-110">Child elements</span></span>

|<span data-ttu-id="f1e1f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f1e1f-111">**Element**</span></span>|<span data-ttu-id="f1e1f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f1e1f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1e1f-113">SubscriptionId （GetEvents）</span><span class="sxs-lookup"><span data-stu-id="f1e1f-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="f1e1f-114">表示订阅的标识符。</span><span class="sxs-lookup"><span data-stu-id="f1e1f-114">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f1e1f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f1e1f-115">Parent elements</span></span>

|<span data-ttu-id="f1e1f-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f1e1f-116">**Element**</span></span>|<span data-ttu-id="f1e1f-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f1e1f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1e1f-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f1e1f-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="f1e1f-119">包含单个[GetStreamingEvents 操作](getstreamingevents-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="f1e1f-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f1e1f-120">文本值</span><span class="sxs-lookup"><span data-stu-id="f1e1f-120">Text value</span></span>

<span data-ttu-id="f1e1f-121">无。</span><span class="sxs-lookup"><span data-stu-id="f1e1f-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1e1f-122">说明</span><span class="sxs-lookup"><span data-stu-id="f1e1f-122">Remarks</span></span>

<span data-ttu-id="f1e1f-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f1e1f-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1e1f-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="f1e1f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1e1f-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="f1e1f-125">Namespace</span></span>  <br/> |<span data-ttu-id="f1e1f-126">https://schemas.microsoft.com/exchange/services/2006/messages 和 https://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="f1e1f-126">https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="f1e1f-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="f1e1f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f1e1f-128">邮件架构;类型架构</span><span class="sxs-lookup"><span data-stu-id="f1e1f-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="f1e1f-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="f1e1f-129">Validation File</span></span>  <br/> |<span data-ttu-id="f1e1f-130">消息 .xsd;类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="f1e1f-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f1e1f-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="f1e1f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="f1e1f-132">False</span><span class="sxs-lookup"><span data-stu-id="f1e1f-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1e1f-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f1e1f-133">See also</span></span>



[<span data-ttu-id="f1e1f-134">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="f1e1f-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="f1e1f-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f1e1f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

