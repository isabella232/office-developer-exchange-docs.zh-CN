---
title: UnreadCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnreadCount
api_type:
- schema
ms.assetid: 53b22647-1453-4707-9ea0-6a8369748d56
description: UnreadCount 元素包含文件夹中的未读项目的计数。
ms.openlocfilehash: fbe887f8f6d83fbcf48ed9593b3d19322a7f48be
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838350"
---
# <a name="unreadcount"></a><span data-ttu-id="8509e-103">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="8509e-103">UnreadCount</span></span>

<span data-ttu-id="8509e-104">**UnreadCount**元素包含文件夹中的未读项目的计数。</span><span class="sxs-lookup"><span data-stu-id="8509e-104">The **UnreadCount** element contains the count of unread items within a folder.</span></span> 
  
```XML
<UnreadCount/>
```

 <span data-ttu-id="8509e-105">**xs:int**</span><span class="sxs-lookup"><span data-stu-id="8509e-105">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8509e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8509e-106">Attributes and elements</span></span>

<span data-ttu-id="8509e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8509e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8509e-108">属性</span><span class="sxs-lookup"><span data-stu-id="8509e-108">Attributes</span></span>

<span data-ttu-id="8509e-109">无。</span><span class="sxs-lookup"><span data-stu-id="8509e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8509e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8509e-110">Child elements</span></span>

<span data-ttu-id="8509e-111">无。</span><span class="sxs-lookup"><span data-stu-id="8509e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8509e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8509e-112">Parent elements</span></span>

|<span data-ttu-id="8509e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8509e-113">**Element**</span></span>|<span data-ttu-id="8509e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8509e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8509e-115">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="8509e-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="8509e-116">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="8509e-116">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="8509e-117">Folder</span><span class="sxs-lookup"><span data-stu-id="8509e-117">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="8509e-118">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="8509e-118">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8509e-119">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="8509e-119">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="8509e-120">表示修改项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="8509e-120">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="8509e-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="8509e-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="8509e-122">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="8509e-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8509e-123">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="8509e-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="8509e-124">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="8509e-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8509e-125">文本值</span><span class="sxs-lookup"><span data-stu-id="8509e-125">Text value</span></span>

<span data-ttu-id="8509e-126">文本值表示的整数值。</span><span class="sxs-lookup"><span data-stu-id="8509e-126">The text value represents an integer value.</span></span> <span data-ttu-id="8509e-127">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="8509e-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8509e-128">备注</span><span class="sxs-lookup"><span data-stu-id="8509e-128">Remarks</span></span>

<span data-ttu-id="8509e-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8509e-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8509e-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="8509e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8509e-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="8509e-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8509e-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="8509e-132">Schema Name</span></span>  <br/> |<span data-ttu-id="8509e-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="8509e-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="8509e-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="8509e-134">Validation File</span></span>  <br/> |<span data-ttu-id="8509e-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8509e-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8509e-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="8509e-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="8509e-137">False</span><span class="sxs-lookup"><span data-stu-id="8509e-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8509e-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8509e-138">See also</span></span>



- [<span data-ttu-id="8509e-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8509e-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

