---
title: UniqueUnreadSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueUnreadSenders
api_type:
- schema
ms.assetid: eb7d1274-ce2e-4ef8-b47f-e911174aab0c
description: UniqueUnreadSenders 元素包含已发送当前文件夹中此对话中当前未读邮件的所有人员的列表。 此元素是只读的。
ms.openlocfilehash: 0e45362e88be4930b8bc2f641c1fb00cc63c0605
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458850"
---
# <a name="uniqueunreadsenders"></a><span data-ttu-id="69169-104">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="69169-104">UniqueUnreadSenders</span></span>

<span data-ttu-id="69169-105">**UniqueUnreadSenders**元素包含已发送当前文件夹中此对话中当前未读邮件的所有人员的列表。</span><span class="sxs-lookup"><span data-stu-id="69169-105">The **UniqueUnreadSenders** element contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="69169-106">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="69169-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="69169-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="69169-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="69169-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="69169-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="69169-109">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="69169-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="69169-110">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="69169-110">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md)
  
```XML
<UniqueUnreadSenders>
   <String/>
</UniqueUnreadSenders>
```

 <span data-ttu-id="69169-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="69169-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69169-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="69169-112">Attributes and elements</span></span>

<span data-ttu-id="69169-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="69169-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69169-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="69169-114">Attributes</span></span>

<span data-ttu-id="69169-115">无。</span><span class="sxs-lookup"><span data-stu-id="69169-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69169-116">子元素</span><span class="sxs-lookup"><span data-stu-id="69169-116">Child elements</span></span>

|<span data-ttu-id="69169-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="69169-117">**Element**</span></span>|<span data-ttu-id="69169-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="69169-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69169-119">字符串</span><span class="sxs-lookup"><span data-stu-id="69169-119">String</span></span>](string.md) <br/> |<span data-ttu-id="69169-120">包含单个对话发件人。</span><span class="sxs-lookup"><span data-stu-id="69169-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69169-121">父元素</span><span class="sxs-lookup"><span data-stu-id="69169-121">Parent elements</span></span>

|<span data-ttu-id="69169-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="69169-122">**Element**</span></span>|<span data-ttu-id="69169-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="69169-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69169-124">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="69169-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="69169-125">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="69169-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="69169-126">文本值</span><span class="sxs-lookup"><span data-stu-id="69169-126">Text value</span></span>

<span data-ttu-id="69169-127">无。</span><span class="sxs-lookup"><span data-stu-id="69169-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69169-128">说明</span><span class="sxs-lookup"><span data-stu-id="69169-128">Remarks</span></span>

<span data-ttu-id="69169-129">此元素是在 Exchange Server 2010 Service Pack 1 （SP1）中引入的。描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="69169-129">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69169-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="69169-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69169-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="69169-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69169-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="69169-132">Schema name</span></span>  <br/> |<span data-ttu-id="69169-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="69169-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="69169-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="69169-134">Validation file</span></span>  <br/> |<span data-ttu-id="69169-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="69169-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="69169-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="69169-136">Can be empty</span></span>  <br/> |<span data-ttu-id="69169-137">False</span><span class="sxs-lookup"><span data-stu-id="69169-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69169-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69169-138">See also</span></span>



[<span data-ttu-id="69169-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="69169-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="69169-140">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="69169-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="69169-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="69169-141">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

