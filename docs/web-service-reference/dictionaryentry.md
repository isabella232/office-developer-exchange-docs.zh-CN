---
title: DictionaryEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DictionaryEntry
api_type:
- schema
ms.assetid: 531ea96a-d411-43e6-9fec-11fa2c959a30
description: DictionaryEntry 元素指定单个词典项属性的内容。
ms.openlocfilehash: 4c5d4c037f0c97b26d518d2f1386f71b31fa2d1f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455658"
---
# <a name="dictionaryentry"></a><span data-ttu-id="81dec-103">DictionaryEntry</span><span class="sxs-lookup"><span data-stu-id="81dec-103">DictionaryEntry</span></span>

<span data-ttu-id="81dec-104">**DictionaryEntry**元素指定单个词典项属性的内容。</span><span class="sxs-lookup"><span data-stu-id="81dec-104">The **DictionaryEntry** element specifies the contents of a single dictionary entry property.</span></span> 
  
```xml
<DictionaryEntry>
   <DictionaryKey/>
   <DictionaryValue/>
</DictionaryEntry>
```

 <span data-ttu-id="81dec-105">**UserConfigurationDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="81dec-105">**UserConfigurationDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81dec-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="81dec-106">Attributes and elements</span></span>

<span data-ttu-id="81dec-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="81dec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81dec-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="81dec-108">Attributes</span></span>

<span data-ttu-id="81dec-109">无。</span><span class="sxs-lookup"><span data-stu-id="81dec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81dec-110">子元素</span><span class="sxs-lookup"><span data-stu-id="81dec-110">Child elements</span></span>

|<span data-ttu-id="81dec-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="81dec-111">**Element**</span></span>|<span data-ttu-id="81dec-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="81dec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81dec-113">DictionaryKey</span><span class="sxs-lookup"><span data-stu-id="81dec-113">DictionaryKey</span></span>](dictionarykey.md) <br/> |<span data-ttu-id="81dec-114">指定 dictionary 属性的字典键。</span><span class="sxs-lookup"><span data-stu-id="81dec-114">Specifies the dictionary key for a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="81dec-115">DictionaryValue</span><span class="sxs-lookup"><span data-stu-id="81dec-115">DictionaryValue</span></span>](dictionaryvalue.md) <br/> |<span data-ttu-id="81dec-116">指定 dictionary 属性的字典值。</span><span class="sxs-lookup"><span data-stu-id="81dec-116">Specifies the dictionary value for a dictionary property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="81dec-117">父元素</span><span class="sxs-lookup"><span data-stu-id="81dec-117">Parent elements</span></span>

|<span data-ttu-id="81dec-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="81dec-118">**Element**</span></span>|<span data-ttu-id="81dec-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="81dec-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81dec-120">"词典"</span><span class="sxs-lookup"><span data-stu-id="81dec-120">[Dictionary](dictionary.md)</span></span> <br/> |<span data-ttu-id="81dec-121">为用户配置对象定义一组字典属性项。</span><span class="sxs-lookup"><span data-stu-id="81dec-121">Defines a set of dictionary property entries for a user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="81dec-122">文本值</span><span class="sxs-lookup"><span data-stu-id="81dec-122">Text value</span></span>

<span data-ttu-id="81dec-123">无。</span><span class="sxs-lookup"><span data-stu-id="81dec-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81dec-124">说明</span><span class="sxs-lookup"><span data-stu-id="81dec-124">Remarks</span></span>

<span data-ttu-id="81dec-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="81dec-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81dec-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="81dec-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81dec-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="81dec-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="81dec-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="81dec-128">Schema Name</span></span>  <br/> |<span data-ttu-id="81dec-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="81dec-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="81dec-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="81dec-130">Validation File</span></span>  <br/> |<span data-ttu-id="81dec-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="81dec-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="81dec-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="81dec-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="81dec-133">False</span><span class="sxs-lookup"><span data-stu-id="81dec-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81dec-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="81dec-134">See also</span></span>

- [<span data-ttu-id="81dec-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="81dec-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

