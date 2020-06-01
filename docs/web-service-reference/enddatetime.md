---
title: EndDateTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDateTime
api_type:
- schema
ms.assetid: 54d14e47-a8f7-400b-a859-c7ea7ce4c6a4
description: EndDateTime 元素指定规则或搜索的结束日期和时间。
ms.openlocfilehash: 9556e4c1ef405ae66a71d19d99d9a71a61f54efc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460132"
---
# <a name="enddatetime"></a><span data-ttu-id="b8e2d-103">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="b8e2d-103">EndDateTime</span></span>

<span data-ttu-id="b8e2d-104">**EndDateTime**元素指定规则或搜索的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-104">The **EndDateTime** element specifies the end date and time for a rule or a search.</span></span> 
  
```XML
<EndDateTime/>
```

 <span data-ttu-id="b8e2d-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="b8e2d-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8e2d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b8e2d-106">Attributes and elements</span></span>

<span data-ttu-id="b8e2d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8e2d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b8e2d-108">Attributes</span></span>

<span data-ttu-id="b8e2d-109">无。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8e2d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b8e2d-110">Child elements</span></span>

<span data-ttu-id="b8e2d-111">无。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b8e2d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b8e2d-112">Parent elements</span></span>

|<span data-ttu-id="b8e2d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b8e2d-113">**Element**</span></span>|<span data-ttu-id="b8e2d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b8e2d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8e2d-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="b8e2d-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="b8e2d-116">包含要查找的邮件的类型的条件。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="b8e2d-117">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="b8e2d-117">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="b8e2d-118">指定要在其中接收传入邮件的日期范围，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-118">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8e2d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="b8e2d-119">Text value</span></span>

<span data-ttu-id="b8e2d-120">如果使用此元素，则表示日期/时间的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-120">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8e2d-121">说明</span><span class="sxs-lookup"><span data-stu-id="b8e2d-121">Remarks</span></span>

<span data-ttu-id="b8e2d-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8e2d-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="b8e2d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8e2d-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="b8e2d-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b8e2d-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="b8e2d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b8e2d-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="b8e2d-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b8e2d-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="b8e2d-127">Validation File</span></span>  <br/> |<span data-ttu-id="b8e2d-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b8e2d-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b8e2d-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="b8e2d-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="b8e2d-130">False</span><span class="sxs-lookup"><span data-stu-id="b8e2d-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8e2d-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b8e2d-131">See also</span></span>



- [<span data-ttu-id="b8e2d-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b8e2d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

