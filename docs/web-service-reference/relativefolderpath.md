---
title: RelativeFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54e3ba52-08a6-4d48-8a44-6fd5fdbffb25
description: RelativeFolderPath 元素包含一个数组指示要创建的文件夹路径的相对文件夹路径的文件夹。
ms.openlocfilehash: f568d282e47a41c0aaf6d70ef383e5ef3e2b54bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827051"
---
# <a name="relativefolderpath"></a><span data-ttu-id="56723-103">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="56723-103">RelativeFolderPath</span></span>

<span data-ttu-id="56723-104">**RelativeFolderPath**元素包含一个数组指示要创建的文件夹路径的相对文件夹路径的文件夹。</span><span class="sxs-lookup"><span data-stu-id="56723-104">The **RelativeFolderPath** element contains an array of folders that indicate the relative folder path of the folder path to be created.</span></span> 
  
```XML
<RelativeFolderPath>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</RelativeFolderPath>
```

 <span data-ttu-id="56723-105">**NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="56723-105">**NonEmptyArrayOfFoldersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="56723-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="56723-106">Attributes and elements</span></span>

<span data-ttu-id="56723-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="56723-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56723-108">属性</span><span class="sxs-lookup"><span data-stu-id="56723-108">Attributes</span></span>

<span data-ttu-id="56723-109">无。</span><span class="sxs-lookup"><span data-stu-id="56723-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="56723-110">子元素</span><span class="sxs-lookup"><span data-stu-id="56723-110">Child elements</span></span>

<span data-ttu-id="56723-111">[文件夹](folder.md) | [CalendarFolder](calendarfolder.md) | [ContactsFolder](contactsfolder.md) | [SearchFolder](searchfolder.md) | [TasksFolder](tasksfolder.md)</span><span class="sxs-lookup"><span data-stu-id="56723-111">[Folder](folder.md) | [CalendarFolder](calendarfolder.md) | [ContactsFolder](contactsfolder.md) | [SearchFolder](searchfolder.md) | [TasksFolder](tasksfolder.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="56723-112">父元素</span><span class="sxs-lookup"><span data-stu-id="56723-112">Parent elements</span></span>

[<span data-ttu-id="56723-113">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="56723-113">CreateFolderPath</span></span>](createfolderpath.md)
  
## <a name="remarks"></a><span data-ttu-id="56723-114">备注</span><span class="sxs-lookup"><span data-stu-id="56723-114">Remarks</span></span>

<span data-ttu-id="56723-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="56723-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="56723-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="56723-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="56723-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="56723-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56723-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="56723-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="56723-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="56723-119">Schema name</span></span>  <br/> |<span data-ttu-id="56723-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="56723-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="56723-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="56723-121">Validation file</span></span>  <br/> |<span data-ttu-id="56723-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="56723-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="56723-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="56723-123">Can be empty</span></span>  <br/> ||
   

