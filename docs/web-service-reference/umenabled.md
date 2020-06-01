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
ms.openlocfilehash: 7ba7be69868cb439177702f74ff4a2f12875b7ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468353"
---
# <a name="umenabled"></a><span data-ttu-id="eb08a-103">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="eb08a-103">UmEnabled</span></span>

<span data-ttu-id="eb08a-104">**UmEnabled**元素指示是否为帐户启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="eb08a-104">The **UmEnabled** element indicates whether Unified Messaging is enabled for an account.</span></span> 
  
```XML
<UmEnabled>true | false</UmEnabled>
```

 <span data-ttu-id="eb08a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="eb08a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb08a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eb08a-106">Attributes and elements</span></span>

<span data-ttu-id="eb08a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eb08a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb08a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="eb08a-108">Attributes</span></span>

<span data-ttu-id="eb08a-109">无。</span><span class="sxs-lookup"><span data-stu-id="eb08a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb08a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="eb08a-110">Child elements</span></span>

<span data-ttu-id="eb08a-111">无。</span><span class="sxs-lookup"><span data-stu-id="eb08a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb08a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="eb08a-112">Parent elements</span></span>

|<span data-ttu-id="eb08a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="eb08a-113">**Element**</span></span>|<span data-ttu-id="eb08a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb08a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb08a-115">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb08a-115">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="eb08a-116">包含统一消息服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="eb08a-116">Contains service configuration information for the Unified Messaging service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eb08a-117">文本值</span><span class="sxs-lookup"><span data-stu-id="eb08a-117">Text value</span></span>

<span data-ttu-id="eb08a-118">如果为帐户启用了统一消息，则**UmEnabled**元素的文本值为**true** ; 否则为 false。否则，该值为**false**。</span><span class="sxs-lookup"><span data-stu-id="eb08a-118">The text value of the **UmEnabled** element is **true** if Unified Messaging is enabled for the account; otherwise, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb08a-119">备注</span><span class="sxs-lookup"><span data-stu-id="eb08a-119">Remarks</span></span>

<span data-ttu-id="eb08a-120">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="eb08a-120">This element is required.</span></span>
  
<span data-ttu-id="eb08a-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eb08a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb08a-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="eb08a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb08a-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="eb08a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb08a-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="eb08a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="eb08a-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="eb08a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="eb08a-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="eb08a-126">Validation File</span></span>  <br/> |<span data-ttu-id="eb08a-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb08a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb08a-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="eb08a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb08a-129">False</span><span class="sxs-lookup"><span data-stu-id="eb08a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb08a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb08a-130">See also</span></span>



- [<span data-ttu-id="eb08a-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="eb08a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

