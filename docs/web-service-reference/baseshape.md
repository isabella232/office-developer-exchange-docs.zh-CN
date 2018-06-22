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
description: BaseShape 元素标识项目或文件夹响应中返回的属性的集。
ms.openlocfilehash: 69b27d23fd75d4c1a274f31dfa419b759dbb2bbe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753323"
---
# <a name="baseshape"></a><span data-ttu-id="6ac3d-103">BaseShape</span><span class="sxs-lookup"><span data-stu-id="6ac3d-103">BaseShape</span></span>

<span data-ttu-id="6ac3d-104">**BaseShape**元素标识项目或文件夹响应中返回的属性的集。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-104">The **BaseShape** element identifies the set of properties to return in an item or folder response.</span></span> 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 <span data-ttu-id="6ac3d-105">**DefaultShapeNamesType**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-105">**DefaultShapeNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ac3d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6ac3d-106">Attributes and elements</span></span>

<span data-ttu-id="6ac3d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ac3d-108">属性</span><span class="sxs-lookup"><span data-stu-id="6ac3d-108">Attributes</span></span>

<span data-ttu-id="6ac3d-109">无。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ac3d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6ac3d-110">Child elements</span></span>

<span data-ttu-id="6ac3d-111">无</span><span class="sxs-lookup"><span data-stu-id="6ac3d-111">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6ac3d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6ac3d-112">Parent elements</span></span>

|<span data-ttu-id="6ac3d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-113">**Element**</span></span>|<span data-ttu-id="6ac3d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ac3d-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="6ac3d-115">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="6ac3d-116">标识要在 GetFolder、 FindFolder 或 SyncFolderHierarchy 响应中包含的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span><br/><br/><span data-ttu-id="6ac3d-117">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="6ac3d-117">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="6ac3d-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="6ac3d-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="6ac3d-119">标识项目属性和 GetItem、 FindItem 或 SyncFolderItems 响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span><br/><br/><span data-ttu-id="6ac3d-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="6ac3d-120">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6ac3d-121">文本值</span><span class="sxs-lookup"><span data-stu-id="6ac3d-121">Text value</span></span>

<span data-ttu-id="6ac3d-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-122">A text value is required.</span></span> <span data-ttu-id="6ac3d-123">下表列出了可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-123">The following table lists the possible text values.</span></span>
  
<span data-ttu-id="6ac3d-124">**BaseShape 元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-124">**Text values for the BaseShape element**</span></span>

|<span data-ttu-id="6ac3d-125">**值**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-125">**Value**</span></span>|<span data-ttu-id="6ac3d-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ac3d-127">IdOnly</span><span class="sxs-lookup"><span data-stu-id="6ac3d-127">IdOnly</span></span>  <br/> |<span data-ttu-id="6ac3d-128">返回仅项目或文件夹的 id。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-128">Returns only the item or folder ID.</span></span>  <br/> |
|<span data-ttu-id="6ac3d-129">默认</span><span class="sxs-lookup"><span data-stu-id="6ac3d-129">Default</span></span>  <br/> |<span data-ttu-id="6ac3d-130">返回一组定义为项目或文件夹的默认属性。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-130">Returns a set of properties that are defined as the default for the item or folder.</span></span>  <br/> |
|<span data-ttu-id="6ac3d-131">AllProperties</span><span class="sxs-lookup"><span data-stu-id="6ac3d-131">AllProperties</span></span>  <br/> |<span data-ttu-id="6ac3d-132">返回所有 Exchange 业务逻辑层用于构造文件夹的属性。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-132">Returns all the properties used by the Exchange Business Logic layer to construct a folder.</span></span>  <br/> |
   
<span data-ttu-id="6ac3d-133">下表列出了 FindFolder 请求返回的默认属性。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-133">The following table lists the default properties that are returned for a FindFolder request.</span></span> <span data-ttu-id="6ac3d-134">按名称顺序返回给定文件夹的所有子文件夹。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-134">All subfolders of a given folder are returned in order by name.</span></span>
  
<span data-ttu-id="6ac3d-135">**默认属性**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-135">**Default properties**</span></span>

|<span data-ttu-id="6ac3d-136">**Folder**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-136">**Folder**</span></span>|<span data-ttu-id="6ac3d-137">**默认属性**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-137">**Default Properties**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ac3d-138">Inbox</span><span class="sxs-lookup"><span data-stu-id="6ac3d-138">Inbox</span></span>  <br/> |<span data-ttu-id="6ac3d-139">文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数</span><span class="sxs-lookup"><span data-stu-id="6ac3d-139">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6ac3d-140">联系人</span><span class="sxs-lookup"><span data-stu-id="6ac3d-140">Contacts</span></span>  <br/> |<span data-ttu-id="6ac3d-141">文件夹 Id，显示名称、 总计、 子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="6ac3d-141">FolderId, display name, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6ac3d-142">日历</span><span class="sxs-lookup"><span data-stu-id="6ac3d-142">Calendar</span></span>  <br/> |<span data-ttu-id="6ac3d-143">文件夹 Id，显示名称子文件夹数</span><span class="sxs-lookup"><span data-stu-id="6ac3d-143">FolderId, display name, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6ac3d-144">草稿</span><span class="sxs-lookup"><span data-stu-id="6ac3d-144">Drafts</span></span>  <br/> |<span data-ttu-id="6ac3d-145">文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数</span><span class="sxs-lookup"><span data-stu-id="6ac3d-145">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6ac3d-146">已删除的项目</span><span class="sxs-lookup"><span data-stu-id="6ac3d-146">Deleted items</span></span>  <br/> |<span data-ttu-id="6ac3d-147">文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数</span><span class="sxs-lookup"><span data-stu-id="6ac3d-147">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6ac3d-148">其他文件夹</span><span class="sxs-lookup"><span data-stu-id="6ac3d-148">Other folders</span></span>  <br/> |<span data-ttu-id="6ac3d-149">文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数</span><span class="sxs-lookup"><span data-stu-id="6ac3d-149">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6ac3d-150">发件箱</span><span class="sxs-lookup"><span data-stu-id="6ac3d-150">Outbox</span></span>  <br/> |<span data-ttu-id="6ac3d-151">文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数</span><span class="sxs-lookup"><span data-stu-id="6ac3d-151">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6ac3d-152">任务</span><span class="sxs-lookup"><span data-stu-id="6ac3d-152">Tasks</span></span>  <br/> |<span data-ttu-id="6ac3d-153">文件夹 Id，显示名称过去截止计数、 总计、 子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="6ac3d-153">FolderId, display name, past due count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6ac3d-154">笔记</span><span class="sxs-lookup"><span data-stu-id="6ac3d-154">Notes</span></span>  <br/> |<span data-ttu-id="6ac3d-155">文件夹 Id，显示名称、 总计、 子文件夹计数</span><span class="sxs-lookup"><span data-stu-id="6ac3d-155">FolderId, display name, total count, subfolder count</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ac3d-156">备注</span><span class="sxs-lookup"><span data-stu-id="6ac3d-156">Remarks</span></span>

<span data-ttu-id="6ac3d-157">若要返回除外标识[BaseShape](baseshape.md)元素的属性，请使用[AdditionalProperties](additionalproperties.md)元素。</span><span class="sxs-lookup"><span data-stu-id="6ac3d-157">To return properties in addition to those identified by the [BaseShape](baseshape.md) element, use the [AdditionalProperties](additionalproperties.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6ac3d-158">示例</span><span class="sxs-lookup"><span data-stu-id="6ac3d-158">Example</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="6ac3d-159">元素信息</span><span class="sxs-lookup"><span data-stu-id="6ac3d-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ac3d-160">命名空间</span><span class="sxs-lookup"><span data-stu-id="6ac3d-160">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6ac3d-161">架构名称</span><span class="sxs-lookup"><span data-stu-id="6ac3d-161">Schema Name</span></span>  <br/> |<span data-ttu-id="6ac3d-162">类型架构</span><span class="sxs-lookup"><span data-stu-id="6ac3d-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="6ac3d-163">验证文件</span><span class="sxs-lookup"><span data-stu-id="6ac3d-163">Validation File</span></span>  <br/> |<span data-ttu-id="6ac3d-164">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6ac3d-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6ac3d-165">可以为空</span><span class="sxs-lookup"><span data-stu-id="6ac3d-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ac3d-166">False</span><span class="sxs-lookup"><span data-stu-id="6ac3d-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ac3d-167">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6ac3d-167">See also</span></span>

- [<span data-ttu-id="6ac3d-168">FolderShape</span><span class="sxs-lookup"><span data-stu-id="6ac3d-168">FolderShape</span></span>](foldershape.md)
- [<span data-ttu-id="6ac3d-169">ItemShape</span><span class="sxs-lookup"><span data-stu-id="6ac3d-169">ItemShape</span></span>](itemshape.md)

