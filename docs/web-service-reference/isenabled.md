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
description: IsEnabled 元素指示是否启用规则。
ms.openlocfilehash: d0f0a77ec1ec952ac1cd9d9ad686ccfcb8f70c42
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826000"
---
# <a name="isenabled"></a><span data-ttu-id="25db3-103">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="25db3-103">IsEnabled</span></span>

<span data-ttu-id="25db3-104">**IsEnabled**元素指示是否启用规则。</span><span class="sxs-lookup"><span data-stu-id="25db3-104">The **IsEnabled** element indicates whether the rule is enabled.</span></span> 
  
```XML
<IsEnabled/>
```

 <span data-ttu-id="25db3-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="25db3-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25db3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="25db3-106">Attributes and elements</span></span>

<span data-ttu-id="25db3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="25db3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25db3-108">属性</span><span class="sxs-lookup"><span data-stu-id="25db3-108">Attributes</span></span>

<span data-ttu-id="25db3-109">无。</span><span class="sxs-lookup"><span data-stu-id="25db3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25db3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="25db3-110">Child elements</span></span>

<span data-ttu-id="25db3-111">无。</span><span class="sxs-lookup"><span data-stu-id="25db3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25db3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="25db3-112">Parent elements</span></span>

|<span data-ttu-id="25db3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="25db3-113">**Element**</span></span>|<span data-ttu-id="25db3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="25db3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25db3-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="25db3-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="25db3-116">表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="25db3-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25db3-117">文本值</span><span class="sxs-lookup"><span data-stu-id="25db3-117">Text value</span></span>

<span data-ttu-id="25db3-118">指示文本值为**true**的规则启用，并且可以执行。</span><span class="sxs-lookup"><span data-stu-id="25db3-118">A text value of **true** indicates that the rule is enabled and can be executed.</span></span> <span data-ttu-id="25db3-119">如果值为**false**指示无法执行规则。</span><span class="sxs-lookup"><span data-stu-id="25db3-119">A value of **false** indicates that the rule cannot be executed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="25db3-120">备注</span><span class="sxs-lookup"><span data-stu-id="25db3-120">Remarks</span></span>

<span data-ttu-id="25db3-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="25db3-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25db3-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="25db3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25db3-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="25db3-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="25db3-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="25db3-124">Schema Name</span></span>  <br/> |<span data-ttu-id="25db3-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="25db3-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="25db3-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="25db3-126">Validation File</span></span>  <br/> |<span data-ttu-id="25db3-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="25db3-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="25db3-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="25db3-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="25db3-129">True</span><span class="sxs-lookup"><span data-stu-id="25db3-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25db3-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="25db3-130">See also</span></span>



- [<span data-ttu-id="25db3-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="25db3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

