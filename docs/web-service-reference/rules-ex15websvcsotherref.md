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
description: Rules 元素包含保护规则的数组。
ms.openlocfilehash: d848abfe0c97d07836f28bc75806f506c5433d44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464936"
---
# <a name="rules"></a><span data-ttu-id="2f8e6-103">规则</span><span class="sxs-lookup"><span data-stu-id="2f8e6-103">Rules</span></span>

<span data-ttu-id="2f8e6-104">**Rules**元素包含保护规则的数组。</span><span class="sxs-lookup"><span data-stu-id="2f8e6-104">The **Rules** element contains an array of protection rules.</span></span> 
  
```xml
<Rules>   <Rule/></Rules>
```

 <span data-ttu-id="2f8e6-105">**ArrayOfProtectionRulesType**</span><span class="sxs-lookup"><span data-stu-id="2f8e6-105">**ArrayOfProtectionRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f8e6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2f8e6-106">Attributes and elements</span></span>

<span data-ttu-id="2f8e6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f8e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f8e6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2f8e6-108">Attributes</span></span>

<span data-ttu-id="2f8e6-109">无。</span><span class="sxs-lookup"><span data-stu-id="2f8e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f8e6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2f8e6-110">Child elements</span></span>

|<span data-ttu-id="2f8e6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f8e6-111">**Element**</span></span>|<span data-ttu-id="2f8e6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f8e6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f8e6-113">Rule</span><span class="sxs-lookup"><span data-stu-id="2f8e6-113">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="2f8e6-114">包含一个保护规则。</span><span class="sxs-lookup"><span data-stu-id="2f8e6-114">Contains a single protection rule.</span></span> <span data-ttu-id="2f8e6-115">此元素可能出现零次或多次。</span><span class="sxs-lookup"><span data-stu-id="2f8e6-115">This element can occur zero or more times.</span></span> <span data-ttu-id="2f8e6-116">当组织未定义任何保护规则时，此元素将出现零次。</span><span class="sxs-lookup"><span data-stu-id="2f8e6-116">This element occurs zero times when no protection rules are defined by the organization.</span></span> <span data-ttu-id="2f8e6-117">如果组织至少定义了一个规则，则会出现一次或多次。</span><span class="sxs-lookup"><span data-stu-id="2f8e6-117">It occurs one or more times if at least one rule is defined by the organization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2f8e6-118">父元素</span><span class="sxs-lookup"><span data-stu-id="2f8e6-118">Parent elements</span></span>

|<span data-ttu-id="2f8e6-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f8e6-119">**Element**</span></span>|<span data-ttu-id="2f8e6-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f8e6-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f8e6-121">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f8e6-121">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="2f8e6-122">包含保护规则服务的服务配置。</span><span class="sxs-lookup"><span data-stu-id="2f8e6-122">Contains service configuration for the protection rules service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f8e6-123">备注</span><span class="sxs-lookup"><span data-stu-id="2f8e6-123">Remarks</span></span>

<span data-ttu-id="2f8e6-124">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2f8e6-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f8e6-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="2f8e6-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f8e6-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="2f8e6-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2f8e6-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="2f8e6-127">Schema Name</span></span>  <br/> |<span data-ttu-id="2f8e6-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="2f8e6-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="2f8e6-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="2f8e6-129">Validation File</span></span>  <br/> |<span data-ttu-id="2f8e6-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2f8e6-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2f8e6-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="2f8e6-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f8e6-132">False</span><span class="sxs-lookup"><span data-stu-id="2f8e6-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f8e6-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f8e6-133">See also</span></span>



- [<span data-ttu-id="2f8e6-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2f8e6-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

