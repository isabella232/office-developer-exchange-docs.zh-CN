---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: FoldersToIgnore 元素标识在对话中获取项目时被忽略的文件夹的列表。 GetConversationItems 响应中不会返回已忽略文件夹中的所有对话项目。
ms.openlocfilehash: 07813a54a9a3afa3de23ae94f1c9b191d1cb6fac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44453355"
---
# <a name="folderstoignore"></a><span data-ttu-id="6f51e-104">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="6f51e-104">FoldersToIgnore</span></span>

<span data-ttu-id="6f51e-105">**FoldersToIgnore**元素标识在对话中获取项目时被忽略的文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="6f51e-105">The **FoldersToIgnore** element identifies a list of folders that are ignored when getting items in a conversation.</span></span> <span data-ttu-id="6f51e-106">**GetConversationItems**响应中不会返回已忽略文件夹中的所有对话项目。</span><span class="sxs-lookup"><span data-stu-id="6f51e-106">All conversation items in the ignored folders are not returned in a **GetConversationItems** response.</span></span> 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 <span data-ttu-id="6f51e-107">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="6f51e-107">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f51e-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f51e-108">Attributes and elements</span></span>

<span data-ttu-id="6f51e-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f51e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f51e-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="6f51e-110">Attributes</span></span>

<span data-ttu-id="6f51e-111">无。</span><span class="sxs-lookup"><span data-stu-id="6f51e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f51e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="6f51e-112">Child elements</span></span>

<span data-ttu-id="6f51e-113">[FolderId](folderid.md)  | [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="6f51e-113">[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f51e-114">父元素</span><span class="sxs-lookup"><span data-stu-id="6f51e-114">Parent elements</span></span>

[<span data-ttu-id="6f51e-115">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="6f51e-115">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="remarks"></a><span data-ttu-id="6f51e-116">备注</span><span class="sxs-lookup"><span data-stu-id="6f51e-116">Remarks</span></span>

<span data-ttu-id="6f51e-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6f51e-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6f51e-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6f51e-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f51e-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f51e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f51e-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f51e-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f51e-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f51e-121">Schema name</span></span>  <br/> |<span data-ttu-id="6f51e-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="6f51e-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f51e-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f51e-123">Validation file</span></span>  <br/> |<span data-ttu-id="6f51e-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6f51e-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f51e-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f51e-125">Can be empty</span></span>  <br/> |<span data-ttu-id="6f51e-126">false</span><span class="sxs-lookup"><span data-stu-id="6f51e-126">false</span></span>  <br/> |
   

