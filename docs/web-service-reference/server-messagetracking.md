---
title: 服务器（MessageTracking）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Server
api_type:
- schema
ms.assetid: eb5408bd-6fa5-4415-9224-24d5e07ec5b3
description: Server 元素表示发生事件的物理服务器。
ms.openlocfilehash: 1a5d2e223acfc402ae964c619598845e4212b639
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462043"
---
# <a name="server-messagetracking"></a><span data-ttu-id="bfe6e-103">服务器（MessageTracking）</span><span class="sxs-lookup"><span data-stu-id="bfe6e-103">Server (MessageTracking)</span></span>

<span data-ttu-id="bfe6e-104">**Server**元素表示发生事件的物理服务器。</span><span class="sxs-lookup"><span data-stu-id="bfe6e-104">The **Server** element represents the physical server where the event occurred.</span></span> 
  
```XML
<Server/>
```

 <span data-ttu-id="bfe6e-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="bfe6e-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bfe6e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bfe6e-106">Attributes and elements</span></span>

<span data-ttu-id="bfe6e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bfe6e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bfe6e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bfe6e-108">Attributes</span></span>

<span data-ttu-id="bfe6e-109">无。</span><span class="sxs-lookup"><span data-stu-id="bfe6e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bfe6e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bfe6e-110">Child elements</span></span>

<span data-ttu-id="bfe6e-111">无。</span><span class="sxs-lookup"><span data-stu-id="bfe6e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bfe6e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bfe6e-112">Parent elements</span></span>

|<span data-ttu-id="bfe6e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="bfe6e-113">**Element**</span></span>|<span data-ttu-id="bfe6e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="bfe6e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfe6e-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="bfe6e-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="bfe6e-116">包含收件人的单个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="bfe6e-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bfe6e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="bfe6e-117">Text value</span></span>

<span data-ttu-id="bfe6e-118">如果使用此元素，则需要一个表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="bfe6e-118">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bfe6e-119">说明</span><span class="sxs-lookup"><span data-stu-id="bfe6e-119">Remarks</span></span>

<span data-ttu-id="bfe6e-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bfe6e-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bfe6e-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="bfe6e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfe6e-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="bfe6e-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bfe6e-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="bfe6e-123">Schema Name</span></span>  <br/> |<span data-ttu-id="bfe6e-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="bfe6e-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="bfe6e-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="bfe6e-125">Validation File</span></span>  <br/> |<span data-ttu-id="bfe6e-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bfe6e-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bfe6e-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="bfe6e-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="bfe6e-128">False</span><span class="sxs-lookup"><span data-stu-id="bfe6e-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfe6e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bfe6e-129">See also</span></span>



- [<span data-ttu-id="bfe6e-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bfe6e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

