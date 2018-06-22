---
title: ArchiveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c2172e61-876a-4f76-bc9c-263c8be11429
description: ArchiveItem 元素包含源文件夹 Id 和项目 Id 关联的存档项目的数组。
ms.openlocfilehash: 7f2d79f5a9e6798fafcf64e8b1bb680390800992
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753256"
---
# <a name="archiveitem"></a><span data-ttu-id="e88dc-103">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="e88dc-103">ArchiveItem</span></span>

<span data-ttu-id="e88dc-104">**ArchiveItem**元素包含源文件夹 Id 和项目 Id 关联的存档项目的数组。</span><span class="sxs-lookup"><span data-stu-id="e88dc-104">The **ArchiveItem** element contains the source folder Id and an array of item Ids for the associated archive item.</span></span> 
  
```XML
<ArchiveItem>
   <ArchiveSourceFolderId/>
   <ItemIds/>
</ArchiveItem>
```

 <span data-ttu-id="e88dc-105">**ArchiveItemType**</span><span class="sxs-lookup"><span data-stu-id="e88dc-105">**ArchiveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e88dc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e88dc-106">Attributes and elements</span></span>

<span data-ttu-id="e88dc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e88dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e88dc-108">属性</span><span class="sxs-lookup"><span data-stu-id="e88dc-108">Attributes</span></span>

<span data-ttu-id="e88dc-109">无。</span><span class="sxs-lookup"><span data-stu-id="e88dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e88dc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e88dc-110">Child elements</span></span>

<span data-ttu-id="e88dc-111">[ArchiveSourceFolderId](archivesourcefolderid.md) | [ItemIds](itemids.md)</span><span class="sxs-lookup"><span data-stu-id="e88dc-111">[ArchiveSourceFolderId](archivesourcefolderid.md) | [ItemIds](itemids.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e88dc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e88dc-112">Parent elements</span></span>

<span data-ttu-id="e88dc-113">无。</span><span class="sxs-lookup"><span data-stu-id="e88dc-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e88dc-114">备注</span><span class="sxs-lookup"><span data-stu-id="e88dc-114">Remarks</span></span>

<span data-ttu-id="e88dc-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e88dc-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e88dc-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e88dc-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e88dc-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="e88dc-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e88dc-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="e88dc-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e88dc-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="e88dc-119">Schema name</span></span>  <br/> |<span data-ttu-id="e88dc-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="e88dc-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e88dc-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="e88dc-121">Validation file</span></span>  <br/> |<span data-ttu-id="e88dc-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e88dc-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e88dc-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="e88dc-123">Can be empty</span></span>  <br/> |<span data-ttu-id="e88dc-124">false</span><span class="sxs-lookup"><span data-stu-id="e88dc-124">false</span></span>  <br/> |
   

