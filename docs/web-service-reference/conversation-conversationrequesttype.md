---
title: 对话 (ConversationRequestType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0308b71c-d4ff-44a8-b9ca-d5965291ee1d
description: Conversation 元素表示 GetConversationItems 响应中返回单个对话。
ms.openlocfilehash: ef56e26fda7d2bf6556069355918aa576ce14cb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753572"
---
# <a name="conversation-conversationrequesttype"></a><span data-ttu-id="34349-103">对话 (ConversationRequestType)</span><span class="sxs-lookup"><span data-stu-id="34349-103">Conversation (ConversationRequestType)</span></span>

<span data-ttu-id="34349-104">**Conversation**元素表示**GetConversationItems**响应中返回单个对话。</span><span class="sxs-lookup"><span data-stu-id="34349-104">The **Conversation** element represents a single conversation returned in a **GetConversationItems** response.</span></span> 
  
```XML
<Conversation>
   <ConversationId/>
   <SyncState/>
</Conversation>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="34349-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="34349-105">Attributes and elements</span></span>

<span data-ttu-id="34349-106">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="34349-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34349-107">属性</span><span class="sxs-lookup"><span data-stu-id="34349-107">Attributes</span></span>

<span data-ttu-id="34349-108">无。</span><span class="sxs-lookup"><span data-stu-id="34349-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34349-109">子元素</span><span class="sxs-lookup"><span data-stu-id="34349-109">Child elements</span></span>

<span data-ttu-id="34349-110">[ConversationId](conversationid.md) | [SyncState (base64Binary)](syncstate-base64binary.md)</span><span class="sxs-lookup"><span data-stu-id="34349-110">[ConversationId](conversationid.md) | [SyncState (base64Binary)](syncstate-base64binary.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="34349-111">父元素</span><span class="sxs-lookup"><span data-stu-id="34349-111">Parent elements</span></span>

[<span data-ttu-id="34349-112">Conversations</span><span class="sxs-lookup"><span data-stu-id="34349-112">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="34349-113">备注</span><span class="sxs-lookup"><span data-stu-id="34349-113">Remarks</span></span>

<span data-ttu-id="34349-114">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="34349-114">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="34349-115">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="34349-115">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34349-116">元素信息</span><span class="sxs-lookup"><span data-stu-id="34349-116">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34349-117">命名空间</span><span class="sxs-lookup"><span data-stu-id="34349-117">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="34349-118">架构名称</span><span class="sxs-lookup"><span data-stu-id="34349-118">Schema name</span></span>  <br/> |<span data-ttu-id="34349-119">类型架构</span><span class="sxs-lookup"><span data-stu-id="34349-119">Types schema</span></span>  <br/> |
|<span data-ttu-id="34349-120">验证文件</span><span class="sxs-lookup"><span data-stu-id="34349-120">Validation file</span></span>  <br/> |<span data-ttu-id="34349-121">types.xsd</span><span class="sxs-lookup"><span data-stu-id="34349-121">types.xsd</span></span>  <br/> |
|<span data-ttu-id="34349-122">可以为空</span><span class="sxs-lookup"><span data-stu-id="34349-122">Can be empty</span></span>  <br/> |<span data-ttu-id="34349-123">false</span><span class="sxs-lookup"><span data-stu-id="34349-123">false</span></span>  <br/> |
   

