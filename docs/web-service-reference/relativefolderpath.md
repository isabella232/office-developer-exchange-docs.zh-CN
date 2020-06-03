---
title: RelativeFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54e3ba52-08a6-4d48-8a44-6fd5fdbffb25
description: RelativeFolderPath 元素包含一个文件夹数组，这些文件夹指示要创建的文件夹路径的相对文件夹路径。
ms.openlocfilehash: 8a0fc0020943afdbe6cd4c79d51d61337f8dd329
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457156"
---
# <a name="relativefolderpath"></a><span data-ttu-id="0c8d1-103">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="0c8d1-103">RelativeFolderPath</span></span>

<span data-ttu-id="0c8d1-104">**RelativeFolderPath**元素包含一个文件夹数组，这些文件夹指示要创建的文件夹路径的相对文件夹路径。</span><span class="sxs-lookup"><span data-stu-id="0c8d1-104">The **RelativeFolderPath** element contains an array of folders that indicate the relative folder path of the folder path to be created.</span></span> 
  
```XML
<RelativeFolderPath>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</RelativeFolderPath>
```

 <span data-ttu-id="0c8d1-105">**NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="0c8d1-105">**NonEmptyArrayOfFoldersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c8d1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0c8d1-106">Attributes and elements</span></span>

<span data-ttu-id="0c8d1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0c8d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c8d1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0c8d1-108">Attributes</span></span>

<span data-ttu-id="0c8d1-109">无。</span><span class="sxs-lookup"><span data-stu-id="0c8d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c8d1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0c8d1-110">Child elements</span></span>

<span data-ttu-id="0c8d1-111">[文件夹](folder.md)  | [CalendarFolder](calendarfolder.md)  | [ContactsFolder](contactsfolder.md)  | [SearchFolder](searchfolder.md)  | [TasksFolder](tasksfolder.md)</span><span class="sxs-lookup"><span data-stu-id="0c8d1-111">[Folder](folder.md) | [CalendarFolder](calendarfolder.md) | [ContactsFolder](contactsfolder.md) | [SearchFolder](searchfolder.md) | [TasksFolder](tasksfolder.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0c8d1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0c8d1-112">Parent elements</span></span>

[<span data-ttu-id="0c8d1-113">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="0c8d1-113">CreateFolderPath</span></span>](createfolderpath.md)
  
## <a name="remarks"></a><span data-ttu-id="0c8d1-114">备注</span><span class="sxs-lookup"><span data-stu-id="0c8d1-114">Remarks</span></span>

<span data-ttu-id="0c8d1-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0c8d1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0c8d1-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0c8d1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c8d1-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="0c8d1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c8d1-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="0c8d1-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0c8d1-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="0c8d1-119">Schema name</span></span>  <br/> |<span data-ttu-id="0c8d1-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="0c8d1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0c8d1-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="0c8d1-121">Validation file</span></span>  <br/> |<span data-ttu-id="0c8d1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0c8d1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0c8d1-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="0c8d1-123">Can be empty</span></span>  <br/> ||
   

