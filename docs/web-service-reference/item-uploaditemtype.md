---
title: Item （UploadItemType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: Item 元素代表要上传到邮箱中的单个项目。
ms.openlocfilehash: 82c0fdf89c06ddfb812c2b2f1899b589eedeb7d8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467548"
---
# <a name="item-uploaditemtype"></a><span data-ttu-id="2dbdd-103">Item （UploadItemType）</span><span class="sxs-lookup"><span data-stu-id="2dbdd-103">Item (UploadItemType)</span></span>

<span data-ttu-id="2dbdd-104">**Item**元素代表要上传到邮箱中的单个项目。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-104">The **Item** element represents a single item to upload into a mailbox.</span></span> 
  
[<span data-ttu-id="2dbdd-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="2dbdd-105">UploadItems</span></span>](uploaditems.md)
  
[<span data-ttu-id="2dbdd-106">项目（NonEmptyArrayOfUploadItemsType）</span><span class="sxs-lookup"><span data-stu-id="2dbdd-106">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
  
[<span data-ttu-id="2dbdd-107">Item （UploadItemType）</span><span class="sxs-lookup"><span data-stu-id="2dbdd-107">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 <span data-ttu-id="2dbdd-108">**UploadItemType**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-108">**UploadItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2dbdd-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2dbdd-109">Attributes and elements</span></span>

<span data-ttu-id="2dbdd-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2dbdd-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="2dbdd-111">Attributes</span></span>

|<span data-ttu-id="2dbdd-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-112">**Attribute**</span></span>|<span data-ttu-id="2dbdd-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2dbdd-114">**CreateAction**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-114">**CreateAction**</span></span> <br/> |<span data-ttu-id="2dbdd-115">指定用于将项目上载到邮箱的操作。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-115">Specifies the action for uploading an item into a mailbox.</span></span> <span data-ttu-id="2dbdd-116">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="2dbdd-117">**IsAssociated**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-117">**IsAssociated**</span></span> <br/> |<span data-ttu-id="2dbdd-118">指定上传的项目是否是与文件夹相关联的项目。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-118">Specifies whether the uploaded item is a folder associated item.</span></span> <span data-ttu-id="2dbdd-119">此属性是一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-119">This attribute is a Boolean value.</span></span> <span data-ttu-id="2dbdd-120">**如果值为 true** ，则表示该项目是一个与文件夹相关联的项目。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-120">A value of **true** indicates that the item is a folder associated item.</span></span> <span data-ttu-id="2dbdd-121">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-121">This attribute is optional.</span></span>  <br/> |
   
#### <a name="createaction-attribute"></a><span data-ttu-id="2dbdd-122">CreateAction 属性</span><span class="sxs-lookup"><span data-stu-id="2dbdd-122">CreateAction Attribute</span></span>

|<span data-ttu-id="2dbdd-123">**值**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-123">**Value**</span></span>|<span data-ttu-id="2dbdd-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2dbdd-125">**CreateNew**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-125">**CreateNew**</span></span> <br/> |<span data-ttu-id="2dbdd-126">指示将原始项目的新副本上载到邮箱。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-126">Indicates that a new copy of the original item is uploaded to the mailbox.</span></span> <span data-ttu-id="2dbdd-127">如果使用了 CreateNew 值，则必须不存在[ItemId](itemid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-127">The [ItemId](itemid.md) element must not be present if the CreateNew value is used.</span></span> <span data-ttu-id="2dbdd-128">在响应中返回新的项目标识符。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-128">The new item identifier is returned in the response.</span></span>  <br/> |
|<span data-ttu-id="2dbdd-129">**更新**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-129">**Update**</span></span> <br/> |<span data-ttu-id="2dbdd-130">指定由**ItemId**元素指示的项目将更新。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-130">Specifies that the item indicated by the **ItemId** element will be updated.</span></span> <span data-ttu-id="2dbdd-131">如果**ItemId**元素不存在或项目不存在于由[ParentFolderId](parentfolderid.md)元素标识的文件夹中，则会返回错误。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-131">An error is returned if the **ItemId** element is not present or if the item does not exist in the folder identified by the [ParentFolderId](parentfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="2dbdd-132">**UpdateOrCreate**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-132">**UpdateOrCreate**</span></span> <br/> |<span data-ttu-id="2dbdd-133">指示第一次尝试更新项目。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-133">Indicates that an attempt is first made to update the item.</span></span> <span data-ttu-id="2dbdd-134">如果**ParentFolderId**元素指定的文件夹中不存在该项目，则会创建一个新项目。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-134">If the item does not exist in the folder specified by the **ParentFolderId** element, a new item is created.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2dbdd-135">子元素</span><span class="sxs-lookup"><span data-stu-id="2dbdd-135">Child elements</span></span>

|<span data-ttu-id="2dbdd-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-136">**Element**</span></span>|<span data-ttu-id="2dbdd-137">**描述**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dbdd-138">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="2dbdd-138">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="2dbdd-139">表示在其中创建新项目或包含要更新的项目的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-139">Represents the identifier of the parent folder where a new item is created or that contains the item to update.</span></span>  <br/> |
|[<span data-ttu-id="2dbdd-140">ItemId</span><span class="sxs-lookup"><span data-stu-id="2dbdd-140">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="2dbdd-141">包含要在 Exchange 存储中创建或更新的项目的唯一标识符和更改密钥。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-141">Contains the unique identifier and change key of an item to create or update in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2dbdd-142">Data （base64Binary）</span><span class="sxs-lookup"><span data-stu-id="2dbdd-142">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="2dbdd-143">包含要上传到邮箱中的单个项目的数据。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-143">Contains the data of a single item to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2dbdd-144">父元素</span><span class="sxs-lookup"><span data-stu-id="2dbdd-144">Parent elements</span></span>

|<span data-ttu-id="2dbdd-145">**元素**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-145">**Element**</span></span>|<span data-ttu-id="2dbdd-146">**描述**</span><span class="sxs-lookup"><span data-stu-id="2dbdd-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dbdd-147">项目（NonEmptyArrayOfUploadItemsType）</span><span class="sxs-lookup"><span data-stu-id="2dbdd-147">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="2dbdd-148">包含要上载到邮箱的项的数组。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-148">Contains an array of item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2dbdd-149">文本值</span><span class="sxs-lookup"><span data-stu-id="2dbdd-149">Text value</span></span>

<span data-ttu-id="2dbdd-150">无。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2dbdd-151">说明</span><span class="sxs-lookup"><span data-stu-id="2dbdd-151">Remarks</span></span>

<span data-ttu-id="2dbdd-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2dbdd-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2dbdd-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="2dbdd-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2dbdd-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="2dbdd-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2dbdd-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="2dbdd-155">Schema Name</span></span>  <br/> |<span data-ttu-id="2dbdd-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="2dbdd-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="2dbdd-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="2dbdd-157">Validation File</span></span>  <br/> |<span data-ttu-id="2dbdd-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2dbdd-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2dbdd-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="2dbdd-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="2dbdd-160">False</span><span class="sxs-lookup"><span data-stu-id="2dbdd-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2dbdd-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2dbdd-161">See also</span></span>



[<span data-ttu-id="2dbdd-162">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="2dbdd-162">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="2dbdd-163">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="2dbdd-163">UploadItems operation</span></span>](uploaditems-operation.md)

