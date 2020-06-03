---
title: RootAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootAddress
api_type:
- schema
ms.assetid: 1dbb130a-e4eb-4baf-ae07-2568a8375bff
description: RootAddress 元素表示为 RecipientTrackingEvent 事件启动事件的第一个地址。
ms.openlocfilehash: e020ff07f271bdde6c2a4172141097dcba66f64e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465091"
---
# <a name="rootaddress"></a><span data-ttu-id="bf5f2-103">RootAddress</span><span class="sxs-lookup"><span data-stu-id="bf5f2-103">RootAddress</span></span>

<span data-ttu-id="bf5f2-104">**RootAddress**元素表示为[RecipientTrackingEvent](recipienttrackingevent.md)事件启动事件的第一个地址。</span><span class="sxs-lookup"><span data-stu-id="bf5f2-104">The **RootAddress** element represents the first address that starts the event for a [RecipientTrackingEvent](recipienttrackingevent.md) event.</span></span> 
  
```xml
<RootAddress/>
```

 <span data-ttu-id="bf5f2-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="bf5f2-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bf5f2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bf5f2-106">Attributes and elements</span></span>

<span data-ttu-id="bf5f2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bf5f2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf5f2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bf5f2-108">Attributes</span></span>

<span data-ttu-id="bf5f2-109">无。</span><span class="sxs-lookup"><span data-stu-id="bf5f2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf5f2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bf5f2-110">Child elements</span></span>

<span data-ttu-id="bf5f2-111">无。</span><span class="sxs-lookup"><span data-stu-id="bf5f2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bf5f2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bf5f2-112">Parent elements</span></span>

|<span data-ttu-id="bf5f2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="bf5f2-113">**Element**</span></span>|<span data-ttu-id="bf5f2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="bf5f2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf5f2-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="bf5f2-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="bf5f2-116">包含收件人的单个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="bf5f2-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bf5f2-117">文本值</span><span class="sxs-lookup"><span data-stu-id="bf5f2-117">Text value</span></span>

<span data-ttu-id="bf5f2-118">文本值是启动跟踪事件的地址。</span><span class="sxs-lookup"><span data-stu-id="bf5f2-118">The text value is the address that starts the tracking event.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf5f2-119">备注</span><span class="sxs-lookup"><span data-stu-id="bf5f2-119">Remarks</span></span>

<span data-ttu-id="bf5f2-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bf5f2-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf5f2-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="bf5f2-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf5f2-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="bf5f2-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bf5f2-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="bf5f2-123">Schema Name</span></span>  <br/> |<span data-ttu-id="bf5f2-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="bf5f2-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="bf5f2-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="bf5f2-125">Validation File</span></span>  <br/> |<span data-ttu-id="bf5f2-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bf5f2-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bf5f2-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="bf5f2-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="bf5f2-128">False</span><span class="sxs-lookup"><span data-stu-id="bf5f2-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf5f2-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bf5f2-129">See also</span></span>



[<span data-ttu-id="bf5f2-130">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="bf5f2-130">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="bf5f2-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bf5f2-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

