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
ms.openlocfilehash: e664fba78f170c9f4c59b49b3a08c0dd2e4ed4cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456746"
---
# <a name="protectionrulesconfiguration"></a><span data-ttu-id="f1f1c-103">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1f1c-103">ProtectionRulesConfiguration</span></span>

<span data-ttu-id="f1f1c-104">**ProtectionRulesConfiguration**元素包含保护规则服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-104">The **ProtectionRulesConfiguration** element contains service configuration information for the protection rules service.</span></span> 
  
```XML
<ProtectionRulesConfiguration RefreshInterval="">
   <Rules/>
   <InternalDomains/>
</ProtectionRulesConfiguration>
```

 <span data-ttu-id="f1f1c-105">**ProtectionRulesServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f1f1c-105">**ProtectionRulesServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1f1c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f1f1c-106">Attributes and elements</span></span>

<span data-ttu-id="f1f1c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1f1c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f1f1c-108">Attributes</span></span>

|<span data-ttu-id="f1f1c-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f1f1c-109">**Attribute**</span></span>|<span data-ttu-id="f1f1c-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f1f1c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1f1c-111">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="f1f1c-111">**RefreshInterval**</span></span> <br/> |<span data-ttu-id="f1f1c-112">指定客户端应从服务器请求保护规则的间隔（以整小时为单位）。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-112">Specifies how often, in whole hours, the client should request protection rules from the server.</span></span> <span data-ttu-id="f1f1c-113">此属性是必需的，它的值必须是大于或等于1的整数。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-113">This attribute is required and its value must be an integer that is equal to or greater than 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f1f1c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="f1f1c-114">Child elements</span></span>

|<span data-ttu-id="f1f1c-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="f1f1c-115">**Element**</span></span>|<span data-ttu-id="f1f1c-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="f1f1c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1f1c-117">原则</span><span class="sxs-lookup"><span data-stu-id="f1f1c-117">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f1f1c-118">一组保护规则。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-118">An array of protection rules.</span></span> <span data-ttu-id="f1f1c-119">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="f1f1c-120">InternalDomains （SmtpDomainList）</span><span class="sxs-lookup"><span data-stu-id="f1f1c-120">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="f1f1c-121">标识组织的内部 SMTP 域的列表。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-121">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="f1f1c-122">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-122">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f1f1c-123">父元素</span><span class="sxs-lookup"><span data-stu-id="f1f1c-123">Parent elements</span></span>

|<span data-ttu-id="f1f1c-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="f1f1c-124">**Element**</span></span>|<span data-ttu-id="f1f1c-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="f1f1c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1f1c-126">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="f1f1c-126">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="f1f1c-127">包含服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-127">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f1f1c-128">文本值</span><span class="sxs-lookup"><span data-stu-id="f1f1c-128">Text value</span></span>

<span data-ttu-id="f1f1c-129">无。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1f1c-130">说明</span><span class="sxs-lookup"><span data-stu-id="f1f1c-130">Remarks</span></span>

<span data-ttu-id="f1f1c-131">保护规则服务配置由规则、内部域和刷新间隔的列表组成。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-131">The protection rules service configuration is comprised of a list of rules, internal domains, and a refresh interval.</span></span>
  
<span data-ttu-id="f1f1c-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f1f1c-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1f1c-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="f1f1c-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1f1c-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="f1f1c-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f1f1c-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="f1f1c-135">Schema Name</span></span>  <br/> |<span data-ttu-id="f1f1c-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="f1f1c-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f1f1c-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="f1f1c-137">Validation File</span></span>  <br/> |<span data-ttu-id="f1f1c-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f1f1c-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f1f1c-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="f1f1c-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="f1f1c-140">False</span><span class="sxs-lookup"><span data-stu-id="f1f1c-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1f1c-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f1f1c-141">See also</span></span>



- [<span data-ttu-id="f1f1c-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f1f1c-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

