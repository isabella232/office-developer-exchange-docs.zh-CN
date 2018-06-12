---
title: 取消订阅
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Unsubscribe
api_type:
- schema
ms.assetid: 5584db5f-553a-47ce-85fb-f9902c9990ab
description: 取消订阅元素包含用来取消订阅的属性。
ms.openlocfilehash: bab797ff74a921e3e93c993229bc6d6d289e0c5c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838355"
---
# <a name="unsubscribe"></a><span data-ttu-id="ea931-103">取消订阅</span><span class="sxs-lookup"><span data-stu-id="ea931-103">Unsubscribe</span></span>

<span data-ttu-id="ea931-104">**取消订阅**元素包含用来取消订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="ea931-104">The **Unsubscribe** element contains the properties used to unsubscribe from a subscription.</span></span> 
  
[<span data-ttu-id="ea931-105">取消订阅</span><span class="sxs-lookup"><span data-stu-id="ea931-105">Unsubscribe</span></span>](unsubscribe.md)
  
```xml
<Unsubscribe>
   <SubscriptionId/>
</Unsubscribe>
```

 <span data-ttu-id="ea931-106">**UnsubscribeType**</span><span class="sxs-lookup"><span data-stu-id="ea931-106">**UnsubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ea931-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ea931-107">Attributes and elements</span></span>

<span data-ttu-id="ea931-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ea931-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea931-109">属性</span><span class="sxs-lookup"><span data-stu-id="ea931-109">Attributes</span></span>

<span data-ttu-id="ea931-110">无。</span><span class="sxs-lookup"><span data-stu-id="ea931-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ea931-111">子元素</span><span class="sxs-lookup"><span data-stu-id="ea931-111">Child elements</span></span>

|<span data-ttu-id="ea931-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="ea931-112">**Element**</span></span>|<span data-ttu-id="ea931-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="ea931-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea931-114">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="ea931-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="ea931-115">表示订阅的标识符。</span><span class="sxs-lookup"><span data-stu-id="ea931-115">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ea931-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ea931-116">Parent elements</span></span>

<span data-ttu-id="ea931-117">无。</span><span class="sxs-lookup"><span data-stu-id="ea931-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ea931-118">备注</span><span class="sxs-lookup"><span data-stu-id="ea931-118">Remarks</span></span>

<span data-ttu-id="ea931-119">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ea931-119">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ea931-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="ea931-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea931-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="ea931-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ea931-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="ea931-122">Schema name</span></span>  <br/> |<span data-ttu-id="ea931-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="ea931-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ea931-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="ea931-124">Validation file</span></span>  <br/> |<span data-ttu-id="ea931-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ea931-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ea931-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="ea931-126">Can be empty</span></span>  <br/> |<span data-ttu-id="ea931-127">False</span><span class="sxs-lookup"><span data-stu-id="ea931-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea931-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ea931-128">See also</span></span>



[<span data-ttu-id="ea931-129">订阅操作</span><span class="sxs-lookup"><span data-stu-id="ea931-129">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="ea931-130">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="ea931-130">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="ea931-131">取消操作</span><span class="sxs-lookup"><span data-stu-id="ea931-131">Unsubscribe operation</span></span>](unsubscribe-operation.md)

