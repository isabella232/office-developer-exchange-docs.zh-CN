---
title: DeleteFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: e37963f4-af9e-4481-b389-16175711e66d
description: DeleteFolder元素定义删除从 Exchange 存储中的邮箱文件夹的请求。
ms.openlocfilehash: eb705a47b78b19c79b2e87561ba3696ed40e09cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458766"
---
# <a name="deletefolder"></a><span data-ttu-id="d41c1-103">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="d41c1-103">DeleteFolder</span></span>

<span data-ttu-id="d41c1-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **DeleteFolder**元素定义删除从 Exchange 存储中的邮箱文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="d41c1-104">The **DeleteFolder** element defines a request to delete folders from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 <span data-ttu-id="d41c1-105">**DeleteFolderType**</span><span class="sxs-lookup"><span data-stu-id="d41c1-105">**DeleteFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d41c1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d41c1-106">Attributes and elements</span></span>

<span data-ttu-id="d41c1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d41c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d41c1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d41c1-108">Attributes</span></span>

|<span data-ttu-id="d41c1-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="d41c1-109">**Attribute**</span></span>|<span data-ttu-id="d41c1-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="d41c1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d41c1-111">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="d41c1-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="d41c1-p101">描述如何删除一个文件夹。此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="d41c1-p101">Describes how a folder is deleted. This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="d41c1-114">DeleteType 属性</span><span class="sxs-lookup"><span data-stu-id="d41c1-114">DeleteType attribute</span></span>

|<span data-ttu-id="d41c1-115">**值**</span><span class="sxs-lookup"><span data-stu-id="d41c1-115">**Value**</span></span>|<span data-ttu-id="d41c1-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="d41c1-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d41c1-117">HardDelete</span><span class="sxs-lookup"><span data-stu-id="d41c1-117">HardDelete</span></span>  <br/> |<span data-ttu-id="d41c1-118">从存储区中永久移除文件夹。</span><span class="sxs-lookup"><span data-stu-id="d41c1-118">A folder is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="d41c1-119">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="d41c1-119">SoftDelete</span></span>  <br/> |<span data-ttu-id="d41c1-120">一个文件夹移动到垃圾站如果转储程序已启用。</span><span class="sxs-lookup"><span data-stu-id="d41c1-120">A folder is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="d41c1-121">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="d41c1-121">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="d41c1-122">文件夹被移动到已删除邮件文件夹中。</span><span class="sxs-lookup"><span data-stu-id="d41c1-122">A folder is moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d41c1-123">子元素</span><span class="sxs-lookup"><span data-stu-id="d41c1-123">Child elements</span></span>

|<span data-ttu-id="d41c1-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="d41c1-124">**Element**</span></span>|<span data-ttu-id="d41c1-125">**描述**</span><span class="sxs-lookup"><span data-stu-id="d41c1-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d41c1-126">FolderIds</span><span class="sxs-lookup"><span data-stu-id="d41c1-126">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="d41c1-127">包含用于标识要删除的文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="d41c1-127">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d41c1-128">父元素</span><span class="sxs-lookup"><span data-stu-id="d41c1-128">Parent elements</span></span>

<span data-ttu-id="d41c1-129">无。</span><span class="sxs-lookup"><span data-stu-id="d41c1-129">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d41c1-130">文本值</span><span class="sxs-lookup"><span data-stu-id="d41c1-130">Text value</span></span>

<span data-ttu-id="d41c1-131">无。</span><span class="sxs-lookup"><span data-stu-id="d41c1-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d41c1-132">说明</span><span class="sxs-lookup"><span data-stu-id="d41c1-132">Remarks</span></span>

<span data-ttu-id="d41c1-p102">**MoveToDeletedItems** 和 **HardDelete** 选项是事务性的这意味着，Web 服务调用完成时，数据库将邮件移至已删除邮件文件夹或从Exchange数据库中永久删除该项目。这种行为是相同的MicrosoftExchange Server 2007和Exchange Server 2010。</span><span class="sxs-lookup"><span data-stu-id="d41c1-p102">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database. This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="d41c1-135">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d41c1-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d41c1-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="d41c1-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d41c1-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="d41c1-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d41c1-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="d41c1-138">Schema Name</span></span>  <br/> |<span data-ttu-id="d41c1-139">消息架构</span><span class="sxs-lookup"><span data-stu-id="d41c1-139">Message schema</span></span>  <br/> |
|<span data-ttu-id="d41c1-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="d41c1-140">Validation File</span></span>  <br/> |<span data-ttu-id="d41c1-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d41c1-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d41c1-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="d41c1-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="d41c1-143">False</span><span class="sxs-lookup"><span data-stu-id="d41c1-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d41c1-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d41c1-144">See also</span></span>

- [<span data-ttu-id="d41c1-145">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="d41c1-145">DeleteFolder operation</span></span>](deletefolder-operation.md)

