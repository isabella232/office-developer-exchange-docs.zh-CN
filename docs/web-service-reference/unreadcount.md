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
description: UnreadCount 元素包含文件夹中未读项目的计数。
ms.openlocfilehash: 72e5d47eac7618408e46ad11eb19eaebf9835502
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467219"
---
# <a name="unreadcount"></a><span data-ttu-id="43358-103">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="43358-103">UnreadCount</span></span>

<span data-ttu-id="43358-104">**UnreadCount**元素包含文件夹中未读项目的计数。</span><span class="sxs-lookup"><span data-stu-id="43358-104">The **UnreadCount** element contains the count of unread items within a folder.</span></span> 
  
```XML
<UnreadCount/>
```

 <span data-ttu-id="43358-105">**xs： int**</span><span class="sxs-lookup"><span data-stu-id="43358-105">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43358-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="43358-106">Attributes and elements</span></span>

<span data-ttu-id="43358-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="43358-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43358-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="43358-108">Attributes</span></span>

<span data-ttu-id="43358-109">无。</span><span class="sxs-lookup"><span data-stu-id="43358-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43358-110">子元素</span><span class="sxs-lookup"><span data-stu-id="43358-110">Child elements</span></span>

<span data-ttu-id="43358-111">无。</span><span class="sxs-lookup"><span data-stu-id="43358-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43358-112">父元素</span><span class="sxs-lookup"><span data-stu-id="43358-112">Parent elements</span></span>

|<span data-ttu-id="43358-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="43358-113">**Element**</span></span>|<span data-ttu-id="43358-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="43358-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43358-115">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="43358-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="43358-116">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="43358-116">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="43358-117">Folder</span><span class="sxs-lookup"><span data-stu-id="43358-117">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="43358-118">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="43358-118">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="43358-119">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="43358-119">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="43358-120">表示一个事件，其中的项或文件夹被修改。</span><span class="sxs-lookup"><span data-stu-id="43358-120">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="43358-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="43358-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="43358-122">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="43358-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="43358-123">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="43358-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="43358-124">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="43358-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="43358-125">文本值</span><span class="sxs-lookup"><span data-stu-id="43358-125">Text value</span></span>

<span data-ttu-id="43358-126">该文本值表示一个整数值。</span><span class="sxs-lookup"><span data-stu-id="43358-126">The text value represents an integer value.</span></span> <span data-ttu-id="43358-127">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="43358-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43358-128">说明</span><span class="sxs-lookup"><span data-stu-id="43358-128">Remarks</span></span>

<span data-ttu-id="43358-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="43358-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43358-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="43358-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43358-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="43358-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43358-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="43358-132">Schema Name</span></span>  <br/> |<span data-ttu-id="43358-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="43358-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="43358-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="43358-134">Validation File</span></span>  <br/> |<span data-ttu-id="43358-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="43358-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43358-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="43358-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="43358-137">False</span><span class="sxs-lookup"><span data-stu-id="43358-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43358-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43358-138">See also</span></span>



- [<span data-ttu-id="43358-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="43358-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

