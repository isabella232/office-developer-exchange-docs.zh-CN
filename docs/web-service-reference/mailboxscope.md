---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: MailboxScope 元素标识是否搜索或进行对话的提取应跨越主邮箱、 存档邮箱或两个主要并存档邮箱。
ms.openlocfilehash: 89c9776079d686b114d6b744150f1c6df3711eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826293"
---
# <a name="mailboxscope"></a><span data-ttu-id="9880b-103">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="9880b-103">MailboxScope</span></span>

<span data-ttu-id="9880b-104">**MailboxScope**元素标识是否搜索或进行对话的提取应跨越主邮箱、 存档邮箱或两个主要并存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="9880b-104">The **MailboxScope** element identifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span> 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

<span data-ttu-id="9880b-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="9880b-105">**MailboxSearchLocationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9880b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9880b-106">Attributes and elements</span></span>

<span data-ttu-id="9880b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9880b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9880b-108">属性</span><span class="sxs-lookup"><span data-stu-id="9880b-108">Attributes</span></span>

<span data-ttu-id="9880b-109">无。</span><span class="sxs-lookup"><span data-stu-id="9880b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9880b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9880b-110">Child elements</span></span>

<span data-ttu-id="9880b-111">无。</span><span class="sxs-lookup"><span data-stu-id="9880b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9880b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9880b-112">Parent elements</span></span>

<span data-ttu-id="9880b-113">[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [对话 (ConversationType)](conversation-conversationtype.md)</span><span class="sxs-lookup"><span data-stu-id="9880b-113">[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [Conversation (ConversationType)](conversation-conversationtype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9880b-114">文本值</span><span class="sxs-lookup"><span data-stu-id="9880b-114">Text value</span></span>

<span data-ttu-id="9880b-115">**MailboxScope**元素的文本值是用于查找的作用域或获取项目在任一主邮箱跨对话中，存档邮箱或两个主和存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="9880b-115">The text value of the **MailboxScope** element is the scope for finding or getting items in a conversation across either primary mailboxes, archive mailboxes, or both primary and archive mailboxes.</span></span> <span data-ttu-id="9880b-116">**PrimaryOnly**文本值表示目标用户的主邮箱的范围。</span><span class="sxs-lookup"><span data-stu-id="9880b-116">A text value of **PrimaryOnly** indicates a scope that targets the primary mailbox for a user.</span></span> <span data-ttu-id="9880b-117">**ArchiveOnly**文本值表示目标用户的存档邮箱的范围。</span><span class="sxs-lookup"><span data-stu-id="9880b-117">A text value of **ArchiveOnly** indicates a scope that targets the archive mailbox for a user.</span></span> <span data-ttu-id="9880b-118">文本值的**所有**表示目标的主邮箱和存档邮箱的范围。</span><span class="sxs-lookup"><span data-stu-id="9880b-118">A text value of **All** indicates a scope that targets both the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9880b-119">备注</span><span class="sxs-lookup"><span data-stu-id="9880b-119">Remarks</span></span>

<span data-ttu-id="9880b-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9880b-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9880b-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9880b-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9880b-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="9880b-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9880b-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="9880b-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9880b-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="9880b-124">Schema name</span></span>  <br/> |<span data-ttu-id="9880b-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="9880b-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9880b-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="9880b-126">Validation file</span></span>  <br/> |<span data-ttu-id="9880b-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9880b-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9880b-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="9880b-128">Can be empty</span></span>  <br/> |<span data-ttu-id="9880b-129">false</span><span class="sxs-lookup"><span data-stu-id="9880b-129">false</span></span>  <br/> |
   

