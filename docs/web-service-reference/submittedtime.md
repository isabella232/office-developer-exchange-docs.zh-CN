---
title: SubmittedTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubmittedTime
api_type:
- schema
ms.assetid: 45c8fa36-c539-42ca-99dc-1ac33cc54afc
description: SubmittedTime 元素均表示邮件输入服务器的时间。
ms.openlocfilehash: 89fc6400914495b8f1bd3994f17421d0ab079460
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827613"
---
# <a name="submittedtime"></a><span data-ttu-id="fe778-103">SubmittedTime</span><span class="sxs-lookup"><span data-stu-id="fe778-103">SubmittedTime</span></span>

<span data-ttu-id="fe778-104">**SubmittedTime**元素均表示邮件输入服务器的时间。</span><span class="sxs-lookup"><span data-stu-id="fe778-104">The **SubmittedTime** element represents the time that the message entered the server.</span></span> 
  
```XML
<SubmittedTime/>
```

 <span data-ttu-id="fe778-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="fe778-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe778-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fe778-106">Attributes and elements</span></span>

<span data-ttu-id="fe778-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fe778-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe778-108">属性</span><span class="sxs-lookup"><span data-stu-id="fe778-108">Attributes</span></span>

<span data-ttu-id="fe778-109">无。</span><span class="sxs-lookup"><span data-stu-id="fe778-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe778-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fe778-110">Child elements</span></span>

<span data-ttu-id="fe778-111">无。</span><span class="sxs-lookup"><span data-stu-id="fe778-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe778-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fe778-112">Parent elements</span></span>

|<span data-ttu-id="fe778-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fe778-113">**Element**</span></span>|<span data-ttu-id="fe778-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe778-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe778-115">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="fe778-115">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="fe778-116">包含单个邮件结果[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="fe778-116">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fe778-117">文本值</span><span class="sxs-lookup"><span data-stu-id="fe778-117">Text value</span></span>

 <span data-ttu-id="fe778-118">如果使用此元素，则需要一个表示日期/时间的文本值。</span><span class="sxs-lookup"><span data-stu-id="fe778-118">A text value that represents a date/time is required if this element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe778-119">备注</span><span class="sxs-lookup"><span data-stu-id="fe778-119">Remarks</span></span>

<span data-ttu-id="fe778-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fe778-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe778-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="fe778-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe778-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="fe778-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fe778-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="fe778-123">Schema Name</span></span>  <br/> |<span data-ttu-id="fe778-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="fe778-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="fe778-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="fe778-125">Validation File</span></span>  <br/> |<span data-ttu-id="fe778-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fe778-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fe778-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="fe778-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="fe778-128">False</span><span class="sxs-lookup"><span data-stu-id="fe778-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe778-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe778-129">See also</span></span>



- [<span data-ttu-id="fe778-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fe778-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

