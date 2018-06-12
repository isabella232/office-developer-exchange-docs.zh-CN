---
title: GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e15dbfca-3b9d-463e-94ec-4f1b6115bee3
description: GetDiscoverySearchConfiguration 元素指定要检索的电子数据展示搜索配置的请求。
ms.openlocfilehash: 41a3cabb2822c4ee6a31aa7ff3074d62987edc92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754518"
---
# <a name="getdiscoverysearchconfiguration"></a><span data-ttu-id="6a711-103">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a711-103">GetDiscoverySearchConfiguration</span></span>

<span data-ttu-id="6a711-104">**GetDiscoverySearchConfiguration**元素指定要检索的电子数据展示搜索配置的请求。</span><span class="sxs-lookup"><span data-stu-id="6a711-104">The **GetDiscoverySearchConfiguration** element specifies a request to retrieve the eDiscovery search configuration.</span></span> 
  
```XML
<GetDiscoverySearchConfiguration>
    <SearchId/>
    <ExpandGroupMembership/>
</GetDiscoverySearchConfiguration>
```

 <span data-ttu-id="6a711-105">**GetDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="6a711-105">**GetDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a711-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6a711-106">Attributes and elements</span></span>

<span data-ttu-id="6a711-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6a711-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a711-108">属性</span><span class="sxs-lookup"><span data-stu-id="6a711-108">Attributes</span></span>

<span data-ttu-id="6a711-109">无。</span><span class="sxs-lookup"><span data-stu-id="6a711-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a711-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6a711-110">Child elements</span></span>

|<span data-ttu-id="6a711-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6a711-111">**Element**</span></span>|<span data-ttu-id="6a711-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6a711-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a711-113">SearchId</span><span class="sxs-lookup"><span data-stu-id="6a711-113">SearchId</span></span>](searchid.md) <br/> |<span data-ttu-id="6a711-114">指定搜索的标识符。</span><span class="sxs-lookup"><span data-stu-id="6a711-114">Specifies the identifier of the search.</span></span>  <br/> |
|[<span data-ttu-id="6a711-115">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="6a711-115">ExpandGroupMembership</span></span>](expandgroupmembership.md) <br/> |<span data-ttu-id="6a711-116">包含一个布尔值，该值指示是否展开**GetSearchableMailboxes**请求返回组的成员。</span><span class="sxs-lookup"><span data-stu-id="6a711-116">Contains a Boolean value that indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6a711-117">父元素</span><span class="sxs-lookup"><span data-stu-id="6a711-117">Parent elements</span></span>

<span data-ttu-id="6a711-118">无。</span><span class="sxs-lookup"><span data-stu-id="6a711-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a711-119">备注</span><span class="sxs-lookup"><span data-stu-id="6a711-119">Remarks</span></span>

<span data-ttu-id="6a711-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6a711-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6a711-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6a711-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a711-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="6a711-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a711-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="6a711-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6a711-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="6a711-124">Schema Name</span></span>  <br/> |<span data-ttu-id="6a711-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="6a711-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="6a711-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="6a711-126">Validation File</span></span>  <br/> |<span data-ttu-id="6a711-127">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6a711-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6a711-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="6a711-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6a711-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6a711-129">See also</span></span>



- [<span data-ttu-id="6a711-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6a711-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

