---
title: GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e15dbfca-3b9d-463e-94ec-4f1b6115bee3
description: GetDiscoverySearchConfiguration 元素指定检索电子数据展示搜索配置的请求。
ms.openlocfilehash: 821c5e1429c160e326f6d99df3ff4fcc831b83d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461000"
---
# <a name="getdiscoverysearchconfiguration"></a><span data-ttu-id="70c8e-103">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="70c8e-103">GetDiscoverySearchConfiguration</span></span>

<span data-ttu-id="70c8e-104">**GetDiscoverySearchConfiguration**元素指定检索电子数据展示搜索配置的请求。</span><span class="sxs-lookup"><span data-stu-id="70c8e-104">The **GetDiscoverySearchConfiguration** element specifies a request to retrieve the eDiscovery search configuration.</span></span> 
  
```XML
<GetDiscoverySearchConfiguration>
    <SearchId/>
    <ExpandGroupMembership/>
</GetDiscoverySearchConfiguration>
```

 <span data-ttu-id="70c8e-105">**GetDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="70c8e-105">**GetDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70c8e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="70c8e-106">Attributes and elements</span></span>

<span data-ttu-id="70c8e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="70c8e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70c8e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="70c8e-108">Attributes</span></span>

<span data-ttu-id="70c8e-109">无。</span><span class="sxs-lookup"><span data-stu-id="70c8e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70c8e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="70c8e-110">Child elements</span></span>

|<span data-ttu-id="70c8e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="70c8e-111">**Element**</span></span>|<span data-ttu-id="70c8e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="70c8e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70c8e-113">SearchId</span><span class="sxs-lookup"><span data-stu-id="70c8e-113">SearchId</span></span>](searchid.md) <br/> |<span data-ttu-id="70c8e-114">指定搜索的标识符。</span><span class="sxs-lookup"><span data-stu-id="70c8e-114">Specifies the identifier of the search.</span></span>  <br/> |
|[<span data-ttu-id="70c8e-115">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="70c8e-115">ExpandGroupMembership</span></span>](expandgroupmembership.md) <br/> |<span data-ttu-id="70c8e-116">包含一个布尔值，该值指示是否扩展从**GetSearchableMailboxes**请求返回的组的成员资格。</span><span class="sxs-lookup"><span data-stu-id="70c8e-116">Contains a Boolean value that indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="70c8e-117">父元素</span><span class="sxs-lookup"><span data-stu-id="70c8e-117">Parent elements</span></span>

<span data-ttu-id="70c8e-118">无。</span><span class="sxs-lookup"><span data-stu-id="70c8e-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70c8e-119">说明</span><span class="sxs-lookup"><span data-stu-id="70c8e-119">Remarks</span></span>

<span data-ttu-id="70c8e-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="70c8e-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="70c8e-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="70c8e-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70c8e-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="70c8e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70c8e-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="70c8e-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="70c8e-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="70c8e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="70c8e-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="70c8e-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="70c8e-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="70c8e-126">Validation File</span></span>  <br/> |<span data-ttu-id="70c8e-127">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="70c8e-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="70c8e-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="70c8e-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="70c8e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70c8e-129">See also</span></span>



- [<span data-ttu-id="70c8e-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="70c8e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

