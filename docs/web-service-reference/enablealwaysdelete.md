---
title: EnableAlwaysDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EnableAlwaysDelete
api_type:
- schema
ms.assetid: 7753aec5-3f93-4aeb-a28e-8b9b42ca7f9b
description: EnableAlwaysDelete 元素指定一个标志，该标志为对话中的所有新项目启用删除。
ms.openlocfilehash: 14784d3a6ba52c76b64b81e15c0522d66d125cbf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526205"
---
# <a name="enablealwaysdelete"></a><span data-ttu-id="aab7f-103">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="aab7f-103">EnableAlwaysDelete</span></span>

<span data-ttu-id="aab7f-104">**EnableAlwaysDelete**元素指定一个标志，该标志为对话中的所有新项目启用删除。</span><span class="sxs-lookup"><span data-stu-id="aab7f-104">The **EnableAlwaysDelete** element specifies a flag that enables deletion for all new items in a conversation.</span></span> 
  
[<span data-ttu-id="aab7f-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="aab7f-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="aab7f-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="aab7f-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="aab7f-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="aab7f-107">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="aab7f-108">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="aab7f-108">EnableAlwaysDelete</span></span>](enablealwaysdelete.md)
  
```XML
<EnableAlwaysDelete/>
```

 <span data-ttu-id="aab7f-109">**xs： boolean**</span><span class="sxs-lookup"><span data-stu-id="aab7f-109">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aab7f-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aab7f-110">Attributes and elements</span></span>

<span data-ttu-id="aab7f-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aab7f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aab7f-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="aab7f-112">Attributes</span></span>

<span data-ttu-id="aab7f-113">无。</span><span class="sxs-lookup"><span data-stu-id="aab7f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aab7f-114">子元素</span><span class="sxs-lookup"><span data-stu-id="aab7f-114">Child elements</span></span>

<span data-ttu-id="aab7f-115">无。</span><span class="sxs-lookup"><span data-stu-id="aab7f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aab7f-116">父元素</span><span class="sxs-lookup"><span data-stu-id="aab7f-116">Parent elements</span></span>

|<span data-ttu-id="aab7f-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="aab7f-117">**Element**</span></span>|<span data-ttu-id="aab7f-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="aab7f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aab7f-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="aab7f-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="aab7f-120">包含要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="aab7f-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aab7f-121">文本值</span><span class="sxs-lookup"><span data-stu-id="aab7f-121">Text value</span></span>

<span data-ttu-id="aab7f-122">**EnableAlwaysDelete**元素的文本值为**true** ，以启用删除对话中的所有项目;否则**为 false**。</span><span class="sxs-lookup"><span data-stu-id="aab7f-122">The text value of the **EnableAlwaysDelete** element is **true** to enable the deletion of all items in conversation; otherwise, **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aab7f-123">备注</span><span class="sxs-lookup"><span data-stu-id="aab7f-123">Remarks</span></span>

<span data-ttu-id="aab7f-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="aab7f-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aab7f-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="aab7f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aab7f-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="aab7f-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aab7f-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="aab7f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="aab7f-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="aab7f-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="aab7f-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="aab7f-129">Validation File</span></span>  <br/> |<span data-ttu-id="aab7f-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aab7f-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aab7f-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="aab7f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="aab7f-132">False</span><span class="sxs-lookup"><span data-stu-id="aab7f-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aab7f-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aab7f-133">See also</span></span>



[<span data-ttu-id="aab7f-134">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="aab7f-134">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

