---
title: SavedItemFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SavedItemFolderId
api_type:
- schema
ms.assetid: 4b8b475c-9ca5-48c9-acb0-8848b53be1ce
description: SavedItemFolderId 元素标识在邮箱中更新、发送和创建项目的操作的目标文件夹。
ms.openlocfilehash: 8e18b8863a54aa4e9d6e65f7a54e20904f5a9599
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465273"
---
# <a name="saveditemfolderid"></a><span data-ttu-id="f12e3-103">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="f12e3-103">SavedItemFolderId</span></span>

<span data-ttu-id="f12e3-104">**SavedItemFolderId**元素标识在邮箱中更新、发送和创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="f12e3-104">The **SavedItemFolderId** element identifies the target folder for operations that update, send, and create items in a mailbox.</span></span> 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

```xml
<SavedItemFolderId>
   <DistinguishedFolderId/>
</SavedItemFolderId>
```

<span data-ttu-id="f12e3-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="f12e3-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f12e3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f12e3-106">Attributes and elements</span></span>

<span data-ttu-id="f12e3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f12e3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f12e3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f12e3-108">Attributes</span></span>

<span data-ttu-id="f12e3-109">无。</span><span class="sxs-lookup"><span data-stu-id="f12e3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f12e3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f12e3-110">Child elements</span></span>

|<span data-ttu-id="f12e3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f12e3-111">**Element**</span></span>|<span data-ttu-id="f12e3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f12e3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f12e3-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="f12e3-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="f12e3-114">包含更新、发送和创建 Exchange 存储中的项的操作的目标文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="f12e3-114">Contains the identifier and change key of a target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f12e3-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="f12e3-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="f12e3-116">通过在 Exchange 存储中更新、发送和创建项目的操作的命名标识符标识目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="f12e3-116">Identifies a target folder by a named identifier for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f12e3-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f12e3-117">Parent elements</span></span>

|<span data-ttu-id="f12e3-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="f12e3-118">**Element**</span></span>|<span data-ttu-id="f12e3-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="f12e3-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f12e3-120">CreateItem</span><span class="sxs-lookup"><span data-stu-id="f12e3-120">CreateItem</span></span>](createitem.md) <br/> |<span data-ttu-id="f12e3-121">定义在 Exchange 存储中创建项目的请求。</span><span class="sxs-lookup"><span data-stu-id="f12e3-121">Defines a request to create an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="f12e3-122">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="f12e3-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateItem` <br/> |
|[<span data-ttu-id="f12e3-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="f12e3-123">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="f12e3-124">定义对 Exchange 存储中的项目的更新请求。</span><span class="sxs-lookup"><span data-stu-id="f12e3-124">Defines a request to update an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="f12e3-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="f12e3-125">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
|[<span data-ttu-id="f12e3-126">SendItem</span><span class="sxs-lookup"><span data-stu-id="f12e3-126">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="f12e3-127">定义在 Exchange 存储中发送项目的请求。</span><span class="sxs-lookup"><span data-stu-id="f12e3-127">Defines a request to send an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="f12e3-128">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="f12e3-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f12e3-129">说明</span><span class="sxs-lookup"><span data-stu-id="f12e3-129">Remarks</span></span>

<span data-ttu-id="f12e3-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f12e3-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f12e3-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="f12e3-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f12e3-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="f12e3-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f12e3-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="f12e3-133">Schema Name</span></span>  <br/> |<span data-ttu-id="f12e3-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="f12e3-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f12e3-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="f12e3-135">Validation File</span></span>  <br/> |<span data-ttu-id="f12e3-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f12e3-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f12e3-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="f12e3-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="f12e3-138">False</span><span class="sxs-lookup"><span data-stu-id="f12e3-138">False</span></span>  <br/> |
   

