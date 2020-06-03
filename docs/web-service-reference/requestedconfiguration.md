---
title: RequestedConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestedConfiguration
api_type:
- schema
ms.assetid: 24921387-f676-49e6-8d7a-ef3115024866
description: RequestedConfiguration 元素包含请求的服务配置。
ms.openlocfilehash: bbc503e6d6f7c56c785365924106bc2468965d0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457149"
---
# <a name="requestedconfiguration"></a><span data-ttu-id="84229-103">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="84229-103">RequestedConfiguration</span></span>

<span data-ttu-id="84229-104">**RequestedConfiguration**元素包含请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="84229-104">The **RequestedConfiguration** element contains the requested service configurations.</span></span> 
  
```XML
<RequestedConfiguration>
   <ConfigurationName/>
</RequestedConfiguration>
```

 <span data-ttu-id="84229-105">**ArrayOfServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="84229-105">**ArrayOfServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84229-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="84229-106">Attributes and elements</span></span>

<span data-ttu-id="84229-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="84229-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84229-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="84229-108">Attributes</span></span>

<span data-ttu-id="84229-109">无。</span><span class="sxs-lookup"><span data-stu-id="84229-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84229-110">子元素</span><span class="sxs-lookup"><span data-stu-id="84229-110">Child elements</span></span>

|<span data-ttu-id="84229-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="84229-111">**Element**</span></span>|<span data-ttu-id="84229-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="84229-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84229-113">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="84229-113">ConfigurationName</span></span>](configurationname.md) <br/> |<span data-ttu-id="84229-114">按名称指定请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="84229-114">Specifies the requested service configurations by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84229-115">父元素</span><span class="sxs-lookup"><span data-stu-id="84229-115">Parent elements</span></span>

|<span data-ttu-id="84229-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="84229-116">**Element**</span></span>|<span data-ttu-id="84229-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="84229-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84229-118">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="84229-118">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="84229-119">定义 GetServiceConfiguration 请求。</span><span class="sxs-lookup"><span data-stu-id="84229-119">Defines a GetServiceConfiguration request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="84229-120">文本值</span><span class="sxs-lookup"><span data-stu-id="84229-120">Text value</span></span>

<span data-ttu-id="84229-121">无。</span><span class="sxs-lookup"><span data-stu-id="84229-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84229-122">说明</span><span class="sxs-lookup"><span data-stu-id="84229-122">Remarks</span></span>

<span data-ttu-id="84229-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="84229-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84229-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="84229-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84229-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="84229-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="84229-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="84229-126">Schema Name</span></span>  <br/> |<span data-ttu-id="84229-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="84229-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="84229-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="84229-128">Validation File</span></span>  <br/> |<span data-ttu-id="84229-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="84229-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="84229-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="84229-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="84229-131">False</span><span class="sxs-lookup"><span data-stu-id="84229-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84229-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84229-132">See also</span></span>



- [<span data-ttu-id="84229-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="84229-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

