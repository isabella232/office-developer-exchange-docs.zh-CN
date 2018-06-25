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
description: EnableAlwaysDelete 元素指定允许的所有新项目在对话中删除的标志。
ms.openlocfilehash: f86765c641604afbf13ac962f4b34fbd8de56200
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754104"
---
# <a name="enablealwaysdelete"></a><span data-ttu-id="ee626-103">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="ee626-103">EnableAlwaysDelete</span></span>

<span data-ttu-id="ee626-104">**EnableAlwaysDelete**元素指定允许的所有新项目在对话中删除的标志。</span><span class="sxs-lookup"><span data-stu-id="ee626-104">The **EnableAlwaysDelete** element specifies a flag that enables deletion for all new items in a conversation.</span></span> 
  
[<span data-ttu-id="ee626-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="ee626-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="ee626-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="ee626-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="ee626-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="ee626-107">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="ee626-108">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="ee626-108">EnableAlwaysDelete</span></span>](enablealwaysdelete.md)
  
```XML
<EnableAlwaysDelete/>
```

 <span data-ttu-id="ee626-109">**xs: boolean**</span><span class="sxs-lookup"><span data-stu-id="ee626-109">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ee626-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ee626-110">Attributes and elements</span></span>

<span data-ttu-id="ee626-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ee626-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee626-112">属性</span><span class="sxs-lookup"><span data-stu-id="ee626-112">Attributes</span></span>

<span data-ttu-id="ee626-113">无。</span><span class="sxs-lookup"><span data-stu-id="ee626-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ee626-114">子元素</span><span class="sxs-lookup"><span data-stu-id="ee626-114">Child elements</span></span>

<span data-ttu-id="ee626-115">无。</span><span class="sxs-lookup"><span data-stu-id="ee626-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ee626-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ee626-116">Parent elements</span></span>

|<span data-ttu-id="ee626-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="ee626-117">**Element**</span></span>|<span data-ttu-id="ee626-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="ee626-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee626-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="ee626-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="ee626-120">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="ee626-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ee626-121">文本值</span><span class="sxs-lookup"><span data-stu-id="ee626-121">Text value</span></span>

<span data-ttu-id="ee626-122">**EnableAlwaysDelete**元素的文本值为**true**以启用对话; 中的所有项的删除否则为**false**。</span><span class="sxs-lookup"><span data-stu-id="ee626-122">The text value of the **EnableAlwaysDelete** element is **true** to enable the deletion of all items in conversation; otherwise, **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee626-123">备注</span><span class="sxs-lookup"><span data-stu-id="ee626-123">Remarks</span></span>

<span data-ttu-id="ee626-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ee626-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ee626-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="ee626-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee626-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="ee626-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ee626-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="ee626-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ee626-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="ee626-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="ee626-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="ee626-129">Validation File</span></span>  <br/> |<span data-ttu-id="ee626-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ee626-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ee626-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="ee626-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="ee626-132">False</span><span class="sxs-lookup"><span data-stu-id="ee626-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee626-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ee626-133">See also</span></span>



[<span data-ttu-id="ee626-134">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="ee626-134">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

