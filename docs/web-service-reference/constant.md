---
title: 常量
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Constant
api_type:
- schema
ms.assetid: 340af0cd-9f12-44ab-b8f1-21d107c8d0c9
description: 常量元素标识限制中的以常量值。
ms.openlocfilehash: 73912bc1981c5d54040f7c4a563ad805916fe721
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753489"
---
# <a name="constant"></a><span data-ttu-id="9b3dc-103">常量</span><span class="sxs-lookup"><span data-stu-id="9b3dc-103">Constant</span></span>

<span data-ttu-id="9b3dc-104">**常量**元素标识限制中的以常量值。</span><span class="sxs-lookup"><span data-stu-id="9b3dc-104">The **Constant** element identifies a constant value in a restriction.</span></span> 
  
```xml
<Constant Value="" />
```

 <span data-ttu-id="9b3dc-105">**ConstantValueType**</span><span class="sxs-lookup"><span data-stu-id="9b3dc-105">**ConstantValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b3dc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9b3dc-106">Attributes and elements</span></span>

<span data-ttu-id="9b3dc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9b3dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b3dc-108">属性</span><span class="sxs-lookup"><span data-stu-id="9b3dc-108">Attributes</span></span>

|<span data-ttu-id="9b3dc-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="9b3dc-109">**Attribute**</span></span>|<span data-ttu-id="9b3dc-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b3dc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b3dc-111">**Value**</span><span class="sxs-lookup"><span data-stu-id="9b3dc-111">**Value**</span></span> <br/> |<span data-ttu-id="9b3dc-112">指定要限制中比较的值。</span><span class="sxs-lookup"><span data-stu-id="9b3dc-112">Specifies the value to compare in the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b3dc-113">子元素</span><span class="sxs-lookup"><span data-stu-id="9b3dc-113">Child elements</span></span>

<span data-ttu-id="9b3dc-114">无。</span><span class="sxs-lookup"><span data-stu-id="9b3dc-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9b3dc-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9b3dc-115">Parent elements</span></span>

|<span data-ttu-id="9b3dc-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b3dc-116">**Element**</span></span>|<span data-ttu-id="9b3dc-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b3dc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b3dc-118">Contains</span><span class="sxs-lookup"><span data-stu-id="9b3dc-118">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="9b3dc-119">代表一个搜索表达式，确定给定的属性是否包含提供常量的字符串值。</span><span class="sxs-lookup"><span data-stu-id="9b3dc-119">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="9b3dc-120">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="9b3dc-120">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="9b3dc-121">代表属性或以常量值，用于比较与另一个属性。</span><span class="sxs-lookup"><span data-stu-id="9b3dc-121">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b3dc-122">注解</span><span class="sxs-lookup"><span data-stu-id="9b3dc-122">Remarks</span></span>

<span data-ttu-id="9b3dc-123">**Value**属性中的字符串值必须可以强制转换为想要进行比较的类型。</span><span class="sxs-lookup"><span data-stu-id="9b3dc-123">The string value in the **Value** attribute must be coercible into the type you are trying to compare against.</span></span> <span data-ttu-id="9b3dc-124">例如，如果您要进行比较以常量值对的日期/时间属性，该字符串值必须表示日期/时间。</span><span class="sxs-lookup"><span data-stu-id="9b3dc-124">For example, if you are comparing a date/time property against a constant value, the string value must represent a date/time.</span></span> 
  
<span data-ttu-id="9b3dc-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9b3dc-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b3dc-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="9b3dc-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b3dc-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="9b3dc-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9b3dc-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="9b3dc-128">Schema Name</span></span>  <br/> |<span data-ttu-id="9b3dc-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="9b3dc-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="9b3dc-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="9b3dc-130">Validation File</span></span>  <br/> |<span data-ttu-id="9b3dc-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9b3dc-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9b3dc-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="9b3dc-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="9b3dc-133">False</span><span class="sxs-lookup"><span data-stu-id="9b3dc-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b3dc-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9b3dc-134">See also</span></span>



- [<span data-ttu-id="9b3dc-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9b3dc-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

