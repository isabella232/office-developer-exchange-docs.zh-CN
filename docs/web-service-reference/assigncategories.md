---
title: AssignCategories
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AssignCategories
api_type:
- schema
ms.assetid: f5c73fed-7b00-446d-8296-71a0c86e7fc6
description: AssignCategories 元素均表示在电子邮件标记的类别。
ms.openlocfilehash: 96c77306d649677c1be745e8cadc2886e4a84c8a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753267"
---
# <a name="assigncategories"></a><span data-ttu-id="cdaa7-103">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="cdaa7-103">AssignCategories</span></span>

<span data-ttu-id="cdaa7-104">**AssignCategories**元素均表示在电子邮件标记的类别。</span><span class="sxs-lookup"><span data-stu-id="cdaa7-104">The **AssignCategories** element represents the categories that are stamped on e-mail messages.</span></span> 
  
- [<span data-ttu-id="cdaa7-105">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="cdaa7-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
- [<span data-ttu-id="cdaa7-106">Actions</span><span class="sxs-lookup"><span data-stu-id="cdaa7-106">Actions</span></span>](actions.md)
  
```XML
<AssignCategories>
   <String/>
</AssignCategories>
```

 <span data-ttu-id="cdaa7-107">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="cdaa7-107">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cdaa7-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cdaa7-108">Attributes and elements</span></span>

<span data-ttu-id="cdaa7-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cdaa7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdaa7-110">属性</span><span class="sxs-lookup"><span data-stu-id="cdaa7-110">Attributes</span></span>

<span data-ttu-id="cdaa7-111">无。</span><span class="sxs-lookup"><span data-stu-id="cdaa7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cdaa7-112">子元素</span><span class="sxs-lookup"><span data-stu-id="cdaa7-112">Child elements</span></span>

|<span data-ttu-id="cdaa7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cdaa7-113">**Element**</span></span>|<span data-ttu-id="cdaa7-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cdaa7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdaa7-115">字符串</span><span class="sxs-lookup"><span data-stu-id="cdaa7-115">String</span></span>](string.md) <br/> |<span data-ttu-id="cdaa7-116">包含标识单个类别的字符串。</span><span class="sxs-lookup"><span data-stu-id="cdaa7-116">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cdaa7-117">父元素</span><span class="sxs-lookup"><span data-stu-id="cdaa7-117">Parent elements</span></span>

|<span data-ttu-id="cdaa7-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="cdaa7-118">**Element**</span></span>|<span data-ttu-id="cdaa7-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="cdaa7-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdaa7-120">操作</span><span class="sxs-lookup"><span data-stu-id="cdaa7-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="cdaa7-121">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="cdaa7-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cdaa7-122">文本值</span><span class="sxs-lookup"><span data-stu-id="cdaa7-122">Text value</span></span>

<span data-ttu-id="cdaa7-123">无。</span><span class="sxs-lookup"><span data-stu-id="cdaa7-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cdaa7-124">备注</span><span class="sxs-lookup"><span data-stu-id="cdaa7-124">Remarks</span></span>

<span data-ttu-id="cdaa7-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cdaa7-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cdaa7-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="cdaa7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdaa7-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="cdaa7-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cdaa7-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="cdaa7-128">Schema Name</span></span>  <br/> |<span data-ttu-id="cdaa7-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="cdaa7-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cdaa7-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="cdaa7-130">Validation File</span></span>  <br/> |<span data-ttu-id="cdaa7-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cdaa7-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cdaa7-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="cdaa7-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="cdaa7-133">True</span><span class="sxs-lookup"><span data-stu-id="cdaa7-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdaa7-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cdaa7-134">See also</span></span>

- [<span data-ttu-id="cdaa7-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cdaa7-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

