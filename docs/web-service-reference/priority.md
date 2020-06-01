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
description: Priority 元素指示规则的运行顺序。
ms.openlocfilehash: a5a894bba583618dd04430fc89f125c8920b0202
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462400"
---
# <a name="priority"></a><span data-ttu-id="e7168-103">优先级</span><span class="sxs-lookup"><span data-stu-id="e7168-103">Priority</span></span>

<span data-ttu-id="e7168-104">**Priority**元素指示规则的运行顺序。</span><span class="sxs-lookup"><span data-stu-id="e7168-104">The **Priority** element indicates the order in which a rule is to be run.</span></span> 
  
```XML
<Priority/>
```

 <span data-ttu-id="e7168-105">**int**</span><span class="sxs-lookup"><span data-stu-id="e7168-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7168-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e7168-106">Attributes and elements</span></span>

<span data-ttu-id="e7168-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e7168-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7168-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e7168-108">Attributes</span></span>

<span data-ttu-id="e7168-109">无。</span><span class="sxs-lookup"><span data-stu-id="e7168-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7168-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e7168-110">Child elements</span></span>

<span data-ttu-id="e7168-111">无。</span><span class="sxs-lookup"><span data-stu-id="e7168-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e7168-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e7168-112">Parent elements</span></span>

|<span data-ttu-id="e7168-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e7168-113">**Element**</span></span>|<span data-ttu-id="e7168-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e7168-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7168-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="e7168-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="e7168-116">表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="e7168-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e7168-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e7168-117">Text value</span></span>

<span data-ttu-id="e7168-118">**Priority**元素的文本值是一个整数，指示应在其中运行规则的执行顺序。</span><span class="sxs-lookup"><span data-stu-id="e7168-118">The text value for the **Priority** element is an integer that indicates the execution order in which a rule should be run.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e7168-119">说明</span><span class="sxs-lookup"><span data-stu-id="e7168-119">Remarks</span></span>

<span data-ttu-id="e7168-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e7168-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7168-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="e7168-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7168-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="e7168-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e7168-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="e7168-123">Schema Name</span></span>  <br/> |<span data-ttu-id="e7168-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="e7168-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e7168-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="e7168-125">Validation File</span></span>  <br/> |<span data-ttu-id="e7168-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e7168-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e7168-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="e7168-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="e7168-128">False</span><span class="sxs-lookup"><span data-stu-id="e7168-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7168-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7168-129">See also</span></span>



- [<span data-ttu-id="e7168-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e7168-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

