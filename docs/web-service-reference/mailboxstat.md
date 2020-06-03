---
title: MailboxStat
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5f24dc30-3ac2-4c82-9dfc-be9dbdb585be
description: MailboxStat 元素指定通过发现搜索搜索的邮箱的统计信息。
ms.openlocfilehash: 417f63f5e1aa34c2157b1d5ad868461113afec7b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44451430"
---
# <a name="mailboxstat"></a><span data-ttu-id="6e54c-103">MailboxStat</span><span class="sxs-lookup"><span data-stu-id="6e54c-103">MailboxStat</span></span>

<span data-ttu-id="6e54c-104">**MailboxStat**元素指定通过发现搜索搜索的邮箱的统计信息。</span><span class="sxs-lookup"><span data-stu-id="6e54c-104">The **MailboxStat** element specifies statistics for a mailbox searched by discovery search.</span></span> 
  
```XML
<MailboxStat>
   <MailboxId/>
   <DisplayName/>
   <ItemCount/>
   <Size/>
</MailboxStat>
```

<span data-ttu-id="6e54c-105">**MailboxStatisticsItemType**</span><span class="sxs-lookup"><span data-stu-id="6e54c-105">**MailboxStatisticsItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6e54c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6e54c-106">Attributes and elements</span></span>

<span data-ttu-id="6e54c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6e54c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e54c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6e54c-108">Attributes</span></span>

<span data-ttu-id="6e54c-109">无。</span><span class="sxs-lookup"><span data-stu-id="6e54c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e54c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6e54c-110">Child elements</span></span>

<span data-ttu-id="6e54c-111">[MailboxId](mailboxid.md)  | [DisplayName （string）](displayname-string.md)  | [ItemCount](itemcount.md)  | [大小（long）](size-long.md)</span><span class="sxs-lookup"><span data-stu-id="6e54c-111">[MailboxId](mailboxid.md) | [DisplayName (string)](displayname-string.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6e54c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6e54c-112">Parent elements</span></span>

[<span data-ttu-id="6e54c-113">MailboxStats</span><span class="sxs-lookup"><span data-stu-id="6e54c-113">MailboxStats</span></span>](mailboxstats.md)
  
## <a name="remarks"></a><span data-ttu-id="6e54c-114">备注</span><span class="sxs-lookup"><span data-stu-id="6e54c-114">Remarks</span></span>

<span data-ttu-id="6e54c-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6e54c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6e54c-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6e54c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e54c-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="6e54c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e54c-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="6e54c-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6e54c-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="6e54c-119">Schema name</span></span>  <br/> |<span data-ttu-id="6e54c-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="6e54c-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="6e54c-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="6e54c-121">Validation file</span></span>  <br/> |<span data-ttu-id="6e54c-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6e54c-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6e54c-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="6e54c-123">Can be empty</span></span>  <br/> |<span data-ttu-id="6e54c-124">false</span><span class="sxs-lookup"><span data-stu-id="6e54c-124">false</span></span>  <br/> |
   

