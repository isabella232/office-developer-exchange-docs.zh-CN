---
title: RecurringMasterItemId (ItemIdType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: RecurringMasterItemId （ItemIdType）元素通过标识一个定期主项目的相关发生项的标识符来标识该项目。
ms.openlocfilehash: c725998ad3a728ef1f47ff6491592b461753b895
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468437"
---
# <a name="recurringmasteritemid-itemidtype"></a><span data-ttu-id="b0995-103">RecurringMasterItemId (ItemIdType)</span><span class="sxs-lookup"><span data-stu-id="b0995-103">RecurringMasterItemId (ItemIdType)</span></span>

<span data-ttu-id="b0995-104">**RecurringMasterItemId （ItemIdType）** 元素通过标识一个定期主项目的相关发生项的标识符来标识该项目。</span><span class="sxs-lookup"><span data-stu-id="b0995-104">The **RecurringMasterItemId (ItemIdType)** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="b0995-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="b0995-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0995-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b0995-106">Attributes and elements</span></span>

<span data-ttu-id="b0995-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b0995-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0995-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b0995-108">Attributes</span></span>

****

|<span data-ttu-id="b0995-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="b0995-109">**Attribute**</span></span>|<span data-ttu-id="b0995-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0995-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0995-111">Id</span><span class="sxs-lookup"><span data-stu-id="b0995-111">Id</span></span>  <br/> |<span data-ttu-id="b0995-112">标识定期主项目的单个事件。</span><span class="sxs-lookup"><span data-stu-id="b0995-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="b0995-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="b0995-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="b0995-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="b0995-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="b0995-115">标识定期主项目的单个事件的特定版本。</span><span class="sxs-lookup"><span data-stu-id="b0995-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="b0995-116">此外，还会标识定期主项目，因为它和单个事件将包含相同的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="b0995-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="b0995-117">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="b0995-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b0995-118">子元素</span><span class="sxs-lookup"><span data-stu-id="b0995-118">Child elements</span></span>

<span data-ttu-id="b0995-119">无。</span><span class="sxs-lookup"><span data-stu-id="b0995-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0995-120">父元素</span><span class="sxs-lookup"><span data-stu-id="b0995-120">Parent elements</span></span>

[<span data-ttu-id="b0995-121">提醒</span><span class="sxs-lookup"><span data-stu-id="b0995-121">Reminder</span></span>](reminder.md)
  
## <a name="remarks"></a><span data-ttu-id="b0995-122">说明</span><span class="sxs-lookup"><span data-stu-id="b0995-122">Remarks</span></span>

<span data-ttu-id="b0995-123">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b0995-123">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="b0995-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b0995-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0995-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="b0995-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0995-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="b0995-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0995-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="b0995-127">Schema Name</span></span>  <br/> |<span data-ttu-id="b0995-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="b0995-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="b0995-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="b0995-129">Validation File</span></span>  <br/> |<span data-ttu-id="b0995-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b0995-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0995-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="b0995-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="b0995-132">True</span><span class="sxs-lookup"><span data-stu-id="b0995-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0995-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b0995-133">See also</span></span>



[<span data-ttu-id="b0995-134">提醒</span><span class="sxs-lookup"><span data-stu-id="b0995-134">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="b0995-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b0995-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

