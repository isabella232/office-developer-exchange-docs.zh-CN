---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: SeekToConditionPageItemView 元素标识用于标识的末尾搜索、 搜索、 返回，最大条目和 FindItem 或 FindConversation 搜索的搜索方向的起始索引的条件。
ms.openlocfilehash: e95246079f8c6e7acffac1dabb278895265767d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827328"
---
# <a name="seektoconditionpageitemview"></a><span data-ttu-id="c3eab-103">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="c3eab-103">SeekToConditionPageItemView</span></span>

<span data-ttu-id="c3eab-104">**SeekToConditionPageItemView**元素标识用于**FindItem**或**FindConversation 标识的末尾搜索、 搜索和返回，最大条目的搜索方向的起始索引的条件**搜索。</span><span class="sxs-lookup"><span data-stu-id="c3eab-104">The **SeekToConditionPageItemView** element identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span> 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 <span data-ttu-id="c3eab-105">**SeekToConditionPageViewType**</span><span class="sxs-lookup"><span data-stu-id="c3eab-105">**SeekToConditionPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c3eab-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c3eab-106">Attributes and elements</span></span>

<span data-ttu-id="c3eab-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c3eab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3eab-108">属性</span><span class="sxs-lookup"><span data-stu-id="c3eab-108">Attributes</span></span>

|<span data-ttu-id="c3eab-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c3eab-109">**Attribute**</span></span>|<span data-ttu-id="c3eab-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c3eab-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c3eab-111">基点</span><span class="sxs-lookup"><span data-stu-id="c3eab-111">BasePoint</span></span>  <br/> |<span data-ttu-id="c3eab-112">**基点**属性的文本值是从将在启动搜索基本点。</span><span class="sxs-lookup"><span data-stu-id="c3eab-112">The text value of the **BasePoint** attribute is the base point from where the search will start.</span></span> <span data-ttu-id="c3eab-113">**开头**的文本值指示搜索将结果集的开头开始。</span><span class="sxs-lookup"><span data-stu-id="c3eab-113">A text value of **Beginning** indicates that the search will start at the beginning of the result set.</span></span> <span data-ttu-id="c3eab-114">**结束**文本值指示搜索将结果集末尾开始。</span><span class="sxs-lookup"><span data-stu-id="c3eab-114">A text value of **End** indicates that the search will start at the end of the result set.</span></span>  <br/> |
|<span data-ttu-id="c3eab-115">MaxEntriesReturned</span><span class="sxs-lookup"><span data-stu-id="c3eab-115">MaxEntriesReturned</span></span>  <br/> |<span data-ttu-id="c3eab-116">**MaxEntriesReturned**属性的文本值是可以在结果集中返回的项的最大数目。</span><span class="sxs-lookup"><span data-stu-id="c3eab-116">The text value of the **MaxEntriesReturned** attribute is the maximum number of items that can be returned in a result set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c3eab-117">子元素</span><span class="sxs-lookup"><span data-stu-id="c3eab-117">Child elements</span></span>

[<span data-ttu-id="c3eab-118">条件 (RestrictionType)</span><span class="sxs-lookup"><span data-stu-id="c3eab-118">Condition (RestrictionType)</span></span>](condition-restrictiontype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="c3eab-119">父元素</span><span class="sxs-lookup"><span data-stu-id="c3eab-119">Parent elements</span></span>

<span data-ttu-id="c3eab-120">[FindConversation](findconversation.md) | [FindItem](finditem.md)</span><span class="sxs-lookup"><span data-stu-id="c3eab-120">[FindConversation](findconversation.md) | [FindItem](finditem.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c3eab-121">备注</span><span class="sxs-lookup"><span data-stu-id="c3eab-121">Remarks</span></span>

<span data-ttu-id="c3eab-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c3eab-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c3eab-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c3eab-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3eab-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c3eab-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3eab-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c3eab-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c3eab-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c3eab-126">Schema name</span></span>  <br/> |<span data-ttu-id="c3eab-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="c3eab-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c3eab-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c3eab-128">Validation file</span></span>  <br/> |<span data-ttu-id="c3eab-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c3eab-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c3eab-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c3eab-130">Can be empty</span></span>  <br/> |<span data-ttu-id="c3eab-131">false</span><span class="sxs-lookup"><span data-stu-id="c3eab-131">false</span></span>  <br/> |
   

