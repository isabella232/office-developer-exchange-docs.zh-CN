---
title: ToFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ToFolderId
api_type:
- schema
ms.assetid: bd6a4265-ad40-43f6-bcc4-0bf5df4e984c
description: ToFolderId 元素均表示复制或移动项目或文件夹的目标的文件夹。
ms.openlocfilehash: 9d2fd6c177711cfe3a5d3415320440259e2f5289
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353656"
---
# <a name="tofolderid"></a><span data-ttu-id="f3c79-103">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="f3c79-103">ToFolderId</span></span>

<span data-ttu-id="f3c79-104">**ToFolderId**元素均表示复制或移动项目或文件夹的目标的文件夹。</span><span class="sxs-lookup"><span data-stu-id="f3c79-104">The **ToFolderId** element represents the destination folder for a copied or moved item or folder.</span></span> 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

```xml
<ToFolderId>
   <DistinguishedFolderId/>
</ToFolderId>
```

<span data-ttu-id="f3c79-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="f3c79-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f3c79-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f3c79-106">Attributes and elements</span></span>

<span data-ttu-id="f3c79-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f3c79-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3c79-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f3c79-108">Attributes</span></span>

<span data-ttu-id="f3c79-109">无。</span><span class="sxs-lookup"><span data-stu-id="f3c79-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3c79-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f3c79-110">Child elements</span></span>

|<span data-ttu-id="f3c79-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f3c79-111">**Element**</span></span>|<span data-ttu-id="f3c79-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3c79-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3c79-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="f3c79-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="f3c79-114">包含用于复制或移动的项或文件夹的目标文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="f3c79-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="f3c79-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="f3c79-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="f3c79-116">标识命名的目标文件夹复制或移动的项或文件夹。</span><span class="sxs-lookup"><span data-stu-id="f3c79-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f3c79-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f3c79-117">Parent elements</span></span>

|<span data-ttu-id="f3c79-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="f3c79-118">**Element**</span></span>|<span data-ttu-id="f3c79-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3c79-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3c79-120">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="f3c79-120">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="f3c79-121">定义将文件夹移 Exchange 存储中的请求。</span><span class="sxs-lookup"><span data-stu-id="f3c79-121">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="f3c79-122">下面是此元素的 XPath 表达式:  </span><span class="sxs-lookup"><span data-stu-id="f3c79-122">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveFolder` <br/> |
|[<span data-ttu-id="f3c79-123">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="f3c79-123">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="f3c79-124">定义在 Exchange 存储中复制文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="f3c79-124">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="f3c79-125">下面是此元素的 XPath 表达式:  </span><span class="sxs-lookup"><span data-stu-id="f3c79-125">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyFolder` <br/> |
|[<span data-ttu-id="f3c79-126">MoveItem</span><span class="sxs-lookup"><span data-stu-id="f3c79-126">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="f3c79-127">定义在 Exchange 存储中移动项目的请求。</span><span class="sxs-lookup"><span data-stu-id="f3c79-127">Defines a request to move an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="f3c79-128">下面是此元素的 XPath 表达式:  </span><span class="sxs-lookup"><span data-stu-id="f3c79-128">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="f3c79-129">CopyItem</span><span class="sxs-lookup"><span data-stu-id="f3c79-129">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="f3c79-130">定义在 Exchange 存储中复制项的请求。</span><span class="sxs-lookup"><span data-stu-id="f3c79-130">Defines a request to copy an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="f3c79-131">下面是此元素的 XPath 表达式:  </span><span class="sxs-lookup"><span data-stu-id="f3c79-131">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3c79-132">说明</span><span class="sxs-lookup"><span data-stu-id="f3c79-132">Remarks</span></span>

<span data-ttu-id="f3c79-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f3c79-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3c79-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="f3c79-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3c79-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="f3c79-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f3c79-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="f3c79-136">Schema Name</span></span>  <br/> |<span data-ttu-id="f3c79-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="f3c79-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f3c79-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="f3c79-138">Validation File</span></span>  <br/> |<span data-ttu-id="f3c79-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f3c79-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f3c79-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="f3c79-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="f3c79-141">False</span><span class="sxs-lookup"><span data-stu-id="f3c79-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3c79-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f3c79-142">See also</span></span>

- [<span data-ttu-id="f3c79-143">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f3c79-143">MoveFolder operation</span></span>](movefolder-operation.md)  
- [<span data-ttu-id="f3c79-144">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f3c79-144">CopyFolder operation</span></span>](copyfolder-operation.md) 
- [<span data-ttu-id="f3c79-145">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="f3c79-145">MoveItem operation</span></span>](moveitem-operation.md) 
- [<span data-ttu-id="f3c79-146">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="f3c79-146">CopyItem operation</span></span>](copyitem-operation.md)

