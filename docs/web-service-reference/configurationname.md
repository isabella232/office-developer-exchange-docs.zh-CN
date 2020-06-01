---
title: ConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConfigurationName
api_type:
- schema
ms.assetid: 3b524a2f-9c6b-4550-9f3d-f78d176b0f7b
description: ConfigurationName 元素按名称指定请求的服务配置。
ms.openlocfilehash: 5e1216253a633af643dbd276827842dbe2db5d5f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463921"
---
# <a name="configurationname"></a><span data-ttu-id="f134c-103">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f134c-103">ConfigurationName</span></span>

<span data-ttu-id="f134c-104">**ConfigurationName**元素按名称指定请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="f134c-104">The **ConfigurationName** element specifies the requested service configurations by name.</span></span> 
  
```xml
<ConfigurationName>MailTips or UnifiedMessagingConfiguration or ProtectionRules</ConfigurationName>
```

 <span data-ttu-id="f134c-105">**ServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="f134c-105">**ServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f134c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f134c-106">Attributes and elements</span></span>

<span data-ttu-id="f134c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f134c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f134c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f134c-108">Attributes</span></span>

<span data-ttu-id="f134c-109">无。</span><span class="sxs-lookup"><span data-stu-id="f134c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f134c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f134c-110">Child elements</span></span>

<span data-ttu-id="f134c-111">无。</span><span class="sxs-lookup"><span data-stu-id="f134c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f134c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f134c-112">Parent elements</span></span>

|<span data-ttu-id="f134c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f134c-113">**Element**</span></span>|<span data-ttu-id="f134c-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="f134c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f134c-115">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="f134c-115">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="f134c-116">包含请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="f134c-116">Contains the requested service configurations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f134c-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f134c-117">Text value</span></span>

<span data-ttu-id="f134c-118">下表列出了**ConfigurationName**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="f134c-118">The following table lists the possible values for the **ConfigurationName** element.</span></span> 
  
<span data-ttu-id="f134c-119">**ConfigurationName 元素值**</span><span class="sxs-lookup"><span data-stu-id="f134c-119">**ConfigurationName element values**</span></span>

|<span data-ttu-id="f134c-120">**值**</span><span class="sxs-lookup"><span data-stu-id="f134c-120">**Value**</span></span>|<span data-ttu-id="f134c-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="f134c-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f134c-122">邮件提示</span><span class="sxs-lookup"><span data-stu-id="f134c-122">MailTips</span></span>  <br/> |<span data-ttu-id="f134c-123">标识邮件提示服务配置。</span><span class="sxs-lookup"><span data-stu-id="f134c-123">Identifies the MailTips service configuration.</span></span>  <br/> |
|<span data-ttu-id="f134c-124">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f134c-124">UnifiedMessagingConfiguration</span></span>  <br/> |<span data-ttu-id="f134c-125">标识统一消息服务配置。</span><span class="sxs-lookup"><span data-stu-id="f134c-125">Identifies the Unified Messaging service configuration.</span></span>  <br/> |
|<span data-ttu-id="f134c-126">ProtectionRules</span><span class="sxs-lookup"><span data-stu-id="f134c-126">ProtectionRules</span></span>  <br/> |<span data-ttu-id="f134c-127">标识保护规则服务配置。</span><span class="sxs-lookup"><span data-stu-id="f134c-127">Identifies the Protection Rules service configuration.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f134c-128">说明</span><span class="sxs-lookup"><span data-stu-id="f134c-128">Remarks</span></span>

<span data-ttu-id="f134c-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f134c-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f134c-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="f134c-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f134c-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="f134c-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f134c-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="f134c-132">Schema Name</span></span>  <br/> |<span data-ttu-id="f134c-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="f134c-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f134c-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="f134c-134">Validation File</span></span>  <br/> |<span data-ttu-id="f134c-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f134c-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f134c-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="f134c-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="f134c-137">False</span><span class="sxs-lookup"><span data-stu-id="f134c-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f134c-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f134c-138">See also</span></span>



- [<span data-ttu-id="f134c-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f134c-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

