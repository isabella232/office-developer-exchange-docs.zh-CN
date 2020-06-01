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
description: AlternatePublicFolderItemId 元素描述要转换为另一种标识符格式的公用文件夹项目标识符。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 11a9fafec78a9bd14e4d98982fd38954d45e4d1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464768"
---
# <a name="alternatepublicfolderitemid"></a><span data-ttu-id="6f3c2-104">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-104">AlternatePublicFolderItemId</span></span>

<span data-ttu-id="6f3c2-105">**AlternatePublicFolderItemId**元素描述要转换为另一种标识符格式的公用文件夹项目标识符。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-105">The **AlternatePublicFolderItemId** element describes a public folder item identifier to convert to another identifier format.</span></span> <span data-ttu-id="6f3c2-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="6f3c2-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="6f3c2-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="6f3c2-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="6f3c2-109">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-109">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 <span data-ttu-id="6f3c2-110">**AlternatePublicFolderItemIdType**</span><span class="sxs-lookup"><span data-stu-id="6f3c2-110">**AlternatePublicFolderItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f3c2-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f3c2-111">Attributes and elements</span></span>

<span data-ttu-id="6f3c2-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f3c2-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="6f3c2-113">Attributes</span></span>

|<span data-ttu-id="6f3c2-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="6f3c2-114">**Attribute**</span></span>|<span data-ttu-id="6f3c2-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f3c2-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6f3c2-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-116">FolderId</span></span>  <br/> |<span data-ttu-id="6f3c2-117">标识包含公用文件夹项目的公用文件夹。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-117">Identifies the public folder that contains the public folder item.</span></span> <span data-ttu-id="6f3c2-118">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="6f3c2-119">Format</span><span class="sxs-lookup"><span data-stu-id="6f3c2-119">Format</span></span>  <br/> |<span data-ttu-id="6f3c2-120">标识描述要转换的公用文件夹项目标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-120">Identifies the format that describes the public folder item identifier to convert.</span></span> <span data-ttu-id="6f3c2-121">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-121">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="6f3c2-122">ItemId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-122">ItemId</span></span>  <br/> |<span data-ttu-id="6f3c2-123">标识符要转换的公用文件夹项目。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-123">Identifier the public folder item to convert.</span></span> <span data-ttu-id="6f3c2-124">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-124">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="6f3c2-125">格式属性值</span><span class="sxs-lookup"><span data-stu-id="6f3c2-125">Format attribute values</span></span>

|<span data-ttu-id="6f3c2-126">**值**</span><span class="sxs-lookup"><span data-stu-id="6f3c2-126">**Value**</span></span>|<span data-ttu-id="6f3c2-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f3c2-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6f3c2-128">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-128">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="6f3c2-129">介绍 exchange 2007 的初始发布版本中的 Exchange Web 服务生成的标识符。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-129">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="6f3c2-130">EwsId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-130">EwsId</span></span>  <br/> |<span data-ttu-id="6f3c2-131">介绍了 Exchange Web 服务从 Exchange 2007 SP1 开始生成的标识符。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-131">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="6f3c2-132">EntryId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-132">EntryId</span></span>  <br/> |<span data-ttu-id="6f3c2-133">描述 MAPI 标识符，如 PR_ENTRYID 属性中所示。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-133">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="6f3c2-134">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-134">HexEntryId</span></span>  <br/> |<span data-ttu-id="6f3c2-135">描述了 PR_ENTRYID 属性的十六进制编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-135">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="6f3c2-136">这是可用性日历事件标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-136">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="6f3c2-137">StoreId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-137">StoreId</span></span>  <br/> |<span data-ttu-id="6f3c2-138">描述 Exchange 存储标识符。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-138">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="6f3c2-139">OwaId</span><span class="sxs-lookup"><span data-stu-id="6f3c2-139">OwaId</span></span>  <br/> |<span data-ttu-id="6f3c2-140">介绍 Outlook Web Access 标识符。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-140">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6f3c2-141">子元素</span><span class="sxs-lookup"><span data-stu-id="6f3c2-141">Child elements</span></span>

<span data-ttu-id="6f3c2-142">无。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-142">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f3c2-143">父元素</span><span class="sxs-lookup"><span data-stu-id="6f3c2-143">Parent elements</span></span>

|<span data-ttu-id="6f3c2-144">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f3c2-144">**Element**</span></span>|<span data-ttu-id="6f3c2-145">**描述**</span><span class="sxs-lookup"><span data-stu-id="6f3c2-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f3c2-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="6f3c2-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="6f3c2-147">包含要转换的源标识符。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-147">Contains the source identifiers to convert.</span></span> <span data-ttu-id="6f3c2-148">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f3c2-149">说明</span><span class="sxs-lookup"><span data-stu-id="6f3c2-149">Remarks</span></span>

<span data-ttu-id="6f3c2-150">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6f3c2-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f3c2-151">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f3c2-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f3c2-152">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f3c2-152">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f3c2-153">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f3c2-153">Schema Name</span></span>  <br/> |<span data-ttu-id="6f3c2-154">类型架构</span><span class="sxs-lookup"><span data-stu-id="6f3c2-154">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f3c2-155">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f3c2-155">Validation File</span></span>  <br/> |<span data-ttu-id="6f3c2-156">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6f3c2-156">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f3c2-157">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f3c2-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f3c2-158">True</span><span class="sxs-lookup"><span data-stu-id="6f3c2-158">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f3c2-159">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f3c2-159">See also</span></span>

- [<span data-ttu-id="6f3c2-160">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="6f3c2-160">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="6f3c2-161">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6f3c2-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="6f3c2-162">转换标识符</span><span class="sxs-lookup"><span data-stu-id="6f3c2-162">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

