---
title: Dictionary
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Dictionary
api_type:
- schema
ms.assetid: 8309e468-115b-4d6e-b33c-c4719dcecc4c
description: Dictionary 元素为用户配置对象定义一组字典属性项。
ms.openlocfilehash: 8e5267717aab2317b2bc1581a775ead81025a08a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455665"
---
# <a name="dictionary"></a><span data-ttu-id="67120-103">Dictionary</span><span class="sxs-lookup"><span data-stu-id="67120-103">Dictionary</span></span>

<span data-ttu-id="67120-104">**Dictionary**元素为用户配置对象定义一组字典属性项。</span><span class="sxs-lookup"><span data-stu-id="67120-104">The **Dictionary** element defines a set of dictionary property entries for a user configuration object.</span></span> 
  
```xml
<Dictionary>
   <DictionaryEntry/>
</Dictionary>
```

 <span data-ttu-id="67120-105">**UserConfigurationDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="67120-105">**UserConfigurationDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67120-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="67120-106">Attributes and elements</span></span>

<span data-ttu-id="67120-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="67120-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67120-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="67120-108">Attributes</span></span>

<span data-ttu-id="67120-109">无。</span><span class="sxs-lookup"><span data-stu-id="67120-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67120-110">子元素</span><span class="sxs-lookup"><span data-stu-id="67120-110">Child elements</span></span>

|<span data-ttu-id="67120-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="67120-111">**Element**</span></span>|<span data-ttu-id="67120-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="67120-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67120-113">DictionaryEntry</span><span class="sxs-lookup"><span data-stu-id="67120-113">DictionaryEntry</span></span>](dictionaryentry.md) <br/> |<span data-ttu-id="67120-114">指定单个词典项属性的内容。</span><span class="sxs-lookup"><span data-stu-id="67120-114">Specifies the contents of a single dictionary entry property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67120-115">父元素</span><span class="sxs-lookup"><span data-stu-id="67120-115">Parent elements</span></span>

|<span data-ttu-id="67120-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="67120-116">**Element**</span></span>|<span data-ttu-id="67120-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="67120-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67120-118">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="67120-118">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="67120-119">定义单个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="67120-119">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="67120-120">文本值</span><span class="sxs-lookup"><span data-stu-id="67120-120">Text value</span></span>

<span data-ttu-id="67120-121">无。</span><span class="sxs-lookup"><span data-stu-id="67120-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67120-122">说明</span><span class="sxs-lookup"><span data-stu-id="67120-122">Remarks</span></span>

<span data-ttu-id="67120-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="67120-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67120-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="67120-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67120-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="67120-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="67120-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="67120-126">Schema Name</span></span>  <br/> |<span data-ttu-id="67120-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="67120-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="67120-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="67120-128">Validation File</span></span>  <br/> |<span data-ttu-id="67120-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="67120-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="67120-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="67120-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="67120-131">False</span><span class="sxs-lookup"><span data-stu-id="67120-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67120-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67120-132">See also</span></span>

- [<span data-ttu-id="67120-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="67120-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

