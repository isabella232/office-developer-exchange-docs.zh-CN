---
title: 对话（ConversationRequestType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0308b71c-d4ff-44a8-b9ca-d5965291ee1d
description: 会话元素表示 GetConversationItems 响应中返回的单个对话。
ms.openlocfilehash: 925fd6fce83cad36f4a0e95bb6228ba65e4e9c43
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466778"
---
# <a name="conversation-conversationrequesttype"></a><span data-ttu-id="03f07-103">对话（ConversationRequestType）</span><span class="sxs-lookup"><span data-stu-id="03f07-103">Conversation (ConversationRequestType)</span></span>

<span data-ttu-id="03f07-104">**会话**元素表示**GetConversationItems**响应中返回的单个对话。</span><span class="sxs-lookup"><span data-stu-id="03f07-104">The **Conversation** element represents a single conversation returned in a **GetConversationItems** response.</span></span> 
  
```XML
<Conversation>
   <ConversationId/>
   <SyncState/>
</Conversation>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="03f07-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="03f07-105">Attributes and elements</span></span>

<span data-ttu-id="03f07-106">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="03f07-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="03f07-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="03f07-107">Attributes</span></span>

<span data-ttu-id="03f07-108">无。</span><span class="sxs-lookup"><span data-stu-id="03f07-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="03f07-109">子元素</span><span class="sxs-lookup"><span data-stu-id="03f07-109">Child elements</span></span>

<span data-ttu-id="03f07-110">[ConversationId](conversationid.md)  | [SyncState （base64Binary）](syncstate-base64binary.md)</span><span class="sxs-lookup"><span data-stu-id="03f07-110">[ConversationId](conversationid.md) | [SyncState (base64Binary)](syncstate-base64binary.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="03f07-111">父元素</span><span class="sxs-lookup"><span data-stu-id="03f07-111">Parent elements</span></span>

[<span data-ttu-id="03f07-112">对话</span><span class="sxs-lookup"><span data-stu-id="03f07-112">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="03f07-113">备注</span><span class="sxs-lookup"><span data-stu-id="03f07-113">Remarks</span></span>

<span data-ttu-id="03f07-114">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="03f07-114">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="03f07-115">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="03f07-115">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="03f07-116">元素信息</span><span class="sxs-lookup"><span data-stu-id="03f07-116">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03f07-117">命名空间</span><span class="sxs-lookup"><span data-stu-id="03f07-117">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="03f07-118">架构名称</span><span class="sxs-lookup"><span data-stu-id="03f07-118">Schema name</span></span>  <br/> |<span data-ttu-id="03f07-119">类型架构</span><span class="sxs-lookup"><span data-stu-id="03f07-119">Types schema</span></span>  <br/> |
|<span data-ttu-id="03f07-120">验证文件</span><span class="sxs-lookup"><span data-stu-id="03f07-120">Validation file</span></span>  <br/> |<span data-ttu-id="03f07-121">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="03f07-121">types.xsd</span></span>  <br/> |
|<span data-ttu-id="03f07-122">可以为空</span><span class="sxs-lookup"><span data-stu-id="03f07-122">Can be empty</span></span>  <br/> |<span data-ttu-id="03f07-123">false</span><span class="sxs-lookup"><span data-stu-id="03f07-123">false</span></span>  <br/> |
   

