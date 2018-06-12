---
title: IsNotSupported
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNotSupported
api_type:
- schema
ms.assetid: 4db469ae-1515-47ea-9905-6aabf199febd
description: IsNotSupported 元素指示是否无法使用 Api 的托管的代码修改该规则。
ms.openlocfilehash: 2468d47dbfdcaf1a28ed1a4afb1e7ea60147d1dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826057"
---
# <a name="isnotsupported"></a><span data-ttu-id="85196-103">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="85196-103">IsNotSupported</span></span>

<span data-ttu-id="85196-104">**IsNotSupported**元素指示是否无法使用 Api 的托管的代码修改该规则。</span><span class="sxs-lookup"><span data-stu-id="85196-104">The **IsNotSupported** element indicates whether the rule cannot be modified by using the managed code APIs.</span></span> 
  
```XML
<IsNotSupported/>
```

 <span data-ttu-id="85196-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="85196-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85196-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="85196-106">Attributes and elements</span></span>

<span data-ttu-id="85196-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="85196-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85196-108">属性</span><span class="sxs-lookup"><span data-stu-id="85196-108">Attributes</span></span>

<span data-ttu-id="85196-109">无。</span><span class="sxs-lookup"><span data-stu-id="85196-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85196-110">子元素</span><span class="sxs-lookup"><span data-stu-id="85196-110">Child elements</span></span>

<span data-ttu-id="85196-111">无。</span><span class="sxs-lookup"><span data-stu-id="85196-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85196-112">父元素</span><span class="sxs-lookup"><span data-stu-id="85196-112">Parent elements</span></span>

|<span data-ttu-id="85196-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="85196-113">**Element**</span></span>|<span data-ttu-id="85196-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="85196-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85196-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="85196-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="85196-116">表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="85196-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="85196-117">文本值</span><span class="sxs-lookup"><span data-stu-id="85196-117">Text value</span></span>

<span data-ttu-id="85196-118">文本值为**true**指示规则不能使用托管的代码 Api 进行修改。</span><span class="sxs-lookup"><span data-stu-id="85196-118">A text value of **true** indicates that the rule cannot be modified by using the managed code APIs.</span></span> <span data-ttu-id="85196-119">如果值为**false**指示可以使用 Api 的托管的代码修改规则。</span><span class="sxs-lookup"><span data-stu-id="85196-119">A value of **false** indicates that the rule can be modified by using the managed code APIs.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85196-120">备注</span><span class="sxs-lookup"><span data-stu-id="85196-120">Remarks</span></span>

<span data-ttu-id="85196-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="85196-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85196-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="85196-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85196-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="85196-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="85196-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="85196-124">Schema Name</span></span>  <br/> |<span data-ttu-id="85196-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="85196-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="85196-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="85196-126">Validation File</span></span>  <br/> |<span data-ttu-id="85196-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="85196-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="85196-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="85196-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="85196-129">True</span><span class="sxs-lookup"><span data-stu-id="85196-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85196-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="85196-130">See also</span></span>



- [<span data-ttu-id="85196-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="85196-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

