---
title: ProtectionRulesConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ProtectionRulesConfiguration
api_type:
- schema
ms.assetid: e5b4699a-476e-4053-bb52-873eb921c046
description: ProtectionRulesConfiguration 元素包含保护规则服务的服务配置信息。
ms.openlocfilehash: 9c286fcf9752d591d53323f45a264f4bdd078c1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826912"
---
# <a name="protectionrulesconfiguration"></a><span data-ttu-id="652d0-103">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="652d0-103">ProtectionRulesConfiguration</span></span>

<span data-ttu-id="652d0-104">**ProtectionRulesConfiguration**元素包含保护规则服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="652d0-104">The **ProtectionRulesConfiguration** element contains service configuration information for the protection rules service.</span></span> 
  
```XML
<ProtectionRulesConfiguration RefreshInterval="">
   <Rules/>
   <InternalDomains/>
</ProtectionRulesConfiguration>
```

 <span data-ttu-id="652d0-105">**ProtectionRulesServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="652d0-105">**ProtectionRulesServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="652d0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="652d0-106">Attributes and elements</span></span>

<span data-ttu-id="652d0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="652d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="652d0-108">属性</span><span class="sxs-lookup"><span data-stu-id="652d0-108">Attributes</span></span>

|<span data-ttu-id="652d0-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="652d0-109">**Attribute**</span></span>|<span data-ttu-id="652d0-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="652d0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="652d0-111">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="652d0-111">**RefreshInterval**</span></span> <br/> |<span data-ttu-id="652d0-112">指定频率，在整个小时内，客户端应保护规则从服务器请求。</span><span class="sxs-lookup"><span data-stu-id="652d0-112">Specifies how often, in whole hours, the client should request protection rules from the server.</span></span> <span data-ttu-id="652d0-113">此属性是必需的其值必须等于或大于 1 的整数。</span><span class="sxs-lookup"><span data-stu-id="652d0-113">This attribute is required and its value must be an integer that is equal to or greater than 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="652d0-114">子元素</span><span class="sxs-lookup"><span data-stu-id="652d0-114">Child elements</span></span>

|<span data-ttu-id="652d0-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="652d0-115">**Element**</span></span>|<span data-ttu-id="652d0-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="652d0-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="652d0-117">规则</span><span class="sxs-lookup"><span data-stu-id="652d0-117">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="652d0-118">保护规则数组。</span><span class="sxs-lookup"><span data-stu-id="652d0-118">An array of protection rules.</span></span> <span data-ttu-id="652d0-119">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="652d0-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="652d0-120">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="652d0-120">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="652d0-121">标识组织的内部 SMTP 域的列表。</span><span class="sxs-lookup"><span data-stu-id="652d0-121">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="652d0-122">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="652d0-122">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="652d0-123">父元素</span><span class="sxs-lookup"><span data-stu-id="652d0-123">Parent elements</span></span>

|<span data-ttu-id="652d0-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="652d0-124">**Element**</span></span>|<span data-ttu-id="652d0-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="652d0-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="652d0-126">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="652d0-126">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="652d0-127">包含服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="652d0-127">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="652d0-128">文本值</span><span class="sxs-lookup"><span data-stu-id="652d0-128">Text value</span></span>

<span data-ttu-id="652d0-129">无。</span><span class="sxs-lookup"><span data-stu-id="652d0-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="652d0-130">注解</span><span class="sxs-lookup"><span data-stu-id="652d0-130">Remarks</span></span>

<span data-ttu-id="652d0-131">保护规则服务配置由一组规则、 内部域和刷新间隔。</span><span class="sxs-lookup"><span data-stu-id="652d0-131">The protection rules service configuration is comprised of a list of rules, internal domains, and a refresh interval.</span></span>
  
<span data-ttu-id="652d0-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="652d0-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="652d0-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="652d0-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="652d0-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="652d0-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="652d0-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="652d0-135">Schema Name</span></span>  <br/> |<span data-ttu-id="652d0-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="652d0-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="652d0-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="652d0-137">Validation File</span></span>  <br/> |<span data-ttu-id="652d0-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="652d0-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="652d0-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="652d0-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="652d0-140">False</span><span class="sxs-lookup"><span data-stu-id="652d0-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="652d0-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="652d0-141">See also</span></span>



- [<span data-ttu-id="652d0-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="652d0-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

