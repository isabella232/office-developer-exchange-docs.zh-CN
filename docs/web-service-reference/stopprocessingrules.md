---
title: StopProcessingRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StopProcessingRules
api_type:
- schema
ms.assetid: 5b89a2cb-ab26-444d-b3dd-2b3858872d63
description: StopProcessingRules元素指示是否计算后续规则。
ms.openlocfilehash: 9f068fd6290a39bbab6e3c1e29066c4fefefc64b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467898"
---
# <a name="stopprocessingrules"></a><span data-ttu-id="142d5-103">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="142d5-103">StopProcessingRules</span></span>

<span data-ttu-id="142d5-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **StopProcessingRules**元素指示是否计算后续规则。</span><span class="sxs-lookup"><span data-stu-id="142d5-104">The **StopProcessingRules** element indicates whether subsequent rules are to be evaluated.</span></span> 
  
```XML
<StopProcessingRules>true | false</StopProcessingRules>
```

 <span data-ttu-id="142d5-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="142d5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="142d5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="142d5-106">Attributes and elements</span></span>

<span data-ttu-id="142d5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="142d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="142d5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="142d5-108">Attributes</span></span>

<span data-ttu-id="142d5-109">无。</span><span class="sxs-lookup"><span data-stu-id="142d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="142d5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="142d5-110">Child elements</span></span>

<span data-ttu-id="142d5-111">无。</span><span class="sxs-lookup"><span data-stu-id="142d5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="142d5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="142d5-112">Parent elements</span></span>

|<span data-ttu-id="142d5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="142d5-113">**Element**</span></span>|<span data-ttu-id="142d5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="142d5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="142d5-115">操作</span><span class="sxs-lookup"><span data-stu-id="142d5-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="142d5-116">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="142d5-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="142d5-117">文本值</span><span class="sxs-lookup"><span data-stu-id="142d5-117">Text value</span></span>

<span data-ttu-id="142d5-p101">文本值为 **true**表示不应处理后续规则。 **false**表示规则之后的规则，继续进行评估。</span><span class="sxs-lookup"><span data-stu-id="142d5-p101">A text value of **true** indicates that subsequent rules should not be processed. A value of **false** indicates that subsequent rules should continue to be evaluated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="142d5-120">说明</span><span class="sxs-lookup"><span data-stu-id="142d5-120">Remarks</span></span>

<span data-ttu-id="142d5-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="142d5-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="142d5-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="142d5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="142d5-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="142d5-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="142d5-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="142d5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="142d5-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="142d5-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="142d5-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="142d5-126">Validation File</span></span>  <br/> |<span data-ttu-id="142d5-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="142d5-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="142d5-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="142d5-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="142d5-129">True</span><span class="sxs-lookup"><span data-stu-id="142d5-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="142d5-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="142d5-130">See also</span></span>



- [<span data-ttu-id="142d5-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="142d5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

