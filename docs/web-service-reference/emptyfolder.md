---
title: EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: EmptyFolder元素定义为空对 Exchange 存储中的邮箱中的文件夹的请求。(可选) 还可以文件夹被清空时删除子文件夹。
ms.openlocfilehash: c72e11cea29e2e55c9c29754eec60e73bd1e4d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754095"
---
# <a name="emptyfolder"></a><span data-ttu-id="397f5-104">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="397f5-104">EmptyFolder</span></span>

<span data-ttu-id="397f5-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **EmptyFolder**元素定义为空对 Exchange 存储中的邮箱中的文件夹的请求。(可选) 还可以文件夹被清空时删除子文件夹。</span><span class="sxs-lookup"><span data-stu-id="397f5-p102">The **EmptyFolder** element defines a request to empty a folder in a mailbox in the Exchange store. Optionally, subfolders can also be deleted when the folder is emptied.</span></span> 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 <span data-ttu-id="397f5-107">**EmptyFolderType**</span><span class="sxs-lookup"><span data-stu-id="397f5-107">**EmptyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="397f5-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="397f5-108">Attributes and elements</span></span>

<span data-ttu-id="397f5-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="397f5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="397f5-110">属性</span><span class="sxs-lookup"><span data-stu-id="397f5-110">Attributes</span></span>

|<span data-ttu-id="397f5-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="397f5-111">**Attribute**</span></span>|<span data-ttu-id="397f5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="397f5-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="397f5-113">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="397f5-113">**DeleteType**</span></span> <br/> |<span data-ttu-id="397f5-p103">指定如何清空文件夹。此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="397f5-p103">Specifies how a folder is emptied. This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="397f5-116">**DeleteSubFolders**</span><span class="sxs-lookup"><span data-stu-id="397f5-116">**DeleteSubFolders**</span></span> <br/> |<span data-ttu-id="397f5-p104">指定是否要删除子文件夹。此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="397f5-p104">Specifies whether subfolders are to be deleted. This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="397f5-119">DeleteType 属性</span><span class="sxs-lookup"><span data-stu-id="397f5-119">DeleteType Attribute</span></span>

|<span data-ttu-id="397f5-120">**值**</span><span class="sxs-lookup"><span data-stu-id="397f5-120">**Value**</span></span>|<span data-ttu-id="397f5-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="397f5-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="397f5-122">HardDelete</span><span class="sxs-lookup"><span data-stu-id="397f5-122">HardDelete</span></span>  <br/> |<span data-ttu-id="397f5-123">一个存储区中永久删除邮件和文件夹。</span><span class="sxs-lookup"><span data-stu-id="397f5-123">A messages and folders are permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="397f5-124">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="397f5-124">SoftDelete</span></span>  <br/> |<span data-ttu-id="397f5-125">一个邮件和文件夹移动到垃圾站如果转储程序已启用。</span><span class="sxs-lookup"><span data-stu-id="397f5-125">A messages and folders are moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="397f5-126">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="397f5-126">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="397f5-127">一个邮件和文件夹移到已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="397f5-127">A messages and folders are moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="397f5-128">子元素</span><span class="sxs-lookup"><span data-stu-id="397f5-128">Child elements</span></span>

|<span data-ttu-id="397f5-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="397f5-129">**Element**</span></span>|<span data-ttu-id="397f5-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="397f5-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="397f5-131">FolderIds</span><span class="sxs-lookup"><span data-stu-id="397f5-131">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="397f5-132">包含用于标识要删除的文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="397f5-132">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="397f5-133">父元素</span><span class="sxs-lookup"><span data-stu-id="397f5-133">Parent elements</span></span>

<span data-ttu-id="397f5-134">无。</span><span class="sxs-lookup"><span data-stu-id="397f5-134">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="397f5-135">文本值</span><span class="sxs-lookup"><span data-stu-id="397f5-135">Text value</span></span>

<span data-ttu-id="397f5-136">无。</span><span class="sxs-lookup"><span data-stu-id="397f5-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="397f5-137">备注</span><span class="sxs-lookup"><span data-stu-id="397f5-137">Remarks</span></span>

<span data-ttu-id="397f5-138">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="397f5-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="397f5-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="397f5-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="397f5-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="397f5-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="397f5-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="397f5-141">Schema Name</span></span>  <br/> |<span data-ttu-id="397f5-142">消息架构</span><span class="sxs-lookup"><span data-stu-id="397f5-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="397f5-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="397f5-143">Validation File</span></span>  <br/> |<span data-ttu-id="397f5-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="397f5-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="397f5-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="397f5-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="397f5-146">False</span><span class="sxs-lookup"><span data-stu-id="397f5-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="397f5-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="397f5-147">See also</span></span>



[<span data-ttu-id="397f5-148">EmptyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="397f5-148">EmptyFolder operation</span></span>](emptyfolder-operation.md)

