---
title: 配置名
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
description: 配置名元素指定名称的请求的服务配置。
ms.openlocfilehash: a03a0bc0ab7ecbc1c2aec31f864503ee0f560908
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753477"
---
# <a name="configurationname"></a><span data-ttu-id="cac00-103">配置名</span><span class="sxs-lookup"><span data-stu-id="cac00-103">ConfigurationName</span></span>

<span data-ttu-id="cac00-104">**配置名**元素指定名称的请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="cac00-104">The **ConfigurationName** element specifies the requested service configurations by name.</span></span> 
  
```xml
<ConfigurationName>MailTips or UnifiedMessagingConfiguration or ProtectionRules</ConfigurationName>
```

 <span data-ttu-id="cac00-105">**ServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="cac00-105">**ServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cac00-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cac00-106">Attributes and elements</span></span>

<span data-ttu-id="cac00-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cac00-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cac00-108">属性</span><span class="sxs-lookup"><span data-stu-id="cac00-108">Attributes</span></span>

<span data-ttu-id="cac00-109">无。</span><span class="sxs-lookup"><span data-stu-id="cac00-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cac00-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cac00-110">Child elements</span></span>

<span data-ttu-id="cac00-111">无。</span><span class="sxs-lookup"><span data-stu-id="cac00-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cac00-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cac00-112">Parent elements</span></span>

|<span data-ttu-id="cac00-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cac00-113">**Element**</span></span>|<span data-ttu-id="cac00-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cac00-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cac00-115">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="cac00-115">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="cac00-116">包含请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="cac00-116">Contains the requested service configurations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cac00-117">文本值</span><span class="sxs-lookup"><span data-stu-id="cac00-117">Text value</span></span>

<span data-ttu-id="cac00-118">下表列出了**配置名**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="cac00-118">The following table lists the possible values for the **ConfigurationName** element.</span></span> 
  
<span data-ttu-id="cac00-119">**配置名元素的值**</span><span class="sxs-lookup"><span data-stu-id="cac00-119">**ConfigurationName element values**</span></span>

|<span data-ttu-id="cac00-120">**值**</span><span class="sxs-lookup"><span data-stu-id="cac00-120">**Value**</span></span>|<span data-ttu-id="cac00-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="cac00-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cac00-122">邮件提示</span><span class="sxs-lookup"><span data-stu-id="cac00-122">MailTips</span></span>  <br/> |<span data-ttu-id="cac00-123">标识邮件提醒服务配置。</span><span class="sxs-lookup"><span data-stu-id="cac00-123">Identifies the MailTips service configuration.</span></span>  <br/> |
|<span data-ttu-id="cac00-124">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cac00-124">UnifiedMessagingConfiguration</span></span>  <br/> |<span data-ttu-id="cac00-125">标识的统一消息服务配置。</span><span class="sxs-lookup"><span data-stu-id="cac00-125">Identifies the Unified Messaging service configuration.</span></span>  <br/> |
|<span data-ttu-id="cac00-126">ProtectionRules</span><span class="sxs-lookup"><span data-stu-id="cac00-126">ProtectionRules</span></span>  <br/> |<span data-ttu-id="cac00-127">标识保护规则服务配置。</span><span class="sxs-lookup"><span data-stu-id="cac00-127">Identifies the Protection Rules service configuration.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cac00-128">备注</span><span class="sxs-lookup"><span data-stu-id="cac00-128">Remarks</span></span>

<span data-ttu-id="cac00-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cac00-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cac00-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="cac00-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cac00-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="cac00-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cac00-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="cac00-132">Schema Name</span></span>  <br/> |<span data-ttu-id="cac00-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="cac00-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cac00-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="cac00-134">Validation File</span></span>  <br/> |<span data-ttu-id="cac00-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cac00-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cac00-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="cac00-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="cac00-137">False</span><span class="sxs-lookup"><span data-stu-id="cac00-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cac00-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cac00-138">See also</span></span>



- [<span data-ttu-id="cac00-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cac00-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

