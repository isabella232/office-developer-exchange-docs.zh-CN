---
title: GlobalUniqueUnreadSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUniqueUnreadSenders
api_type:
- schema
ms.assetid: 490abe30-7608-407a-923b-a4b3ddbca610
description: GlobalUniqueUnreadSenders 元素指定在此对话中的所有文件夹中已发送当前未读邮件的所有人员的列表。
ms.openlocfilehash: 5a26053158a262d65993dba4be90888ee97f2112
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530816"
---
# <a name="globaluniqueunreadsenders"></a><span data-ttu-id="ac892-103">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="ac892-103">GlobalUniqueUnreadSenders</span></span>

<span data-ttu-id="ac892-104">**GlobalUniqueUnreadSenders**元素指定在此对话中的所有文件夹中已发送当前未读邮件的所有人员的列表。</span><span class="sxs-lookup"><span data-stu-id="ac892-104">The **GlobalUniqueUnreadSenders** element specifies a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span> 
  
[<span data-ttu-id="ac892-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="ac892-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="ac892-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="ac892-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="ac892-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ac892-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="ac892-108">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="ac892-108">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md)
  
```XML
<GlobalUniqueUnreadSenders>
   <String/>
</GlobalUniqueUnreadSenders>
```

 <span data-ttu-id="ac892-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="ac892-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac892-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ac892-110">Attributes and elements</span></span>

<span data-ttu-id="ac892-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ac892-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac892-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="ac892-112">Attributes</span></span>

<span data-ttu-id="ac892-113">无。</span><span class="sxs-lookup"><span data-stu-id="ac892-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac892-114">子元素</span><span class="sxs-lookup"><span data-stu-id="ac892-114">Child elements</span></span>

|<span data-ttu-id="ac892-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="ac892-115">**Element**</span></span>|<span data-ttu-id="ac892-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="ac892-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac892-117">字符串</span><span class="sxs-lookup"><span data-stu-id="ac892-117">String</span></span>](string.md) <br/> |<span data-ttu-id="ac892-118">包含单个对话发件人。</span><span class="sxs-lookup"><span data-stu-id="ac892-118">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ac892-119">父元素</span><span class="sxs-lookup"><span data-stu-id="ac892-119">Parent elements</span></span>

|<span data-ttu-id="ac892-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="ac892-120">**Element**</span></span>|<span data-ttu-id="ac892-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="ac892-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac892-122">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ac892-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="ac892-123">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="ac892-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ac892-124">文本值</span><span class="sxs-lookup"><span data-stu-id="ac892-124">Text value</span></span>

<span data-ttu-id="ac892-125">无。</span><span class="sxs-lookup"><span data-stu-id="ac892-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ac892-126">说明</span><span class="sxs-lookup"><span data-stu-id="ac892-126">Remarks</span></span>

<span data-ttu-id="ac892-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ac892-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac892-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="ac892-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac892-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="ac892-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac892-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="ac892-130">Schema name</span></span>  <br/> |<span data-ttu-id="ac892-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="ac892-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac892-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="ac892-132">Validation file</span></span>  <br/> |<span data-ttu-id="ac892-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ac892-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac892-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="ac892-134">Can be empty</span></span>  <br/> |<span data-ttu-id="ac892-135">False</span><span class="sxs-lookup"><span data-stu-id="ac892-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac892-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ac892-136">See also</span></span>



[<span data-ttu-id="ac892-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="ac892-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="ac892-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="ac892-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="ac892-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="ac892-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

