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
description: DictionaryEntry 元素指定的单个字典条目属性的内容。
ms.openlocfilehash: 75d7dd1aa82a4cc6c363b9c787cfb15b4d15b656
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753863"
---
# <a name="dictionaryentry"></a><span data-ttu-id="06407-103">DictionaryEntry</span><span class="sxs-lookup"><span data-stu-id="06407-103">DictionaryEntry</span></span>

<span data-ttu-id="06407-104">**DictionaryEntry**元素指定的单个字典条目属性的内容。</span><span class="sxs-lookup"><span data-stu-id="06407-104">The **DictionaryEntry** element specifies the contents of a single dictionary entry property.</span></span> 
  
```xml
<DictionaryEntry>
   <DictionaryKey/>
   <DictionaryValue/>
</DictionaryEntry>
```

 <span data-ttu-id="06407-105">**UserConfigurationDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="06407-105">**UserConfigurationDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="06407-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="06407-106">Attributes and elements</span></span>

<span data-ttu-id="06407-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="06407-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06407-108">属性</span><span class="sxs-lookup"><span data-stu-id="06407-108">Attributes</span></span>

<span data-ttu-id="06407-109">无。</span><span class="sxs-lookup"><span data-stu-id="06407-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06407-110">子元素</span><span class="sxs-lookup"><span data-stu-id="06407-110">Child elements</span></span>

|<span data-ttu-id="06407-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="06407-111">**Element**</span></span>|<span data-ttu-id="06407-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="06407-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06407-113">DictionaryKey</span><span class="sxs-lookup"><span data-stu-id="06407-113">DictionaryKey</span></span>](dictionarykey.md) <br/> |<span data-ttu-id="06407-114">指定词典属性的词典键。</span><span class="sxs-lookup"><span data-stu-id="06407-114">Specifies the dictionary key for a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="06407-115">DictionaryValue</span><span class="sxs-lookup"><span data-stu-id="06407-115">DictionaryValue</span></span>](dictionaryvalue.md) <br/> |<span data-ttu-id="06407-116">指定字典词典属性的值。</span><span class="sxs-lookup"><span data-stu-id="06407-116">Specifies the dictionary value for a dictionary property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="06407-117">父元素</span><span class="sxs-lookup"><span data-stu-id="06407-117">Parent elements</span></span>

|<span data-ttu-id="06407-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="06407-118">**Element**</span></span>|<span data-ttu-id="06407-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="06407-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06407-120">"词典"</span><span class="sxs-lookup"><span data-stu-id="06407-120">[Dictionary](dictionary.md)</span></span> <br/> |<span data-ttu-id="06407-121">定义一组用户配置对象的词典属性条目。</span><span class="sxs-lookup"><span data-stu-id="06407-121">Defines a set of dictionary property entries for a user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="06407-122">文本值</span><span class="sxs-lookup"><span data-stu-id="06407-122">Text value</span></span>

<span data-ttu-id="06407-123">无。</span><span class="sxs-lookup"><span data-stu-id="06407-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06407-124">备注</span><span class="sxs-lookup"><span data-stu-id="06407-124">Remarks</span></span>

<span data-ttu-id="06407-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="06407-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06407-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="06407-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06407-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="06407-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06407-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="06407-128">Schema Name</span></span>  <br/> |<span data-ttu-id="06407-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="06407-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="06407-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="06407-130">Validation File</span></span>  <br/> |<span data-ttu-id="06407-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="06407-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="06407-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="06407-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="06407-133">False</span><span class="sxs-lookup"><span data-stu-id="06407-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06407-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="06407-134">See also</span></span>

- [<span data-ttu-id="06407-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="06407-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

