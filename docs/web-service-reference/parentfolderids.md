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
description: ParentFolderIds 元素标识用于搜索的 FindItem 和 FindFolder 操作的文件夹。
ms.openlocfilehash: 6bc4b9cfe96c6c83cbeb623ec176e33177356bbc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465427"
---
# <a name="parentfolderids"></a><span data-ttu-id="838e0-103">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="838e0-103">ParentFolderIds</span></span>

<span data-ttu-id="838e0-104">**ParentFolderIds**元素标识用于搜索的 FindItem 和 FindFolder 操作的文件夹。</span><span class="sxs-lookup"><span data-stu-id="838e0-104">The **ParentFolderIds** element identifies folders for the FindItem and FindFolder operations to search.</span></span> 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
<ParentFolderIds>
```

```xml
<ParentFolderIds>
   <FolderId/> 
<ParentFolderIds>
```

<span data-ttu-id="838e0-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="838e0-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="838e0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="838e0-106">Attributes and elements</span></span>

<span data-ttu-id="838e0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="838e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="838e0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="838e0-108">Attributes</span></span>

<span data-ttu-id="838e0-109">无。</span><span class="sxs-lookup"><span data-stu-id="838e0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="838e0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="838e0-110">Child elements</span></span>

|<span data-ttu-id="838e0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="838e0-111">**Element**</span></span>|<span data-ttu-id="838e0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="838e0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="838e0-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="838e0-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="838e0-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="838e0-114">Contains the identifier and change key of a folder.</span></span> <span data-ttu-id="838e0-115">**ParentFolderIds**元素必须使用此元素或[DistinguishedFolderId](distinguishedfolderid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="838e0-115">The **ParentFolderIds** element must use either this element or the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="838e0-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="838e0-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="838e0-117">标识可通过名称引用的 Microsoft Exchange Server 2007 文件夹。</span><span class="sxs-lookup"><span data-stu-id="838e0-117">Identifies Microsoft Exchange Server 2007 folders that can be referenced by name.</span></span> <span data-ttu-id="838e0-118">**ParentFolderIds**元素必须使用此元素或[FolderId](folderid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="838e0-118">The **ParentFolderIds** element must use either this element or the [FolderId](folderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="838e0-119">父元素</span><span class="sxs-lookup"><span data-stu-id="838e0-119">Parent elements</span></span>

|<span data-ttu-id="838e0-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="838e0-120">**Element**</span></span>|<span data-ttu-id="838e0-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="838e0-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="838e0-122">FindFolder</span><span class="sxs-lookup"><span data-stu-id="838e0-122">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="838e0-123">定义用于标识邮箱中的文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="838e0-123">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="838e0-124">FindItem</span><span class="sxs-lookup"><span data-stu-id="838e0-124">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="838e0-125">定义在邮箱中查找项目的请求。</span><span class="sxs-lookup"><span data-stu-id="838e0-125">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="838e0-126">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="838e0-126">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="838e0-127">定义用于解析不明确名称的请求。</span><span class="sxs-lookup"><span data-stu-id="838e0-127">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="838e0-128">备注</span><span class="sxs-lookup"><span data-stu-id="838e0-128">Remarks</span></span>

<span data-ttu-id="838e0-129">**ParentFolderIds**元素必须使用[FolderId](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="838e0-129">The **ParentFolderIds** element must use either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> <span data-ttu-id="838e0-130">可以为搜索定义无限制数量的文件夹。</span><span class="sxs-lookup"><span data-stu-id="838e0-130">An unlimited number of folders can be defined for the search.</span></span> 
  
## <a name="example"></a><span data-ttu-id="838e0-131">示例</span><span class="sxs-lookup"><span data-stu-id="838e0-131">Example</span></span>

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

## <a name="element-information"></a><span data-ttu-id="838e0-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="838e0-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="838e0-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="838e0-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="838e0-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="838e0-134">Schema Name</span></span>  <br/> |<span data-ttu-id="838e0-135">消息架构</span><span class="sxs-lookup"><span data-stu-id="838e0-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="838e0-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="838e0-136">Validation File</span></span>  <br/> |<span data-ttu-id="838e0-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="838e0-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="838e0-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="838e0-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="838e0-139">False</span><span class="sxs-lookup"><span data-stu-id="838e0-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="838e0-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="838e0-140">See also</span></span>

- [<span data-ttu-id="838e0-141">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="838e0-141">FindFolder operation</span></span>](findfolder-operation.md)  
- [<span data-ttu-id="838e0-142">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="838e0-142">FindItem operation</span></span>](finditem-operation.md) 
- [<span data-ttu-id="838e0-143">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="838e0-143">ResolveNames operation</span></span>](resolvenames-operation.md)

