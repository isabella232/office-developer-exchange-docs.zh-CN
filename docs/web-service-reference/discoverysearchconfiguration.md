---
title: DiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 085384f9-dca4-4534-82e2-dd782471d0da
description: DiscoverySearchConfiguration 元素指定电子数据展示搜索的配置。
ms.openlocfilehash: 8819d951f35ccc215bdf0128d2a16b60bbf20f2a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529054"
---
# <a name="discoverysearchconfiguration"></a><span data-ttu-id="e1475-103">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1475-103">DiscoverySearchConfiguration</span></span>

<span data-ttu-id="e1475-104">**DiscoverySearchConfiguration**元素指定电子数据展示搜索的配置。</span><span class="sxs-lookup"><span data-stu-id="e1475-104">The **DiscoverySearchConfiguration** element specifies the configuration for eDiscovery search.</span></span> 
  
```XML
<DiscoverySearchConfiguration>
    <SearchId></SearchId>
    <SearchQuery></SearchQuery>
    <SearchableMailboxes></SearchableMailboxes>
</DiscoverySearchConfiguration>
```

 <span data-ttu-id="e1475-105">**DiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="e1475-105">**DiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e1475-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e1475-106">Attributes and elements</span></span>

<span data-ttu-id="e1475-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e1475-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1475-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e1475-108">Attributes</span></span>

<span data-ttu-id="e1475-109">无。</span><span class="sxs-lookup"><span data-stu-id="e1475-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e1475-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e1475-110">Child elements</span></span>

|<span data-ttu-id="e1475-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e1475-111">**Element**</span></span>|<span data-ttu-id="e1475-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e1475-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1475-113">SearchId</span><span class="sxs-lookup"><span data-stu-id="e1475-113">SearchId</span></span>](searchid.md) <br/> |<span data-ttu-id="e1475-114">指定搜索的标识符。</span><span class="sxs-lookup"><span data-stu-id="e1475-114">Specifies the identifier of the search.</span></span>  <br/> |
|[<span data-ttu-id="e1475-115">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="e1475-115">SearchQuery</span></span>](searchquery.md) <br/> |<span data-ttu-id="e1475-116">指定电子数据展示搜索查询的名称。</span><span class="sxs-lookup"><span data-stu-id="e1475-116">Specifies the name of an eDiscovery search query.</span></span>  <br/> |
|[<span data-ttu-id="e1475-117">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="e1475-117">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="e1475-118">包含从**GetSearchableMailboxes**请求返回的邮箱的列表。</span><span class="sxs-lookup"><span data-stu-id="e1475-118">Contains a list of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e1475-119">父元素</span><span class="sxs-lookup"><span data-stu-id="e1475-119">Parent elements</span></span>

|<span data-ttu-id="e1475-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="e1475-120">**Element**</span></span>|<span data-ttu-id="e1475-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="e1475-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1475-122">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="e1475-122">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md) <br/> |<span data-ttu-id="e1475-123">指定**DiscoverySearchConfiguration**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="e1475-123">Specifies an array of **DiscoverySearchConfiguration** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1475-124">备注</span><span class="sxs-lookup"><span data-stu-id="e1475-124">Remarks</span></span>

<span data-ttu-id="e1475-125">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e1475-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e1475-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e1475-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e1475-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="e1475-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1475-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="e1475-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e1475-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="e1475-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e1475-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="e1475-130">Message schema</span></span>  <br/> |
|<span data-ttu-id="e1475-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="e1475-131">Validation File</span></span>  <br/> |<span data-ttu-id="e1475-132">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="e1475-132">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e1475-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="e1475-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e1475-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e1475-134">See also</span></span>

- [<span data-ttu-id="e1475-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e1475-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

