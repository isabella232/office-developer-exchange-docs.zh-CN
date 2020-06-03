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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458850"
---
# <a name="uniqueunreadsenders"></a><span data-ttu-id="75e45-104">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="75e45-104">UniqueUnreadSenders</span></span>

<span data-ttu-id="75e45-105">**UniqueUnreadSenders**元素包含已发送当前文件夹中此对话中当前未读邮件的所有人员的列表。</span><span class="sxs-lookup"><span data-stu-id="75e45-105">The **UniqueUnreadSenders** element contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="75e45-106">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="75e45-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="75e45-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="75e45-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="75e45-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="75e45-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="75e45-109">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="75e45-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="75e45-110">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="75e45-110">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md)
  
```XML
<UniqueUnreadSenders>
   <String/>
</UniqueUnreadSenders>
```

 <span data-ttu-id="75e45-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="75e45-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75e45-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="75e45-112">Attributes and elements</span></span>

<span data-ttu-id="75e45-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="75e45-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75e45-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="75e45-114">Attributes</span></span>

<span data-ttu-id="75e45-115">无。</span><span class="sxs-lookup"><span data-stu-id="75e45-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75e45-116">子元素</span><span class="sxs-lookup"><span data-stu-id="75e45-116">Child elements</span></span>

|<span data-ttu-id="75e45-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="75e45-117">**Element**</span></span>|<span data-ttu-id="75e45-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="75e45-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75e45-119">字符串</span><span class="sxs-lookup"><span data-stu-id="75e45-119">String</span></span>](string.md) <br/> |<span data-ttu-id="75e45-120">包含单个对话发件人。</span><span class="sxs-lookup"><span data-stu-id="75e45-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="75e45-121">父元素</span><span class="sxs-lookup"><span data-stu-id="75e45-121">Parent elements</span></span>

|<span data-ttu-id="75e45-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="75e45-122">**Element**</span></span>|<span data-ttu-id="75e45-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="75e45-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75e45-124">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="75e45-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="75e45-125">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="75e45-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="75e45-126">文本值</span><span class="sxs-lookup"><span data-stu-id="75e45-126">Text value</span></span>

<span data-ttu-id="75e45-127">无。</span><span class="sxs-lookup"><span data-stu-id="75e45-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75e45-128">说明</span><span class="sxs-lookup"><span data-stu-id="75e45-128">Remarks</span></span>

<span data-ttu-id="75e45-129">此元素是在 Exchange Server 2010 Service Pack 1 （SP1）中引入的。描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="75e45-129">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75e45-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="75e45-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75e45-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="75e45-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="75e45-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="75e45-132">Schema name</span></span>  <br/> |<span data-ttu-id="75e45-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="75e45-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="75e45-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="75e45-134">Validation file</span></span>  <br/> |<span data-ttu-id="75e45-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="75e45-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="75e45-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="75e45-136">Can be empty</span></span>  <br/> |<span data-ttu-id="75e45-137">False</span><span class="sxs-lookup"><span data-stu-id="75e45-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75e45-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="75e45-138">See also</span></span>



[<span data-ttu-id="75e45-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="75e45-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="75e45-140">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="75e45-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="75e45-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="75e45-141">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

