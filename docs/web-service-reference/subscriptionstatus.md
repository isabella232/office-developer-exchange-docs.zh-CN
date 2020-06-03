---
title: SubscriptionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: SubscriptionStatus 元素描述推送订阅的状态。
ms.openlocfilehash: 195ab229380f4386b39e5c3fd48208cf66e224f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530942"
---
# <a name="subscriptionstatus"></a><span data-ttu-id="c6ead-103">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="c6ead-103">SubscriptionStatus</span></span>

<span data-ttu-id="c6ead-104">**SubscriptionStatus**元素描述推送订阅的状态。</span><span class="sxs-lookup"><span data-stu-id="c6ead-104">The **SubscriptionStatus** element describes the status of a push subscription.</span></span> 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 <span data-ttu-id="c6ead-105">**SubscriptionStatusType**</span><span class="sxs-lookup"><span data-stu-id="c6ead-105">**SubscriptionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6ead-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6ead-106">Attributes and elements</span></span>

<span data-ttu-id="c6ead-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6ead-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6ead-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c6ead-108">Attributes</span></span>

<span data-ttu-id="c6ead-109">无。</span><span class="sxs-lookup"><span data-stu-id="c6ead-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6ead-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c6ead-110">Child elements</span></span>

<span data-ttu-id="c6ead-111">无。</span><span class="sxs-lookup"><span data-stu-id="c6ead-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c6ead-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c6ead-112">Parent elements</span></span>

|<span data-ttu-id="c6ead-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6ead-113">**Element**</span></span>|<span data-ttu-id="c6ead-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6ead-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6ead-115">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="c6ead-115">SendNotificationResult</span></span>](sendnotificationresult.md) <br/> |<span data-ttu-id="c6ead-116">包含客户端应用程序对推送通知的响应。</span><span class="sxs-lookup"><span data-stu-id="c6ead-116">Contains the response of the client application' to a push notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c6ead-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c6ead-117">Text value</span></span>

<span data-ttu-id="c6ead-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="c6ead-118">A text value is required.</span></span> <span data-ttu-id="c6ead-119">以下是此元素的可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="c6ead-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="c6ead-120">确定</span><span class="sxs-lookup"><span data-stu-id="c6ead-120">OK</span></span>
    
- <span data-ttu-id="c6ead-121">取消订阅</span><span class="sxs-lookup"><span data-stu-id="c6ead-121">Unsubscribe</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6ead-122">备注</span><span class="sxs-lookup"><span data-stu-id="c6ead-122">Remarks</span></span>

<span data-ttu-id="c6ead-123">此元素描述订阅的状态。</span><span class="sxs-lookup"><span data-stu-id="c6ead-123">This element describes the status of the subscription.</span></span> <span data-ttu-id="c6ead-124">推送订阅客户端应用程序将状态返回到运行 Exchange 2007 且在每个推送通知之后安装了客户端访问服务器角色的计算机。</span><span class="sxs-lookup"><span data-stu-id="c6ead-124">The push subscription client application sends the status back to the computer that is running Exchange 2007 that has the Client Access server role installed after each push notification.</span></span> <span data-ttu-id="c6ead-125">如果**SubscriptionStatus**值等于 "**取消订阅**"，客户端访问服务器将停止发送通知并结束订阅。</span><span class="sxs-lookup"><span data-stu-id="c6ead-125">If the **SubscriptionStatus** value equals **Unsubscribe**, the Client Access server will stop sending notifications and end the subscription.</span></span> <span data-ttu-id="c6ead-126">如果**SubscriptionStatus**值等于 **"确定"**，客户端访问服务器将继续发送通知。</span><span class="sxs-lookup"><span data-stu-id="c6ead-126">If the **SubscriptionStatus** value equals **OK**, the Client Access server will continue to send notifications.</span></span>
  
<span data-ttu-id="c6ead-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c6ead-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6ead-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="c6ead-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6ead-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="c6ead-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c6ead-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="c6ead-130">Schema Name</span></span>  <br/> |<span data-ttu-id="c6ead-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="c6ead-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c6ead-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="c6ead-132">Validation File</span></span>  <br/> |<span data-ttu-id="c6ead-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c6ead-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c6ead-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="c6ead-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="c6ead-135">False</span><span class="sxs-lookup"><span data-stu-id="c6ead-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6ead-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6ead-136">See also</span></span>



- [<span data-ttu-id="c6ead-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c6ead-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

