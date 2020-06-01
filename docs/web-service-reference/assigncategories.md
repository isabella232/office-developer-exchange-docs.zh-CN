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
description: AssignCategories 元素表示在电子邮件上标记的类别。
ms.openlocfilehash: e2dad0e2ef46421ae92a0d2826d161e5e2af3b93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464740"
---
# <a name="assigncategories"></a><span data-ttu-id="e3341-103">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="e3341-103">AssignCategories</span></span>

<span data-ttu-id="e3341-104">**AssignCategories**元素表示在电子邮件上标记的类别。</span><span class="sxs-lookup"><span data-stu-id="e3341-104">The **AssignCategories** element represents the categories that are stamped on e-mail messages.</span></span> 
  
- [<span data-ttu-id="e3341-105">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="e3341-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
- [<span data-ttu-id="e3341-106">Actions</span><span class="sxs-lookup"><span data-stu-id="e3341-106">Actions</span></span>](actions.md)
  
```XML
<AssignCategories>
   <String/>
</AssignCategories>
```

 <span data-ttu-id="e3341-107">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="e3341-107">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3341-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e3341-108">Attributes and elements</span></span>

<span data-ttu-id="e3341-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e3341-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3341-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="e3341-110">Attributes</span></span>

<span data-ttu-id="e3341-111">无。</span><span class="sxs-lookup"><span data-stu-id="e3341-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3341-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e3341-112">Child elements</span></span>

|<span data-ttu-id="e3341-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e3341-113">**Element**</span></span>|<span data-ttu-id="e3341-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3341-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3341-115">字符串</span><span class="sxs-lookup"><span data-stu-id="e3341-115">String</span></span>](string.md) <br/> |<span data-ttu-id="e3341-116">包含用于标识单个类别的字符串。</span><span class="sxs-lookup"><span data-stu-id="e3341-116">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e3341-117">父元素</span><span class="sxs-lookup"><span data-stu-id="e3341-117">Parent elements</span></span>

|<span data-ttu-id="e3341-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="e3341-118">**Element**</span></span>|<span data-ttu-id="e3341-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3341-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3341-120">操作</span><span class="sxs-lookup"><span data-stu-id="e3341-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="e3341-121">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="e3341-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3341-122">文本值</span><span class="sxs-lookup"><span data-stu-id="e3341-122">Text value</span></span>

<span data-ttu-id="e3341-123">无。</span><span class="sxs-lookup"><span data-stu-id="e3341-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3341-124">说明</span><span class="sxs-lookup"><span data-stu-id="e3341-124">Remarks</span></span>

<span data-ttu-id="e3341-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e3341-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3341-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="e3341-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3341-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="e3341-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e3341-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="e3341-128">Schema Name</span></span>  <br/> |<span data-ttu-id="e3341-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="e3341-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e3341-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="e3341-130">Validation File</span></span>  <br/> |<span data-ttu-id="e3341-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e3341-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3341-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="e3341-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3341-133">True</span><span class="sxs-lookup"><span data-stu-id="e3341-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3341-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3341-134">See also</span></span>

- [<span data-ttu-id="e3341-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e3341-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

