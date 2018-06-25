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
ms.openlocfilehash: 48799975f8c928bf291fcdcdb83f2ff8768af8b9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827593"
---
# <a name="stopprocessingrules"></a><span data-ttu-id="cba89-103">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="cba89-103">StopProcessingRules</span></span>

<span data-ttu-id="cba89-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **StopProcessingRules**元素指示是否计算后续规则。</span><span class="sxs-lookup"><span data-stu-id="cba89-104">The **StopProcessingRules** element indicates whether subsequent rules are to be evaluated.</span></span> 
  
```XML
<StopProcessingRules>true | false</StopProcessingRules>
```

 <span data-ttu-id="cba89-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cba89-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cba89-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cba89-106">Attributes and elements</span></span>

<span data-ttu-id="cba89-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cba89-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cba89-108">属性</span><span class="sxs-lookup"><span data-stu-id="cba89-108">Attributes</span></span>

<span data-ttu-id="cba89-109">无。</span><span class="sxs-lookup"><span data-stu-id="cba89-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cba89-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cba89-110">Child elements</span></span>

<span data-ttu-id="cba89-111">无。</span><span class="sxs-lookup"><span data-stu-id="cba89-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cba89-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cba89-112">Parent elements</span></span>

|<span data-ttu-id="cba89-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cba89-113">**Element**</span></span>|<span data-ttu-id="cba89-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cba89-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cba89-115">操作</span><span class="sxs-lookup"><span data-stu-id="cba89-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="cba89-116">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="cba89-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cba89-117">文本值</span><span class="sxs-lookup"><span data-stu-id="cba89-117">Text value</span></span>

<span data-ttu-id="cba89-p101">文本值为 **true**表示不应处理后续规则。 **false**表示规则之后的规则，继续进行评估。</span><span class="sxs-lookup"><span data-stu-id="cba89-p101">A text value of **true** indicates that subsequent rules should not be processed. A value of **false** indicates that subsequent rules should continue to be evaluated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cba89-120">备注</span><span class="sxs-lookup"><span data-stu-id="cba89-120">Remarks</span></span>

<span data-ttu-id="cba89-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cba89-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cba89-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="cba89-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cba89-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="cba89-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cba89-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="cba89-124">Schema Name</span></span>  <br/> |<span data-ttu-id="cba89-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="cba89-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cba89-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="cba89-126">Validation File</span></span>  <br/> |<span data-ttu-id="cba89-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cba89-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cba89-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="cba89-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="cba89-129">True</span><span class="sxs-lookup"><span data-stu-id="cba89-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cba89-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cba89-130">See also</span></span>



- [<span data-ttu-id="cba89-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cba89-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

