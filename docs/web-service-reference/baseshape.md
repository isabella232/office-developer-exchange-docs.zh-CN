---
title: BaseShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: BaseShape 元素标识要在项目或文件夹响应中返回的属性集。
ms.openlocfilehash: 9b3f00ff94fbfe6ad6373b16ad95eb9136f81c64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464488"
---
# <a name="baseshape"></a><span data-ttu-id="64080-103">BaseShape</span><span class="sxs-lookup"><span data-stu-id="64080-103">BaseShape</span></span>

<span data-ttu-id="64080-104">**BaseShape**元素标识要在项目或文件夹响应中返回的属性集。</span><span class="sxs-lookup"><span data-stu-id="64080-104">The **BaseShape** element identifies the set of properties to return in an item or folder response.</span></span> 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 <span data-ttu-id="64080-105">**DefaultShapeNamesType**</span><span class="sxs-lookup"><span data-stu-id="64080-105">**DefaultShapeNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="64080-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="64080-106">Attributes and elements</span></span>

<span data-ttu-id="64080-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="64080-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64080-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="64080-108">Attributes</span></span>

<span data-ttu-id="64080-109">无。</span><span class="sxs-lookup"><span data-stu-id="64080-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64080-110">子元素</span><span class="sxs-lookup"><span data-stu-id="64080-110">Child elements</span></span>

<span data-ttu-id="64080-111">无</span><span class="sxs-lookup"><span data-stu-id="64080-111">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="64080-112">父元素</span><span class="sxs-lookup"><span data-stu-id="64080-112">Parent elements</span></span>

|<span data-ttu-id="64080-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="64080-113">**Element**</span></span>|<span data-ttu-id="64080-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="64080-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64080-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="64080-115">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="64080-116">标识要包括在 GetFolder、FindFolder 或 SyncFolderHierarchy 响应中的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="64080-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span><br/><br/><span data-ttu-id="64080-117">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="64080-117">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="64080-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="64080-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="64080-119">标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="64080-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span><br/><br/><span data-ttu-id="64080-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="64080-120">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="64080-121">文本值</span><span class="sxs-lookup"><span data-stu-id="64080-121">Text value</span></span>

<span data-ttu-id="64080-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="64080-122">A text value is required.</span></span> <span data-ttu-id="64080-123">下表列出了可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="64080-123">The following table lists the possible text values.</span></span>
  
<span data-ttu-id="64080-124">**BaseShape 元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="64080-124">**Text values for the BaseShape element**</span></span>

|<span data-ttu-id="64080-125">**值**</span><span class="sxs-lookup"><span data-stu-id="64080-125">**Value**</span></span>|<span data-ttu-id="64080-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="64080-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64080-127">IdOnly</span><span class="sxs-lookup"><span data-stu-id="64080-127">IdOnly</span></span>  <br/> |<span data-ttu-id="64080-128">仅返回项或文件夹 ID。</span><span class="sxs-lookup"><span data-stu-id="64080-128">Returns only the item or folder ID.</span></span>  <br/> |
|<span data-ttu-id="64080-129">默认</span><span class="sxs-lookup"><span data-stu-id="64080-129">Default</span></span>  <br/> |<span data-ttu-id="64080-130">返回一组属性，这些属性定义为项或文件夹的默认值。</span><span class="sxs-lookup"><span data-stu-id="64080-130">Returns a set of properties that are defined as the default for the item or folder.</span></span>  <br/> |
|<span data-ttu-id="64080-131">AllProperties</span><span class="sxs-lookup"><span data-stu-id="64080-131">AllProperties</span></span>  <br/> |<span data-ttu-id="64080-132">返回 Exchange 业务逻辑层用来构造文件夹的所有属性。</span><span class="sxs-lookup"><span data-stu-id="64080-132">Returns all the properties used by the Exchange Business Logic layer to construct a folder.</span></span>  <br/> |
   
<span data-ttu-id="64080-133">下表列出了为 FindFolder 请求返回的默认属性。</span><span class="sxs-lookup"><span data-stu-id="64080-133">The following table lists the default properties that are returned for a FindFolder request.</span></span> <span data-ttu-id="64080-134">给定文件夹的所有子文件夹按名称的顺序返回。</span><span class="sxs-lookup"><span data-stu-id="64080-134">All subfolders of a given folder are returned in order by name.</span></span>
  
<span data-ttu-id="64080-135">**默认属性**</span><span class="sxs-lookup"><span data-stu-id="64080-135">**Default properties**</span></span>

|<span data-ttu-id="64080-136">**Folder**</span><span class="sxs-lookup"><span data-stu-id="64080-136">**Folder**</span></span>|<span data-ttu-id="64080-137">**默认属性**</span><span class="sxs-lookup"><span data-stu-id="64080-137">**Default Properties**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64080-138">Inbox</span><span class="sxs-lookup"><span data-stu-id="64080-138">Inbox</span></span>  <br/> |<span data-ttu-id="64080-139">FolderId、显示名称、未读计数、总计计数、子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="64080-139">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="64080-140">联系人</span><span class="sxs-lookup"><span data-stu-id="64080-140">Contacts</span></span>  <br/> |<span data-ttu-id="64080-141">FolderId、显示名称、总计计数、子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="64080-141">FolderId, display name, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="64080-142">日历</span><span class="sxs-lookup"><span data-stu-id="64080-142">Calendar</span></span>  <br/> |<span data-ttu-id="64080-143">FolderId、显示名称、子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="64080-143">FolderId, display name, subfolder count</span></span>  <br/> |
|<span data-ttu-id="64080-144">草稿</span><span class="sxs-lookup"><span data-stu-id="64080-144">Drafts</span></span>  <br/> |<span data-ttu-id="64080-145">FolderId、显示名称、未读计数、总计计数、子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="64080-145">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="64080-146">已删除项目</span><span class="sxs-lookup"><span data-stu-id="64080-146">Deleted items</span></span>  <br/> |<span data-ttu-id="64080-147">FolderId、显示名称、未读计数、总计计数、子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="64080-147">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="64080-148">其他文件夹</span><span class="sxs-lookup"><span data-stu-id="64080-148">Other folders</span></span>  <br/> |<span data-ttu-id="64080-149">FolderId、显示名称、未读计数、总计计数、子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="64080-149">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="64080-150">发件箱</span><span class="sxs-lookup"><span data-stu-id="64080-150">Outbox</span></span>  <br/> |<span data-ttu-id="64080-151">FolderId、显示名称、未读计数、总计计数、子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="64080-151">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="64080-152">任务</span><span class="sxs-lookup"><span data-stu-id="64080-152">Tasks</span></span>  <br/> |<span data-ttu-id="64080-153">FolderId、显示名称、过期计数、总计计数、子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="64080-153">FolderId, display name, past due count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="64080-154">注释</span><span class="sxs-lookup"><span data-stu-id="64080-154">Notes</span></span>  <br/> |<span data-ttu-id="64080-155">FolderId、显示名称、总计计数、子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="64080-155">FolderId, display name, total count, subfolder count</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64080-156">备注</span><span class="sxs-lookup"><span data-stu-id="64080-156">Remarks</span></span>

<span data-ttu-id="64080-157">若要返回除[BaseShape](baseshape.md)元素标识的属性之外的属性，请使用[AdditionalProperties](additionalproperties.md)元素。</span><span class="sxs-lookup"><span data-stu-id="64080-157">To return properties in addition to those identified by the [BaseShape](baseshape.md) element, use the [AdditionalProperties](additionalproperties.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="64080-158">示例</span><span class="sxs-lookup"><span data-stu-id="64080-158">Example</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="64080-159">元素信息</span><span class="sxs-lookup"><span data-stu-id="64080-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64080-160">命名空间</span><span class="sxs-lookup"><span data-stu-id="64080-160">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="64080-161">架构名称</span><span class="sxs-lookup"><span data-stu-id="64080-161">Schema Name</span></span>  <br/> |<span data-ttu-id="64080-162">类型架构</span><span class="sxs-lookup"><span data-stu-id="64080-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="64080-163">验证文件</span><span class="sxs-lookup"><span data-stu-id="64080-163">Validation File</span></span>  <br/> |<span data-ttu-id="64080-164">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="64080-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="64080-165">可以为空</span><span class="sxs-lookup"><span data-stu-id="64080-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="64080-166">False</span><span class="sxs-lookup"><span data-stu-id="64080-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64080-167">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64080-167">See also</span></span>

- [<span data-ttu-id="64080-168">FolderShape</span><span class="sxs-lookup"><span data-stu-id="64080-168">FolderShape</span></span>](foldershape.md)
- [<span data-ttu-id="64080-169">ItemShape</span><span class="sxs-lookup"><span data-stu-id="64080-169">ItemShape</span></span>](itemshape.md)

