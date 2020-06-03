---
title: ConnectionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionStatus
api_type:
- schema
ms.assetid: 4300f9d6-8bf9-48c2-9f07-d80197864e17
description: ConnectionStatus 元素提供流式订阅的状态的文本说明。
ms.openlocfilehash: 928537201041950011ae06444e3c412228d252ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462715"
---
# <a name="connectionstatus"></a><span data-ttu-id="6f59d-103">ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="6f59d-103">ConnectionStatus</span></span>

<span data-ttu-id="6f59d-104">**ConnectionStatus**元素提供流式订阅的状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="6f59d-104">The **ConnectionStatus** element provides a text description of the status of a streaming subscription.</span></span> 
  
```xml
<ConnectionStatus>OK or Closed</ConnectionStatus>
```

 <span data-ttu-id="6f59d-105">**ConnectionStatusType**</span><span class="sxs-lookup"><span data-stu-id="6f59d-105">**ConnectionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f59d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f59d-106">Attributes and elements</span></span>

<span data-ttu-id="6f59d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f59d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f59d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6f59d-108">Attributes</span></span>

<span data-ttu-id="6f59d-109">无。</span><span class="sxs-lookup"><span data-stu-id="6f59d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f59d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6f59d-110">Child elements</span></span>

<span data-ttu-id="6f59d-111">无。</span><span class="sxs-lookup"><span data-stu-id="6f59d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f59d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6f59d-112">Parent elements</span></span>

|<span data-ttu-id="6f59d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f59d-113">**Element**</span></span>|<span data-ttu-id="6f59d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f59d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f59d-115">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6f59d-115">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="6f59d-116">包含单个[GetStreamingEvents 操作](getstreamingevents-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="6f59d-116">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6f59d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="6f59d-117">Text value</span></span>

<span data-ttu-id="6f59d-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="6f59d-118">A text value is required.</span></span> <span data-ttu-id="6f59d-119">以下是此元素的可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="6f59d-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="6f59d-120">确定</span><span class="sxs-lookup"><span data-stu-id="6f59d-120">OK</span></span>
    
- <span data-ttu-id="6f59d-121">Closed</span><span class="sxs-lookup"><span data-stu-id="6f59d-121">Closed</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f59d-122">备注</span><span class="sxs-lookup"><span data-stu-id="6f59d-122">Remarks</span></span>

<span data-ttu-id="6f59d-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6f59d-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f59d-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f59d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f59d-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f59d-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6f59d-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f59d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6f59d-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="6f59d-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6f59d-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f59d-128">Validation File</span></span>  <br/> |<span data-ttu-id="6f59d-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6f59d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6f59d-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f59d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f59d-131">False</span><span class="sxs-lookup"><span data-stu-id="6f59d-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f59d-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f59d-132">See also</span></span>



[<span data-ttu-id="6f59d-133">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="6f59d-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="6f59d-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6f59d-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

