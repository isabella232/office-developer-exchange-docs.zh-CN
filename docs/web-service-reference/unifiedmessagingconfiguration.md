---
title: UnifiedMessagingConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnifiedMessagingConfiguration
api_type:
- schema
ms.assetid: cbdb4268-077e-44ed-8ec2-9d759c84cc6d
description: UnifiedMessagingConfiguration 元素包含统一消息服务的服务配置信息。
ms.openlocfilehash: 3ad8f66ecdf21062c00c2a6ac6f65fac875da38c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838317"
---
# <a name="unifiedmessagingconfiguration"></a><span data-ttu-id="fb85c-103">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb85c-103">UnifiedMessagingConfiguration</span></span>

<span data-ttu-id="fb85c-104">**UnifiedMessagingConfiguration**元素包含统一消息服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="fb85c-104">The **UnifiedMessagingConfiguration** element contains service configuration information for the Unified Messaging service.</span></span> 
  
```XML
<UnifiedMessagingConfiguration>
   <UmEnabled/>
   <PlayOnPhoneDialString/>
   <PlayOnPhoneEnabled/>
</UnifiedMessagingConfiguration>
```

 <span data-ttu-id="fb85c-105">**UnifiedMessageServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="fb85c-105">**UnifiedMessageServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fb85c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fb85c-106">Attributes and elements</span></span>

<span data-ttu-id="fb85c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fb85c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb85c-108">属性</span><span class="sxs-lookup"><span data-stu-id="fb85c-108">Attributes</span></span>

<span data-ttu-id="fb85c-109">无。</span><span class="sxs-lookup"><span data-stu-id="fb85c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb85c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fb85c-110">Child elements</span></span>

|<span data-ttu-id="fb85c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fb85c-111">**Element**</span></span>|<span data-ttu-id="fb85c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb85c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb85c-113">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="fb85c-113">UmEnabled</span></span>](umenabled.md) <br/> |<span data-ttu-id="fb85c-114">指示是否为帐户启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="fb85c-114">Indicates whether Unified Messaging is enabled for an account.</span></span> <span data-ttu-id="fb85c-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="fb85c-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="fb85c-116">PlayOnPhoneDialString （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="fb85c-116">PlayOnPhoneDialString (Exchange Web Services)</span></span>](playonphonedialstring-exchange-web-services.md) <br/> |<span data-ttu-id="fb85c-117">标识播放接听电话拨号字符串。</span><span class="sxs-lookup"><span data-stu-id="fb85c-117">Identifies the Play-on-Phone dial string.</span></span> <span data-ttu-id="fb85c-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="fb85c-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="fb85c-119">PlayOnPhoneEnabled</span><span class="sxs-lookup"><span data-stu-id="fb85c-119">PlayOnPhoneEnabled</span></span>](playonphoneenabled.md) <br/> |<span data-ttu-id="fb85c-120">指示是否启用播放接听电话功能。</span><span class="sxs-lookup"><span data-stu-id="fb85c-120">Indicates whether the Play-on-Phone feature is enabled.</span></span> <span data-ttu-id="fb85c-121">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="fb85c-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fb85c-122">父元素</span><span class="sxs-lookup"><span data-stu-id="fb85c-122">Parent elements</span></span>

|<span data-ttu-id="fb85c-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="fb85c-123">**Element**</span></span>|<span data-ttu-id="fb85c-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb85c-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb85c-125">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="fb85c-125">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="fb85c-126">包含服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="fb85c-126">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fb85c-127">文本值</span><span class="sxs-lookup"><span data-stu-id="fb85c-127">Text value</span></span>

<span data-ttu-id="fb85c-128">无。</span><span class="sxs-lookup"><span data-stu-id="fb85c-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb85c-129">备注</span><span class="sxs-lookup"><span data-stu-id="fb85c-129">Remarks</span></span>

<span data-ttu-id="fb85c-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fb85c-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb85c-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="fb85c-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb85c-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="fb85c-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fb85c-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="fb85c-133">Schema Name</span></span>  <br/> |<span data-ttu-id="fb85c-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="fb85c-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fb85c-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="fb85c-135">Validation File</span></span>  <br/> |<span data-ttu-id="fb85c-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fb85c-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fb85c-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="fb85c-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="fb85c-138">False</span><span class="sxs-lookup"><span data-stu-id="fb85c-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb85c-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fb85c-139">See also</span></span>



- [<span data-ttu-id="fb85c-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fb85c-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

