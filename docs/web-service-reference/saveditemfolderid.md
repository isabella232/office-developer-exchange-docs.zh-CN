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
description: SavedItemFolderId 元素标识用于更新、 发送和邮箱中创建项目的操作的目标文件夹。
ms.openlocfilehash: 3f46070a538f5e03007925565a8888efe06b62b7
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354160"
---
# <a name="saveditemfolderid"></a><span data-ttu-id="718a4-103">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="718a4-103">SavedItemFolderId</span></span>

<span data-ttu-id="718a4-104">**SavedItemFolderId**元素标识用于更新、 发送和邮箱中创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="718a4-104">The **SavedItemFolderId** element identifies the target folder for operations that update, send, and create items in a mailbox.</span></span> 
  
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

<span data-ttu-id="718a4-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="718a4-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="718a4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="718a4-106">Attributes and elements</span></span>

<span data-ttu-id="718a4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="718a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="718a4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="718a4-108">Attributes</span></span>

<span data-ttu-id="718a4-109">无。</span><span class="sxs-lookup"><span data-stu-id="718a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="718a4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="718a4-110">Child elements</span></span>

|<span data-ttu-id="718a4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="718a4-111">**Element**</span></span>|<span data-ttu-id="718a4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="718a4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="718a4-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="718a4-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="718a4-114">包含标识符和更改密钥的目标文件夹的更新、 发送和在 Exchange 存储中创建项目操作。</span><span class="sxs-lookup"><span data-stu-id="718a4-114">Contains the identifier and change key of a target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="718a4-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="718a4-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="718a4-116">通过更新、 发送和在 Exchange 存储中创建项目的操作的命名标识符标识目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="718a4-116">Identifies a target folder by a named identifier for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="718a4-117">父元素</span><span class="sxs-lookup"><span data-stu-id="718a4-117">Parent elements</span></span>

|<span data-ttu-id="718a4-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="718a4-118">**Element**</span></span>|<span data-ttu-id="718a4-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="718a4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="718a4-120">CreateItem</span><span class="sxs-lookup"><span data-stu-id="718a4-120">CreateItem</span></span>](createitem.md) <br/> |<span data-ttu-id="718a4-121">定义在 Exchange 存储中创建项的请求。</span><span class="sxs-lookup"><span data-stu-id="718a4-121">Defines a request to create an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="718a4-122">下面是此元素的 XPath 表达式:  </span><span class="sxs-lookup"><span data-stu-id="718a4-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateItem` <br/> |
|[<span data-ttu-id="718a4-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="718a4-123">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="718a4-124">定义更新 Exchange 存储中的项的请求。</span><span class="sxs-lookup"><span data-stu-id="718a4-124">Defines a request to update an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="718a4-125">下面是此元素的 XPath 表达式:  </span><span class="sxs-lookup"><span data-stu-id="718a4-125">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
|[<span data-ttu-id="718a4-126">SendItem</span><span class="sxs-lookup"><span data-stu-id="718a4-126">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="718a4-127">定义发送 Exchange 存储中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="718a4-127">Defines a request to send an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="718a4-128">下面是此元素的 XPath 表达式:  </span><span class="sxs-lookup"><span data-stu-id="718a4-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="718a4-129">说明</span><span class="sxs-lookup"><span data-stu-id="718a4-129">Remarks</span></span>

<span data-ttu-id="718a4-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="718a4-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="718a4-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="718a4-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="718a4-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="718a4-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="718a4-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="718a4-133">Schema Name</span></span>  <br/> |<span data-ttu-id="718a4-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="718a4-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="718a4-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="718a4-135">Validation File</span></span>  <br/> |<span data-ttu-id="718a4-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="718a4-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="718a4-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="718a4-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="718a4-138">False</span><span class="sxs-lookup"><span data-stu-id="718a4-138">False</span></span>  <br/> |
   

