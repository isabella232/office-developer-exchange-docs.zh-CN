---
title: 项目 (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: Item 元素表示单个项目上载到邮箱。
ms.openlocfilehash: 8fecef9a2368a44e38633eb9fddaa8197620f6a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826138"
---
# <a name="item-uploaditemtype"></a><span data-ttu-id="a85f0-103">项目 (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="a85f0-103">Item (UploadItemType)</span></span>

<span data-ttu-id="a85f0-104">**Item**元素表示单个项目上载到邮箱。</span><span class="sxs-lookup"><span data-stu-id="a85f0-104">The **Item** element represents a single item to upload into a mailbox.</span></span> 
  
[<span data-ttu-id="a85f0-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="a85f0-105">UploadItems</span></span>](uploaditems.md)
  
[<span data-ttu-id="a85f0-106">项目 (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="a85f0-106">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
  
[<span data-ttu-id="a85f0-107">项目 (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="a85f0-107">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 <span data-ttu-id="a85f0-108">**UploadItemType**</span><span class="sxs-lookup"><span data-stu-id="a85f0-108">**UploadItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a85f0-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a85f0-109">Attributes and elements</span></span>

<span data-ttu-id="a85f0-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a85f0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a85f0-111">属性</span><span class="sxs-lookup"><span data-stu-id="a85f0-111">Attributes</span></span>

|<span data-ttu-id="a85f0-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="a85f0-112">**Attribute**</span></span>|<span data-ttu-id="a85f0-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="a85f0-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a85f0-114">**CreateAction**</span><span class="sxs-lookup"><span data-stu-id="a85f0-114">**CreateAction**</span></span> <br/> |<span data-ttu-id="a85f0-115">指定用于将项目上载到邮箱的操作。</span><span class="sxs-lookup"><span data-stu-id="a85f0-115">Specifies the action for uploading an item into a mailbox.</span></span> <span data-ttu-id="a85f0-116">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="a85f0-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="a85f0-117">**IsAssociated**</span><span class="sxs-lookup"><span data-stu-id="a85f0-117">**IsAssociated**</span></span> <br/> |<span data-ttu-id="a85f0-118">指定是否已上载的项目是关联文件夹项。</span><span class="sxs-lookup"><span data-stu-id="a85f0-118">Specifies whether the uploaded item is a folder associated item.</span></span> <span data-ttu-id="a85f0-119">此属性是一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="a85f0-119">This attribute is a Boolean value.</span></span> <span data-ttu-id="a85f0-120">值为**true**指示项关联的项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="a85f0-120">A value of **true** indicates that the item is a folder associated item.</span></span> <span data-ttu-id="a85f0-121">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="a85f0-121">This attribute is optional.</span></span>  <br/> |
   
#### <a name="createaction-attribute"></a><span data-ttu-id="a85f0-122">创建动作属性</span><span class="sxs-lookup"><span data-stu-id="a85f0-122">CreateAction Attribute</span></span>

|<span data-ttu-id="a85f0-123">**值**</span><span class="sxs-lookup"><span data-stu-id="a85f0-123">**Value**</span></span>|<span data-ttu-id="a85f0-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="a85f0-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a85f0-125">**CreateNew**</span><span class="sxs-lookup"><span data-stu-id="a85f0-125">**CreateNew**</span></span> <br/> |<span data-ttu-id="a85f0-126">指示原始项目的新副本上载到邮箱。</span><span class="sxs-lookup"><span data-stu-id="a85f0-126">Indicates that a new copy of the original item is uploaded to the mailbox.</span></span> <span data-ttu-id="a85f0-127">[ItemId](itemid.md)元素必须存在，如果使用了 CreateNew 值。</span><span class="sxs-lookup"><span data-stu-id="a85f0-127">The [ItemId](itemid.md) element must not be present if the CreateNew value is used.</span></span> <span data-ttu-id="a85f0-128">在响应中返回新的项标识符。</span><span class="sxs-lookup"><span data-stu-id="a85f0-128">The new item identifier is returned in the response.</span></span>  <br/> |
|<span data-ttu-id="a85f0-129">**更新**</span><span class="sxs-lookup"><span data-stu-id="a85f0-129">**Update**</span></span> <br/> |<span data-ttu-id="a85f0-130">指定将由**ItemId**元素指示的项进行了更新。</span><span class="sxs-lookup"><span data-stu-id="a85f0-130">Specifies that the item indicated by the **ItemId** element will be updated.</span></span> <span data-ttu-id="a85f0-131">如果不存在**ItemId**元素或项目中由[ParentFolderId](parentfolderid.md)元素标识的文件夹不存在，则返回错误。</span><span class="sxs-lookup"><span data-stu-id="a85f0-131">An error is returned if the **ItemId** element is not present or if the item does not exist in the folder identified by the [ParentFolderId](parentfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="a85f0-132">**UpdateOrCreate**</span><span class="sxs-lookup"><span data-stu-id="a85f0-132">**UpdateOrCreate**</span></span> <br/> |<span data-ttu-id="a85f0-133">指示尝试首先进行更新此项目。</span><span class="sxs-lookup"><span data-stu-id="a85f0-133">Indicates that an attempt is first made to update the item.</span></span> <span data-ttu-id="a85f0-134">如果项目不存在**ParentFolderId**元素所指定的文件夹中，将创建一个新项。</span><span class="sxs-lookup"><span data-stu-id="a85f0-134">If the item does not exist in the folder specified by the **ParentFolderId** element, a new item is created.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a85f0-135">子元素</span><span class="sxs-lookup"><span data-stu-id="a85f0-135">Child elements</span></span>

|<span data-ttu-id="a85f0-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="a85f0-136">**Element**</span></span>|<span data-ttu-id="a85f0-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="a85f0-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a85f0-138">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="a85f0-138">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="a85f0-139">表示在其中创建新项目或包含要更新的项的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="a85f0-139">Represents the identifier of the parent folder where a new item is created or that contains the item to update.</span></span>  <br/> |
|[<span data-ttu-id="a85f0-140">ItemId</span><span class="sxs-lookup"><span data-stu-id="a85f0-140">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="a85f0-141">包含要创建或更新 Exchange 存储中的项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="a85f0-141">Contains the unique identifier and change key of an item to create or update in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a85f0-142">数据 (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="a85f0-142">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="a85f0-143">包含要上载到邮箱的单个项的数据。</span><span class="sxs-lookup"><span data-stu-id="a85f0-143">Contains the data of a single item to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a85f0-144">父元素</span><span class="sxs-lookup"><span data-stu-id="a85f0-144">Parent elements</span></span>

|<span data-ttu-id="a85f0-145">**元素**</span><span class="sxs-lookup"><span data-stu-id="a85f0-145">**Element**</span></span>|<span data-ttu-id="a85f0-146">**说明**</span><span class="sxs-lookup"><span data-stu-id="a85f0-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a85f0-147">项目 (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="a85f0-147">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="a85f0-148">包含项目上载到邮箱的数组。</span><span class="sxs-lookup"><span data-stu-id="a85f0-148">Contains an array of item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a85f0-149">文本值</span><span class="sxs-lookup"><span data-stu-id="a85f0-149">Text value</span></span>

<span data-ttu-id="a85f0-150">无。</span><span class="sxs-lookup"><span data-stu-id="a85f0-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a85f0-151">备注</span><span class="sxs-lookup"><span data-stu-id="a85f0-151">Remarks</span></span>

<span data-ttu-id="a85f0-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a85f0-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a85f0-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="a85f0-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a85f0-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="a85f0-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a85f0-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="a85f0-155">Schema Name</span></span>  <br/> |<span data-ttu-id="a85f0-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="a85f0-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="a85f0-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="a85f0-157">Validation File</span></span>  <br/> |<span data-ttu-id="a85f0-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a85f0-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a85f0-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="a85f0-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="a85f0-160">False</span><span class="sxs-lookup"><span data-stu-id="a85f0-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a85f0-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a85f0-161">See also</span></span>



[<span data-ttu-id="a85f0-162">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="a85f0-162">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="a85f0-163">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="a85f0-163">UploadItems operation</span></span>](uploaditems-operation.md)

