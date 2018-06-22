---
title: DiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 085384f9-dca4-4534-82e2-dd782471d0da
description: DiscoverySearchConfiguration 元素指定的电子数据展示搜索的配置。
ms.openlocfilehash: 11bf90d8fe73bb0b308deb7ae51f1443488f87e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753913"
---
# <a name="discoverysearchconfiguration"></a><span data-ttu-id="4d8f3-103">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d8f3-103">DiscoverySearchConfiguration</span></span>

<span data-ttu-id="4d8f3-104">**DiscoverySearchConfiguration**元素指定的电子数据展示搜索的配置。</span><span class="sxs-lookup"><span data-stu-id="4d8f3-104">The **DiscoverySearchConfiguration** element specifies the configuration for eDiscovery search.</span></span> 
  
```XML
<DiscoverySearchConfiguration>
    <SearchId></SearchId>
    <SearchQuery></SearchQuery>
    <SearchableMailboxes></SearchableMailboxes>
</DiscoverySearchConfiguration>
```

 <span data-ttu-id="4d8f3-105">**DiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="4d8f3-105">**DiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d8f3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4d8f3-106">Attributes and elements</span></span>

<span data-ttu-id="4d8f3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4d8f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d8f3-108">属性</span><span class="sxs-lookup"><span data-stu-id="4d8f3-108">Attributes</span></span>

<span data-ttu-id="4d8f3-109">无。</span><span class="sxs-lookup"><span data-stu-id="4d8f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d8f3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4d8f3-110">Child elements</span></span>

|<span data-ttu-id="4d8f3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d8f3-111">**Element**</span></span>|<span data-ttu-id="4d8f3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d8f3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d8f3-113">SearchId</span><span class="sxs-lookup"><span data-stu-id="4d8f3-113">SearchId</span></span>](searchid.md) <br/> |<span data-ttu-id="4d8f3-114">指定搜索的标识符。</span><span class="sxs-lookup"><span data-stu-id="4d8f3-114">Specifies the identifier of the search.</span></span>  <br/> |
|[<span data-ttu-id="4d8f3-115">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="4d8f3-115">SearchQuery</span></span>](searchquery.md) <br/> |<span data-ttu-id="4d8f3-116">指定的电子数据展示搜索查询的名称。</span><span class="sxs-lookup"><span data-stu-id="4d8f3-116">Specifies the name of an eDiscovery search query.</span></span>  <br/> |
|[<span data-ttu-id="4d8f3-117">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="4d8f3-117">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="4d8f3-118">包含从**GetSearchableMailboxes**请求返回的邮箱的列表。</span><span class="sxs-lookup"><span data-stu-id="4d8f3-118">Contains a list of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4d8f3-119">父元素</span><span class="sxs-lookup"><span data-stu-id="4d8f3-119">Parent elements</span></span>

|<span data-ttu-id="4d8f3-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d8f3-120">**Element**</span></span>|<span data-ttu-id="4d8f3-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d8f3-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d8f3-122">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="4d8f3-122">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md) <br/> |<span data-ttu-id="4d8f3-123">指定**DiscoverySearchConfiguration**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="4d8f3-123">Specifies an array of **DiscoverySearchConfiguration** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d8f3-124">备注</span><span class="sxs-lookup"><span data-stu-id="4d8f3-124">Remarks</span></span>

<span data-ttu-id="4d8f3-125">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4d8f3-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4d8f3-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4d8f3-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d8f3-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="4d8f3-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d8f3-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="4d8f3-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4d8f3-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="4d8f3-129">Schema Name</span></span>  <br/> |<span data-ttu-id="4d8f3-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="4d8f3-130">Message schema</span></span>  <br/> |
|<span data-ttu-id="4d8f3-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="4d8f3-131">Validation File</span></span>  <br/> |<span data-ttu-id="4d8f3-132">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4d8f3-132">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4d8f3-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="4d8f3-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4d8f3-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d8f3-134">See also</span></span>

- [<span data-ttu-id="4d8f3-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4d8f3-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

