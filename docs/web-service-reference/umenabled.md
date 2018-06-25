---
title: UmEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UmEnabled
api_type:
- schema
ms.assetid: 87382d9b-0c02-49ec-85dc-3f5918df3195
description: UmEnabled 元素指示是否为帐户启用统一消息。
ms.openlocfilehash: 8324e02136adc6704bc0badb77131e9671ee569f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838305"
---
# <a name="umenabled"></a><span data-ttu-id="50fa1-103">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="50fa1-103">UmEnabled</span></span>

<span data-ttu-id="50fa1-104">**UmEnabled**元素指示是否为帐户启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="50fa1-104">The **UmEnabled** element indicates whether Unified Messaging is enabled for an account.</span></span> 
  
```XML
<UmEnabled>true | false</UmEnabled>
```

 <span data-ttu-id="50fa1-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="50fa1-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50fa1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="50fa1-106">Attributes and elements</span></span>

<span data-ttu-id="50fa1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="50fa1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50fa1-108">属性</span><span class="sxs-lookup"><span data-stu-id="50fa1-108">Attributes</span></span>

<span data-ttu-id="50fa1-109">无。</span><span class="sxs-lookup"><span data-stu-id="50fa1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50fa1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="50fa1-110">Child elements</span></span>

<span data-ttu-id="50fa1-111">无。</span><span class="sxs-lookup"><span data-stu-id="50fa1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="50fa1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="50fa1-112">Parent elements</span></span>

|<span data-ttu-id="50fa1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="50fa1-113">**Element**</span></span>|<span data-ttu-id="50fa1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="50fa1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50fa1-115">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="50fa1-115">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="50fa1-116">包含服务统一消息服务的配置信息。</span><span class="sxs-lookup"><span data-stu-id="50fa1-116">Contains service configuration information for the Unified Messaging service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="50fa1-117">文本值</span><span class="sxs-lookup"><span data-stu-id="50fa1-117">Text value</span></span>

<span data-ttu-id="50fa1-118">**UmEnabled**元素的文本值为**true** ，如果帐户; 启用了统一消息否则，值为**false**。</span><span class="sxs-lookup"><span data-stu-id="50fa1-118">The text value of the **UmEnabled** element is **true** if Unified Messaging is enabled for the account; otherwise, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50fa1-119">注解</span><span class="sxs-lookup"><span data-stu-id="50fa1-119">Remarks</span></span>

<span data-ttu-id="50fa1-120">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="50fa1-120">This element is required.</span></span>
  
<span data-ttu-id="50fa1-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="50fa1-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50fa1-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="50fa1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50fa1-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="50fa1-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50fa1-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="50fa1-124">Schema Name</span></span>  <br/> |<span data-ttu-id="50fa1-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="50fa1-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="50fa1-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="50fa1-126">Validation File</span></span>  <br/> |<span data-ttu-id="50fa1-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="50fa1-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="50fa1-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="50fa1-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="50fa1-129">False</span><span class="sxs-lookup"><span data-stu-id="50fa1-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50fa1-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="50fa1-130">See also</span></span>



- [<span data-ttu-id="50fa1-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="50fa1-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

