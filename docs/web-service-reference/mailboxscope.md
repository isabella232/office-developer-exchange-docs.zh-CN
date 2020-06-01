---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: MailboxScope 元素确定对话的搜索或获取是否应跨越主邮箱、存档邮箱或主邮箱和存档邮箱。
ms.openlocfilehash: 92823c06d4fe186917c3cfb532eda821bd6a95a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455371"
---
# <a name="mailboxscope"></a><span data-ttu-id="540a6-103">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="540a6-103">MailboxScope</span></span>

<span data-ttu-id="540a6-104">**MailboxScope**元素确定对话的搜索或获取是否应跨越主邮箱、存档邮箱或主邮箱和存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="540a6-104">The **MailboxScope** element identifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span> 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

<span data-ttu-id="540a6-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="540a6-105">**MailboxSearchLocationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="540a6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="540a6-106">Attributes and elements</span></span>

<span data-ttu-id="540a6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="540a6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="540a6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="540a6-108">Attributes</span></span>

<span data-ttu-id="540a6-109">无。</span><span class="sxs-lookup"><span data-stu-id="540a6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="540a6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="540a6-110">Child elements</span></span>

<span data-ttu-id="540a6-111">无。</span><span class="sxs-lookup"><span data-stu-id="540a6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="540a6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="540a6-112">Parent elements</span></span>

<span data-ttu-id="540a6-113">[FindConversation](findconversation.md)  | [GetConversationItems](getconversationitems.md)  | [对话（ConversationType）](conversation-conversationtype.md)</span><span class="sxs-lookup"><span data-stu-id="540a6-113">[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [Conversation (ConversationType)](conversation-conversationtype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="540a6-114">文本值</span><span class="sxs-lookup"><span data-stu-id="540a6-114">Text value</span></span>

<span data-ttu-id="540a6-115">**MailboxScope**元素的文本值是在整个主邮箱、存档邮箱或主邮箱和存档邮箱中查找或获取项目的作用域。</span><span class="sxs-lookup"><span data-stu-id="540a6-115">The text value of the **MailboxScope** element is the scope for finding or getting items in a conversation across either primary mailboxes, archive mailboxes, or both primary and archive mailboxes.</span></span> <span data-ttu-id="540a6-116">**PrimaryOnly**的文本值表示针对某个用户的主邮箱的作用域。</span><span class="sxs-lookup"><span data-stu-id="540a6-116">A text value of **PrimaryOnly** indicates a scope that targets the primary mailbox for a user.</span></span> <span data-ttu-id="540a6-117">**ArchiveOnly**的文本值表示针对某个用户的存档邮箱的作用域。</span><span class="sxs-lookup"><span data-stu-id="540a6-117">A text value of **ArchiveOnly** indicates a scope that targets the archive mailbox for a user.</span></span> <span data-ttu-id="540a6-118">"**全部**" 文本值表示一个作用域，该作用域面向主邮箱和存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="540a6-118">A text value of **All** indicates a scope that targets both the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="540a6-119">备注</span><span class="sxs-lookup"><span data-stu-id="540a6-119">Remarks</span></span>

<span data-ttu-id="540a6-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="540a6-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="540a6-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="540a6-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="540a6-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="540a6-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="540a6-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="540a6-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="540a6-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="540a6-124">Schema name</span></span>  <br/> |<span data-ttu-id="540a6-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="540a6-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="540a6-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="540a6-126">Validation file</span></span>  <br/> |<span data-ttu-id="540a6-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="540a6-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="540a6-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="540a6-128">Can be empty</span></span>  <br/> |<span data-ttu-id="540a6-129">false</span><span class="sxs-lookup"><span data-stu-id="540a6-129">false</span></span>  <br/> |
   

