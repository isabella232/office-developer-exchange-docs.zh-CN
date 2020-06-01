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
description: 退订元素包含用于取消订阅订阅的属性。
ms.openlocfilehash: d3d9c3bf9ad97cc0fdabf574c6505c797583838a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467212"
---
# <a name="unsubscribe"></a><span data-ttu-id="82489-103">取消订阅</span><span class="sxs-lookup"><span data-stu-id="82489-103">Unsubscribe</span></span>

<span data-ttu-id="82489-104">**退订**元素包含用于取消订阅订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="82489-104">The **Unsubscribe** element contains the properties used to unsubscribe from a subscription.</span></span> 
  
[<span data-ttu-id="82489-105">取消订阅</span><span class="sxs-lookup"><span data-stu-id="82489-105">Unsubscribe</span></span>](unsubscribe.md)
  
```xml
<Unsubscribe>
   <SubscriptionId/>
</Unsubscribe>
```

 <span data-ttu-id="82489-106">**UnsubscribeType**</span><span class="sxs-lookup"><span data-stu-id="82489-106">**UnsubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82489-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="82489-107">Attributes and elements</span></span>

<span data-ttu-id="82489-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="82489-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82489-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="82489-109">Attributes</span></span>

<span data-ttu-id="82489-110">无。</span><span class="sxs-lookup"><span data-stu-id="82489-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82489-111">子元素</span><span class="sxs-lookup"><span data-stu-id="82489-111">Child elements</span></span>

|<span data-ttu-id="82489-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="82489-112">**Element**</span></span>|<span data-ttu-id="82489-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="82489-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82489-114">SubscriptionId （GetEvents）</span><span class="sxs-lookup"><span data-stu-id="82489-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="82489-115">表示订阅的标识符。</span><span class="sxs-lookup"><span data-stu-id="82489-115">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="82489-116">父元素</span><span class="sxs-lookup"><span data-stu-id="82489-116">Parent elements</span></span>

<span data-ttu-id="82489-117">无。</span><span class="sxs-lookup"><span data-stu-id="82489-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82489-118">说明</span><span class="sxs-lookup"><span data-stu-id="82489-118">Remarks</span></span>

<span data-ttu-id="82489-119">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="82489-119">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82489-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="82489-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82489-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="82489-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="82489-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="82489-122">Schema name</span></span>  <br/> |<span data-ttu-id="82489-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="82489-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="82489-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="82489-124">Validation file</span></span>  <br/> |<span data-ttu-id="82489-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="82489-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="82489-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="82489-126">Can be empty</span></span>  <br/> |<span data-ttu-id="82489-127">False</span><span class="sxs-lookup"><span data-stu-id="82489-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82489-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="82489-128">See also</span></span>



[<span data-ttu-id="82489-129">订阅操作</span><span class="sxs-lookup"><span data-stu-id="82489-129">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="82489-130">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="82489-130">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="82489-131">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="82489-131">Unsubscribe operation</span></span>](unsubscribe-operation.md)

