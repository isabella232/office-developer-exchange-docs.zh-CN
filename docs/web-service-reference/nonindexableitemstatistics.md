---
title: NonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12f2934a-008c-4236-b8b3-7c7b6b5707e2
description: NonIndexableItemStatistics 元素包含无法编制索引的项的一系列统计信息。
ms.openlocfilehash: 5a11bd4d7ef0c574f26580613063a885530176f9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466729"
---
# <a name="nonindexableitemstatistics"></a><span data-ttu-id="08d0a-103">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="08d0a-103">NonIndexableItemStatistics</span></span>

<span data-ttu-id="08d0a-104">**NonIndexableItemStatistics**元素包含无法编制索引的项的一系列统计信息。</span><span class="sxs-lookup"><span data-stu-id="08d0a-104">The **NonIndexableItemStatistics** element contains an array of statistics for items that could not be indexed.</span></span> 
  
```XML
<NonIndexableItemStatistics>
   <NonIndexableItemStatistic/>
</NonIndexableItemStatistics>
```

 <span data-ttu-id="08d0a-105">**ArrayOfNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="08d0a-105">**ArrayOfNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="08d0a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="08d0a-106">Attributes and elements</span></span>

<span data-ttu-id="08d0a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="08d0a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08d0a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="08d0a-108">Attributes</span></span>

<span data-ttu-id="08d0a-109">无。</span><span class="sxs-lookup"><span data-stu-id="08d0a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="08d0a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="08d0a-110">Child elements</span></span>

[<span data-ttu-id="08d0a-111">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="08d0a-111">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
  
### <a name="parent-elements"></a><span data-ttu-id="08d0a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="08d0a-112">Parent elements</span></span>

<span data-ttu-id="08d0a-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) 、 [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="08d0a-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) , [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08d0a-114">备注</span><span class="sxs-lookup"><span data-stu-id="08d0a-114">Remarks</span></span>

<span data-ttu-id="08d0a-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="08d0a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="08d0a-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="08d0a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08d0a-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="08d0a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08d0a-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="08d0a-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="08d0a-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="08d0a-119">Schema name</span></span>  <br/> |<span data-ttu-id="08d0a-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="08d0a-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="08d0a-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="08d0a-121">Validation file</span></span>  <br/> |<span data-ttu-id="08d0a-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="08d0a-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="08d0a-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="08d0a-123">Can be empty</span></span>  <br/> |<span data-ttu-id="08d0a-124">False</span><span class="sxs-lookup"><span data-stu-id="08d0a-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08d0a-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="08d0a-125">See also</span></span>



[<span data-ttu-id="08d0a-126">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="08d0a-126">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)


- [<span data-ttu-id="08d0a-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="08d0a-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

