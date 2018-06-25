---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: FoldersToIgnore 元素标识会话中获取项目时，将忽略的文件夹的列表。 忽略文件夹中的所有对话项目不 GetConversationItems 响应中返回。
ms.openlocfilehash: 96c094996c601e685dc1c7e6b869a790ce7d74a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754406"
---
# <a name="folderstoignore"></a><span data-ttu-id="6c8bf-104">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="6c8bf-104">FoldersToIgnore</span></span>

<span data-ttu-id="6c8bf-105">**FoldersToIgnore**元素标识会话中获取项目时，将忽略的文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="6c8bf-105">The **FoldersToIgnore** element identifies a list of folders that are ignored when getting items in a conversation.</span></span> <span data-ttu-id="6c8bf-106">忽略文件夹中的所有对话项目不**GetConversationItems**响应中返回。</span><span class="sxs-lookup"><span data-stu-id="6c8bf-106">All conversation items in the ignored folders are not returned in a **GetConversationItems** response.</span></span> 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 <span data-ttu-id="6c8bf-107">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="6c8bf-107">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c8bf-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6c8bf-108">Attributes and elements</span></span>

<span data-ttu-id="6c8bf-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6c8bf-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c8bf-110">属性</span><span class="sxs-lookup"><span data-stu-id="6c8bf-110">Attributes</span></span>

<span data-ttu-id="6c8bf-111">无。</span><span class="sxs-lookup"><span data-stu-id="6c8bf-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c8bf-112">子元素</span><span class="sxs-lookup"><span data-stu-id="6c8bf-112">Child elements</span></span>

<span data-ttu-id="6c8bf-113">[文件夹 Id](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="6c8bf-113">[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6c8bf-114">父元素</span><span class="sxs-lookup"><span data-stu-id="6c8bf-114">Parent elements</span></span>

[<span data-ttu-id="6c8bf-115">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="6c8bf-115">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="remarks"></a><span data-ttu-id="6c8bf-116">备注</span><span class="sxs-lookup"><span data-stu-id="6c8bf-116">Remarks</span></span>

<span data-ttu-id="6c8bf-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6c8bf-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6c8bf-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6c8bf-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c8bf-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="6c8bf-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c8bf-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="6c8bf-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6c8bf-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="6c8bf-121">Schema name</span></span>  <br/> |<span data-ttu-id="6c8bf-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="6c8bf-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="6c8bf-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="6c8bf-123">Validation file</span></span>  <br/> |<span data-ttu-id="6c8bf-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6c8bf-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6c8bf-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="6c8bf-125">Can be empty</span></span>  <br/> |<span data-ttu-id="6c8bf-126">false</span><span class="sxs-lookup"><span data-stu-id="6c8bf-126">false</span></span>  <br/> |
   

