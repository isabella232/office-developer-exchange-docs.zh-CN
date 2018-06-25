---
title: 规则
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rules
api_type:
- schema
ms.assetid: 53f59054-8f68-4eaa-be9c-ccfc9383bcf2
description: 规则元素包含一个数组保护规则。
ms.openlocfilehash: 5d511f977f3eb3273dc43f56356a059985b2a929
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827269"
---
# <a name="rules"></a><span data-ttu-id="88fd3-103">规则</span><span class="sxs-lookup"><span data-stu-id="88fd3-103">Rules</span></span>

<span data-ttu-id="88fd3-104">**规则**元素包含一个数组保护规则。</span><span class="sxs-lookup"><span data-stu-id="88fd3-104">The **Rules** element contains an array of protection rules.</span></span> 
  
```xml
<Rules>   <Rule/></Rules>
```

 <span data-ttu-id="88fd3-105">**ArrayOfProtectionRulesType**</span><span class="sxs-lookup"><span data-stu-id="88fd3-105">**ArrayOfProtectionRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="88fd3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="88fd3-106">Attributes and elements</span></span>

<span data-ttu-id="88fd3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="88fd3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88fd3-108">属性</span><span class="sxs-lookup"><span data-stu-id="88fd3-108">Attributes</span></span>

<span data-ttu-id="88fd3-109">无。</span><span class="sxs-lookup"><span data-stu-id="88fd3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88fd3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="88fd3-110">Child elements</span></span>

|<span data-ttu-id="88fd3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="88fd3-111">**Element**</span></span>|<span data-ttu-id="88fd3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="88fd3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88fd3-113">Rule</span><span class="sxs-lookup"><span data-stu-id="88fd3-113">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="88fd3-114">包含单个保护规则。</span><span class="sxs-lookup"><span data-stu-id="88fd3-114">Contains a single protection rule.</span></span> <span data-ttu-id="88fd3-115">此元素可以发生零个或多个时间。</span><span class="sxs-lookup"><span data-stu-id="88fd3-115">This element can occur zero or more times.</span></span> <span data-ttu-id="88fd3-116">此元素发生零次时由组织定义无保护规则。</span><span class="sxs-lookup"><span data-stu-id="88fd3-116">This element occurs zero times when no protection rules are defined by the organization.</span></span> <span data-ttu-id="88fd3-117">如果至少一个规则组织中定义，它会出现一个或多个时间。</span><span class="sxs-lookup"><span data-stu-id="88fd3-117">It occurs one or more times if at least one rule is defined by the organization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88fd3-118">父元素</span><span class="sxs-lookup"><span data-stu-id="88fd3-118">Parent elements</span></span>

|<span data-ttu-id="88fd3-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="88fd3-119">**Element**</span></span>|<span data-ttu-id="88fd3-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="88fd3-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88fd3-121">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="88fd3-121">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="88fd3-122">包含保护规则服务的服务配置。</span><span class="sxs-lookup"><span data-stu-id="88fd3-122">Contains service configuration for the protection rules service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88fd3-123">注解</span><span class="sxs-lookup"><span data-stu-id="88fd3-123">Remarks</span></span>

<span data-ttu-id="88fd3-124">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="88fd3-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88fd3-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="88fd3-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88fd3-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="88fd3-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="88fd3-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="88fd3-127">Schema Name</span></span>  <br/> |<span data-ttu-id="88fd3-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="88fd3-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="88fd3-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="88fd3-129">Validation File</span></span>  <br/> |<span data-ttu-id="88fd3-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="88fd3-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="88fd3-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="88fd3-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="88fd3-132">False</span><span class="sxs-lookup"><span data-stu-id="88fd3-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88fd3-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="88fd3-133">See also</span></span>



- [<span data-ttu-id="88fd3-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="88fd3-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

