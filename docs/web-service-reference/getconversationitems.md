---
title: GetConversationItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f7bcd0f-140c-4cbc-a5ed-daeffded1df1
description: GetConversationItems 元素定义一个请求以获取一组相关的同一个会话中的项。
ms.openlocfilehash: 9be300318a07173e4a8e11e5a6ca78b885de1199
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754490"
---
# <a name="getconversationitems"></a><span data-ttu-id="ea776-103">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="ea776-103">GetConversationItems</span></span>

<span data-ttu-id="ea776-104">**GetConversationItems**元素定义一个请求以获取一组相关的同一个会话中的项。</span><span class="sxs-lookup"><span data-stu-id="ea776-104">The **GetConversationItems** element defines a request to get a set of items that are related by being in the same conversation.</span></span> 
  
```XML
<GetConversationItems>
   <ItemShape/>
   <FoldersToIgnore/>
   <MaxItemsToReturn/>
   <SortOrder/>
   <MailboxScope/>
   <Conversations/>
</GetConversationItems>
```

 <span data-ttu-id="ea776-105">**GetConversationItemsType**</span><span class="sxs-lookup"><span data-stu-id="ea776-105">**GetConversationItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ea776-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ea776-106">Attributes and elements</span></span>

<span data-ttu-id="ea776-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ea776-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea776-108">属性</span><span class="sxs-lookup"><span data-stu-id="ea776-108">Attributes</span></span>

<span data-ttu-id="ea776-109">无。</span><span class="sxs-lookup"><span data-stu-id="ea776-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ea776-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ea776-110">Child elements</span></span>

<span data-ttu-id="ea776-111">[ItemShape](itemshape.md) | [FoldersToIgnore](folderstoignore.md) | [MaxItemsToReturn](maxitemstoreturn.md) | [SortOrder (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md) | [MailboxScope](mailboxscope.md) | [对话](conversations-ex15websvcsotherref.md)</span><span class="sxs-lookup"><span data-stu-id="ea776-111">[ItemShape](itemshape.md) | [FoldersToIgnore](folderstoignore.md) | [MaxItemsToReturn](maxitemstoreturn.md) | [SortOrder (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md) | [MailboxScope](mailboxscope.md) | [Conversations](conversations-ex15websvcsotherref.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ea776-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ea776-112">Parent elements</span></span>

<span data-ttu-id="ea776-113">无。</span><span class="sxs-lookup"><span data-stu-id="ea776-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ea776-114">备注</span><span class="sxs-lookup"><span data-stu-id="ea776-114">Remarks</span></span>

<span data-ttu-id="ea776-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ea776-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ea776-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ea776-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ea776-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="ea776-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea776-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="ea776-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ea776-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="ea776-119">Schema name</span></span>  <br/> |<span data-ttu-id="ea776-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="ea776-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ea776-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="ea776-121">Validation file</span></span>  <br/> |<span data-ttu-id="ea776-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ea776-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ea776-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="ea776-123">Can be empty</span></span>  <br/> |<span data-ttu-id="ea776-124">false</span><span class="sxs-lookup"><span data-stu-id="ea776-124">false</span></span>  <br/> |
   

