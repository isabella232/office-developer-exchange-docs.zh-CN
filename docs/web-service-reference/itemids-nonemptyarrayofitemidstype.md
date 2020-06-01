---
title: ItemIds (NonEmptyArrayOfItemIdsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemIds
api_type:
- schema
ms.assetid: e895782a-74fe-4216-8ac2-c3c88c4b232d
description: ItemIds 元素包含项标识符的数组，这些标识符标识要从邮箱中导出的项。
ms.openlocfilehash: 16c2633528e2ecbc863cfdde645e0f431b4c4297
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468591"
---
# <a name="itemids-nonemptyarrayofitemidstype"></a><span data-ttu-id="897a1-103">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="897a1-103">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>

<span data-ttu-id="897a1-104">**ItemIds**元素包含项标识符的数组，这些标识符标识要从邮箱中导出的项。</span><span class="sxs-lookup"><span data-stu-id="897a1-104">The **ItemIds** element contains an array of item identifiers that identify the items to export from a mailbox.</span></span> 
  
[<span data-ttu-id="897a1-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="897a1-105">ExportItems</span></span>](exportitems.md)
  
[<span data-ttu-id="897a1-106">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="897a1-106">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md)
  
```XML
<ItemIds>
   <ItemId/>
</ItemIds>
```

 <span data-ttu-id="897a1-107">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="897a1-107">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="897a1-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="897a1-108">Attributes and elements</span></span>

<span data-ttu-id="897a1-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="897a1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="897a1-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="897a1-110">Attributes</span></span>

<span data-ttu-id="897a1-111">无。</span><span class="sxs-lookup"><span data-stu-id="897a1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="897a1-112">子元素</span><span class="sxs-lookup"><span data-stu-id="897a1-112">Child elements</span></span>

|<span data-ttu-id="897a1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="897a1-113">**Element**</span></span>|<span data-ttu-id="897a1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="897a1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="897a1-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="897a1-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="897a1-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="897a1-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="897a1-117">父元素</span><span class="sxs-lookup"><span data-stu-id="897a1-117">Parent elements</span></span>

|<span data-ttu-id="897a1-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="897a1-118">**Element**</span></span>|<span data-ttu-id="897a1-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="897a1-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="897a1-120">ExportItems</span><span class="sxs-lookup"><span data-stu-id="897a1-120">ExportItems</span></span>](exportitems.md) <br/> |<span data-ttu-id="897a1-121">表示从邮箱导出项目的请求。</span><span class="sxs-lookup"><span data-stu-id="897a1-121">Represents a request to export items from a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="897a1-122">文本值</span><span class="sxs-lookup"><span data-stu-id="897a1-122">Text value</span></span>

<span data-ttu-id="897a1-123">无。</span><span class="sxs-lookup"><span data-stu-id="897a1-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="897a1-124">说明</span><span class="sxs-lookup"><span data-stu-id="897a1-124">Remarks</span></span>

<span data-ttu-id="897a1-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="897a1-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="897a1-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="897a1-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="897a1-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="897a1-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="897a1-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="897a1-128">Schema Name</span></span>  <br/> |<span data-ttu-id="897a1-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="897a1-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="897a1-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="897a1-130">Validation File</span></span>  <br/> |<span data-ttu-id="897a1-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="897a1-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="897a1-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="897a1-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="897a1-133">False</span><span class="sxs-lookup"><span data-stu-id="897a1-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="897a1-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="897a1-134">See also</span></span>



[<span data-ttu-id="897a1-135">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="897a1-135">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="897a1-136">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="897a1-136">UploadItems operation</span></span>](uploaditems-operation.md)

