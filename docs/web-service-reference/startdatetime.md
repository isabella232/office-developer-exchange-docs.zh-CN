---
title: 开始日期时间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartDateTime
api_type:
- schema
ms.assetid: 6fd41b7b-6c83-43b6-8b16-0bdb3d173d73
description: 开始日期时间元素指定的开始日期和时间规则或搜索。
ms.openlocfilehash: 4bc32ed5626d692fc73dfa8bd7c46923aba72f9e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827552"
---
# <a name="startdatetime"></a><span data-ttu-id="dd2ac-103">开始日期时间</span><span class="sxs-lookup"><span data-stu-id="dd2ac-103">StartDateTime</span></span>

<span data-ttu-id="dd2ac-104">**开始日期时间**元素指定的开始日期和时间规则或搜索。</span><span class="sxs-lookup"><span data-stu-id="dd2ac-104">The **StartDateTime** element specifies the start date and time for a rule or a search.</span></span> 
  
```XML
<StartDate/>
```

<span data-ttu-id="dd2ac-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="dd2ac-105">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dd2ac-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dd2ac-106">Attributes and elements</span></span>

<span data-ttu-id="dd2ac-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dd2ac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd2ac-108">属性</span><span class="sxs-lookup"><span data-stu-id="dd2ac-108">Attributes</span></span>

<span data-ttu-id="dd2ac-109">无。</span><span class="sxs-lookup"><span data-stu-id="dd2ac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd2ac-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dd2ac-110">Child elements</span></span>

<span data-ttu-id="dd2ac-111">无。</span><span class="sxs-lookup"><span data-stu-id="dd2ac-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dd2ac-112">父元素</span><span class="sxs-lookup"><span data-stu-id="dd2ac-112">Parent elements</span></span>

|<span data-ttu-id="dd2ac-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="dd2ac-113">**Element**</span></span>|<span data-ttu-id="dd2ac-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="dd2ac-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd2ac-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="dd2ac-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="dd2ac-116">指定条件的邮件，以查找的类型。</span><span class="sxs-lookup"><span data-stu-id="dd2ac-116">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="dd2ac-117">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="dd2ac-117">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="dd2ac-118">指定在其中传入消息必须已收到的条件或例外的顺序应用中的日期范围。</span><span class="sxs-lookup"><span data-stu-id="dd2ac-118">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dd2ac-119">文本值</span><span class="sxs-lookup"><span data-stu-id="dd2ac-119">Text value</span></span>

 <span data-ttu-id="dd2ac-120">如果使用此元素，则需要一个表示日期/时间的文本值。</span><span class="sxs-lookup"><span data-stu-id="dd2ac-120">A text value that represents a date/time is required if this element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dd2ac-121">备注</span><span class="sxs-lookup"><span data-stu-id="dd2ac-121">Remarks</span></span>

<span data-ttu-id="dd2ac-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dd2ac-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd2ac-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="dd2ac-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd2ac-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="dd2ac-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd2ac-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="dd2ac-125">Schema Name</span></span>  <br/> |<span data-ttu-id="dd2ac-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="dd2ac-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dd2ac-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="dd2ac-127">Validation File</span></span>  <br/> |<span data-ttu-id="dd2ac-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dd2ac-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd2ac-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="dd2ac-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd2ac-130">False</span><span class="sxs-lookup"><span data-stu-id="dd2ac-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd2ac-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dd2ac-131">See also</span></span>

- [<span data-ttu-id="dd2ac-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dd2ac-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

