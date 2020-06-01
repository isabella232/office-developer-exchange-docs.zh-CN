---
title: 项目（NonEmptyArrayOfUploadItemsType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: 402bfa6d-11d7-4547-b8bd-197e9922ab49
description: Items 元素包含要上载到邮箱中的项目数组。
ms.openlocfilehash: 5c69134c1613b0a4595a6aa876fa09fde63043ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44441546"
---
# <a name="items-nonemptyarrayofuploaditemstype"></a><span data-ttu-id="aa126-103">项目（NonEmptyArrayOfUploadItemsType）</span><span class="sxs-lookup"><span data-stu-id="aa126-103">Items (NonEmptyArrayOfUploadItemsType)</span></span>

<span data-ttu-id="aa126-104">**Items**元素包含要上载到邮箱中的项目数组。</span><span class="sxs-lookup"><span data-stu-id="aa126-104">The **Items** element contains an array of items to upload into a mailbox.</span></span> 
  
[<span data-ttu-id="aa126-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="aa126-105">UploadItems</span></span>](uploaditems.md)
  
[<span data-ttu-id="aa126-106">项目（NonEmptyArrayOfUploadItemsType）</span><span class="sxs-lookup"><span data-stu-id="aa126-106">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
  
```XML
<Items>
   <Item/>
</Items>
```

 <span data-ttu-id="aa126-107">**NonEmptyArrayOfUploadItemsType**</span><span class="sxs-lookup"><span data-stu-id="aa126-107">**NonEmptyArrayOfUploadItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa126-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aa126-108">Attributes and elements</span></span>

<span data-ttu-id="aa126-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aa126-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa126-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="aa126-110">Attributes</span></span>

<span data-ttu-id="aa126-111">无。</span><span class="sxs-lookup"><span data-stu-id="aa126-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa126-112">子元素</span><span class="sxs-lookup"><span data-stu-id="aa126-112">Child elements</span></span>

|<span data-ttu-id="aa126-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa126-113">**Element**</span></span>|<span data-ttu-id="aa126-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa126-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa126-115">Item （UploadItemType）</span><span class="sxs-lookup"><span data-stu-id="aa126-115">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="aa126-116">代表要上传到邮箱中的单个项目。</span><span class="sxs-lookup"><span data-stu-id="aa126-116">Represents a single item to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa126-117">父元素</span><span class="sxs-lookup"><span data-stu-id="aa126-117">Parent elements</span></span>

|<span data-ttu-id="aa126-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa126-118">**Element**</span></span>|<span data-ttu-id="aa126-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa126-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa126-120">UploadItems</span><span class="sxs-lookup"><span data-stu-id="aa126-120">UploadItems</span></span>](uploaditems.md) <br/> |<span data-ttu-id="aa126-121">表示将项目上传到邮箱的请求。</span><span class="sxs-lookup"><span data-stu-id="aa126-121">Represents a request to upload items into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aa126-122">文本值</span><span class="sxs-lookup"><span data-stu-id="aa126-122">Text value</span></span>

<span data-ttu-id="aa126-123">无。</span><span class="sxs-lookup"><span data-stu-id="aa126-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa126-124">说明</span><span class="sxs-lookup"><span data-stu-id="aa126-124">Remarks</span></span>

<span data-ttu-id="aa126-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="aa126-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa126-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="aa126-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa126-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="aa126-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aa126-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="aa126-128">Schema Name</span></span>  <br/> |<span data-ttu-id="aa126-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="aa126-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="aa126-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="aa126-130">Validation File</span></span>  <br/> |<span data-ttu-id="aa126-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="aa126-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aa126-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="aa126-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa126-133">False</span><span class="sxs-lookup"><span data-stu-id="aa126-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa126-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa126-134">See also</span></span>



[<span data-ttu-id="aa126-135">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="aa126-135">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="aa126-136">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="aa126-136">UploadItems operation</span></span>](uploaditems-operation.md)

