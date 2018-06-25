---
title: InternalDomains (SmtpDomainList)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternalDomains
api_type:
- schema
ms.assetid: 0f2cbb05-338d-4302-8871-a06e78b33f98
description: InternalDomains 元素标识组织的内部 SMTP 域的列表。
ms.openlocfilehash: f37a31f4348a7eb0024656489f249dec349bc67b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825953"
---
# <a name="internaldomains-smtpdomainlist"></a><span data-ttu-id="f7bff-103">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="f7bff-103">InternalDomains (SmtpDomainList)</span></span>

<span data-ttu-id="f7bff-104">**InternalDomains**元素标识组织的内部 SMTP 域的列表。</span><span class="sxs-lookup"><span data-stu-id="f7bff-104">The **InternalDomains** element identifies the list of internal SMTP domains of the organization.</span></span> 
  
```XML
<InternalDomains>
   <Domain/>
</InternalDomains>
```

 <span data-ttu-id="f7bff-105">**SmtpDomainList**</span><span class="sxs-lookup"><span data-stu-id="f7bff-105">**SmtpDomainList**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7bff-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f7bff-106">Attributes and elements</span></span>

<span data-ttu-id="f7bff-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f7bff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7bff-108">属性</span><span class="sxs-lookup"><span data-stu-id="f7bff-108">Attributes</span></span>

<span data-ttu-id="f7bff-109">无。</span><span class="sxs-lookup"><span data-stu-id="f7bff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7bff-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f7bff-110">Child elements</span></span>

|<span data-ttu-id="f7bff-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7bff-111">**Element**</span></span>|<span data-ttu-id="f7bff-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7bff-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7bff-113">Domain</span><span class="sxs-lookup"><span data-stu-id="f7bff-113">Domain</span></span>](domain.md) <br/> |<span data-ttu-id="f7bff-114">标识单个 SMTP 域。</span><span class="sxs-lookup"><span data-stu-id="f7bff-114">Identifies a single SMTP domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f7bff-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f7bff-115">Parent elements</span></span>

|<span data-ttu-id="f7bff-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7bff-116">**Element**</span></span>|<span data-ttu-id="f7bff-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7bff-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7bff-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="f7bff-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="f7bff-119">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="f7bff-119">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="f7bff-120">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7bff-120">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="f7bff-121">包含保护规则服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="f7bff-121">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f7bff-122">文本值</span><span class="sxs-lookup"><span data-stu-id="f7bff-122">Text value</span></span>

<span data-ttu-id="f7bff-123">无。</span><span class="sxs-lookup"><span data-stu-id="f7bff-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7bff-124">注解</span><span class="sxs-lookup"><span data-stu-id="f7bff-124">Remarks</span></span>

<span data-ttu-id="f7bff-125">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="f7bff-125">This element is required.</span></span> 
  
<span data-ttu-id="f7bff-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f7bff-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7bff-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="f7bff-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7bff-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="f7bff-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f7bff-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="f7bff-129">Schema Name</span></span>  <br/> |<span data-ttu-id="f7bff-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="f7bff-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="f7bff-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="f7bff-131">Validation File</span></span>  <br/> |<span data-ttu-id="f7bff-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f7bff-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f7bff-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="f7bff-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7bff-134">False</span><span class="sxs-lookup"><span data-stu-id="f7bff-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7bff-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f7bff-135">See also</span></span>



- [<span data-ttu-id="f7bff-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f7bff-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

