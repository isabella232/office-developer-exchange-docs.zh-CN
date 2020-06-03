---
title: 域
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Domain
api_type:
- schema
ms.assetid: 7e45a061-856f-4b44-b053-a7c4d5ad569e
description: Domain 元素标识单个 SMTP 域。
ms.openlocfilehash: 3bf8e132b5fa588171ac4f3c095692bc68394663
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461329"
---
# <a name="domain"></a><span data-ttu-id="d2570-103">域</span><span class="sxs-lookup"><span data-stu-id="d2570-103">Domain</span></span>

<span data-ttu-id="d2570-104">**Domain**元素标识单个 SMTP 域。</span><span class="sxs-lookup"><span data-stu-id="d2570-104">The **Domain** element identifies a single SMTP domain.</span></span> 
  
```xml
<Domain Name="" IncludeSubdomains="" />
```

 <span data-ttu-id="d2570-105">**StmpDomain**</span><span class="sxs-lookup"><span data-stu-id="d2570-105">**StmpDomain**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2570-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d2570-106">Attributes and elements</span></span>

<span data-ttu-id="d2570-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d2570-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2570-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d2570-108">Attributes</span></span>

|<span data-ttu-id="d2570-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="d2570-109">**Attribute**</span></span>|<span data-ttu-id="d2570-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="d2570-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2570-111">名称</span><span class="sxs-lookup"><span data-stu-id="d2570-111">Name</span></span>  <br/> |<span data-ttu-id="d2570-112">标识域的名称。</span><span class="sxs-lookup"><span data-stu-id="d2570-112">Identifies the name of a domain.</span></span> <span data-ttu-id="d2570-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="d2570-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="d2570-114">IncludeSubdomains</span><span class="sxs-lookup"><span data-stu-id="d2570-114">IncludeSubdomains</span></span>  <br/> |<span data-ttu-id="d2570-115">指示由**Name**属性标识的域的子域是否被视为内部域。</span><span class="sxs-lookup"><span data-stu-id="d2570-115">Indicates whether subdomains of the domain identified by the **Name** attribute are considered internal.</span></span> <span data-ttu-id="d2570-116">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="d2570-116">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d2570-117">子元素</span><span class="sxs-lookup"><span data-stu-id="d2570-117">Child elements</span></span>

<span data-ttu-id="d2570-118">无。</span><span class="sxs-lookup"><span data-stu-id="d2570-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2570-119">父元素</span><span class="sxs-lookup"><span data-stu-id="d2570-119">Parent elements</span></span>

|<span data-ttu-id="d2570-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="d2570-120">**Element**</span></span>|<span data-ttu-id="d2570-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="d2570-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2570-122">InternalDomains （SmtpDomainList）</span><span class="sxs-lookup"><span data-stu-id="d2570-122">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="d2570-123">标识组织的内部 SMTP 域的列表。</span><span class="sxs-lookup"><span data-stu-id="d2570-123">Identifies the list of internal SMTP domains of the organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d2570-124">文本值</span><span class="sxs-lookup"><span data-stu-id="d2570-124">Text value</span></span>

<span data-ttu-id="d2570-125">无。</span><span class="sxs-lookup"><span data-stu-id="d2570-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2570-126">说明</span><span class="sxs-lookup"><span data-stu-id="d2570-126">Remarks</span></span>

<span data-ttu-id="d2570-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d2570-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2570-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="d2570-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2570-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="d2570-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d2570-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="d2570-130">Schema Name</span></span>  <br/> |<span data-ttu-id="d2570-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="d2570-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="d2570-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="d2570-132">Validation File</span></span>  <br/> |<span data-ttu-id="d2570-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d2570-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d2570-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="d2570-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2570-135">False</span><span class="sxs-lookup"><span data-stu-id="d2570-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2570-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2570-136">See also</span></span>

- [<span data-ttu-id="d2570-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d2570-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

