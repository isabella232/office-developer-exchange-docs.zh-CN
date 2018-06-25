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
ms.openlocfilehash: 1edc6394360250c9a9810fe614c975cb48eba3f0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827130"
---
# <a name="requestedconfiguration"></a><span data-ttu-id="57f07-103">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="57f07-103">RequestedConfiguration</span></span>

<span data-ttu-id="57f07-104">**RequestedConfiguration**元素包含请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="57f07-104">The **RequestedConfiguration** element contains the requested service configurations.</span></span> 
  
```XML
<RequestedConfiguration>
   <ConfigurationName/>
</RequestedConfiguration>
```

 <span data-ttu-id="57f07-105">**ArrayOfServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="57f07-105">**ArrayOfServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="57f07-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="57f07-106">Attributes and elements</span></span>

<span data-ttu-id="57f07-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="57f07-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57f07-108">属性</span><span class="sxs-lookup"><span data-stu-id="57f07-108">Attributes</span></span>

<span data-ttu-id="57f07-109">无。</span><span class="sxs-lookup"><span data-stu-id="57f07-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57f07-110">子元素</span><span class="sxs-lookup"><span data-stu-id="57f07-110">Child elements</span></span>

|<span data-ttu-id="57f07-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="57f07-111">**Element**</span></span>|<span data-ttu-id="57f07-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="57f07-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57f07-113">配置名</span><span class="sxs-lookup"><span data-stu-id="57f07-113">ConfigurationName</span></span>](configurationname.md) <br/> |<span data-ttu-id="57f07-114">按名称指定的请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="57f07-114">Specifies the requested service configurations by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="57f07-115">父元素</span><span class="sxs-lookup"><span data-stu-id="57f07-115">Parent elements</span></span>

|<span data-ttu-id="57f07-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="57f07-116">**Element**</span></span>|<span data-ttu-id="57f07-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="57f07-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57f07-118">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="57f07-118">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="57f07-119">定义 GetServiceConfiguration 请求。</span><span class="sxs-lookup"><span data-stu-id="57f07-119">Defines a GetServiceConfiguration request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="57f07-120">文本值</span><span class="sxs-lookup"><span data-stu-id="57f07-120">Text value</span></span>

<span data-ttu-id="57f07-121">无。</span><span class="sxs-lookup"><span data-stu-id="57f07-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57f07-122">备注</span><span class="sxs-lookup"><span data-stu-id="57f07-122">Remarks</span></span>

<span data-ttu-id="57f07-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="57f07-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57f07-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="57f07-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57f07-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="57f07-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="57f07-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="57f07-126">Schema Name</span></span>  <br/> |<span data-ttu-id="57f07-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="57f07-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="57f07-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="57f07-128">Validation File</span></span>  <br/> |<span data-ttu-id="57f07-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="57f07-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="57f07-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="57f07-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="57f07-131">False</span><span class="sxs-lookup"><span data-stu-id="57f07-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57f07-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="57f07-132">See also</span></span>



- [<span data-ttu-id="57f07-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="57f07-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

