---
title: InternalDomains （SmtpDomainList）
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
ms.openlocfilehash: ec7ef2d72ae922c751f8f50b72ff7d6b31b212ca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459964"
---
# <a name="internaldomains-smtpdomainlist"></a><span data-ttu-id="0324c-103">InternalDomains （SmtpDomainList）</span><span class="sxs-lookup"><span data-stu-id="0324c-103">InternalDomains (SmtpDomainList)</span></span>

<span data-ttu-id="0324c-104">**InternalDomains**元素标识组织的内部 SMTP 域的列表。</span><span class="sxs-lookup"><span data-stu-id="0324c-104">The **InternalDomains** element identifies the list of internal SMTP domains of the organization.</span></span> 
  
```XML
<InternalDomains>
   <Domain/>
</InternalDomains>
```

 <span data-ttu-id="0324c-105">**SmtpDomainList**</span><span class="sxs-lookup"><span data-stu-id="0324c-105">**SmtpDomainList**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0324c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0324c-106">Attributes and elements</span></span>

<span data-ttu-id="0324c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0324c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0324c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0324c-108">Attributes</span></span>

<span data-ttu-id="0324c-109">无。</span><span class="sxs-lookup"><span data-stu-id="0324c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0324c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0324c-110">Child elements</span></span>

|<span data-ttu-id="0324c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0324c-111">**Element**</span></span>|<span data-ttu-id="0324c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0324c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0324c-113">域</span><span class="sxs-lookup"><span data-stu-id="0324c-113">Domain</span></span>](domain.md) <br/> |<span data-ttu-id="0324c-114">标识单个 SMTP 域。</span><span class="sxs-lookup"><span data-stu-id="0324c-114">Identifies a single SMTP domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0324c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="0324c-115">Parent elements</span></span>

|<span data-ttu-id="0324c-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="0324c-116">**Element**</span></span>|<span data-ttu-id="0324c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="0324c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0324c-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="0324c-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="0324c-119">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0324c-119">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="0324c-120">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="0324c-120">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="0324c-121">包含保护规则服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="0324c-121">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0324c-122">文本值</span><span class="sxs-lookup"><span data-stu-id="0324c-122">Text value</span></span>

<span data-ttu-id="0324c-123">无。</span><span class="sxs-lookup"><span data-stu-id="0324c-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0324c-124">说明</span><span class="sxs-lookup"><span data-stu-id="0324c-124">Remarks</span></span>

<span data-ttu-id="0324c-125">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="0324c-125">This element is required.</span></span> 
  
<span data-ttu-id="0324c-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0324c-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0324c-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="0324c-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0324c-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="0324c-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0324c-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="0324c-129">Schema Name</span></span>  <br/> |<span data-ttu-id="0324c-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="0324c-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="0324c-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="0324c-131">Validation File</span></span>  <br/> |<span data-ttu-id="0324c-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0324c-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0324c-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="0324c-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="0324c-134">False</span><span class="sxs-lookup"><span data-stu-id="0324c-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0324c-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0324c-135">See also</span></span>



- [<span data-ttu-id="0324c-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0324c-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

