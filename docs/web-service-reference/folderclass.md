---
title: FolderClass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderClass
api_type:
- schema
ms.assetid: 0041d135-2869-4612-89a5-d1aa86aa1093
description: FolderClass 元素表示文件夹的文件夹类。
ms.openlocfilehash: ee5d382251a66ab5fbcd8054e6b5cfac82b5f994
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460055"
---
# <a name="folderclass"></a><span data-ttu-id="704f2-103">FolderClass</span><span class="sxs-lookup"><span data-stu-id="704f2-103">FolderClass</span></span>

<span data-ttu-id="704f2-104">**FolderClass**元素表示文件夹的文件夹类。</span><span class="sxs-lookup"><span data-stu-id="704f2-104">The **FolderClass** element represents the folder class for a folder.</span></span> 
  
```xml
<FolderClass/>
```

 <span data-ttu-id="704f2-105">**string**</span><span class="sxs-lookup"><span data-stu-id="704f2-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="704f2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="704f2-106">Attributes and elements</span></span>

<span data-ttu-id="704f2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="704f2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="704f2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="704f2-108">Attributes</span></span>

<span data-ttu-id="704f2-109">无。</span><span class="sxs-lookup"><span data-stu-id="704f2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="704f2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="704f2-110">Child elements</span></span>

<span data-ttu-id="704f2-111">无。</span><span class="sxs-lookup"><span data-stu-id="704f2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="704f2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="704f2-112">Parent elements</span></span>

|<span data-ttu-id="704f2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="704f2-113">**Element**</span></span>|<span data-ttu-id="704f2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="704f2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="704f2-115">Folder</span><span class="sxs-lookup"><span data-stu-id="704f2-115">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="704f2-116">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="704f2-116">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="704f2-117">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="704f2-117">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="704f2-118">代表邮箱中的 "日历" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="704f2-118">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="704f2-119">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="704f2-119">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="704f2-120">表示邮箱中的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="704f2-120">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="704f2-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="704f2-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="704f2-122">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="704f2-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="704f2-123">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="704f2-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="704f2-124">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="704f2-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="704f2-125">文本值</span><span class="sxs-lookup"><span data-stu-id="704f2-125">Text value</span></span>

<span data-ttu-id="704f2-126">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="704f2-126">A text value is required.</span></span> <span data-ttu-id="704f2-127">文件夹类通常以 "IPF" 开头。</span><span class="sxs-lookup"><span data-stu-id="704f2-127">Folder classes typically start with "IPF."</span></span>
  
## <a name="remarks"></a><span data-ttu-id="704f2-128">说明</span><span class="sxs-lookup"><span data-stu-id="704f2-128">Remarks</span></span>

<span data-ttu-id="704f2-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="704f2-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="704f2-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="704f2-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="704f2-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="704f2-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="704f2-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="704f2-132">Schema Name</span></span>  <br/> |<span data-ttu-id="704f2-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="704f2-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="704f2-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="704f2-134">Validation File</span></span>  <br/> |<span data-ttu-id="704f2-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="704f2-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="704f2-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="704f2-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="704f2-137">False</span><span class="sxs-lookup"><span data-stu-id="704f2-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="704f2-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="704f2-138">See also</span></span>



- [<span data-ttu-id="704f2-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="704f2-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

