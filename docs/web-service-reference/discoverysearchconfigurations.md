---
title: DiscoverySearchConfigurations
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f04b14c9-384c-4016-b113-52a49e15e73b
description: DiscoverySearchConfigurations 元素指定 DiscoverySearchConfiguration 元素的数组。
ms.openlocfilehash: 6af4c8198f2ad73f8b39f9718e11b88aa8075c39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461378"
---
# <a name="discoverysearchconfigurations"></a><span data-ttu-id="74e18-103">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="74e18-103">DiscoverySearchConfigurations</span></span>

<span data-ttu-id="74e18-104">**DiscoverySearchConfigurations**元素指定**DiscoverySearchConfiguration**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="74e18-104">The **DiscoverySearchConfigurations** element specifies an array of **DiscoverySearchConfiguration** elements.</span></span> 
  
```XML
<DiscoverySearchConfigurations>
    <DiscoverySearchConfiguration></DiscoverySearchConfiguration>
</DiscoverySearchConfigurations>
```

 <span data-ttu-id="74e18-105">**ArrayOfDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="74e18-105">**ArrayOfDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="74e18-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="74e18-106">Attributes and elements</span></span>

<span data-ttu-id="74e18-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="74e18-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="74e18-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="74e18-108">Attributes</span></span>

<span data-ttu-id="74e18-109">无。</span><span class="sxs-lookup"><span data-stu-id="74e18-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="74e18-110">子元素</span><span class="sxs-lookup"><span data-stu-id="74e18-110">Child elements</span></span>

|<span data-ttu-id="74e18-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="74e18-111">**Element**</span></span>|<span data-ttu-id="74e18-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="74e18-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74e18-113">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="74e18-113">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md) <br/> |<span data-ttu-id="74e18-114">指定电子数据展示搜索的配置。</span><span class="sxs-lookup"><span data-stu-id="74e18-114">Specifies the configuration for eDiscovery search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="74e18-115">父元素</span><span class="sxs-lookup"><span data-stu-id="74e18-115">Parent elements</span></span>

|<span data-ttu-id="74e18-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="74e18-116">**Element**</span></span>|<span data-ttu-id="74e18-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="74e18-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74e18-118">GetDiscoverySearchConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="74e18-118">GetDiscoverySearchConfigurationResponseMessage</span></span>](getdiscoverysearchconfigurationresponsemessage.md) <br/> |<span data-ttu-id="74e18-119">指定**GetDiscoverySearchConfiguration**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="74e18-119">Specifies the response message for a **GetDiscoverySearchConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74e18-120">备注</span><span class="sxs-lookup"><span data-stu-id="74e18-120">Remarks</span></span>

<span data-ttu-id="74e18-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="74e18-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="74e18-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="74e18-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="74e18-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="74e18-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74e18-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="74e18-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="74e18-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="74e18-125">Schema Name</span></span>  <br/> |<span data-ttu-id="74e18-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="74e18-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="74e18-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="74e18-127">Validation File</span></span>  <br/> |<span data-ttu-id="74e18-128">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="74e18-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="74e18-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="74e18-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="74e18-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="74e18-130">See also</span></span>

- [<span data-ttu-id="74e18-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="74e18-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

