---
title: CreateFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282576cb-a921-49f7-8748-64158fd50c41
description: CreateFolderPath 元素用于创建文件夹路径，并包含父文件夹 Id 和相对文件夹路径。
ms.openlocfilehash: e6ce6c9b6e12a6a0fb6792b63368a79c87d06f07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457534"
---
# <a name="createfolderpath"></a><span data-ttu-id="1a303-103">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="1a303-103">CreateFolderPath</span></span>

<span data-ttu-id="1a303-104">**CreateFolderPath**元素用于创建文件夹路径，并包含父文件夹 Id 和相对文件夹路径。</span><span class="sxs-lookup"><span data-stu-id="1a303-104">The **CreateFolderPath** element is used to create a folder path and includes a parent folder Id and a relative folder path.</span></span> 
  
```XML
<CreateFolderPath>
   <ParentFolderId/>
   <RelativeFolderPath/>
</CreateFolderPath>
```

 <span data-ttu-id="1a303-105">**CreateFolderPathType**</span><span class="sxs-lookup"><span data-stu-id="1a303-105">**CreateFolderPathType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a303-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1a303-106">Attributes and elements</span></span>

<span data-ttu-id="1a303-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1a303-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a303-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1a303-108">Attributes</span></span>

<span data-ttu-id="1a303-109">无。</span><span class="sxs-lookup"><span data-stu-id="1a303-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a303-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1a303-110">Child elements</span></span>

<span data-ttu-id="1a303-111">[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)  | [RelativeFolderPath](relativefolderpath.md)</span><span class="sxs-lookup"><span data-stu-id="1a303-111">[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [RelativeFolderPath](relativefolderpath.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1a303-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1a303-112">Parent elements</span></span>

<span data-ttu-id="1a303-113">无。</span><span class="sxs-lookup"><span data-stu-id="1a303-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a303-114">说明</span><span class="sxs-lookup"><span data-stu-id="1a303-114">Remarks</span></span>

<span data-ttu-id="1a303-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1a303-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1a303-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1a303-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a303-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1a303-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a303-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1a303-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1a303-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1a303-119">Schema name</span></span>  <br/> |<span data-ttu-id="1a303-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="1a303-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1a303-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1a303-121">Validation file</span></span>  <br/> |<span data-ttu-id="1a303-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="1a303-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1a303-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1a303-123">Can be empty</span></span>  <br/> |<span data-ttu-id="1a303-124">false</span><span class="sxs-lookup"><span data-stu-id="1a303-124">false</span></span>  <br/> |
   

