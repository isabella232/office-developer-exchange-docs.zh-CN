---
title: IsEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsEnabled
api_type:
- schema
ms.assetid: c7e3035e-a4ef-4c11-8cb0-214790a554ff
description: IsEnabled 元素指示是否已启用该规则。
ms.openlocfilehash: 7a150dc4a27cf4ff7da9825d1daae2b747088539
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455308"
---
# <a name="isenabled"></a><span data-ttu-id="d3888-103">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="d3888-103">IsEnabled</span></span>

<span data-ttu-id="d3888-104">**IsEnabled**元素指示是否已启用该规则。</span><span class="sxs-lookup"><span data-stu-id="d3888-104">The **IsEnabled** element indicates whether the rule is enabled.</span></span> 
  
```XML
<IsEnabled/>
```

 <span data-ttu-id="d3888-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d3888-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3888-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d3888-106">Attributes and elements</span></span>

<span data-ttu-id="d3888-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d3888-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3888-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d3888-108">Attributes</span></span>

<span data-ttu-id="d3888-109">无。</span><span class="sxs-lookup"><span data-stu-id="d3888-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3888-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d3888-110">Child elements</span></span>

<span data-ttu-id="d3888-111">无。</span><span class="sxs-lookup"><span data-stu-id="d3888-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d3888-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d3888-112">Parent elements</span></span>

|<span data-ttu-id="d3888-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d3888-113">**Element**</span></span>|<span data-ttu-id="d3888-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d3888-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3888-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="d3888-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="d3888-116">表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="d3888-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d3888-117">文本值</span><span class="sxs-lookup"><span data-stu-id="d3888-117">Text value</span></span>

<span data-ttu-id="d3888-118">如果文本值为**true** ，则表示已启用并可执行该规则。</span><span class="sxs-lookup"><span data-stu-id="d3888-118">A text value of **true** indicates that the rule is enabled and can be executed.</span></span> <span data-ttu-id="d3888-119">**如果值为 false** ，则表示无法执行该规则。</span><span class="sxs-lookup"><span data-stu-id="d3888-119">A value of **false** indicates that the rule cannot be executed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d3888-120">说明</span><span class="sxs-lookup"><span data-stu-id="d3888-120">Remarks</span></span>

<span data-ttu-id="d3888-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d3888-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3888-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="d3888-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3888-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="d3888-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d3888-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="d3888-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d3888-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="d3888-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d3888-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="d3888-126">Validation File</span></span>  <br/> |<span data-ttu-id="d3888-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d3888-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d3888-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="d3888-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3888-129">True</span><span class="sxs-lookup"><span data-stu-id="d3888-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3888-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d3888-130">See also</span></span>



- [<span data-ttu-id="d3888-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d3888-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

