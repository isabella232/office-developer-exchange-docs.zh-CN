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
description: DictionaryKey 元素指定 dictionary 属性的字典键。
ms.openlocfilehash: 8d9d897c86eb5048068936433c6c0d77917ff777
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462148"
---
# <a name="dictionarykey"></a><span data-ttu-id="41099-103">DictionaryKey</span><span class="sxs-lookup"><span data-stu-id="41099-103">DictionaryKey</span></span>

<span data-ttu-id="41099-104">**DictionaryKey**元素指定 dictionary 属性的字典键。</span><span class="sxs-lookup"><span data-stu-id="41099-104">The **DictionaryKey** element specifies the dictionary key for a dictionary property.</span></span> 
  
```xml
<DictionaryKey>
   <Type/>
   <Value/>
</DictionaryKey>
```

 <span data-ttu-id="41099-105">**UserConfigurationDictionaryObjectType**</span><span class="sxs-lookup"><span data-stu-id="41099-105">**UserConfigurationDictionaryObjectType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41099-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41099-106">Attributes and elements</span></span>

<span data-ttu-id="41099-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41099-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41099-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="41099-108">Attributes</span></span>

<span data-ttu-id="41099-109">无。</span><span class="sxs-lookup"><span data-stu-id="41099-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41099-110">子元素</span><span class="sxs-lookup"><span data-stu-id="41099-110">Child elements</span></span>

|<span data-ttu-id="41099-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="41099-111">**Element**</span></span>|<span data-ttu-id="41099-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="41099-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41099-113">类型（UserConfiguration）</span><span class="sxs-lookup"><span data-stu-id="41099-113">Type (UserConfiguration)</span></span>](type-userconfiguration.md) <br/> | <span data-ttu-id="41099-114">指定 dictionary 对象类型。</span><span class="sxs-lookup"><span data-stu-id="41099-114">Specifies a dictionary object type.</span></span><br/><br/><span data-ttu-id="41099-115">键入的值可以是下列字符串值之一：</span><span class="sxs-lookup"><span data-stu-id="41099-115">The type can be one of the following string values:</span></span><br/><br/><span data-ttu-id="41099-116">-DateTime</span><span class="sxs-lookup"><span data-stu-id="41099-116">-  DateTime</span></span>  <br/><span data-ttu-id="41099-117">-布尔值</span><span class="sxs-lookup"><span data-stu-id="41099-117">-  Boolean</span></span>  <br/><span data-ttu-id="41099-118">-Byte</span><span class="sxs-lookup"><span data-stu-id="41099-118">-  Byte</span></span>  <br/><span data-ttu-id="41099-119">-String</span><span class="sxs-lookup"><span data-stu-id="41099-119">-  String</span></span>  <br/><span data-ttu-id="41099-120">- Integer32</span><span class="sxs-lookup"><span data-stu-id="41099-120">-  Integer32</span></span>  <br/><span data-ttu-id="41099-121">- UnsignedInteger32</span><span class="sxs-lookup"><span data-stu-id="41099-121">-  UnsignedInteger32</span></span>  <br/><span data-ttu-id="41099-122">- Integer64</span><span class="sxs-lookup"><span data-stu-id="41099-122">-  Integer64</span></span>  <br/><span data-ttu-id="41099-123">- UnsignedInteger64</span><span class="sxs-lookup"><span data-stu-id="41099-123">-  UnsignedInteger64</span></span>  <br/><span data-ttu-id="41099-124">- StringArray</span><span class="sxs-lookup"><span data-stu-id="41099-124">-  StringArray</span></span>  <br/><span data-ttu-id="41099-125">- ByteArray</span><span class="sxs-lookup"><span data-stu-id="41099-125">-  ByteArray</span></span>  <br/> |
|[<span data-ttu-id="41099-126">Value （UserConfiguration）</span><span class="sxs-lookup"><span data-stu-id="41099-126">Value (UserConfiguration)</span></span>](value-userconfiguration.md) <br/> |<span data-ttu-id="41099-127">将 dictionary 对象值指定为字符串。</span><span class="sxs-lookup"><span data-stu-id="41099-127">Specifies the dictionary object value as a string.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="41099-128">父元素</span><span class="sxs-lookup"><span data-stu-id="41099-128">Parent elements</span></span>

|<span data-ttu-id="41099-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="41099-129">**Element**</span></span>|<span data-ttu-id="41099-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="41099-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41099-131">DictionaryEntry</span><span class="sxs-lookup"><span data-stu-id="41099-131">DictionaryEntry</span></span>](dictionaryentry.md) <br/> |<span data-ttu-id="41099-132">指定单个词典项属性的内容。</span><span class="sxs-lookup"><span data-stu-id="41099-132">Specifies the contents of a single dictionary entry property.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41099-133">文本值</span><span class="sxs-lookup"><span data-stu-id="41099-133">Text value</span></span>

<span data-ttu-id="41099-134">无。</span><span class="sxs-lookup"><span data-stu-id="41099-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41099-135">说明</span><span class="sxs-lookup"><span data-stu-id="41099-135">Remarks</span></span>

<span data-ttu-id="41099-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="41099-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41099-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="41099-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41099-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="41099-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="41099-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="41099-139">Schema Name</span></span>  <br/> |<span data-ttu-id="41099-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="41099-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="41099-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="41099-141">Validation File</span></span>  <br/> |<span data-ttu-id="41099-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="41099-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="41099-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="41099-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="41099-144">False</span><span class="sxs-lookup"><span data-stu-id="41099-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41099-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41099-145">See also</span></span>

- [<span data-ttu-id="41099-146">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="41099-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

