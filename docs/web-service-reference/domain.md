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
description: 域元素标识单个 SMTP 域。
ms.openlocfilehash: 78eb1edfd347a513b84b9c15d143d76425041e85
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753974"
---
# <a name="domain"></a><span data-ttu-id="f5d43-103">域</span><span class="sxs-lookup"><span data-stu-id="f5d43-103">Domain</span></span>

<span data-ttu-id="f5d43-104">**域**元素标识单个 SMTP 域。</span><span class="sxs-lookup"><span data-stu-id="f5d43-104">The **Domain** element identifies a single SMTP domain.</span></span> 
  
```xml
<Domain Name="" IncludeSubdomains="" />
```

 <span data-ttu-id="f5d43-105">**StmpDomain**</span><span class="sxs-lookup"><span data-stu-id="f5d43-105">**StmpDomain**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f5d43-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f5d43-106">Attributes and elements</span></span>

<span data-ttu-id="f5d43-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f5d43-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5d43-108">属性</span><span class="sxs-lookup"><span data-stu-id="f5d43-108">Attributes</span></span>

|<span data-ttu-id="f5d43-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f5d43-109">**Attribute**</span></span>|<span data-ttu-id="f5d43-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5d43-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5d43-111">名称</span><span class="sxs-lookup"><span data-stu-id="f5d43-111">Name</span></span>  <br/> |<span data-ttu-id="f5d43-112">标识域的名称。</span><span class="sxs-lookup"><span data-stu-id="f5d43-112">Identifies the name of a domain.</span></span> <span data-ttu-id="f5d43-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="f5d43-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="f5d43-114">IncludeSubdomains</span><span class="sxs-lookup"><span data-stu-id="f5d43-114">IncludeSubdomains</span></span>  <br/> |<span data-ttu-id="f5d43-115">指示是否由**Name**属性标识的域的子域均被视为内部。</span><span class="sxs-lookup"><span data-stu-id="f5d43-115">Indicates whether subdomains of the domain identified by the **Name** attribute are considered internal.</span></span> <span data-ttu-id="f5d43-116">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="f5d43-116">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f5d43-117">子元素</span><span class="sxs-lookup"><span data-stu-id="f5d43-117">Child elements</span></span>

<span data-ttu-id="f5d43-118">无。</span><span class="sxs-lookup"><span data-stu-id="f5d43-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f5d43-119">父元素</span><span class="sxs-lookup"><span data-stu-id="f5d43-119">Parent elements</span></span>

|<span data-ttu-id="f5d43-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5d43-120">**Element**</span></span>|<span data-ttu-id="f5d43-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5d43-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5d43-122">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="f5d43-122">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="f5d43-123">标识组织的内部 SMTP 域的列表。</span><span class="sxs-lookup"><span data-stu-id="f5d43-123">Identifies the list of internal SMTP domains of the organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f5d43-124">文本值</span><span class="sxs-lookup"><span data-stu-id="f5d43-124">Text value</span></span>

<span data-ttu-id="f5d43-125">无。</span><span class="sxs-lookup"><span data-stu-id="f5d43-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f5d43-126">备注</span><span class="sxs-lookup"><span data-stu-id="f5d43-126">Remarks</span></span>

<span data-ttu-id="f5d43-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f5d43-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f5d43-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="f5d43-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5d43-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="f5d43-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f5d43-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="f5d43-130">Schema Name</span></span>  <br/> |<span data-ttu-id="f5d43-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="f5d43-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="f5d43-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="f5d43-132">Validation File</span></span>  <br/> |<span data-ttu-id="f5d43-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f5d43-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f5d43-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="f5d43-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="f5d43-135">False</span><span class="sxs-lookup"><span data-stu-id="f5d43-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5d43-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5d43-136">See also</span></span>

- [<span data-ttu-id="f5d43-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f5d43-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

