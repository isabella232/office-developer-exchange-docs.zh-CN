---
title: AlternatePublicFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderId
api_type:
- schema
ms.assetid: 0a4dc1cc-959e-4b93-aa3a-3020ca8b8a02
description: AlternatePublicFolderId 元素描述要转换为另一种标识符格式的公用文件夹标识符。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 54ad663117839222ea1174cd1c25600f31aa6b43
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464796"
---
# <a name="alternatepublicfolderid"></a><span data-ttu-id="c94a2-104">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="c94a2-104">AlternatePublicFolderId</span></span>

<span data-ttu-id="c94a2-105">**AlternatePublicFolderId**元素描述要转换为另一种标识符格式的公用文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="c94a2-105">The **AlternatePublicFolderId** element describes a public folder identifier to convert to another identifier format.</span></span> <span data-ttu-id="c94a2-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c94a2-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="c94a2-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="c94a2-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="c94a2-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="c94a2-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="c94a2-109">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="c94a2-109">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md)
  
```xml
<AlternatePublicFolderId FolderId="" Format="" />
```

 <span data-ttu-id="c94a2-110">**AlternatePublicFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="c94a2-110">**AlternatePublicFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c94a2-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c94a2-111">Attributes and elements</span></span>

<span data-ttu-id="c94a2-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c94a2-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c94a2-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="c94a2-113">Attributes</span></span>

|<span data-ttu-id="c94a2-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="c94a2-114">**Attribute**</span></span>|<span data-ttu-id="c94a2-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="c94a2-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c94a2-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="c94a2-116">FolderId</span></span>  <br/> |<span data-ttu-id="c94a2-117">包含要转换的公用文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="c94a2-117">Contains the public folder identifier to convert.</span></span> <span data-ttu-id="c94a2-118">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="c94a2-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="c94a2-119">Format</span><span class="sxs-lookup"><span data-stu-id="c94a2-119">Format</span></span>  <br/> |<span data-ttu-id="c94a2-120">标识描述要转换的公用文件夹标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="c94a2-120">Identifies the format that describes the public folder identifier to convert.</span></span> <span data-ttu-id="c94a2-121">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="c94a2-121">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute"></a><span data-ttu-id="c94a2-122">Format 属性</span><span class="sxs-lookup"><span data-stu-id="c94a2-122">Format attribute</span></span>

|<span data-ttu-id="c94a2-123">**值**</span><span class="sxs-lookup"><span data-stu-id="c94a2-123">**Value**</span></span>|<span data-ttu-id="c94a2-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="c94a2-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c94a2-125">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="c94a2-125">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="c94a2-126">介绍 exchange 2007 的初始发布版本中的 Exchange Web 服务生成的标识符。</span><span class="sxs-lookup"><span data-stu-id="c94a2-126">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="c94a2-127">EwsId</span><span class="sxs-lookup"><span data-stu-id="c94a2-127">EwsId</span></span>  <br/> |<span data-ttu-id="c94a2-128">介绍了 Exchange Web 服务从 Exchange 2007 SP1 开始生成的标识符。</span><span class="sxs-lookup"><span data-stu-id="c94a2-128">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="c94a2-129">EntryId</span><span class="sxs-lookup"><span data-stu-id="c94a2-129">EntryId</span></span>  <br/> |<span data-ttu-id="c94a2-130">描述 MAPI 标识符，如 PR_ENTRYID 属性中所示。</span><span class="sxs-lookup"><span data-stu-id="c94a2-130">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="c94a2-131">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="c94a2-131">HexEntryId</span></span>  <br/> |<span data-ttu-id="c94a2-132">描述了 PR_ENTRYID 属性的十六进制编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="c94a2-132">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="c94a2-133">这是可用性日历事件标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="c94a2-133">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="c94a2-134">StoreId</span><span class="sxs-lookup"><span data-stu-id="c94a2-134">StoreId</span></span>  <br/> |<span data-ttu-id="c94a2-135">描述 Exchange 存储标识符。</span><span class="sxs-lookup"><span data-stu-id="c94a2-135">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="c94a2-136">OwaId</span><span class="sxs-lookup"><span data-stu-id="c94a2-136">OwaId</span></span>  <br/> |<span data-ttu-id="c94a2-137">介绍 Outlook Web Access 标识符。</span><span class="sxs-lookup"><span data-stu-id="c94a2-137">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c94a2-138">子元素</span><span class="sxs-lookup"><span data-stu-id="c94a2-138">Child elements</span></span>

<span data-ttu-id="c94a2-139">无。</span><span class="sxs-lookup"><span data-stu-id="c94a2-139">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c94a2-140">父元素</span><span class="sxs-lookup"><span data-stu-id="c94a2-140">Parent elements</span></span>

|<span data-ttu-id="c94a2-141">**元素**</span><span class="sxs-lookup"><span data-stu-id="c94a2-141">**Element**</span></span>|<span data-ttu-id="c94a2-142">**描述**</span><span class="sxs-lookup"><span data-stu-id="c94a2-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c94a2-143">SourceIds</span><span class="sxs-lookup"><span data-stu-id="c94a2-143">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="c94a2-144">包含要转换的源标识符。</span><span class="sxs-lookup"><span data-stu-id="c94a2-144">Contains the source identifiers to convert.</span></span> <span data-ttu-id="c94a2-145">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c94a2-145">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="c94a2-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="c94a2-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c94a2-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="c94a2-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c94a2-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="c94a2-148">Schema Name</span></span>  <br/> |<span data-ttu-id="c94a2-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="c94a2-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="c94a2-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="c94a2-150">Validation File</span></span>  <br/> |<span data-ttu-id="c94a2-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c94a2-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c94a2-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="c94a2-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="c94a2-153">True</span><span class="sxs-lookup"><span data-stu-id="c94a2-153">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c94a2-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c94a2-154">See also</span></span>

- [<span data-ttu-id="c94a2-155">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="c94a2-155">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="c94a2-156">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c94a2-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="c94a2-157">转换标识符</span><span class="sxs-lookup"><span data-stu-id="c94a2-157">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

