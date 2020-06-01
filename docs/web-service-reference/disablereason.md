---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: DisableReason 元素指定禁用应用程序的原因。
ms.openlocfilehash: 1406d69647bde5389dc9bb61adf7537a57d5adfc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463669"
---
# <a name="disablereason"></a><span data-ttu-id="1c427-103">DisableReason</span><span class="sxs-lookup"><span data-stu-id="1c427-103">DisableReason</span></span>

<span data-ttu-id="1c427-104">**DisableReason**元素指定禁用应用程序的原因。</span><span class="sxs-lookup"><span data-stu-id="1c427-104">The **DisableReason** element specifies the reason for disabling an app.</span></span> 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 <span data-ttu-id="1c427-105">**DisableReasonType**</span><span class="sxs-lookup"><span data-stu-id="1c427-105">**DisableReasonType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c427-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1c427-106">Attributes and elements</span></span>

<span data-ttu-id="1c427-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1c427-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c427-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1c427-108">Attributes</span></span>

<span data-ttu-id="1c427-109">无。</span><span class="sxs-lookup"><span data-stu-id="1c427-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c427-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1c427-110">Child elements</span></span>

<span data-ttu-id="1c427-111">无。</span><span class="sxs-lookup"><span data-stu-id="1c427-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1c427-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1c427-112">Parent elements</span></span>

|<span data-ttu-id="1c427-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1c427-113">**Element**</span></span>|<span data-ttu-id="1c427-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="1c427-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c427-115">DisableApp</span><span class="sxs-lookup"><span data-stu-id="1c427-115">DisableApp</span></span>](disableapp.md) <br/> |<span data-ttu-id="1c427-116">指定要禁用应用程序的请求。</span><span class="sxs-lookup"><span data-stu-id="1c427-116">Specifies a request to disable an app.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1c427-117">文本值</span><span class="sxs-lookup"><span data-stu-id="1c427-117">Text value</span></span>

<span data-ttu-id="1c427-118">**DisableReason 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="1c427-118">**DisableReason element text value**</span></span>

|<span data-ttu-id="1c427-119">**值**</span><span class="sxs-lookup"><span data-stu-id="1c427-119">**Value**</span></span>|<span data-ttu-id="1c427-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="1c427-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c427-121">NoReason</span><span class="sxs-lookup"><span data-stu-id="1c427-121">NoReason</span></span>  <br/> |<span data-ttu-id="1c427-122">没有给定原因</span><span class="sxs-lookup"><span data-stu-id="1c427-122">No reason given</span></span>  <br/> |
|<span data-ttu-id="1c427-123">OutlookClientPerformance</span><span class="sxs-lookup"><span data-stu-id="1c427-123">OutlookClientPerformance</span></span>  <br/> |<span data-ttu-id="1c427-124">提高电子邮件客户端的性能。</span><span class="sxs-lookup"><span data-stu-id="1c427-124">To improve email client performance.</span></span>  <br/> |
|<span data-ttu-id="1c427-125">OWAClientPerformance</span><span class="sxs-lookup"><span data-stu-id="1c427-125">OWAClientPerformance</span></span>  <br/> |<span data-ttu-id="1c427-126">以提高 Web 应用程序客户端的性能。</span><span class="sxs-lookup"><span data-stu-id="1c427-126">To improve Web app client performance.</span></span>  <br/> |
|<span data-ttu-id="1c427-127">MobileClientPerformance</span><span class="sxs-lookup"><span data-stu-id="1c427-127">MobileClientPerformance</span></span>  <br/> |<span data-ttu-id="1c427-128">提高移动客户端的性能。</span><span class="sxs-lookup"><span data-stu-id="1c427-128">To improve mobile client performance.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c427-129">备注</span><span class="sxs-lookup"><span data-stu-id="1c427-129">Remarks</span></span>

<span data-ttu-id="1c427-130">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1c427-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1c427-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1c427-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c427-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="1c427-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c427-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="1c427-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1c427-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="1c427-134">Schema Name</span></span>  <br/> |<span data-ttu-id="1c427-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="1c427-135">Type schema</span></span>  <br/> |
|<span data-ttu-id="1c427-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="1c427-136">Validation File</span></span>  <br/> |<span data-ttu-id="1c427-137">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="1c427-137">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1c427-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="1c427-138">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1c427-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1c427-139">See also</span></span>

- [<span data-ttu-id="1c427-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1c427-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

