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
ms.openlocfilehash: 567308d79eaccba24230deddf5d78a724b8746af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753486"
---
# <a name="connectionstatus"></a><span data-ttu-id="c952f-103">ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="c952f-103">ConnectionStatus</span></span>

<span data-ttu-id="c952f-104">**ConnectionStatus**元素提供流式订阅的状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c952f-104">The **ConnectionStatus** element provides a text description of the status of a streaming subscription.</span></span> 
  
```xml
<ConnectionStatus>OK or Closed</ConnectionStatus>
```

 <span data-ttu-id="c952f-105">**ConnectionStatusType**</span><span class="sxs-lookup"><span data-stu-id="c952f-105">**ConnectionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c952f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c952f-106">Attributes and elements</span></span>

<span data-ttu-id="c952f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c952f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c952f-108">属性</span><span class="sxs-lookup"><span data-stu-id="c952f-108">Attributes</span></span>

<span data-ttu-id="c952f-109">无。</span><span class="sxs-lookup"><span data-stu-id="c952f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c952f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c952f-110">Child elements</span></span>

<span data-ttu-id="c952f-111">无。</span><span class="sxs-lookup"><span data-stu-id="c952f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c952f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c952f-112">Parent elements</span></span>

|<span data-ttu-id="c952f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c952f-113">**Element**</span></span>|<span data-ttu-id="c952f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c952f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c952f-115">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c952f-115">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="c952f-116">包含状态和的单个结果[GetStreamingEvents 操作](getstreamingevents-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="c952f-116">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c952f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c952f-117">Text value</span></span>

<span data-ttu-id="c952f-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="c952f-118">A text value is required.</span></span> <span data-ttu-id="c952f-119">此元素的可能的文本值如下：</span><span class="sxs-lookup"><span data-stu-id="c952f-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="c952f-120">确定</span><span class="sxs-lookup"><span data-stu-id="c952f-120">OK</span></span>
    
- <span data-ttu-id="c952f-121">关闭</span><span class="sxs-lookup"><span data-stu-id="c952f-121">Closed</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c952f-122">备注</span><span class="sxs-lookup"><span data-stu-id="c952f-122">Remarks</span></span>

<span data-ttu-id="c952f-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c952f-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c952f-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c952f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c952f-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c952f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c952f-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c952f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c952f-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="c952f-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c952f-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c952f-128">Validation File</span></span>  <br/> |<span data-ttu-id="c952f-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c952f-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c952f-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c952f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="c952f-131">False</span><span class="sxs-lookup"><span data-stu-id="c952f-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c952f-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c952f-132">See also</span></span>



[<span data-ttu-id="c952f-133">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="c952f-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="c952f-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c952f-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

