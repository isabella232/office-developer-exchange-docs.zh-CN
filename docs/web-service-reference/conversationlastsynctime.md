---
title: ConversationLastSyncTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationLastSyncTime
api_type:
- schema
ms.assetid: 90f8f9e3-5fc6-4a6a-bdfb-fc91fa51f8a2
description: ConversationLastSyncTime 元素包含上次同步会话的日期和时间。 在尝试删除会话中的所有已收到指定时间的项目时，必须存在此元素。
ms.openlocfilehash: f7cc6e205ab9936685d7b8c1f34129b799a53021
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461427"
---
# <a name="conversationlastsynctime"></a><span data-ttu-id="1aa4b-104">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="1aa4b-104">ConversationLastSyncTime</span></span>

<span data-ttu-id="1aa4b-105">**ConversationLastSyncTime**元素包含上次同步会话的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="1aa4b-105">The **ConversationLastSyncTime** element contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="1aa4b-106">在尝试删除会话中的所有已收到指定时间的项目时，必须存在此元素。</span><span class="sxs-lookup"><span data-stu-id="1aa4b-106">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span> 
  
[<span data-ttu-id="1aa4b-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="1aa4b-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="1aa4b-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="1aa4b-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="1aa4b-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="1aa4b-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="1aa4b-110">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="1aa4b-110">ConversationLastSyncTime</span></span>](conversationlastsynctime.md)
  
```XML
<ConversationLastSyncTime/>
```

 <span data-ttu-id="1aa4b-111">**xs： dateTime**</span><span class="sxs-lookup"><span data-stu-id="1aa4b-111">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1aa4b-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1aa4b-112">Attributes and elements</span></span>

<span data-ttu-id="1aa4b-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1aa4b-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1aa4b-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="1aa4b-114">Attributes</span></span>

<span data-ttu-id="1aa4b-115">无。</span><span class="sxs-lookup"><span data-stu-id="1aa4b-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1aa4b-116">子元素</span><span class="sxs-lookup"><span data-stu-id="1aa4b-116">Child elements</span></span>

<span data-ttu-id="1aa4b-117">无。</span><span class="sxs-lookup"><span data-stu-id="1aa4b-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1aa4b-118">父元素</span><span class="sxs-lookup"><span data-stu-id="1aa4b-118">Parent elements</span></span>

|<span data-ttu-id="1aa4b-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="1aa4b-119">**Element**</span></span>|<span data-ttu-id="1aa4b-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="1aa4b-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aa4b-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="1aa4b-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="1aa4b-122">包含要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="1aa4b-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1aa4b-123">文本值</span><span class="sxs-lookup"><span data-stu-id="1aa4b-123">Text value</span></span>

<span data-ttu-id="1aa4b-124">**ConversationLastSyncTime**的文本值指示上次同步会话的时间。</span><span class="sxs-lookup"><span data-stu-id="1aa4b-124">The text value of the **ConversationLastSyncTime** indicates the last time the conversation was synchronized.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1aa4b-125">备注</span><span class="sxs-lookup"><span data-stu-id="1aa4b-125">Remarks</span></span>

<span data-ttu-id="1aa4b-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1aa4b-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1aa4b-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="1aa4b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1aa4b-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="1aa4b-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1aa4b-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="1aa4b-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1aa4b-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="1aa4b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="1aa4b-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="1aa4b-131">Validation File</span></span>  <br/> |<span data-ttu-id="1aa4b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1aa4b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1aa4b-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="1aa4b-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1aa4b-134">False</span><span class="sxs-lookup"><span data-stu-id="1aa4b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1aa4b-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1aa4b-135">See also</span></span>



[<span data-ttu-id="1aa4b-136">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="1aa4b-136">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="1aa4b-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1aa4b-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

