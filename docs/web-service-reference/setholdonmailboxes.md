---
title: SetHoldOnMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fd5b9f0e-23e8-428c-8168-2d6b4ecd6beb
description: SetHoldOnMailboxes 元素包含一个 SetHoldOnMailboxes 请求。
ms.openlocfilehash: 7d226de908c4d5a474129e3e1f2344ec1318f538
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827413"
---
# <a name="setholdonmailboxes"></a><span data-ttu-id="82329-103">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="82329-103">SetHoldOnMailboxes</span></span>

<span data-ttu-id="82329-104">**SetHoldOnMailboxes**元素包含一个**SetHoldOnMailboxes**请求。</span><span class="sxs-lookup"><span data-stu-id="82329-104">The **SetHoldOnMailboxes** element contains a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxes>
   <ActionType/>
   <HoldId/>
   <Query/>
   <Mailboxes/>
   <Language/>
   <IncludeNonIndexableItems/>
   <Deduplication/>
   <InPlaceHoldIdentity/>
</SetHoldOnMailboxes>
```

 <span data-ttu-id="82329-105">**SetHoldOnMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="82329-105">**SetHoldOnMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82329-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="82329-106">Attributes and elements</span></span>

<span data-ttu-id="82329-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="82329-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82329-108">属性</span><span class="sxs-lookup"><span data-stu-id="82329-108">Attributes</span></span>

<span data-ttu-id="82329-109">无。</span><span class="sxs-lookup"><span data-stu-id="82329-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82329-110">子元素</span><span class="sxs-lookup"><span data-stu-id="82329-110">Child elements</span></span>

<span data-ttu-id="82329-111">[ActionType (HoldActionType)](actiontype-holdactiontype.md) | [HoldId](holdid.md) | [查询](query.md) | [邮箱 (ArrayOfStringsType)](mailboxes-arrayofstringstype.md) | [语言](language.md) | [IncludeNonIndexableItems](includenonindexableitems.md) | [消除](deduplication.md)  |  [InPlaceHoldIdentity](inplaceholdidentity.md)</span><span class="sxs-lookup"><span data-stu-id="82329-111">[ActionType (HoldActionType)](actiontype-holdactiontype.md) | [HoldId](holdid.md) | [Query](query.md) | [Mailboxes (ArrayOfStringsType)](mailboxes-arrayofstringstype.md) | [Language](language.md) | [IncludeNonIndexableItems](includenonindexableitems.md) | [Deduplication](deduplication.md) | [InPlaceHoldIdentity](inplaceholdidentity.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="82329-112">父元素</span><span class="sxs-lookup"><span data-stu-id="82329-112">Parent elements</span></span>

<span data-ttu-id="82329-113">无。</span><span class="sxs-lookup"><span data-stu-id="82329-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82329-114">备注</span><span class="sxs-lookup"><span data-stu-id="82329-114">Remarks</span></span>

<span data-ttu-id="82329-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="82329-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="82329-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="82329-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82329-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="82329-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82329-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="82329-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="82329-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="82329-119">Schema name</span></span>  <br/> |<span data-ttu-id="82329-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="82329-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="82329-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="82329-121">Validation file</span></span>  <br/> |<span data-ttu-id="82329-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="82329-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="82329-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="82329-123">Can be empty</span></span>  <br/> ||
   

