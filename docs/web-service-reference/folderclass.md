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
description: FolderClass 元素表示的文件夹的文件夹类。
ms.openlocfilehash: 87be00563d0375abebf32159ff38d62d03112b95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754384"
---
# <a name="folderclass"></a><span data-ttu-id="59467-103">FolderClass</span><span class="sxs-lookup"><span data-stu-id="59467-103">FolderClass</span></span>

<span data-ttu-id="59467-104">**FolderClass**元素表示的文件夹的文件夹类。</span><span class="sxs-lookup"><span data-stu-id="59467-104">The **FolderClass** element represents the folder class for a folder.</span></span> 
  
```xml
<FolderClass/>
```

 <span data-ttu-id="59467-105">**string**</span><span class="sxs-lookup"><span data-stu-id="59467-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59467-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="59467-106">Attributes and elements</span></span>

<span data-ttu-id="59467-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="59467-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59467-108">属性</span><span class="sxs-lookup"><span data-stu-id="59467-108">Attributes</span></span>

<span data-ttu-id="59467-109">无。</span><span class="sxs-lookup"><span data-stu-id="59467-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59467-110">子元素</span><span class="sxs-lookup"><span data-stu-id="59467-110">Child elements</span></span>

<span data-ttu-id="59467-111">无。</span><span class="sxs-lookup"><span data-stu-id="59467-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="59467-112">父元素</span><span class="sxs-lookup"><span data-stu-id="59467-112">Parent elements</span></span>

|<span data-ttu-id="59467-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="59467-113">**Element**</span></span>|<span data-ttu-id="59467-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="59467-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59467-115">Folder</span><span class="sxs-lookup"><span data-stu-id="59467-115">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="59467-116">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="59467-116">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="59467-117">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="59467-117">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="59467-118">表示邮箱中的日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="59467-118">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="59467-119">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="59467-119">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="59467-120">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="59467-120">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="59467-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="59467-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="59467-122">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="59467-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="59467-123">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="59467-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="59467-124">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="59467-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="59467-125">文本值</span><span class="sxs-lookup"><span data-stu-id="59467-125">Text value</span></span>

<span data-ttu-id="59467-126">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="59467-126">A text value is required.</span></span> <span data-ttu-id="59467-127">文件夹类通常开头"IPF。"</span><span class="sxs-lookup"><span data-stu-id="59467-127">Folder classes typically start with "IPF."</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59467-128">备注</span><span class="sxs-lookup"><span data-stu-id="59467-128">Remarks</span></span>

<span data-ttu-id="59467-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="59467-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59467-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="59467-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59467-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="59467-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="59467-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="59467-132">Schema Name</span></span>  <br/> |<span data-ttu-id="59467-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="59467-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="59467-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="59467-134">Validation File</span></span>  <br/> |<span data-ttu-id="59467-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="59467-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="59467-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="59467-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="59467-137">False</span><span class="sxs-lookup"><span data-stu-id="59467-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59467-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="59467-138">See also</span></span>



- [<span data-ttu-id="59467-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="59467-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

