---
title: MarkImportance
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MarkImportance
api_type:
- schema
ms.assetid: 32b8b08f-65e9-4764-b40a-63245551f4a3
description: MarkImportance 元素指定要在邮件上标记的重要性。
ms.openlocfilehash: 051307c0943a22e0c46439410806d168603d8a69
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530879"
---
# <a name="markimportance"></a><span data-ttu-id="6b6fd-103">MarkImportance</span><span class="sxs-lookup"><span data-stu-id="6b6fd-103">MarkImportance</span></span>

<span data-ttu-id="6b6fd-104">**MarkImportance**元素指定要在邮件上标记的重要性。</span><span class="sxs-lookup"><span data-stu-id="6b6fd-104">The **MarkImportance** element specifies the importance that is to be stamped on messages.</span></span> 
  
```XML
<MarkImportance/>
```

 <span data-ttu-id="6b6fd-105">**ImportanceChoicesType**</span><span class="sxs-lookup"><span data-stu-id="6b6fd-105">**ImportanceChoicesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b6fd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6b6fd-106">Attributes and elements</span></span>

<span data-ttu-id="6b6fd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6b6fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b6fd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6b6fd-108">Attributes</span></span>

<span data-ttu-id="6b6fd-109">无。</span><span class="sxs-lookup"><span data-stu-id="6b6fd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b6fd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6b6fd-110">Child elements</span></span>

<span data-ttu-id="6b6fd-111">无。</span><span class="sxs-lookup"><span data-stu-id="6b6fd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6b6fd-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6b6fd-112">Parent elements</span></span>

|<span data-ttu-id="6b6fd-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6b6fd-113">**Element**</span></span>|<span data-ttu-id="6b6fd-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6b6fd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b6fd-115">操作</span><span class="sxs-lookup"><span data-stu-id="6b6fd-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="6b6fd-116">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="6b6fd-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6b6fd-117">文本值</span><span class="sxs-lookup"><span data-stu-id="6b6fd-117">Text value</span></span>

<span data-ttu-id="6b6fd-118">此元素的文本值被限制为以下字符串值之一：</span><span class="sxs-lookup"><span data-stu-id="6b6fd-118">The text value for this element is restricted to one of the following string values:</span></span>
  
- <span data-ttu-id="6b6fd-119">低</span><span class="sxs-lookup"><span data-stu-id="6b6fd-119">Low</span></span>
    
- <span data-ttu-id="6b6fd-120">一般</span><span class="sxs-lookup"><span data-stu-id="6b6fd-120">Normal</span></span>
    
- <span data-ttu-id="6b6fd-121">高</span><span class="sxs-lookup"><span data-stu-id="6b6fd-121">High</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b6fd-122">说明</span><span class="sxs-lookup"><span data-stu-id="6b6fd-122">Remarks</span></span>

<span data-ttu-id="6b6fd-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6b6fd-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b6fd-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="6b6fd-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b6fd-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="6b6fd-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6b6fd-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="6b6fd-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6b6fd-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="6b6fd-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6b6fd-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="6b6fd-128">Validation File</span></span>  <br/> |<span data-ttu-id="6b6fd-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6b6fd-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6b6fd-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="6b6fd-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6b6fd-131">True</span><span class="sxs-lookup"><span data-stu-id="6b6fd-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b6fd-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6b6fd-132">See also</span></span>



- [<span data-ttu-id="6b6fd-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6b6fd-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

