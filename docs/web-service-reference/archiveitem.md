---
title: ArchiveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c2172e61-876a-4f76-bc9c-263c8be11429
description: ArchiveItem 元素包含源文件夹 Id 和关联存档项的项 Id 的数组。
ms.openlocfilehash: e1694619c90160084980cb8f3a7c8a0ed1876295
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463403"
---
# <a name="archiveitem"></a><span data-ttu-id="a205c-103">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="a205c-103">ArchiveItem</span></span>

<span data-ttu-id="a205c-104">**ArchiveItem**元素包含源文件夹 Id 和关联存档项的项 id 的数组。</span><span class="sxs-lookup"><span data-stu-id="a205c-104">The **ArchiveItem** element contains the source folder Id and an array of item Ids for the associated archive item.</span></span> 
  
```XML
<ArchiveItem>
   <ArchiveSourceFolderId/>
   <ItemIds/>
</ArchiveItem>
```

 <span data-ttu-id="a205c-105">**ArchiveItemType**</span><span class="sxs-lookup"><span data-stu-id="a205c-105">**ArchiveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a205c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a205c-106">Attributes and elements</span></span>

<span data-ttu-id="a205c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a205c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a205c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a205c-108">Attributes</span></span>

<span data-ttu-id="a205c-109">无。</span><span class="sxs-lookup"><span data-stu-id="a205c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a205c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a205c-110">Child elements</span></span>

<span data-ttu-id="a205c-111">[ArchiveSourceFolderId](archivesourcefolderid.md)  | [ItemIds](itemids.md)</span><span class="sxs-lookup"><span data-stu-id="a205c-111">[ArchiveSourceFolderId](archivesourcefolderid.md) | [ItemIds](itemids.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a205c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a205c-112">Parent elements</span></span>

<span data-ttu-id="a205c-113">无。</span><span class="sxs-lookup"><span data-stu-id="a205c-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a205c-114">说明</span><span class="sxs-lookup"><span data-stu-id="a205c-114">Remarks</span></span>

<span data-ttu-id="a205c-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a205c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a205c-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a205c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a205c-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="a205c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a205c-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="a205c-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a205c-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="a205c-119">Schema name</span></span>  <br/> |<span data-ttu-id="a205c-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="a205c-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a205c-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="a205c-121">Validation file</span></span>  <br/> |<span data-ttu-id="a205c-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="a205c-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a205c-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="a205c-123">Can be empty</span></span>  <br/> |<span data-ttu-id="a205c-124">false</span><span class="sxs-lookup"><span data-stu-id="a205c-124">false</span></span>  <br/> |
   

