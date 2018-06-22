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
ms.openlocfilehash: f900bd1b98b294900f767c778b9c5f87f74042ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753895"
---
# <a name="disablereason"></a><span data-ttu-id="9430c-103">DisableReason</span><span class="sxs-lookup"><span data-stu-id="9430c-103">DisableReason</span></span>

<span data-ttu-id="9430c-104">**DisableReason**元素指定禁用应用程序的原因。</span><span class="sxs-lookup"><span data-stu-id="9430c-104">The **DisableReason** element specifies the reason for disabling an app.</span></span> 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 <span data-ttu-id="9430c-105">**DisableReasonType**</span><span class="sxs-lookup"><span data-stu-id="9430c-105">**DisableReasonType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9430c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9430c-106">Attributes and elements</span></span>

<span data-ttu-id="9430c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9430c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9430c-108">属性</span><span class="sxs-lookup"><span data-stu-id="9430c-108">Attributes</span></span>

<span data-ttu-id="9430c-109">无。</span><span class="sxs-lookup"><span data-stu-id="9430c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9430c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9430c-110">Child elements</span></span>

<span data-ttu-id="9430c-111">无。</span><span class="sxs-lookup"><span data-stu-id="9430c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9430c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9430c-112">Parent elements</span></span>

|<span data-ttu-id="9430c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9430c-113">**Element**</span></span>|<span data-ttu-id="9430c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9430c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9430c-115">DisableApp</span><span class="sxs-lookup"><span data-stu-id="9430c-115">DisableApp</span></span>](disableapp.md) <br/> |<span data-ttu-id="9430c-116">指定要禁用应用程序的请求。</span><span class="sxs-lookup"><span data-stu-id="9430c-116">Specifies a request to disable an app.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9430c-117">文本值</span><span class="sxs-lookup"><span data-stu-id="9430c-117">Text value</span></span>

<span data-ttu-id="9430c-118">**DisableReason 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="9430c-118">**DisableReason element text value**</span></span>

|<span data-ttu-id="9430c-119">**值**</span><span class="sxs-lookup"><span data-stu-id="9430c-119">**Value**</span></span>|<span data-ttu-id="9430c-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="9430c-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9430c-121">NoReason</span><span class="sxs-lookup"><span data-stu-id="9430c-121">NoReason</span></span>  <br/> |<span data-ttu-id="9430c-122">没有给定原因。</span><span class="sxs-lookup"><span data-stu-id="9430c-122">No reason given</span></span>  <br/> |
|<span data-ttu-id="9430c-123">OutlookClientPerformance</span><span class="sxs-lookup"><span data-stu-id="9430c-123">OutlookClientPerformance</span></span>  <br/> |<span data-ttu-id="9430c-124">若要提高电子邮件客户端性能。</span><span class="sxs-lookup"><span data-stu-id="9430c-124">To improve email client performance.</span></span>  <br/> |
|<span data-ttu-id="9430c-125">OWAClientPerformance</span><span class="sxs-lookup"><span data-stu-id="9430c-125">OWAClientPerformance</span></span>  <br/> |<span data-ttu-id="9430c-126">若要提高 Web 应用程序客户端性能。</span><span class="sxs-lookup"><span data-stu-id="9430c-126">To improve Web app client performance.</span></span>  <br/> |
|<span data-ttu-id="9430c-127">MobileClientPerformance</span><span class="sxs-lookup"><span data-stu-id="9430c-127">MobileClientPerformance</span></span>  <br/> |<span data-ttu-id="9430c-128">若要提高移动客户端性能。</span><span class="sxs-lookup"><span data-stu-id="9430c-128">To improve mobile client performance.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9430c-129">备注</span><span class="sxs-lookup"><span data-stu-id="9430c-129">Remarks</span></span>

<span data-ttu-id="9430c-130">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9430c-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9430c-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9430c-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9430c-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="9430c-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9430c-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="9430c-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9430c-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="9430c-134">Schema Name</span></span>  <br/> |<span data-ttu-id="9430c-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="9430c-135">Type schema</span></span>  <br/> |
|<span data-ttu-id="9430c-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="9430c-136">Validation File</span></span>  <br/> |<span data-ttu-id="9430c-137">types.xsd</span><span class="sxs-lookup"><span data-stu-id="9430c-137">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9430c-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="9430c-138">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9430c-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9430c-139">See also</span></span>

- [<span data-ttu-id="9430c-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9430c-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

