---
title: SyncFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderId
api_type:
- schema
ms.assetid: 3645fa03-236d-4e5f-b8b9-5d98f7f35fa2
description: SyncFolderId 元素表示包含要同步的项的文件夹。
ms.openlocfilehash: c90a20095ca4706f0c6edae3e98eaadd6024d817
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354398"
---
# <a name="syncfolderid"></a><span data-ttu-id="3edc2-103">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="3edc2-103">SyncFolderId</span></span>

<span data-ttu-id="3edc2-104">**SyncFolderId**元素表示包含要同步的项的文件夹。</span><span class="sxs-lookup"><span data-stu-id="3edc2-104">The **SyncFolderId** element represents the folder that contains the items to synchronize.</span></span> 
  
```xml
<SyncFolderId>
   <FolderId/>
</SyncFolderId>
```

```xml
<SyncFolderId>
   <DistinguishedFolderId/> 
</SyncFolderId>
```

<span data-ttu-id="3edc2-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="3edc2-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3edc2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3edc2-106">Attributes and elements</span></span>

<span data-ttu-id="3edc2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3edc2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3edc2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3edc2-108">Attributes</span></span>

<span data-ttu-id="3edc2-109">无。</span><span class="sxs-lookup"><span data-stu-id="3edc2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3edc2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3edc2-110">Child elements</span></span>

|<span data-ttu-id="3edc2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3edc2-111">**Element**</span></span>|<span data-ttu-id="3edc2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3edc2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3edc2-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="3edc2-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="3edc2-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="3edc2-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="3edc2-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="3edc2-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="3edc2-116">标识可以通过名称引用的 MicrosoftExchange Server 2007 文件夹。</span><span class="sxs-lookup"><span data-stu-id="3edc2-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3edc2-117">父元素</span><span class="sxs-lookup"><span data-stu-id="3edc2-117">Parent elements</span></span>

|<span data-ttu-id="3edc2-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="3edc2-118">**Element**</span></span>|<span data-ttu-id="3edc2-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="3edc2-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3edc2-120">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="3edc2-120">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="3edc2-121">定义同步 Exchange 存储中的文件夹层次结构的请求。</span><span class="sxs-lookup"><span data-stu-id="3edc2-121">Defines a request to synchronize a folder hierarchy in an Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3edc2-122">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="3edc2-122">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="3edc2-123">定义同步 Exchange 存储区文件夹中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="3edc2-123">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3edc2-124">说明</span><span class="sxs-lookup"><span data-stu-id="3edc2-124">Remarks</span></span>

<span data-ttu-id="3edc2-125">描述此元素的架构位于运行 Exchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3edc2-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3edc2-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="3edc2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3edc2-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="3edc2-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3edc2-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="3edc2-128">Schema name</span></span>  <br/> |<span data-ttu-id="3edc2-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="3edc2-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3edc2-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="3edc2-130">Validation file</span></span>  <br/> |<span data-ttu-id="3edc2-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3edc2-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3edc2-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="3edc2-132">Can be empty</span></span>  <br/> |<span data-ttu-id="3edc2-133">False</span><span class="sxs-lookup"><span data-stu-id="3edc2-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3edc2-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3edc2-134">See also</span></span>

- [<span data-ttu-id="3edc2-135">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="3edc2-135">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="3edc2-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3edc2-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

