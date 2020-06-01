---
title: NonIndexableItemStatistic
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 593e0c79-9ec2-4040-a6a3-3c5c61cbdf7c
description: NonIndexableItemStatistic 元素包含无法编制索引的项目的单个统计信息
ms.openlocfilehash: cc7bee9fd2759a16dd16538d6712e40ceb005fec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462680"
---
# <a name="nonindexableitemstatistic"></a><span data-ttu-id="76bf4-103">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="76bf4-103">NonIndexableItemStatistic</span></span>

<span data-ttu-id="76bf4-104">**NonIndexableItemStatistic**元素包含无法编制索引的项目的单个统计信息</span><span class="sxs-lookup"><span data-stu-id="76bf4-104">The **NonIndexableItemStatistic** element contains a single statistic for an item that could not be indexed</span></span> 
  
```XML
<NonIndexableItemStatistic>
   <Mailbox/>
   <ItemCount/>
   <ErrorMessage/>
</NonIndexableItemStatistic>
```

 <span data-ttu-id="76bf4-105">**NonIndexableItemStatisticType**</span><span class="sxs-lookup"><span data-stu-id="76bf4-105">**NonIndexableItemStatisticType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76bf4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="76bf4-106">Attributes and elements</span></span>

<span data-ttu-id="76bf4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="76bf4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76bf4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="76bf4-108">Attributes</span></span>

<span data-ttu-id="76bf4-109">无。</span><span class="sxs-lookup"><span data-stu-id="76bf4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76bf4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="76bf4-110">Child elements</span></span>

<span data-ttu-id="76bf4-111">[邮箱（字符串）](mailbox-string.md)  | [ItemCount](itemcount.md)  | [ErrorMessage](errormessage.md)</span><span class="sxs-lookup"><span data-stu-id="76bf4-111">[Mailbox (string)](mailbox-string.md) | [ItemCount](itemcount.md) | [ErrorMessage](errormessage.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="76bf4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="76bf4-112">Parent elements</span></span>

[<span data-ttu-id="76bf4-113">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="76bf4-113">NonIndexableItemStatistics</span></span>](nonindexableitemstatistics.md)
  
## <a name="remarks"></a><span data-ttu-id="76bf4-114">备注</span><span class="sxs-lookup"><span data-stu-id="76bf4-114">Remarks</span></span>

<span data-ttu-id="76bf4-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="76bf4-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="76bf4-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="76bf4-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76bf4-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="76bf4-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76bf4-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="76bf4-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="76bf4-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="76bf4-119">Schema name</span></span>  <br/> |<span data-ttu-id="76bf4-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="76bf4-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="76bf4-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="76bf4-121">Validation file</span></span>  <br/> |<span data-ttu-id="76bf4-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="76bf4-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="76bf4-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="76bf4-123">Can be empty</span></span>  <br/> |<span data-ttu-id="76bf4-124">False</span><span class="sxs-lookup"><span data-stu-id="76bf4-124">False</span></span>  <br/> |
   

