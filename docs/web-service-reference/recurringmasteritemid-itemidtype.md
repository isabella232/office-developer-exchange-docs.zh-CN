---
title: RecurringMasterItemId (ItemIdType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: RecurringMasterItemId (ItemIdType) 元素标识定期主项目通过标识之一的及其相关的匹配项的标识符。
ms.openlocfilehash: 89089067963e99ac1a6cae6ea6e1e8350d148e82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827010"
---
# <a name="recurringmasteritemid-itemidtype"></a><span data-ttu-id="7beca-103">RecurringMasterItemId (ItemIdType)</span><span class="sxs-lookup"><span data-stu-id="7beca-103">RecurringMasterItemId (ItemIdType)</span></span>

<span data-ttu-id="7beca-104">**RecurringMasterItemId (ItemIdType)** 元素标识定期主项目通过标识之一的及其相关的匹配项的标识符。</span><span class="sxs-lookup"><span data-stu-id="7beca-104">The **RecurringMasterItemId (ItemIdType)** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="7beca-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="7beca-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7beca-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7beca-106">Attributes and elements</span></span>

<span data-ttu-id="7beca-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7beca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7beca-108">属性</span><span class="sxs-lookup"><span data-stu-id="7beca-108">Attributes</span></span>

****

|<span data-ttu-id="7beca-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="7beca-109">**Attribute**</span></span>|<span data-ttu-id="7beca-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="7beca-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7beca-111">Id</span><span class="sxs-lookup"><span data-stu-id="7beca-111">Id</span></span>  <br/> |<span data-ttu-id="7beca-112">标识定期主项目的一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="7beca-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="7beca-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="7beca-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="7beca-114">更改密钥</span><span class="sxs-lookup"><span data-stu-id="7beca-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="7beca-115">标识定期主项目的一个匹配项的特定版本。</span><span class="sxs-lookup"><span data-stu-id="7beca-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="7beca-116">此外，因为它和一次将包含相同的更改键，也被标识定期主项目。</span><span class="sxs-lookup"><span data-stu-id="7beca-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="7beca-117">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="7beca-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7beca-118">子元素</span><span class="sxs-lookup"><span data-stu-id="7beca-118">Child elements</span></span>

<span data-ttu-id="7beca-119">无。</span><span class="sxs-lookup"><span data-stu-id="7beca-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7beca-120">父元素</span><span class="sxs-lookup"><span data-stu-id="7beca-120">Parent elements</span></span>

[<span data-ttu-id="7beca-121">提醒</span><span class="sxs-lookup"><span data-stu-id="7beca-121">Reminder</span></span>](reminder.md)
  
## <a name="remarks"></a><span data-ttu-id="7beca-122">备注</span><span class="sxs-lookup"><span data-stu-id="7beca-122">Remarks</span></span>

<span data-ttu-id="7beca-123">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7beca-123">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="7beca-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7beca-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7beca-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="7beca-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7beca-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="7beca-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7beca-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="7beca-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7beca-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="7beca-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="7beca-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="7beca-129">Validation File</span></span>  <br/> |<span data-ttu-id="7beca-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7beca-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7beca-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="7beca-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="7beca-132">True</span><span class="sxs-lookup"><span data-stu-id="7beca-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7beca-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7beca-133">See also</span></span>



[<span data-ttu-id="7beca-134">提醒</span><span class="sxs-lookup"><span data-stu-id="7beca-134">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="7beca-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7beca-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

