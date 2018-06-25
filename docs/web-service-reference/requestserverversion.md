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
description: RequestServerVersion 元素包含标识目标的请求的架构版本的版本控制信息。
ms.openlocfilehash: 0092d90a5fc479363f6d774b793c7148ad29f21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827143"
---
# <a name="requestserverversion"></a><span data-ttu-id="eb9dd-103">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="eb9dd-103">RequestServerVersion</span></span>

<span data-ttu-id="eb9dd-104">**RequestServerVersion**元素包含标识目标的请求的架构版本的版本控制信息。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-104">The **RequestServerVersion** element contains the versioning information that identifies the schema version to target for a request.</span></span> 
  
```XML
<RequestServerVersion Version=""/>
```

 <span data-ttu-id="eb9dd-105">**ExchangeVersionType**</span><span class="sxs-lookup"><span data-stu-id="eb9dd-105">**ExchangeVersionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb9dd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eb9dd-106">Attributes and elements</span></span>

<span data-ttu-id="eb9dd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb9dd-108">属性</span><span class="sxs-lookup"><span data-stu-id="eb9dd-108">Attributes</span></span>

|<span data-ttu-id="eb9dd-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="eb9dd-109">**Attribute**</span></span>|<span data-ttu-id="eb9dd-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb9dd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb9dd-111">版本</span><span class="sxs-lookup"><span data-stu-id="eb9dd-111">Version</span></span>  <br/> |<span data-ttu-id="eb9dd-112">描述到请求的目标的版本。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-112">Describes the version to target for the request.</span></span> <span data-ttu-id="eb9dd-113">目标服务器版本的 Exchange Server 2010 开头的 Exchange 版本时，此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-113">This attribute is required when the target server version is a version of Exchange starting with Exchange Server 2010.</span></span>  <br/> |
   
#### <a name="version-attribute-values"></a><span data-ttu-id="eb9dd-114">版本属性值</span><span class="sxs-lookup"><span data-stu-id="eb9dd-114">Version attribute values</span></span>

|<span data-ttu-id="eb9dd-115">**值**</span><span class="sxs-lookup"><span data-stu-id="eb9dd-115">**Value**</span></span>|<span data-ttu-id="eb9dd-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb9dd-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb9dd-117">Exchange2007</span><span class="sxs-lookup"><span data-stu-id="eb9dd-117">Exchange2007</span></span>  <br/> |<span data-ttu-id="eb9dd-118">目标初始发行版 Exchange 2007 的架构文件。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-118">Target the schema files for the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="eb9dd-119">Exchange2007_SP1</span><span class="sxs-lookup"><span data-stu-id="eb9dd-119">Exchange2007_SP1</span></span>  <br/> |<span data-ttu-id="eb9dd-120">面向 Exchange 2007 Service Pack 1 (SP1)、 Exchange 2007 Service Pack 2 (SP2) 和 Exchange 2007 Service Pack 3 (SP3) 的架构文件。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-120">Target the schema files for Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2), and Exchange 2007 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="eb9dd-121">Exchange2010</span><span class="sxs-lookup"><span data-stu-id="eb9dd-121">Exchange2010</span></span>  <br/> |<span data-ttu-id="eb9dd-122">面向 Exchange 2010 的架构文件。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-122">Target the schema files for Exchange 2010.</span></span>  <br/> |
|<span data-ttu-id="eb9dd-123">Exchange2010_SP1</span><span class="sxs-lookup"><span data-stu-id="eb9dd-123">Exchange2010_SP1</span></span>  <br/> |<span data-ttu-id="eb9dd-124">面向 Exchange 2010 Service Pack 1 (SP1) 的架构文件。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-124">Target the schema files for Exchange 2010 Service Pack 1 (SP1).</span></span>  <br/> |
|<span data-ttu-id="eb9dd-125">Exchange2010_SP2</span><span class="sxs-lookup"><span data-stu-id="eb9dd-125">Exchange2010_SP2</span></span>  <br/> |<span data-ttu-id="eb9dd-126">面向 Exchange 2010 Service Pack 2 (SP2) 和 Exchange 2010 Service Pack 3 (SP3) 的架构文件。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-126">Target the schema files for Exchange 2010 Service Pack 2 (SP2) and Exchange 2010 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="eb9dd-127">Exchange2013</span><span class="sxs-lookup"><span data-stu-id="eb9dd-127">Exchange2013</span></span>  <br/> |<span data-ttu-id="eb9dd-128">面向 Exchange 2013 的架构文件。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-128">Target the schema files for Exchange 2013.</span></span>  <br/> |
|<span data-ttu-id="eb9dd-129">Exchange2013_SP1</span><span class="sxs-lookup"><span data-stu-id="eb9dd-129">Exchange2013_SP1</span></span>  <br/> |<span data-ttu-id="eb9dd-130">面向 Exchange 2013 Service Pack 1 (SP1) 的架构文件。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-130">Target the schema files for Exchange 2013 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eb9dd-131">子元素</span><span class="sxs-lookup"><span data-stu-id="eb9dd-131">Child elements</span></span>

<span data-ttu-id="eb9dd-132">无。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb9dd-133">父元素</span><span class="sxs-lookup"><span data-stu-id="eb9dd-133">Parent elements</span></span>

<span data-ttu-id="eb9dd-134">**RequestServerVersion**元素位于的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-134">The **RequestServerVersion** element is located in the SOAP header.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eb9dd-135">备注</span><span class="sxs-lookup"><span data-stu-id="eb9dd-135">Remarks</span></span>

<span data-ttu-id="eb9dd-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eb9dd-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb9dd-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="eb9dd-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb9dd-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="eb9dd-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb9dd-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="eb9dd-139">Schema Name</span></span>  <br/> |<span data-ttu-id="eb9dd-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="eb9dd-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="eb9dd-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="eb9dd-141">Validation File</span></span>  <br/> |<span data-ttu-id="eb9dd-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb9dd-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb9dd-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="eb9dd-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb9dd-144">False</span><span class="sxs-lookup"><span data-stu-id="eb9dd-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb9dd-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb9dd-145">See also</span></span>



- [<span data-ttu-id="eb9dd-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="eb9dd-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="eb9dd-147">版本控制请求</span><span class="sxs-lookup"><span data-stu-id="eb9dd-147">Versioning Requests</span></span>](http://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

