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
description: UniqueUnreadSenders 元素包含所有已发送邮件的当前文件夹中的此对话中当前未读的人员列表。 此元素是只读的。
ms.openlocfilehash: d1f5593f6b86745aa27d86e9d25487f5855cb0cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838335"
---
# <a name="uniqueunreadsenders"></a><span data-ttu-id="7edc1-104">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="7edc1-104">UniqueUnreadSenders</span></span>

<span data-ttu-id="7edc1-105">**UniqueUnreadSenders**元素包含所有已发送邮件的当前文件夹中的此对话中当前未读的人员列表。</span><span class="sxs-lookup"><span data-stu-id="7edc1-105">The **UniqueUnreadSenders** element contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="7edc1-106">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="7edc1-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="7edc1-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="7edc1-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="7edc1-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="7edc1-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="7edc1-109">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="7edc1-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="7edc1-110">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="7edc1-110">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md)
  
```XML
<UniqueUnreadSenders>
   <String/>
</UniqueUnreadSenders>
```

 <span data-ttu-id="7edc1-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="7edc1-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7edc1-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7edc1-112">Attributes and elements</span></span>

<span data-ttu-id="7edc1-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7edc1-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7edc1-114">属性</span><span class="sxs-lookup"><span data-stu-id="7edc1-114">Attributes</span></span>

<span data-ttu-id="7edc1-115">无。</span><span class="sxs-lookup"><span data-stu-id="7edc1-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7edc1-116">子元素</span><span class="sxs-lookup"><span data-stu-id="7edc1-116">Child elements</span></span>

|<span data-ttu-id="7edc1-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="7edc1-117">**Element**</span></span>|<span data-ttu-id="7edc1-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="7edc1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7edc1-119">字符串</span><span class="sxs-lookup"><span data-stu-id="7edc1-119">String</span></span>](string.md) <br/> |<span data-ttu-id="7edc1-120">包含单个对话发件人。</span><span class="sxs-lookup"><span data-stu-id="7edc1-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7edc1-121">父元素</span><span class="sxs-lookup"><span data-stu-id="7edc1-121">Parent elements</span></span>

|<span data-ttu-id="7edc1-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="7edc1-122">**Element**</span></span>|<span data-ttu-id="7edc1-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="7edc1-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7edc1-124">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="7edc1-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="7edc1-125">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="7edc1-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7edc1-126">文本值</span><span class="sxs-lookup"><span data-stu-id="7edc1-126">Text value</span></span>

<span data-ttu-id="7edc1-127">无。</span><span class="sxs-lookup"><span data-stu-id="7edc1-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7edc1-128">备注</span><span class="sxs-lookup"><span data-stu-id="7edc1-128">Remarks</span></span>

<span data-ttu-id="7edc1-129">此元素是在 Exchange Server 2010 Service Pack 1 (SP1) 中引入的。描述此元素的架构位于承载 Exchange Web 服务的 IIS 虚拟目录。</span><span class="sxs-lookup"><span data-stu-id="7edc1-129">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7edc1-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="7edc1-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7edc1-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="7edc1-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7edc1-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="7edc1-132">Schema name</span></span>  <br/> |<span data-ttu-id="7edc1-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="7edc1-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="7edc1-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="7edc1-134">Validation file</span></span>  <br/> |<span data-ttu-id="7edc1-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7edc1-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7edc1-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="7edc1-136">Can be empty</span></span>  <br/> |<span data-ttu-id="7edc1-137">False</span><span class="sxs-lookup"><span data-stu-id="7edc1-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7edc1-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7edc1-138">See also</span></span>



[<span data-ttu-id="7edc1-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="7edc1-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="7edc1-140">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="7edc1-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="7edc1-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="7edc1-141">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

