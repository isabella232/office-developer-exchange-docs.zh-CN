---
title: TotalCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TotalCount
api_type:
- schema
ms.assetid: c48c6388-8449-4622-bc38-6f0e84293872
description: TotalCount 元素均表示给定文件夹中的项目总数。
ms.openlocfilehash: e4a7bcb70d04bc5bcf66087c0272732a7be1231a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838265"
---
# <a name="totalcount"></a><span data-ttu-id="d7070-103">TotalCount</span><span class="sxs-lookup"><span data-stu-id="d7070-103">TotalCount</span></span>

<span data-ttu-id="d7070-104">**TotalCount**元素均表示给定文件夹中的项目总数。</span><span class="sxs-lookup"><span data-stu-id="d7070-104">The **TotalCount** element represents the total count of items within a given folder.</span></span> 
  
```xml
<TotalCount/>
```

 <span data-ttu-id="d7070-105">**int**</span><span class="sxs-lookup"><span data-stu-id="d7070-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7070-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d7070-106">Attributes and elements</span></span>

<span data-ttu-id="d7070-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d7070-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7070-108">属性</span><span class="sxs-lookup"><span data-stu-id="d7070-108">Attributes</span></span>

<span data-ttu-id="d7070-109">无。</span><span class="sxs-lookup"><span data-stu-id="d7070-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7070-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d7070-110">Child elements</span></span>

<span data-ttu-id="d7070-111">无。</span><span class="sxs-lookup"><span data-stu-id="d7070-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d7070-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d7070-112">Parent elements</span></span>

|<span data-ttu-id="d7070-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d7070-113">**Element**</span></span>|<span data-ttu-id="d7070-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d7070-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7070-115">Folder</span><span class="sxs-lookup"><span data-stu-id="d7070-115">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="d7070-116">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7070-116">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d7070-117">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="d7070-117">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="d7070-118">表示邮箱中的日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7070-118">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d7070-119">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="d7070-119">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="d7070-120">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7070-120">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d7070-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="d7070-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="d7070-122">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7070-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d7070-123">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="d7070-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="d7070-124">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7070-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d7070-125">文本值</span><span class="sxs-lookup"><span data-stu-id="d7070-125">Text value</span></span>

<span data-ttu-id="d7070-126">文本值表示的整数值。</span><span class="sxs-lookup"><span data-stu-id="d7070-126">The text value represents an integer value.</span></span> <span data-ttu-id="d7070-127">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="d7070-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7070-128">备注</span><span class="sxs-lookup"><span data-stu-id="d7070-128">Remarks</span></span>

<span data-ttu-id="d7070-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d7070-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7070-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="d7070-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7070-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="d7070-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d7070-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="d7070-132">Schema Name</span></span>  <br/> |<span data-ttu-id="d7070-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="d7070-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="d7070-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="d7070-134">Validation File</span></span>  <br/> |<span data-ttu-id="d7070-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d7070-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d7070-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="d7070-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="d7070-137">False</span><span class="sxs-lookup"><span data-stu-id="d7070-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7070-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d7070-138">See also</span></span>



- [<span data-ttu-id="d7070-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d7070-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

