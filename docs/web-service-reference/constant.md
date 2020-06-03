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
description: 常量元素标识限制中的常量值。
ms.openlocfilehash: 6cb2eaa4227a8fd0985e8ff5a15d647c3bb1cd6a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461553"
---
# <a name="constant"></a><span data-ttu-id="d8c90-103">常量</span><span class="sxs-lookup"><span data-stu-id="d8c90-103">Constant</span></span>

<span data-ttu-id="d8c90-104">**常量**元素标识限制中的常量值。</span><span class="sxs-lookup"><span data-stu-id="d8c90-104">The **Constant** element identifies a constant value in a restriction.</span></span> 
  
```xml
<Constant Value="" />
```

 <span data-ttu-id="d8c90-105">**ConstantValueType**</span><span class="sxs-lookup"><span data-stu-id="d8c90-105">**ConstantValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8c90-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d8c90-106">Attributes and elements</span></span>

<span data-ttu-id="d8c90-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d8c90-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8c90-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d8c90-108">Attributes</span></span>

|<span data-ttu-id="d8c90-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="d8c90-109">**Attribute**</span></span>|<span data-ttu-id="d8c90-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="d8c90-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8c90-111">**值**</span><span class="sxs-lookup"><span data-stu-id="d8c90-111">**Value**</span></span> <br/> |<span data-ttu-id="d8c90-112">指定要在限制中比较的值。</span><span class="sxs-lookup"><span data-stu-id="d8c90-112">Specifies the value to compare in the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d8c90-113">子元素</span><span class="sxs-lookup"><span data-stu-id="d8c90-113">Child elements</span></span>

<span data-ttu-id="d8c90-114">无。</span><span class="sxs-lookup"><span data-stu-id="d8c90-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d8c90-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d8c90-115">Parent elements</span></span>

|<span data-ttu-id="d8c90-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="d8c90-116">**Element**</span></span>|<span data-ttu-id="d8c90-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="d8c90-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8c90-118">Contains</span><span class="sxs-lookup"><span data-stu-id="d8c90-118">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="d8c90-119">表示一个搜索表达式，该表达式确定给定属性是否包含提供的常量字符串值。</span><span class="sxs-lookup"><span data-stu-id="d8c90-119">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="d8c90-120">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="d8c90-120">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="d8c90-121">表示与其他属性进行比较时要使用的属性或常数值。</span><span class="sxs-lookup"><span data-stu-id="d8c90-121">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8c90-122">备注</span><span class="sxs-lookup"><span data-stu-id="d8c90-122">Remarks</span></span>

<span data-ttu-id="d8c90-123">**Value**属性中的字符串值必须强制转换为您尝试进行比较的类型。</span><span class="sxs-lookup"><span data-stu-id="d8c90-123">The string value in the **Value** attribute must be coercible into the type you are trying to compare against.</span></span> <span data-ttu-id="d8c90-124">例如，如果要将日期/时间属性与常量值进行比较，则字符串值必须代表日期/时间。</span><span class="sxs-lookup"><span data-stu-id="d8c90-124">For example, if you are comparing a date/time property against a constant value, the string value must represent a date/time.</span></span> 
  
<span data-ttu-id="d8c90-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d8c90-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8c90-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="d8c90-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8c90-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="d8c90-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d8c90-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="d8c90-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d8c90-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="d8c90-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="d8c90-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="d8c90-130">Validation File</span></span>  <br/> |<span data-ttu-id="d8c90-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d8c90-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d8c90-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="d8c90-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d8c90-133">False</span><span class="sxs-lookup"><span data-stu-id="d8c90-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8c90-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d8c90-134">See also</span></span>



- [<span data-ttu-id="d8c90-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d8c90-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

