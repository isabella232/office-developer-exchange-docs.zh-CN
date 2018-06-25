---
title: MailboxStat
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5f24dc30-3ac2-4c82-9dfc-be9dbdb585be
description: MailboxStat 元素指定搜索发现搜索邮箱统计信息。
ms.openlocfilehash: 692f15904467ce192074b14f7c2a742b3e76de8e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826296"
---
# <a name="mailboxstat"></a><span data-ttu-id="e9b4b-103">MailboxStat</span><span class="sxs-lookup"><span data-stu-id="e9b4b-103">MailboxStat</span></span>

<span data-ttu-id="e9b4b-104">**MailboxStat**元素指定搜索发现搜索邮箱统计信息。</span><span class="sxs-lookup"><span data-stu-id="e9b4b-104">The **MailboxStat** element specifies statistics for a mailbox searched by discovery search.</span></span> 
  
```XML
<MailboxStat>
   <MailboxId/>
   <DisplayName/>
   <ItemCount/>
   <Size/>
</MailboxStat>
```

<span data-ttu-id="e9b4b-105">**MailboxStatisticsItemType**</span><span class="sxs-lookup"><span data-stu-id="e9b4b-105">**MailboxStatisticsItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e9b4b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e9b4b-106">Attributes and elements</span></span>

<span data-ttu-id="e9b4b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e9b4b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9b4b-108">属性</span><span class="sxs-lookup"><span data-stu-id="e9b4b-108">Attributes</span></span>

<span data-ttu-id="e9b4b-109">无。</span><span class="sxs-lookup"><span data-stu-id="e9b4b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9b4b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e9b4b-110">Child elements</span></span>

<span data-ttu-id="e9b4b-111">[MailboxId](mailboxid.md) | [DisplayName （字符串）](displayname-string.md) | [ItemCount](itemcount.md) | [大小 (long)](size-long.md)</span><span class="sxs-lookup"><span data-stu-id="e9b4b-111">[MailboxId](mailboxid.md) | [DisplayName (string)](displayname-string.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e9b4b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e9b4b-112">Parent elements</span></span>

[<span data-ttu-id="e9b4b-113">MailboxStats</span><span class="sxs-lookup"><span data-stu-id="e9b4b-113">MailboxStats</span></span>](mailboxstats.md)
  
## <a name="remarks"></a><span data-ttu-id="e9b4b-114">备注</span><span class="sxs-lookup"><span data-stu-id="e9b4b-114">Remarks</span></span>

<span data-ttu-id="e9b4b-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e9b4b-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e9b4b-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e9b4b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9b4b-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="e9b4b-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9b4b-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="e9b4b-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e9b4b-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="e9b4b-119">Schema name</span></span>  <br/> |<span data-ttu-id="e9b4b-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="e9b4b-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="e9b4b-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="e9b4b-121">Validation file</span></span>  <br/> |<span data-ttu-id="e9b4b-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e9b4b-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e9b4b-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="e9b4b-123">Can be empty</span></span>  <br/> |<span data-ttu-id="e9b4b-124">false</span><span class="sxs-lookup"><span data-stu-id="e9b4b-124">false</span></span>  <br/> |
   

