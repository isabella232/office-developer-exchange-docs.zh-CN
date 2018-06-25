---
title: NonIndexableItemStatistic
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 593e0c79-9ec2-4040-a6a3-3c5c61cbdf7c
description: NonIndexableItemStatistic 元素包含无法索引项的单个统计信息
ms.openlocfilehash: e604f73216aab4cca259bc6cb7eb80a2fd36cd23
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826540"
---
# <a name="nonindexableitemstatistic"></a><span data-ttu-id="2f7ce-103">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="2f7ce-103">NonIndexableItemStatistic</span></span>

<span data-ttu-id="2f7ce-104">**NonIndexableItemStatistic**元素包含无法索引项的单个统计信息</span><span class="sxs-lookup"><span data-stu-id="2f7ce-104">The **NonIndexableItemStatistic** element contains a single statistic for an item that could not be indexed</span></span> 
  
```XML
<NonIndexableItemStatistic>
   <Mailbox/>
   <ItemCount/>
   <ErrorMessage/>
</NonIndexableItemStatistic>
```

 <span data-ttu-id="2f7ce-105">**NonIndexableItemStatisticType**</span><span class="sxs-lookup"><span data-stu-id="2f7ce-105">**NonIndexableItemStatisticType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f7ce-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2f7ce-106">Attributes and elements</span></span>

<span data-ttu-id="2f7ce-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f7ce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f7ce-108">属性</span><span class="sxs-lookup"><span data-stu-id="2f7ce-108">Attributes</span></span>

<span data-ttu-id="2f7ce-109">无。</span><span class="sxs-lookup"><span data-stu-id="2f7ce-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f7ce-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2f7ce-110">Child elements</span></span>

<span data-ttu-id="2f7ce-111">[邮箱 （字符串）](mailbox-string.md) | [ItemCount](itemcount.md) | [ErrorMessage](errormessage.md)</span><span class="sxs-lookup"><span data-stu-id="2f7ce-111">[Mailbox (string)](mailbox-string.md) | [ItemCount](itemcount.md) | [ErrorMessage](errormessage.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f7ce-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2f7ce-112">Parent elements</span></span>

[<span data-ttu-id="2f7ce-113">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="2f7ce-113">NonIndexableItemStatistics</span></span>](nonindexableitemstatistics.md)
  
## <a name="remarks"></a><span data-ttu-id="2f7ce-114">备注</span><span class="sxs-lookup"><span data-stu-id="2f7ce-114">Remarks</span></span>

<span data-ttu-id="2f7ce-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2f7ce-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2f7ce-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2f7ce-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f7ce-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="2f7ce-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f7ce-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="2f7ce-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2f7ce-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="2f7ce-119">Schema name</span></span>  <br/> |<span data-ttu-id="2f7ce-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="2f7ce-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2f7ce-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="2f7ce-121">Validation file</span></span>  <br/> |<span data-ttu-id="2f7ce-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2f7ce-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f7ce-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="2f7ce-123">Can be empty</span></span>  <br/> |<span data-ttu-id="2f7ce-124">False</span><span class="sxs-lookup"><span data-stu-id="2f7ce-124">False</span></span>  <br/> |
   

