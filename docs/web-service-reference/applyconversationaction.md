---
title: ApplyConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationAction
api_type:
- schema
ms.assetid: e0ee8f30-529b-4d87-8bc0-b6616e75fb6b
description: ApplyConversationAction 元素定义一个请求，以将操作应用于会话中的项目。
ms.openlocfilehash: 659b3392778bb1a318c3942a0c8e314f12110c12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461686"
---
# <a name="applyconversationaction"></a><span data-ttu-id="15261-103">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="15261-103">ApplyConversationAction</span></span>

<span data-ttu-id="15261-104">**ApplyConversationAction**元素定义一个请求，以将操作应用于会话中的项目。</span><span class="sxs-lookup"><span data-stu-id="15261-104">The **ApplyConversationAction** element defines a request to apply actions to items in a conversation.</span></span> 
  
[<span data-ttu-id="15261-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="15261-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
```XML
<ApplyConversationAction>
   <ConversationActions/>
</ApplyConversationAction>
```

 <span data-ttu-id="15261-106">**ApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="15261-106">**ApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15261-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="15261-107">Attributes and elements</span></span>

<span data-ttu-id="15261-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="15261-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15261-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="15261-109">Attributes</span></span>

<span data-ttu-id="15261-110">无。</span><span class="sxs-lookup"><span data-stu-id="15261-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15261-111">子元素</span><span class="sxs-lookup"><span data-stu-id="15261-111">Child elements</span></span>

|<span data-ttu-id="15261-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="15261-112">**Element**</span></span>|<span data-ttu-id="15261-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="15261-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15261-114">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="15261-114">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="15261-115">包含对话的集合以及要应用于它们的操作。</span><span class="sxs-lookup"><span data-stu-id="15261-115">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15261-116">父元素</span><span class="sxs-lookup"><span data-stu-id="15261-116">Parent elements</span></span>

<span data-ttu-id="15261-117">无。</span><span class="sxs-lookup"><span data-stu-id="15261-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="15261-118">文本值</span><span class="sxs-lookup"><span data-stu-id="15261-118">Text value</span></span>

<span data-ttu-id="15261-119">无。</span><span class="sxs-lookup"><span data-stu-id="15261-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15261-120">说明</span><span class="sxs-lookup"><span data-stu-id="15261-120">Remarks</span></span>

<span data-ttu-id="15261-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="15261-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15261-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="15261-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15261-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="15261-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="15261-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="15261-124">Schema Name</span></span>  <br/> |<span data-ttu-id="15261-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="15261-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="15261-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="15261-126">Validation File</span></span>  <br/> |<span data-ttu-id="15261-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="15261-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="15261-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="15261-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="15261-129">False</span><span class="sxs-lookup"><span data-stu-id="15261-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15261-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15261-130">See also</span></span>

- [<span data-ttu-id="15261-131">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="15261-131">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="15261-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="15261-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

