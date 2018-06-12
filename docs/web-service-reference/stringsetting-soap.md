---
title: StringSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bf7096d8-42d4-4bf5-bbdd-851af2754000
description: StringSetting 元素均表示的值是 string 类型的用户设置。
ms.openlocfilehash: af2c8ed243182e3491723be172ae162554250951
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827606"
---
# <a name="stringsetting-soap"></a><span data-ttu-id="9ca42-103">StringSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9ca42-103">StringSetting (SOAP)</span></span>

<span data-ttu-id="9ca42-104">**StringSetting**元素均表示的值是 string 类型的用户设置。</span><span class="sxs-lookup"><span data-stu-id="9ca42-104">The **StringSetting** element represents a user setting the value of which is of type string.</span></span> 
  
```XML
<StringSetting>
   <Name/>
   <Value/>
</StringSetting>
```

 <span data-ttu-id="9ca42-105">**StringSetting**</span><span class="sxs-lookup"><span data-stu-id="9ca42-105">**StringSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9ca42-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9ca42-106">Attributes and elements</span></span>

<span data-ttu-id="9ca42-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9ca42-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ca42-108">属性</span><span class="sxs-lookup"><span data-stu-id="9ca42-108">Attributes</span></span>

<span data-ttu-id="9ca42-109">无。</span><span class="sxs-lookup"><span data-stu-id="9ca42-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9ca42-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9ca42-110">Child elements</span></span>

|<span data-ttu-id="9ca42-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ca42-111">**Element**</span></span>|<span data-ttu-id="9ca42-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ca42-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ca42-113">名称 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9ca42-113">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="9ca42-114">代表用户设置名称。</span><span class="sxs-lookup"><span data-stu-id="9ca42-114">Represents a user setting name.</span></span>  <br/> |
|[<span data-ttu-id="9ca42-115">值 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9ca42-115">Value (SOAP)</span></span>](value-soap.md) <br/> |<span data-ttu-id="9ca42-116">代表用户设置值。</span><span class="sxs-lookup"><span data-stu-id="9ca42-116">Represents a user setting value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9ca42-117">父元素</span><span class="sxs-lookup"><span data-stu-id="9ca42-117">Parent elements</span></span>

<span data-ttu-id="9ca42-118">无。</span><span class="sxs-lookup"><span data-stu-id="9ca42-118">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9ca42-119">文本值</span><span class="sxs-lookup"><span data-stu-id="9ca42-119">Text value</span></span>

<span data-ttu-id="9ca42-120">无。</span><span class="sxs-lookup"><span data-stu-id="9ca42-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9ca42-121">备注</span><span class="sxs-lookup"><span data-stu-id="9ca42-121">Remarks</span></span>

<span data-ttu-id="9ca42-122">**StringSetting**类型扩展了**UserSetting**类型。</span><span class="sxs-lookup"><span data-stu-id="9ca42-122">The **StringSetting** type extends the **UserSetting** type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9ca42-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="9ca42-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ca42-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="9ca42-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9ca42-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="9ca42-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9ca42-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="9ca42-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9ca42-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="9ca42-127">Validation File</span></span>  <br/> |<span data-ttu-id="9ca42-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9ca42-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9ca42-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="9ca42-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9ca42-130">True</span><span class="sxs-lookup"><span data-stu-id="9ca42-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ca42-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9ca42-131">See also</span></span>



[<span data-ttu-id="9ca42-132">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9ca42-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="9ca42-133">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9ca42-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="9ca42-134">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9ca42-134">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)
