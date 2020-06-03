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
description: SubmittedTime 元素表示邮件进入服务器的时间。
ms.openlocfilehash: bf9495aa700d2887d199eccb38289e0ebd2e8636
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465406"
---
# <a name="submittedtime"></a><span data-ttu-id="f912e-103">SubmittedTime</span><span class="sxs-lookup"><span data-stu-id="f912e-103">SubmittedTime</span></span>

<span data-ttu-id="f912e-104">**SubmittedTime**元素表示邮件进入服务器的时间。</span><span class="sxs-lookup"><span data-stu-id="f912e-104">The **SubmittedTime** element represents the time that the message entered the server.</span></span> 
  
```XML
<SubmittedTime/>
```

 <span data-ttu-id="f912e-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="f912e-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f912e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f912e-106">Attributes and elements</span></span>

<span data-ttu-id="f912e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f912e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f912e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f912e-108">Attributes</span></span>

<span data-ttu-id="f912e-109">无。</span><span class="sxs-lookup"><span data-stu-id="f912e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f912e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f912e-110">Child elements</span></span>

<span data-ttu-id="f912e-111">无。</span><span class="sxs-lookup"><span data-stu-id="f912e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f912e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f912e-112">Parent elements</span></span>

|<span data-ttu-id="f912e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f912e-113">**Element**</span></span>|<span data-ttu-id="f912e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f912e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f912e-115">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="f912e-115">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="f912e-116">包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="f912e-116">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f912e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f912e-117">Text value</span></span>

 <span data-ttu-id="f912e-118">如果使用此元素，则表示日期/时间的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="f912e-118">A text value that represents a date/time is required if this element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f912e-119">说明</span><span class="sxs-lookup"><span data-stu-id="f912e-119">Remarks</span></span>

<span data-ttu-id="f912e-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f912e-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f912e-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="f912e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f912e-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="f912e-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f912e-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="f912e-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f912e-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="f912e-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="f912e-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="f912e-125">Validation File</span></span>  <br/> |<span data-ttu-id="f912e-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f912e-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f912e-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="f912e-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f912e-128">False</span><span class="sxs-lookup"><span data-stu-id="f912e-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f912e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f912e-129">See also</span></span>



- [<span data-ttu-id="f912e-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f912e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

