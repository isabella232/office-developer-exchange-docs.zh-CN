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
description: AlternatePublicFolderId 元素描述将转换为另一个标识符格式的公用文件夹标识符。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 32e6e75eb381e479baf5fdb5ad0a40b32c1b02a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753145"
---
# <a name="alternatepublicfolderid"></a><span data-ttu-id="fcaa8-104">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="fcaa8-104">AlternatePublicFolderId</span></span>

<span data-ttu-id="fcaa8-105">**AlternatePublicFolderId**元素描述将转换为另一个标识符格式的公用文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-105">The **AlternatePublicFolderId** element describes a public folder identifier to convert to another identifier format.</span></span> <span data-ttu-id="fcaa8-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="fcaa8-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="fcaa8-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="fcaa8-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="fcaa8-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="fcaa8-109">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="fcaa8-109">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md)
  
```xml
<AlternatePublicFolderId FolderId="" Format="" />
```

 <span data-ttu-id="fcaa8-110">**AlternatePublicFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="fcaa8-110">**AlternatePublicFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fcaa8-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fcaa8-111">Attributes and elements</span></span>

<span data-ttu-id="fcaa8-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fcaa8-113">属性</span><span class="sxs-lookup"><span data-stu-id="fcaa8-113">Attributes</span></span>

|<span data-ttu-id="fcaa8-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="fcaa8-114">**Attribute**</span></span>|<span data-ttu-id="fcaa8-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="fcaa8-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fcaa8-116">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="fcaa8-116">FolderId</span></span>  <br/> |<span data-ttu-id="fcaa8-117">包含要转换的公用文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-117">Contains the public folder identifier to convert.</span></span> <span data-ttu-id="fcaa8-118">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="fcaa8-119">格式</span><span class="sxs-lookup"><span data-stu-id="fcaa8-119">Format</span></span>  <br/> |<span data-ttu-id="fcaa8-120">标识描述要转换的公用文件夹标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-120">Identifies the format that describes the public folder identifier to convert.</span></span> <span data-ttu-id="fcaa8-121">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-121">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute"></a><span data-ttu-id="fcaa8-122">Format 属性</span><span class="sxs-lookup"><span data-stu-id="fcaa8-122">Format attribute</span></span>

|<span data-ttu-id="fcaa8-123">**值**</span><span class="sxs-lookup"><span data-stu-id="fcaa8-123">**Value**</span></span>|<span data-ttu-id="fcaa8-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="fcaa8-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fcaa8-125">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="fcaa8-125">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="fcaa8-126">描述所产生的 Exchange Web 服务的初始发行版本的 Exchange 2007 中的标识符。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-126">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="fcaa8-127">EwsId</span><span class="sxs-lookup"><span data-stu-id="fcaa8-127">EwsId</span></span>  <br/> |<span data-ttu-id="fcaa8-128">描述所产生的开头 Exchange 2007 SP1 的 Exchange Web 服务的标识符。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-128">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="fcaa8-129">EntryId</span><span class="sxs-lookup"><span data-stu-id="fcaa8-129">EntryId</span></span>  <br/> |<span data-ttu-id="fcaa8-130">描述 MAPI 标识符，如 PR_ENTRYID 属性中所示。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-130">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="fcaa8-131">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="fcaa8-131">HexEntryId</span></span>  <br/> |<span data-ttu-id="fcaa8-132">介绍 PR_ENTRYID 属性的十六进制编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-132">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="fcaa8-133">这是可用性日历事件标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-133">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="fcaa8-134">StoreId</span><span class="sxs-lookup"><span data-stu-id="fcaa8-134">StoreId</span></span>  <br/> |<span data-ttu-id="fcaa8-135">描述 Exchange 存储区标识符。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-135">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="fcaa8-136">OwaId</span><span class="sxs-lookup"><span data-stu-id="fcaa8-136">OwaId</span></span>  <br/> |<span data-ttu-id="fcaa8-137">介绍 Outlook Web Access 标识符。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-137">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fcaa8-138">子元素</span><span class="sxs-lookup"><span data-stu-id="fcaa8-138">Child elements</span></span>

<span data-ttu-id="fcaa8-139">无。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-139">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fcaa8-140">父元素</span><span class="sxs-lookup"><span data-stu-id="fcaa8-140">Parent elements</span></span>

|<span data-ttu-id="fcaa8-141">**元素**</span><span class="sxs-lookup"><span data-stu-id="fcaa8-141">**Element**</span></span>|<span data-ttu-id="fcaa8-142">**说明**</span><span class="sxs-lookup"><span data-stu-id="fcaa8-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fcaa8-143">SourceIds</span><span class="sxs-lookup"><span data-stu-id="fcaa8-143">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="fcaa8-144">包含要转换的源标识符。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-144">Contains the source identifiers to convert.</span></span> <span data-ttu-id="fcaa8-145">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fcaa8-145">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="fcaa8-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="fcaa8-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcaa8-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="fcaa8-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fcaa8-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="fcaa8-148">Schema Name</span></span>  <br/> |<span data-ttu-id="fcaa8-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="fcaa8-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="fcaa8-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="fcaa8-150">Validation File</span></span>  <br/> |<span data-ttu-id="fcaa8-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fcaa8-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fcaa8-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="fcaa8-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="fcaa8-153">True</span><span class="sxs-lookup"><span data-stu-id="fcaa8-153">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcaa8-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fcaa8-154">See also</span></span>

- [<span data-ttu-id="fcaa8-155">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="fcaa8-155">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="fcaa8-156">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fcaa8-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="fcaa8-157">转换标识符</span><span class="sxs-lookup"><span data-stu-id="fcaa8-157">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

