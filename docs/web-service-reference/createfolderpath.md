---
title: CreateFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282576cb-a921-49f7-8748-64158fd50c41
description: CreateFolderPath 元素用于创建的文件夹路径，包括父文件夹 Id 和相对文件夹路径。
ms.openlocfilehash: bfe31d894cfaa0f36da2d1d0045f723e0d261759
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753643"
---
# <a name="createfolderpath"></a><span data-ttu-id="4da7d-103">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="4da7d-103">CreateFolderPath</span></span>

<span data-ttu-id="4da7d-104">**CreateFolderPath**元素用于创建的文件夹路径，包括父文件夹 Id 和相对文件夹路径。</span><span class="sxs-lookup"><span data-stu-id="4da7d-104">The **CreateFolderPath** element is used to create a folder path and includes a parent folder Id and a relative folder path.</span></span> 
  
```XML
<CreateFolderPath>
   <ParentFolderId/>
   <RelativeFolderPath/>
</CreateFolderPath>
```

 <span data-ttu-id="4da7d-105">**CreateFolderPathType**</span><span class="sxs-lookup"><span data-stu-id="4da7d-105">**CreateFolderPathType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4da7d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4da7d-106">Attributes and elements</span></span>

<span data-ttu-id="4da7d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4da7d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4da7d-108">属性</span><span class="sxs-lookup"><span data-stu-id="4da7d-108">Attributes</span></span>

<span data-ttu-id="4da7d-109">无。</span><span class="sxs-lookup"><span data-stu-id="4da7d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4da7d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4da7d-110">Child elements</span></span>

<span data-ttu-id="4da7d-111">[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [RelativeFolderPath](relativefolderpath.md)</span><span class="sxs-lookup"><span data-stu-id="4da7d-111">[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [RelativeFolderPath](relativefolderpath.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4da7d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4da7d-112">Parent elements</span></span>

<span data-ttu-id="4da7d-113">无。</span><span class="sxs-lookup"><span data-stu-id="4da7d-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4da7d-114">备注</span><span class="sxs-lookup"><span data-stu-id="4da7d-114">Remarks</span></span>

<span data-ttu-id="4da7d-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4da7d-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4da7d-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4da7d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4da7d-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="4da7d-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4da7d-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="4da7d-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4da7d-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="4da7d-119">Schema name</span></span>  <br/> |<span data-ttu-id="4da7d-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="4da7d-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4da7d-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="4da7d-121">Validation file</span></span>  <br/> |<span data-ttu-id="4da7d-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4da7d-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4da7d-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="4da7d-123">Can be empty</span></span>  <br/> |<span data-ttu-id="4da7d-124">false</span><span class="sxs-lookup"><span data-stu-id="4da7d-124">false</span></span>  <br/> |
   

