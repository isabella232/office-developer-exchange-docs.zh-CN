---
title: ParentFolderId (TargetFolderIdType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 0e3e6e5f-06d0-499b-8ca4-d36036521658
description: ParentFolderId 元素标识的文件夹中创建一个新的文件夹或搜索 FindConversation 操作的文件夹。
ms.openlocfilehash: 61072e1dd3321beb5f3b76d9accf20530b443796
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826686"
---
# <a name="parentfolderid-targetfolderidtype"></a><span data-ttu-id="dee2b-103">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="dee2b-103">ParentFolderId (TargetFolderIdType)</span></span>

<span data-ttu-id="dee2b-104">**ParentFolderId**元素标识的文件夹中创建一个新的文件夹或搜索[FindConversation 操作](findconversation-operation.md)的文件夹。</span><span class="sxs-lookup"><span data-stu-id="dee2b-104">The **ParentFolderId** element identifies the folder in which a new folder is created or the folder to search for the [FindConversation operation](findconversation-operation.md).</span></span>
  
```xml
<ParentFolderId>
   <DistinguishedFolderId/>
</ParentFolderId>
```

<span data-ttu-id="dee2b-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="dee2b-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dee2b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dee2b-106">Attributes and elements</span></span>

<span data-ttu-id="dee2b-107">**ParentFolderId**元素包含两个子元素。</span><span class="sxs-lookup"><span data-stu-id="dee2b-107">The **ParentFolderId** element contains two child elements.</span></span> <span data-ttu-id="dee2b-108">子元素的架构中相互排斥。</span><span class="sxs-lookup"><span data-stu-id="dee2b-108">The child elements are mutually exclusive in the schema.</span></span> 
  
### <a name="attributes"></a><span data-ttu-id="dee2b-109">属性</span><span class="sxs-lookup"><span data-stu-id="dee2b-109">Attributes</span></span>

<span data-ttu-id="dee2b-110">无。</span><span class="sxs-lookup"><span data-stu-id="dee2b-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dee2b-111">子元素</span><span class="sxs-lookup"><span data-stu-id="dee2b-111">Child elements</span></span>

|<span data-ttu-id="dee2b-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="dee2b-112">**Element**</span></span>|<span data-ttu-id="dee2b-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="dee2b-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dee2b-114">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="dee2b-114">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="dee2b-115">包含所需的标识符和文件夹中的可选更改密钥其创建一个新文件夹或[FindConversation 操作](findconversation-operation.md)搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="dee2b-115">Contains the required identifier and the optional change key of a folder in which a new folder is created or the folder that is searched for the [FindConversation operation](findconversation-operation.md).</span></span> <span data-ttu-id="dee2b-116">使用此元素不包括[DistinguishedFolderId](distinguishedfolderid.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="dee2b-116">Using this element excludes the use of the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="dee2b-117">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="dee2b-117">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="dee2b-118">标识默认的 Microsoft Exchange Server 2007 文件夹。</span><span class="sxs-lookup"><span data-stu-id="dee2b-118">Identifies default Microsoft Exchange Server 2007 folders.</span></span> <span data-ttu-id="dee2b-119">使用此元素不包括[文件夹 Id](folderid.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="dee2b-119">Using this element excludes the use of the [FolderId](folderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dee2b-120">父元素</span><span class="sxs-lookup"><span data-stu-id="dee2b-120">Parent elements</span></span>

|<span data-ttu-id="dee2b-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="dee2b-121">**Element**</span></span>|<span data-ttu-id="dee2b-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="dee2b-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dee2b-123">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="dee2b-123">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="dee2b-124">定义一个请求 Exchange 数据库中创建文件夹。</span><span class="sxs-lookup"><span data-stu-id="dee2b-124">Defines a request to create a folder in the Exchange database.</span></span>  <br/> <span data-ttu-id="dee2b-125">下面是此元素的 XPath 表达式:  `/CreateFolder`</span><span class="sxs-lookup"><span data-stu-id="dee2b-125">The following is the XPath expression to this element:  `/CreateFolder`</span></span> <br/> |
|[<span data-ttu-id="dee2b-126">FindConversation</span><span class="sxs-lookup"><span data-stu-id="dee2b-126">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="dee2b-127">定义查找邮箱中的对话的请求。</span><span class="sxs-lookup"><span data-stu-id="dee2b-127">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dee2b-128">文本值</span><span class="sxs-lookup"><span data-stu-id="dee2b-128">Text value</span></span>

<span data-ttu-id="dee2b-129">无。</span><span class="sxs-lookup"><span data-stu-id="dee2b-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dee2b-130">注解</span><span class="sxs-lookup"><span data-stu-id="dee2b-130">Remarks</span></span>

<span data-ttu-id="dee2b-131">两个子元素用于定义将包含新文件夹的文件夹。</span><span class="sxs-lookup"><span data-stu-id="dee2b-131">The two child elements are used to define the folder that will contain the new folder.</span></span> <span data-ttu-id="dee2b-132">您必须选择[文件夹 Id](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素来标识新的文件夹的父文件夹。</span><span class="sxs-lookup"><span data-stu-id="dee2b-132">You must select either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element to identify the parent folder of the new folder.</span></span> <span data-ttu-id="dee2b-133">不能同时使用这两个元素。</span><span class="sxs-lookup"><span data-stu-id="dee2b-133">You cannot use both elements at the same time.</span></span> <span data-ttu-id="dee2b-134">此元素需要创建文件夹。</span><span class="sxs-lookup"><span data-stu-id="dee2b-134">This element is required to create folders.</span></span> 
  
<span data-ttu-id="dee2b-135">[ParentFolderId](parentfolderid.md)元素描述现有项目和文件夹的位置。</span><span class="sxs-lookup"><span data-stu-id="dee2b-135">The [ParentFolderId](parentfolderid.md) element describes the location of existing items and folders.</span></span> 
  
<span data-ttu-id="dee2b-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dee2b-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dee2b-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="dee2b-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dee2b-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="dee2b-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dee2b-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="dee2b-139">Schema Name</span></span>  <br/> |<span data-ttu-id="dee2b-140">消息架构</span><span class="sxs-lookup"><span data-stu-id="dee2b-140">Message schema</span></span>  <br/> |
|<span data-ttu-id="dee2b-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="dee2b-141">Validation File</span></span>  <br/> |<span data-ttu-id="dee2b-142">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dee2b-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dee2b-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="dee2b-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="dee2b-144">False</span><span class="sxs-lookup"><span data-stu-id="dee2b-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dee2b-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dee2b-145">See also</span></span>

- [<span data-ttu-id="dee2b-146">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="dee2b-146">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="dee2b-147">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="dee2b-147">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="dee2b-148">Creating Folders (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="dee2b-148">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

