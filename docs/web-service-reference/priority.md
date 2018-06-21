---
title: 优先级
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Priority
api_type:
- schema
ms.assetid: e1adb8b9-e3d5-469a-b188-822733d2503e
description: 优先级元素指示是用来运行规则的顺序。
ms.openlocfilehash: 49e9bda063d8766ff49c8a2e9574c986bcfdbeb2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2018
ms.locfileid: "19826888"
---
# <a name="priority"></a><span data-ttu-id="f5a81-103">优先级</span><span class="sxs-lookup"><span data-stu-id="f5a81-103">Priority</span></span>

<span data-ttu-id="f5a81-104">**优先级**元素指示是用来运行规则的顺序。</span><span class="sxs-lookup"><span data-stu-id="f5a81-104">The **Priority** element indicates the order in which a rule is to be run.</span></span> 
  
```XML
<Priority/>
```

 <span data-ttu-id="f5a81-105">**int**</span><span class="sxs-lookup"><span data-stu-id="f5a81-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f5a81-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f5a81-106">Attributes and elements</span></span>

<span data-ttu-id="f5a81-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f5a81-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5a81-108">属性</span><span class="sxs-lookup"><span data-stu-id="f5a81-108">Attributes</span></span>

<span data-ttu-id="f5a81-109">无。</span><span class="sxs-lookup"><span data-stu-id="f5a81-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f5a81-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f5a81-110">Child elements</span></span>

<span data-ttu-id="f5a81-111">无。</span><span class="sxs-lookup"><span data-stu-id="f5a81-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f5a81-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f5a81-112">Parent elements</span></span>

|<span data-ttu-id="f5a81-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5a81-113">**Element**</span></span>|<span data-ttu-id="f5a81-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5a81-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5a81-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="f5a81-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="f5a81-116">表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="f5a81-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f5a81-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f5a81-117">Text value</span></span>

<span data-ttu-id="f5a81-118">**优先级**元素的文本值为整数类型的值，该值指示应在其中运行规则执行顺序。</span><span class="sxs-lookup"><span data-stu-id="f5a81-118">The text value for the **Priority** element is an integer that indicates the execution order in which a rule should be run.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f5a81-119">备注</span><span class="sxs-lookup"><span data-stu-id="f5a81-119">Remarks</span></span>

<span data-ttu-id="f5a81-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f5a81-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f5a81-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="f5a81-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5a81-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="f5a81-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f5a81-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="f5a81-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f5a81-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="f5a81-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f5a81-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="f5a81-125">Validation File</span></span>  <br/> |<span data-ttu-id="f5a81-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f5a81-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f5a81-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="f5a81-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f5a81-128">False</span><span class="sxs-lookup"><span data-stu-id="f5a81-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5a81-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5a81-129">See also</span></span>



- [<span data-ttu-id="f5a81-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f5a81-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

