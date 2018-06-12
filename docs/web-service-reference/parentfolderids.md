---
title: ParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderIds
api_type:
- schema
ms.assetid: e7998023-e5e0-465c-91fa-2aa6d1559f64
description: ParentFolderIds 元素标识 FindItem 和 FindFolder 操作搜索的文件夹。
ms.openlocfilehash: 4dd23b45dcc397e29e67fc08b29dd773e50f0db1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826688"
---
# <a name="parentfolderids"></a><span data-ttu-id="e1c33-103">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="e1c33-103">ParentFolderIds</span></span>

<span data-ttu-id="e1c33-104">**ParentFolderIds**元素标识 FindItem 和 FindFolder 操作搜索的文件夹。</span><span class="sxs-lookup"><span data-stu-id="e1c33-104">The **ParentFolderIds** element identifies folders for the FindItem and FindFolder operations to search.</span></span> 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
<ParentFolderIds>
```

<span data-ttu-id="e1c33-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="e1c33-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e1c33-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e1c33-106">Attributes and elements</span></span>

<span data-ttu-id="e1c33-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e1c33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1c33-108">属性</span><span class="sxs-lookup"><span data-stu-id="e1c33-108">Attributes</span></span>

<span data-ttu-id="e1c33-109">无。</span><span class="sxs-lookup"><span data-stu-id="e1c33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e1c33-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e1c33-110">Child elements</span></span>

|<span data-ttu-id="e1c33-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e1c33-111">**Element**</span></span>|<span data-ttu-id="e1c33-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e1c33-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1c33-113">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="e1c33-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="e1c33-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="e1c33-114">Contains the identifier and change key of a folder.</span></span> <span data-ttu-id="e1c33-115">此元素或[DistinguishedFolderId](distinguishedfolderid.md)元素，则必须使用**ParentFolderIds**元素。</span><span class="sxs-lookup"><span data-stu-id="e1c33-115">The **ParentFolderIds** element must use either this element or the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="e1c33-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="e1c33-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="e1c33-117">标识可以通过名称引用的 Microsoft Exchange Server 2007 文件夹。</span><span class="sxs-lookup"><span data-stu-id="e1c33-117">Identifies Microsoft Exchange Server 2007 folders that can be referenced by name.</span></span> <span data-ttu-id="e1c33-118">此元素或[文件夹 Id](folderid.md)元素，则必须使用**ParentFolderIds**元素。</span><span class="sxs-lookup"><span data-stu-id="e1c33-118">The **ParentFolderIds** element must use either this element or the [FolderId](folderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e1c33-119">父元素</span><span class="sxs-lookup"><span data-stu-id="e1c33-119">Parent elements</span></span>

|<span data-ttu-id="e1c33-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="e1c33-120">**Element**</span></span>|<span data-ttu-id="e1c33-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="e1c33-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1c33-122">FindFolder</span><span class="sxs-lookup"><span data-stu-id="e1c33-122">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="e1c33-123">定义一个请求，以确定邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="e1c33-123">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e1c33-124">FindItem</span><span class="sxs-lookup"><span data-stu-id="e1c33-124">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="e1c33-125">定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="e1c33-125">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e1c33-126">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e1c33-126">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="e1c33-127">定义请求解析模糊名称。</span><span class="sxs-lookup"><span data-stu-id="e1c33-127">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1c33-128">备注</span><span class="sxs-lookup"><span data-stu-id="e1c33-128">Remarks</span></span>

<span data-ttu-id="e1c33-129">[文件夹 Id](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素，则必须使用**ParentFolderIds**元素。</span><span class="sxs-lookup"><span data-stu-id="e1c33-129">The **ParentFolderIds** element must use either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> <span data-ttu-id="e1c33-130">搜索可以定义任意的数量的文件夹。</span><span class="sxs-lookup"><span data-stu-id="e1c33-130">An unlimited number of folders can be defined for the search.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e1c33-131">示例</span><span class="sxs-lookup"><span data-stu-id="e1c33-131">Example</span></span>

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

## <a name="element-information"></a><span data-ttu-id="e1c33-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="e1c33-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1c33-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="e1c33-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e1c33-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="e1c33-134">Schema Name</span></span>  <br/> |<span data-ttu-id="e1c33-135">消息架构</span><span class="sxs-lookup"><span data-stu-id="e1c33-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e1c33-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="e1c33-136">Validation File</span></span>  <br/> |<span data-ttu-id="e1c33-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e1c33-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e1c33-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="e1c33-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="e1c33-139">False</span><span class="sxs-lookup"><span data-stu-id="e1c33-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1c33-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e1c33-140">See also</span></span>

- [<span data-ttu-id="e1c33-141">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="e1c33-141">FindFolder operation</span></span>](findfolder-operation.md)  
- [<span data-ttu-id="e1c33-142">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="e1c33-142">FindItem operation</span></span>](finditem-operation.md) 
- [<span data-ttu-id="e1c33-143">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="e1c33-143">ResolveNames operation</span></span>](resolvenames-operation.md)
