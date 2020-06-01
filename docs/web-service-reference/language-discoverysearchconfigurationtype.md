---
title: 语言（DiscoverySearchConfigurationType）
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: Language （DiscoverySearchConfigurationType）元素标识要用于特定于区域的日期范围格式的区域性。 它还指定在搜索查询中使用的语言。
ms.openlocfilehash: 3cf85525147bec5d6dfc6fe2b2af5916d42c44be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463284"
---
# <a name="language-discoverysearchconfigurationtype"></a><span data-ttu-id="00027-104">语言（DiscoverySearchConfigurationType）</span><span class="sxs-lookup"><span data-stu-id="00027-104">Language (DiscoverySearchConfigurationType)</span></span>

<span data-ttu-id="00027-105">**Language （DiscoverySearchConfigurationType）** 元素标识要用于特定于区域的日期范围格式的区域性。</span><span class="sxs-lookup"><span data-stu-id="00027-105">The **Language (DiscoverySearchConfigurationType)** element identifies the culture to be used for the culture-specific format of date ranges.</span></span> <span data-ttu-id="00027-106">它还指定在搜索查询中使用的语言。</span><span class="sxs-lookup"><span data-stu-id="00027-106">It also specifies the language used in a search query.</span></span> 
  
```XML
<Language />
```

 <span data-ttu-id="00027-107">**string**</span><span class="sxs-lookup"><span data-stu-id="00027-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="00027-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="00027-108">Attributes and elements</span></span>

<span data-ttu-id="00027-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="00027-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00027-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="00027-110">Attributes</span></span>

<span data-ttu-id="00027-111">无。</span><span class="sxs-lookup"><span data-stu-id="00027-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="00027-112">子元素</span><span class="sxs-lookup"><span data-stu-id="00027-112">Child elements</span></span>

<span data-ttu-id="00027-113">无。</span><span class="sxs-lookup"><span data-stu-id="00027-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="00027-114">父元素</span><span class="sxs-lookup"><span data-stu-id="00027-114">Parent elements</span></span>

[<span data-ttu-id="00027-115">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="00027-115">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
  
## <a name="text-value"></a><span data-ttu-id="00027-116">文本值</span><span class="sxs-lookup"><span data-stu-id="00027-116">Text value</span></span>

<span data-ttu-id="00027-117">**Language （DiscoverySearchConfigurationType）** 元素的文本值是一种区域性或语言。</span><span class="sxs-lookup"><span data-stu-id="00027-117">The text value of the **Language (DiscoverySearchConfigurationType)** element is a culture or language.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="00027-118">备注</span><span class="sxs-lookup"><span data-stu-id="00027-118">Remarks</span></span>

<span data-ttu-id="00027-119">此元素指定在[SearchMailboxes 操作](searchmailboxes-operation.md)或[SetHoldOnMailboxes 操作](setholdonmailboxes-operation.md)中指定的日期范围的格式。</span><span class="sxs-lookup"><span data-stu-id="00027-119">This element specifies the format of date ranges specified in the [SearchMailboxes operation](searchmailboxes-operation.md) or the [SetHoldOnMailboxes operation](setholdonmailboxes-operation.md).</span></span>
  
<span data-ttu-id="00027-120">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="00027-120">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="00027-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="00027-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00027-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="00027-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00027-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="00027-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="00027-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="00027-124">Schema Name</span></span>  <br/> |<span data-ttu-id="00027-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="00027-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="00027-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="00027-126">Validation File</span></span>  <br/> |<span data-ttu-id="00027-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="00027-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="00027-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="00027-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="00027-129">True</span><span class="sxs-lookup"><span data-stu-id="00027-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00027-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="00027-130">See also</span></span>



[<span data-ttu-id="00027-131">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="00027-131">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)


- [<span data-ttu-id="00027-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="00027-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

