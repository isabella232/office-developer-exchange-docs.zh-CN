---
title: SendNotificationResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendNotificationResult
api_type:
- schema
ms.assetid: fa9d6202-fa66-4f10-9858-53f4f1ce14bc
description: SendNotificationResult 元素包含推送通知的客户端应用程序的响应。
ms.openlocfilehash: 9acaa396430cf4e06a9c996834874d19dcab50ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827350"
---
# <a name="sendnotificationresult"></a><span data-ttu-id="0fb98-103">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="0fb98-103">SendNotificationResult</span></span>

<span data-ttu-id="0fb98-104">**SendNotificationResult**元素包含推送通知的客户端应用程序的响应。</span><span class="sxs-lookup"><span data-stu-id="0fb98-104">The **SendNotificationResult** element contains the response of a client application to a push notification.</span></span> 
  
```xml
<SendNotificationResult>
   <SubscriptionStatus/>
</SendNotificationResult>
```

 <span data-ttu-id="0fb98-105">**SendNotificationResultType**</span><span class="sxs-lookup"><span data-stu-id="0fb98-105">**SendNotificationResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0fb98-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0fb98-106">Attributes and elements</span></span>

<span data-ttu-id="0fb98-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0fb98-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fb98-108">属性</span><span class="sxs-lookup"><span data-stu-id="0fb98-108">Attributes</span></span>

<span data-ttu-id="0fb98-109">无。</span><span class="sxs-lookup"><span data-stu-id="0fb98-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0fb98-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0fb98-110">Child elements</span></span>

|<span data-ttu-id="0fb98-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0fb98-111">**Element**</span></span>|<span data-ttu-id="0fb98-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0fb98-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fb98-113">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="0fb98-113">SubscriptionStatus</span></span>](subscriptionstatus.md) <br/> |<span data-ttu-id="0fb98-114">介绍推送订阅的状态。</span><span class="sxs-lookup"><span data-stu-id="0fb98-114">Describes the status of a push subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0fb98-115">父元素</span><span class="sxs-lookup"><span data-stu-id="0fb98-115">Parent elements</span></span>

<span data-ttu-id="0fb98-116">无。</span><span class="sxs-lookup"><span data-stu-id="0fb98-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0fb98-117">备注</span><span class="sxs-lookup"><span data-stu-id="0fb98-117">Remarks</span></span>

<span data-ttu-id="0fb98-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0fb98-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0fb98-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="0fb98-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0fb98-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="0fb98-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0fb98-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="0fb98-121">Schema Name</span></span>  <br/> |<span data-ttu-id="0fb98-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="0fb98-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0fb98-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="0fb98-123">Validation File</span></span>  <br/> |<span data-ttu-id="0fb98-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0fb98-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0fb98-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="0fb98-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="0fb98-126">False</span><span class="sxs-lookup"><span data-stu-id="0fb98-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0fb98-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0fb98-127">See also</span></span>



- [<span data-ttu-id="0fb98-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0fb98-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

