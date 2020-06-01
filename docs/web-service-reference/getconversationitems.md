---
title: GetConversationItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f7bcd0f-140c-4cbc-a5ed-daeffded1df1
description: GetConversationItems 元素定义一个请求，以获取一组与同一对话相关的项目。
ms.openlocfilehash: cde4bc2c39ccbc51b7436c87c4bc06e3b8d7e52c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457744"
---
# <a name="getconversationitems"></a><span data-ttu-id="52cde-103">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="52cde-103">GetConversationItems</span></span>

<span data-ttu-id="52cde-104">**GetConversationItems**元素定义一个请求，以获取一组与同一对话相关的项目。</span><span class="sxs-lookup"><span data-stu-id="52cde-104">The **GetConversationItems** element defines a request to get a set of items that are related by being in the same conversation.</span></span> 
  
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

 <span data-ttu-id="52cde-105">**GetConversationItemsType**</span><span class="sxs-lookup"><span data-stu-id="52cde-105">**GetConversationItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52cde-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52cde-106">Attributes and elements</span></span>

<span data-ttu-id="52cde-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52cde-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52cde-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="52cde-108">Attributes</span></span>

<span data-ttu-id="52cde-109">无。</span><span class="sxs-lookup"><span data-stu-id="52cde-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52cde-110">子元素</span><span class="sxs-lookup"><span data-stu-id="52cde-110">Child elements</span></span>

<span data-ttu-id="52cde-111">[ItemShape](itemshape.md)  | [FoldersToIgnore](folderstoignore.md)  | [MaxItemsToReturn](maxitemstoreturn.md)  | [SortOrder （ConversationNodeSortOrder）](sortorder-conversationnodesortorder.md)  | [MailboxScope](mailboxscope.md)  | [对话](conversations-ex15websvcsotherref.md)</span><span class="sxs-lookup"><span data-stu-id="52cde-111">[ItemShape](itemshape.md) | [FoldersToIgnore](folderstoignore.md) | [MaxItemsToReturn](maxitemstoreturn.md) | [SortOrder (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md) | [MailboxScope](mailboxscope.md) | [Conversations](conversations-ex15websvcsotherref.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="52cde-112">父元素</span><span class="sxs-lookup"><span data-stu-id="52cde-112">Parent elements</span></span>

<span data-ttu-id="52cde-113">无。</span><span class="sxs-lookup"><span data-stu-id="52cde-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52cde-114">说明</span><span class="sxs-lookup"><span data-stu-id="52cde-114">Remarks</span></span>

<span data-ttu-id="52cde-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="52cde-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="52cde-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52cde-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52cde-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="52cde-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52cde-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="52cde-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="52cde-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="52cde-119">Schema name</span></span>  <br/> |<span data-ttu-id="52cde-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="52cde-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="52cde-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="52cde-121">Validation file</span></span>  <br/> |<span data-ttu-id="52cde-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="52cde-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52cde-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="52cde-123">Can be empty</span></span>  <br/> |<span data-ttu-id="52cde-124">false</span><span class="sxs-lookup"><span data-stu-id="52cde-124">false</span></span>  <br/> |
   

