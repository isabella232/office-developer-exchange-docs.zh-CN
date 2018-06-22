---
title: DictionaryKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DictionaryKey
api_type:
- schema
ms.assetid: f331c8ac-f1c7-4248-a570-97701969d5bf
description: DictionaryKey 元素指定的词典属性的词典键。
ms.openlocfilehash: 7e706f16fe155278ea56f303ffbb5971c1779879
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753865"
---
# <a name="dictionarykey"></a><span data-ttu-id="6a0a2-103">DictionaryKey</span><span class="sxs-lookup"><span data-stu-id="6a0a2-103">DictionaryKey</span></span>

<span data-ttu-id="6a0a2-104">**DictionaryKey**元素指定的词典属性的词典键。</span><span class="sxs-lookup"><span data-stu-id="6a0a2-104">The **DictionaryKey** element specifies the dictionary key for a dictionary property.</span></span> 
  
```xml
<DictionaryKey>
   <Type/>
   <Value/>
</DictionaryKey>
```

 <span data-ttu-id="6a0a2-105">**UserConfigurationDictionaryObjectType**</span><span class="sxs-lookup"><span data-stu-id="6a0a2-105">**UserConfigurationDictionaryObjectType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a0a2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6a0a2-106">Attributes and elements</span></span>

<span data-ttu-id="6a0a2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6a0a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a0a2-108">属性</span><span class="sxs-lookup"><span data-stu-id="6a0a2-108">Attributes</span></span>

<span data-ttu-id="6a0a2-109">无。</span><span class="sxs-lookup"><span data-stu-id="6a0a2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a0a2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6a0a2-110">Child elements</span></span>

|<span data-ttu-id="6a0a2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6a0a2-111">**Element**</span></span>|<span data-ttu-id="6a0a2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6a0a2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a0a2-113">类型 (UserConfiguration)</span><span class="sxs-lookup"><span data-stu-id="6a0a2-113">Type (UserConfiguration)</span></span>](type-userconfiguration.md) <br/> | <span data-ttu-id="6a0a2-114">指定词典对象类型。</span><span class="sxs-lookup"><span data-stu-id="6a0a2-114">Specifies a dictionary object type.</span></span><br/><br/><span data-ttu-id="6a0a2-115">键入可以是下列字符串值之一：</span><span class="sxs-lookup"><span data-stu-id="6a0a2-115">The type can be one of the following string values:</span></span><br/><br/><span data-ttu-id="6a0a2-116">-日期时间</span><span class="sxs-lookup"><span data-stu-id="6a0a2-116">-  DateTime</span></span>  <br/><span data-ttu-id="6a0a2-117">布尔</span><span class="sxs-lookup"><span data-stu-id="6a0a2-117">-  Boolean</span></span>  <br/><span data-ttu-id="6a0a2-118">字节</span><span class="sxs-lookup"><span data-stu-id="6a0a2-118">-  Byte</span></span>  <br/><span data-ttu-id="6a0a2-119">字符串</span><span class="sxs-lookup"><span data-stu-id="6a0a2-119">-  String</span></span>  <br/><span data-ttu-id="6a0a2-120">-Integer32</span><span class="sxs-lookup"><span data-stu-id="6a0a2-120">-  Integer32</span></span>  <br/><span data-ttu-id="6a0a2-121">-UnsignedInteger32</span><span class="sxs-lookup"><span data-stu-id="6a0a2-121">-  UnsignedInteger32</span></span>  <br/><span data-ttu-id="6a0a2-122">-Integer64</span><span class="sxs-lookup"><span data-stu-id="6a0a2-122">-  Integer64</span></span>  <br/><span data-ttu-id="6a0a2-123">-UnsignedInteger64</span><span class="sxs-lookup"><span data-stu-id="6a0a2-123">-  UnsignedInteger64</span></span>  <br/><span data-ttu-id="6a0a2-124">-StringArray</span><span class="sxs-lookup"><span data-stu-id="6a0a2-124">-  StringArray</span></span>  <br/><span data-ttu-id="6a0a2-125">-ByteArray</span><span class="sxs-lookup"><span data-stu-id="6a0a2-125">-  ByteArray</span></span>  <br/> |
|[<span data-ttu-id="6a0a2-126">值 (UserConfiguration)</span><span class="sxs-lookup"><span data-stu-id="6a0a2-126">Value (UserConfiguration)</span></span>](value-userconfiguration.md) <br/> |<span data-ttu-id="6a0a2-127">作为字符串指定的词典对象值。</span><span class="sxs-lookup"><span data-stu-id="6a0a2-127">Specifies the dictionary object value as a string.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6a0a2-128">父元素</span><span class="sxs-lookup"><span data-stu-id="6a0a2-128">Parent elements</span></span>

|<span data-ttu-id="6a0a2-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="6a0a2-129">**Element**</span></span>|<span data-ttu-id="6a0a2-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="6a0a2-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a0a2-131">DictionaryEntry</span><span class="sxs-lookup"><span data-stu-id="6a0a2-131">DictionaryEntry</span></span>](dictionaryentry.md) <br/> |<span data-ttu-id="6a0a2-132">指定单个字典条目属性的内容。</span><span class="sxs-lookup"><span data-stu-id="6a0a2-132">Specifies the contents of a single dictionary entry property.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6a0a2-133">文本值</span><span class="sxs-lookup"><span data-stu-id="6a0a2-133">Text value</span></span>

<span data-ttu-id="6a0a2-134">无。</span><span class="sxs-lookup"><span data-stu-id="6a0a2-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a0a2-135">备注</span><span class="sxs-lookup"><span data-stu-id="6a0a2-135">Remarks</span></span>

<span data-ttu-id="6a0a2-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6a0a2-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a0a2-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="6a0a2-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a0a2-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="6a0a2-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6a0a2-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="6a0a2-139">Schema Name</span></span>  <br/> |<span data-ttu-id="6a0a2-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="6a0a2-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="6a0a2-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="6a0a2-141">Validation File</span></span>  <br/> |<span data-ttu-id="6a0a2-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6a0a2-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6a0a2-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="6a0a2-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="6a0a2-144">False</span><span class="sxs-lookup"><span data-stu-id="6a0a2-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a0a2-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6a0a2-145">See also</span></span>

- [<span data-ttu-id="6a0a2-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6a0a2-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

