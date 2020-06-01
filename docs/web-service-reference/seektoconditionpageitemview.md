---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: SeekToConditionPageItemView 元素标识用于标识搜索的结束的条件、搜索的起始索引、要返回的最大项数以及 FindItem 或 FindConversation 搜索的搜索说明。
ms.openlocfilehash: dbb073263740ccdf75367f85f672b7d5ec78f7a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466834"
---
# <a name="seektoconditionpageitemview"></a><span data-ttu-id="3353e-103">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="3353e-103">SeekToConditionPageItemView</span></span>

<span data-ttu-id="3353e-104">**SeekToConditionPageItemView**元素标识用于标识搜索的结束的条件、搜索的起始索引、要返回的最大项数以及**FindItem**或**FindConversation**搜索的搜索说明。</span><span class="sxs-lookup"><span data-stu-id="3353e-104">The **SeekToConditionPageItemView** element identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span> 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 <span data-ttu-id="3353e-105">**SeekToConditionPageViewType**</span><span class="sxs-lookup"><span data-stu-id="3353e-105">**SeekToConditionPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3353e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3353e-106">Attributes and elements</span></span>

<span data-ttu-id="3353e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3353e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3353e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3353e-108">Attributes</span></span>

|<span data-ttu-id="3353e-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="3353e-109">**Attribute**</span></span>|<span data-ttu-id="3353e-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="3353e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3353e-111">BasePoint</span><span class="sxs-lookup"><span data-stu-id="3353e-111">BasePoint</span></span>  <br/> |<span data-ttu-id="3353e-112">**BasePoint**属性的文本值是搜索将从该处开始的基点。</span><span class="sxs-lookup"><span data-stu-id="3353e-112">The text value of the **BasePoint** attribute is the base point from where the search will start.</span></span> <span data-ttu-id="3353e-113">文本值为 "**开始**" 指示搜索将从结果集的开头开始。</span><span class="sxs-lookup"><span data-stu-id="3353e-113">A text value of **Beginning** indicates that the search will start at the beginning of the result set.</span></span> <span data-ttu-id="3353e-114">文本值为**end**表示搜索将从结果集的末尾开始。</span><span class="sxs-lookup"><span data-stu-id="3353e-114">A text value of **End** indicates that the search will start at the end of the result set.</span></span>  <br/> |
|<span data-ttu-id="3353e-115">MaxEntriesReturned</span><span class="sxs-lookup"><span data-stu-id="3353e-115">MaxEntriesReturned</span></span>  <br/> |<span data-ttu-id="3353e-116">**MaxEntriesReturned**属性的文本值是在结果集中可返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="3353e-116">The text value of the **MaxEntriesReturned** attribute is the maximum number of items that can be returned in a result set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3353e-117">子元素</span><span class="sxs-lookup"><span data-stu-id="3353e-117">Child elements</span></span>

[<span data-ttu-id="3353e-118">条件（RestrictionType）</span><span class="sxs-lookup"><span data-stu-id="3353e-118">Condition (RestrictionType)</span></span>](condition-restrictiontype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="3353e-119">父元素</span><span class="sxs-lookup"><span data-stu-id="3353e-119">Parent elements</span></span>

<span data-ttu-id="3353e-120">[FindConversation](findconversation.md)  | [FindItem](finditem.md)</span><span class="sxs-lookup"><span data-stu-id="3353e-120">[FindConversation](findconversation.md) | [FindItem](finditem.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3353e-121">备注</span><span class="sxs-lookup"><span data-stu-id="3353e-121">Remarks</span></span>

<span data-ttu-id="3353e-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3353e-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3353e-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3353e-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3353e-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="3353e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3353e-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="3353e-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3353e-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="3353e-126">Schema name</span></span>  <br/> |<span data-ttu-id="3353e-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="3353e-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3353e-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="3353e-128">Validation file</span></span>  <br/> |<span data-ttu-id="3353e-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3353e-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3353e-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="3353e-130">Can be empty</span></span>  <br/> |<span data-ttu-id="3353e-131">false</span><span class="sxs-lookup"><span data-stu-id="3353e-131">false</span></span>  <br/> |
   

