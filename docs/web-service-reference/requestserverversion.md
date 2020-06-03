---
title: RequestServerVersion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: RequestServerVersion 元素包含的版本信息用于标识针对请求的目标的架构版本。
ms.openlocfilehash: c4ae59a03c812d21153e4338734185d933d914ec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468318"
---
# <a name="requestserverversion"></a><span data-ttu-id="b0bc7-103">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="b0bc7-103">RequestServerVersion</span></span>

<span data-ttu-id="b0bc7-104">**RequestServerVersion**元素包含的版本信息用于标识针对请求的目标的架构版本。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-104">The **RequestServerVersion** element contains the versioning information that identifies the schema version to target for a request.</span></span> 
  
```XML
<RequestServerVersion Version=""/>
```

 <span data-ttu-id="b0bc7-105">**ExchangeVersionType**</span><span class="sxs-lookup"><span data-stu-id="b0bc7-105">**ExchangeVersionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0bc7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b0bc7-106">Attributes and elements</span></span>

<span data-ttu-id="b0bc7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0bc7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b0bc7-108">Attributes</span></span>

|<span data-ttu-id="b0bc7-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="b0bc7-109">**Attribute**</span></span>|<span data-ttu-id="b0bc7-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0bc7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0bc7-111">版本</span><span class="sxs-lookup"><span data-stu-id="b0bc7-111">Version</span></span>  <br/> |<span data-ttu-id="b0bc7-112">介绍了请求的目标版本。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-112">Describes the version to target for the request.</span></span> <span data-ttu-id="b0bc7-113">当目标服务器版本是从 Exchange Server 2010 开始的 Exchange 版本时，此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-113">This attribute is required when the target server version is a version of Exchange starting with Exchange Server 2010.</span></span>  <br/> |
   
#### <a name="version-attribute-values"></a><span data-ttu-id="b0bc7-114">版本属性值</span><span class="sxs-lookup"><span data-stu-id="b0bc7-114">Version attribute values</span></span>

|<span data-ttu-id="b0bc7-115">**值**</span><span class="sxs-lookup"><span data-stu-id="b0bc7-115">**Value**</span></span>|<span data-ttu-id="b0bc7-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0bc7-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0bc7-117">Exchange2007</span><span class="sxs-lookup"><span data-stu-id="b0bc7-117">Exchange2007</span></span>  <br/> |<span data-ttu-id="b0bc7-118">面向 Exchange 2007 的初始发布版本的架构文件。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-118">Target the schema files for the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="b0bc7-119">Exchange2007_SP1</span><span class="sxs-lookup"><span data-stu-id="b0bc7-119">Exchange2007_SP1</span></span>  <br/> |<span data-ttu-id="b0bc7-120">将 Exchange 2007 Service Pack 1 （SP1）、Exchange 2007 Service Pack 2 （SP2）和 Exchange 2007 Service Pack 3 （SP3）的架构文件作为目标。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-120">Target the schema files for Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2), and Exchange 2007 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="b0bc7-121">Exchange2010</span><span class="sxs-lookup"><span data-stu-id="b0bc7-121">Exchange2010</span></span>  <br/> |<span data-ttu-id="b0bc7-122">将 Exchange 2010 的架构文件作为目标。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-122">Target the schema files for Exchange 2010.</span></span>  <br/> |
|<span data-ttu-id="b0bc7-123">Exchange2010_SP1</span><span class="sxs-lookup"><span data-stu-id="b0bc7-123">Exchange2010_SP1</span></span>  <br/> |<span data-ttu-id="b0bc7-124">将 Exchange 2010 Service Pack 1 （SP1）的架构文件作为目标。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-124">Target the schema files for Exchange 2010 Service Pack 1 (SP1).</span></span>  <br/> |
|<span data-ttu-id="b0bc7-125">Exchange2010_SP2</span><span class="sxs-lookup"><span data-stu-id="b0bc7-125">Exchange2010_SP2</span></span>  <br/> |<span data-ttu-id="b0bc7-126">面向 Exchange 2010 Service Pack 2 （SP2）和 Exchange 2010 Service Pack 3 （SP3）的架构文件。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-126">Target the schema files for Exchange 2010 Service Pack 2 (SP2) and Exchange 2010 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="b0bc7-127">Exchange2013</span><span class="sxs-lookup"><span data-stu-id="b0bc7-127">Exchange2013</span></span>  <br/> |<span data-ttu-id="b0bc7-128">将 Exchange 2013 的架构文件作为目标。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-128">Target the schema files for Exchange 2013.</span></span>  <br/> |
|<span data-ttu-id="b0bc7-129">Exchange2013_SP1</span><span class="sxs-lookup"><span data-stu-id="b0bc7-129">Exchange2013_SP1</span></span>  <br/> |<span data-ttu-id="b0bc7-130">将 Exchange 2013 Service Pack 1 （SP1）的架构文件作为目标。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-130">Target the schema files for Exchange 2013 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b0bc7-131">子元素</span><span class="sxs-lookup"><span data-stu-id="b0bc7-131">Child elements</span></span>

<span data-ttu-id="b0bc7-132">无。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0bc7-133">父元素</span><span class="sxs-lookup"><span data-stu-id="b0bc7-133">Parent elements</span></span>

<span data-ttu-id="b0bc7-134">**RequestServerVersion**元素位于 SOAP 标头中。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-134">The **RequestServerVersion** element is located in the SOAP header.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b0bc7-135">说明</span><span class="sxs-lookup"><span data-stu-id="b0bc7-135">Remarks</span></span>

<span data-ttu-id="b0bc7-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b0bc7-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0bc7-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="b0bc7-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0bc7-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="b0bc7-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0bc7-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="b0bc7-139">Schema Name</span></span>  <br/> |<span data-ttu-id="b0bc7-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="b0bc7-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="b0bc7-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="b0bc7-141">Validation File</span></span>  <br/> |<span data-ttu-id="b0bc7-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b0bc7-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0bc7-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="b0bc7-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="b0bc7-144">False</span><span class="sxs-lookup"><span data-stu-id="b0bc7-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0bc7-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b0bc7-145">See also</span></span>



- [<span data-ttu-id="b0bc7-146">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b0bc7-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b0bc7-147">版本控制请求</span><span class="sxs-lookup"><span data-stu-id="b0bc7-147">Versioning Requests</span></span>](https://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

