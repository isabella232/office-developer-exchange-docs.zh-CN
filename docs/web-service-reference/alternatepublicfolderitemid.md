---
title: AlternatePublicFolderItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderItemId
api_type:
- schema
ms.assetid: a67df9b9-8fdb-42de-b9c5-8377b71fa3d9
description: AlternatePublicFolderItemId 元素描述将转换为另一个标识符格式的公用文件夹项标识符。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 2240f3ff80c2c5b705611c3cf9286faa62d204cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753144"
---
# <a name="alternatepublicfolderitemid"></a><span data-ttu-id="9b72e-104">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="9b72e-104">AlternatePublicFolderItemId</span></span>

<span data-ttu-id="9b72e-105">**AlternatePublicFolderItemId**元素描述将转换为另一个标识符格式的公用文件夹项标识符。</span><span class="sxs-lookup"><span data-stu-id="9b72e-105">The **AlternatePublicFolderItemId** element describes a public folder item identifier to convert to another identifier format.</span></span> <span data-ttu-id="9b72e-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9b72e-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="9b72e-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="9b72e-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="9b72e-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="9b72e-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="9b72e-109">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="9b72e-109">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 <span data-ttu-id="9b72e-110">**AlternatePublicFolderItemIdType**</span><span class="sxs-lookup"><span data-stu-id="9b72e-110">**AlternatePublicFolderItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b72e-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9b72e-111">Attributes and elements</span></span>

<span data-ttu-id="9b72e-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9b72e-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b72e-113">属性</span><span class="sxs-lookup"><span data-stu-id="9b72e-113">Attributes</span></span>

|<span data-ttu-id="9b72e-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="9b72e-114">**Attribute**</span></span>|<span data-ttu-id="9b72e-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b72e-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b72e-116">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="9b72e-116">FolderId</span></span>  <br/> |<span data-ttu-id="9b72e-117">标识的公用文件夹的包含公用文件夹项。</span><span class="sxs-lookup"><span data-stu-id="9b72e-117">Identifies the public folder that contains the public folder item.</span></span> <span data-ttu-id="9b72e-118">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="9b72e-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="9b72e-119">格式</span><span class="sxs-lookup"><span data-stu-id="9b72e-119">Format</span></span>  <br/> |<span data-ttu-id="9b72e-120">标识描述要转换的公用文件夹项标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="9b72e-120">Identifies the format that describes the public folder item identifier to convert.</span></span> <span data-ttu-id="9b72e-121">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="9b72e-121">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="9b72e-122">ItemId</span><span class="sxs-lookup"><span data-stu-id="9b72e-122">ItemId</span></span>  <br/> |<span data-ttu-id="9b72e-123">标识符要转换的公用文件夹项。</span><span class="sxs-lookup"><span data-stu-id="9b72e-123">Identifier the public folder item to convert.</span></span> <span data-ttu-id="9b72e-124">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="9b72e-124">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="9b72e-125">Format 属性值</span><span class="sxs-lookup"><span data-stu-id="9b72e-125">Format attribute values</span></span>

|<span data-ttu-id="9b72e-126">**值**</span><span class="sxs-lookup"><span data-stu-id="9b72e-126">**Value**</span></span>|<span data-ttu-id="9b72e-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b72e-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b72e-128">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="9b72e-128">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="9b72e-129">描述所产生的 Exchange Web 服务的初始发行版本的 Exchange 2007 中的标识符。</span><span class="sxs-lookup"><span data-stu-id="9b72e-129">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="9b72e-130">EwsId</span><span class="sxs-lookup"><span data-stu-id="9b72e-130">EwsId</span></span>  <br/> |<span data-ttu-id="9b72e-131">描述所产生的开头 Exchange 2007 SP1 的 Exchange Web 服务的标识符。</span><span class="sxs-lookup"><span data-stu-id="9b72e-131">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="9b72e-132">EntryId</span><span class="sxs-lookup"><span data-stu-id="9b72e-132">EntryId</span></span>  <br/> |<span data-ttu-id="9b72e-133">描述 MAPI 标识符，如 PR_ENTRYID 属性中所示。</span><span class="sxs-lookup"><span data-stu-id="9b72e-133">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="9b72e-134">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="9b72e-134">HexEntryId</span></span>  <br/> |<span data-ttu-id="9b72e-135">介绍 PR_ENTRYID 属性的十六进制编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="9b72e-135">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="9b72e-136">这是可用性日历事件标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="9b72e-136">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="9b72e-137">StoreId</span><span class="sxs-lookup"><span data-stu-id="9b72e-137">StoreId</span></span>  <br/> |<span data-ttu-id="9b72e-138">描述 Exchange 存储区标识符。</span><span class="sxs-lookup"><span data-stu-id="9b72e-138">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="9b72e-139">OwaId</span><span class="sxs-lookup"><span data-stu-id="9b72e-139">OwaId</span></span>  <br/> |<span data-ttu-id="9b72e-140">介绍 Outlook Web Access 标识符。</span><span class="sxs-lookup"><span data-stu-id="9b72e-140">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b72e-141">子元素</span><span class="sxs-lookup"><span data-stu-id="9b72e-141">Child elements</span></span>

<span data-ttu-id="9b72e-142">无。</span><span class="sxs-lookup"><span data-stu-id="9b72e-142">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9b72e-143">父元素</span><span class="sxs-lookup"><span data-stu-id="9b72e-143">Parent elements</span></span>

|<span data-ttu-id="9b72e-144">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b72e-144">**Element**</span></span>|<span data-ttu-id="9b72e-145">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b72e-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b72e-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="9b72e-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="9b72e-147">包含要转换的源标识符。</span><span class="sxs-lookup"><span data-stu-id="9b72e-147">Contains the source identifiers to convert.</span></span> <span data-ttu-id="9b72e-148">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9b72e-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b72e-149">备注</span><span class="sxs-lookup"><span data-stu-id="9b72e-149">Remarks</span></span>

<span data-ttu-id="9b72e-150">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9b72e-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b72e-151">元素信息</span><span class="sxs-lookup"><span data-stu-id="9b72e-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b72e-152">命名空间</span><span class="sxs-lookup"><span data-stu-id="9b72e-152">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9b72e-153">架构名称</span><span class="sxs-lookup"><span data-stu-id="9b72e-153">Schema Name</span></span>  <br/> |<span data-ttu-id="9b72e-154">类型架构</span><span class="sxs-lookup"><span data-stu-id="9b72e-154">Types schema</span></span>  <br/> |
|<span data-ttu-id="9b72e-155">验证文件</span><span class="sxs-lookup"><span data-stu-id="9b72e-155">Validation File</span></span>  <br/> |<span data-ttu-id="9b72e-156">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9b72e-156">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9b72e-157">可以为空</span><span class="sxs-lookup"><span data-stu-id="9b72e-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="9b72e-158">True</span><span class="sxs-lookup"><span data-stu-id="9b72e-158">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b72e-159">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9b72e-159">See also</span></span>

- [<span data-ttu-id="9b72e-160">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="9b72e-160">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="9b72e-161">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9b72e-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="9b72e-162">转换标识符</span><span class="sxs-lookup"><span data-stu-id="9b72e-162">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

