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
ms.openlocfilehash: 3f9f4ed65721929c552615c07e2239f48ef837f3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528690"
---
# <a name="unifiedmessagingconfiguration"></a><span data-ttu-id="27709-103">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="27709-103">UnifiedMessagingConfiguration</span></span>

<span data-ttu-id="27709-104">**UnifiedMessagingConfiguration**元素包含统一消息服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="27709-104">The **UnifiedMessagingConfiguration** element contains service configuration information for the Unified Messaging service.</span></span> 
  
```XML
<UnifiedMessagingConfiguration>
   <UmEnabled/>
   <PlayOnPhoneDialString/>
   <PlayOnPhoneEnabled/>
</UnifiedMessagingConfiguration>
```

 <span data-ttu-id="27709-105">**UnifiedMessageServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="27709-105">**UnifiedMessageServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27709-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="27709-106">Attributes and elements</span></span>

<span data-ttu-id="27709-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="27709-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27709-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="27709-108">Attributes</span></span>

<span data-ttu-id="27709-109">无。</span><span class="sxs-lookup"><span data-stu-id="27709-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27709-110">子元素</span><span class="sxs-lookup"><span data-stu-id="27709-110">Child elements</span></span>

|<span data-ttu-id="27709-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="27709-111">**Element**</span></span>|<span data-ttu-id="27709-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="27709-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27709-113">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="27709-113">UmEnabled</span></span>](umenabled.md) <br/> |<span data-ttu-id="27709-114">指示是否为帐户启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="27709-114">Indicates whether Unified Messaging is enabled for an account.</span></span> <span data-ttu-id="27709-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="27709-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="27709-116">PlayOnPhoneDialString （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="27709-116">PlayOnPhoneDialString (Exchange Web Services)</span></span>](playonphonedialstring-exchange-web-services.md) <br/> |<span data-ttu-id="27709-117">标识 "电话拨入" 拨号字符串。</span><span class="sxs-lookup"><span data-stu-id="27709-117">Identifies the Play-on-Phone dial string.</span></span> <span data-ttu-id="27709-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="27709-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="27709-119">PlayOnPhoneEnabled</span><span class="sxs-lookup"><span data-stu-id="27709-119">PlayOnPhoneEnabled</span></span>](playonphoneenabled.md) <br/> |<span data-ttu-id="27709-120">指示是否启用 "电话上播放" 功能。</span><span class="sxs-lookup"><span data-stu-id="27709-120">Indicates whether the Play-on-Phone feature is enabled.</span></span> <span data-ttu-id="27709-121">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="27709-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27709-122">父元素</span><span class="sxs-lookup"><span data-stu-id="27709-122">Parent elements</span></span>

|<span data-ttu-id="27709-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="27709-123">**Element**</span></span>|<span data-ttu-id="27709-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="27709-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27709-125">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="27709-125">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="27709-126">包含服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="27709-126">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="27709-127">文本值</span><span class="sxs-lookup"><span data-stu-id="27709-127">Text value</span></span>

<span data-ttu-id="27709-128">无。</span><span class="sxs-lookup"><span data-stu-id="27709-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27709-129">说明</span><span class="sxs-lookup"><span data-stu-id="27709-129">Remarks</span></span>

<span data-ttu-id="27709-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="27709-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27709-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="27709-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27709-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="27709-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="27709-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="27709-133">Schema Name</span></span>  <br/> |<span data-ttu-id="27709-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="27709-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="27709-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="27709-135">Validation File</span></span>  <br/> |<span data-ttu-id="27709-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="27709-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="27709-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="27709-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="27709-138">False</span><span class="sxs-lookup"><span data-stu-id="27709-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27709-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27709-139">See also</span></span>



- [<span data-ttu-id="27709-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="27709-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

