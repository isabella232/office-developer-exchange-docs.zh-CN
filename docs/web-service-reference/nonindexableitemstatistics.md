---
title: NonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12f2934a-008c-4236-b8b3-7c7b6b5707e2
description: NonIndexableItemStatistics 元素包含数组的无法索引的项目的统计信息。
ms.openlocfilehash: 1414053b6d39f4cd08ccfd1a11faaf1b13c2052b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826544"
---
# <a name="nonindexableitemstatistics"></a><span data-ttu-id="75966-103">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="75966-103">NonIndexableItemStatistics</span></span>

<span data-ttu-id="75966-104">**NonIndexableItemStatistics**元素包含数组的无法索引的项目的统计信息。</span><span class="sxs-lookup"><span data-stu-id="75966-104">The **NonIndexableItemStatistics** element contains an array of statistics for items that could not be indexed.</span></span> 
  
```XML
<NonIndexableItemStatistics>
   <NonIndexableItemStatistic/>
</NonIndexableItemStatistics>
```

 <span data-ttu-id="75966-105">**ArrayOfNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="75966-105">**ArrayOfNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75966-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="75966-106">Attributes and elements</span></span>

<span data-ttu-id="75966-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="75966-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75966-108">属性</span><span class="sxs-lookup"><span data-stu-id="75966-108">Attributes</span></span>

<span data-ttu-id="75966-109">无。</span><span class="sxs-lookup"><span data-stu-id="75966-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75966-110">子元素</span><span class="sxs-lookup"><span data-stu-id="75966-110">Child elements</span></span>

[<span data-ttu-id="75966-111">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="75966-111">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
  
### <a name="parent-elements"></a><span data-ttu-id="75966-112">父元素</span><span class="sxs-lookup"><span data-stu-id="75966-112">Parent elements</span></span>

<span data-ttu-id="75966-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="75966-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) , [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75966-114">备注</span><span class="sxs-lookup"><span data-stu-id="75966-114">Remarks</span></span>

<span data-ttu-id="75966-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="75966-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="75966-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="75966-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75966-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="75966-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75966-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="75966-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="75966-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="75966-119">Schema name</span></span>  <br/> |<span data-ttu-id="75966-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="75966-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="75966-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="75966-121">Validation file</span></span>  <br/> |<span data-ttu-id="75966-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="75966-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="75966-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="75966-123">Can be empty</span></span>  <br/> |<span data-ttu-id="75966-124">False</span><span class="sxs-lookup"><span data-stu-id="75966-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75966-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="75966-125">See also</span></span>



[<span data-ttu-id="75966-126">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="75966-126">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)


- [<span data-ttu-id="75966-127">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="75966-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

