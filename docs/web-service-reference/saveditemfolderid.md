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
ms.openlocfilehash: c57a7fb4abc2f7ee7b599f56f016811d6ff2c21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827277"
---
# <a name="saveditemfolderid"></a><span data-ttu-id="59a58-103">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="59a58-103">SavedItemFolderId</span></span>

<span data-ttu-id="59a58-104">**SavedItemFolderId**元素标识用于更新、 发送和邮箱中创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="59a58-104">The **SavedItemFolderId** element identifies the target folder for operations that update, send, and create items in a mailbox.</span></span> 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

 <span data-ttu-id="59a58-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="59a58-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59a58-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="59a58-106">Attributes and elements</span></span>

<span data-ttu-id="59a58-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="59a58-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59a58-108">属性</span><span class="sxs-lookup"><span data-stu-id="59a58-108">Attributes</span></span>

<span data-ttu-id="59a58-109">无。</span><span class="sxs-lookup"><span data-stu-id="59a58-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59a58-110">子元素</span><span class="sxs-lookup"><span data-stu-id="59a58-110">Child elements</span></span>

|<span data-ttu-id="59a58-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="59a58-111">**Element**</span></span>|<span data-ttu-id="59a58-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="59a58-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59a58-113">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="59a58-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="59a58-114">包含标识符和更改密钥的目标文件夹的更新、 发送和在 Exchange 存储中创建项目操作。</span><span class="sxs-lookup"><span data-stu-id="59a58-114">Contains the identifier and change key of a target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="59a58-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="59a58-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="59a58-116">通过更新、 发送和在 Exchange 存储中创建项目的操作的命名标识符标识目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="59a58-116">Identifies a target folder by a named identifier for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="59a58-117">父元素</span><span class="sxs-lookup"><span data-stu-id="59a58-117">Parent elements</span></span>

|<span data-ttu-id="59a58-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="59a58-118">**Element**</span></span>|<span data-ttu-id="59a58-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="59a58-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59a58-120">CreateItem</span><span class="sxs-lookup"><span data-stu-id="59a58-120">CreateItem</span></span>](createitem.md) <br/> |<span data-ttu-id="59a58-121">定义在 Exchange 存储中创建项的请求。</span><span class="sxs-lookup"><span data-stu-id="59a58-121">Defines a request to create an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="59a58-122">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="59a58-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateItem` <br/> |
|[<span data-ttu-id="59a58-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="59a58-123">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="59a58-124">定义更新 Exchange 存储中的项的请求。</span><span class="sxs-lookup"><span data-stu-id="59a58-124">Defines a request to update an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="59a58-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="59a58-125">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
|[<span data-ttu-id="59a58-126">SendItem</span><span class="sxs-lookup"><span data-stu-id="59a58-126">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="59a58-127">定义发送 Exchange 存储中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="59a58-127">Defines a request to send an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="59a58-128">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="59a58-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59a58-129">备注</span><span class="sxs-lookup"><span data-stu-id="59a58-129">Remarks</span></span>

<span data-ttu-id="59a58-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="59a58-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59a58-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="59a58-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59a58-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="59a58-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="59a58-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="59a58-133">Schema Name</span></span>  <br/> |<span data-ttu-id="59a58-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="59a58-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="59a58-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="59a58-135">Validation File</span></span>  <br/> |<span data-ttu-id="59a58-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="59a58-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="59a58-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="59a58-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="59a58-138">False</span><span class="sxs-lookup"><span data-stu-id="59a58-138">False</span></span>  <br/> |
   

