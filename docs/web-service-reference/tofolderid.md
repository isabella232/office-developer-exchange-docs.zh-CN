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
description: ToFolderId 元素表示复制或移动的项或文件夹的目标文件夹。
ms.openlocfilehash: c9cceb17fd55b7357d54b37bf4c8da1137d39b6a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468773"
---
# <a name="tofolderid"></a><span data-ttu-id="f7d1b-103">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="f7d1b-103">ToFolderId</span></span>

<span data-ttu-id="f7d1b-104">**ToFolderId**元素表示复制或移动的项或文件夹的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-104">The **ToFolderId** element represents the destination folder for a copied or moved item or folder.</span></span> 
  
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

<span data-ttu-id="f7d1b-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="f7d1b-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f7d1b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f7d1b-106">Attributes and elements</span></span>

<span data-ttu-id="f7d1b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7d1b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f7d1b-108">Attributes</span></span>

<span data-ttu-id="f7d1b-109">无。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7d1b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f7d1b-110">Child elements</span></span>

|<span data-ttu-id="f7d1b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7d1b-111">**Element**</span></span>|<span data-ttu-id="f7d1b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7d1b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7d1b-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="f7d1b-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="f7d1b-114">包含用于复制或移动的项或文件夹的目标文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="f7d1b-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="f7d1b-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="f7d1b-116">标识命名的目标文件夹复制或移动的项或文件夹。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f7d1b-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f7d1b-117">Parent elements</span></span>

|<span data-ttu-id="f7d1b-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7d1b-118">**Element**</span></span>|<span data-ttu-id="f7d1b-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7d1b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7d1b-120">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="f7d1b-120">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="f7d1b-121">定义在 Exchange 存储中移动文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-121">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="f7d1b-122">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="f7d1b-122">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveFolder` <br/> |
|[<span data-ttu-id="f7d1b-123">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="f7d1b-123">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="f7d1b-124">定义在 Exchange 存储中复制文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-124">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="f7d1b-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="f7d1b-125">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyFolder` <br/> |
|[<span data-ttu-id="f7d1b-126">MoveItem</span><span class="sxs-lookup"><span data-stu-id="f7d1b-126">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="f7d1b-127">定义在 Exchange 存储中移动项目的请求。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-127">Defines a request to move an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="f7d1b-128">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="f7d1b-128">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="f7d1b-129">CopyItem</span><span class="sxs-lookup"><span data-stu-id="f7d1b-129">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="f7d1b-130">定义在 Exchange 存储中复制项目的请求。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-130">Defines a request to copy an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="f7d1b-131">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="f7d1b-131">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7d1b-132">说明</span><span class="sxs-lookup"><span data-stu-id="f7d1b-132">Remarks</span></span>

<span data-ttu-id="f7d1b-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f7d1b-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7d1b-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="f7d1b-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7d1b-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="f7d1b-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f7d1b-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="f7d1b-136">Schema Name</span></span>  <br/> |<span data-ttu-id="f7d1b-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="f7d1b-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f7d1b-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="f7d1b-138">Validation File</span></span>  <br/> |<span data-ttu-id="f7d1b-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f7d1b-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f7d1b-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="f7d1b-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7d1b-141">False</span><span class="sxs-lookup"><span data-stu-id="f7d1b-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7d1b-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f7d1b-142">See also</span></span>

- [<span data-ttu-id="f7d1b-143">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f7d1b-143">MoveFolder operation</span></span>](movefolder-operation.md)  
- [<span data-ttu-id="f7d1b-144">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f7d1b-144">CopyFolder operation</span></span>](copyfolder-operation.md) 
- [<span data-ttu-id="f7d1b-145">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="f7d1b-145">MoveItem operation</span></span>](moveitem-operation.md) 
- [<span data-ttu-id="f7d1b-146">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="f7d1b-146">CopyItem operation</span></span>](copyitem-operation.md)

