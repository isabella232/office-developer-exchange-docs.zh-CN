---
title: ReturnQueueEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReturnQueueEvents
api_type:
- schema
ms.assetid: 69d22417-320c-4c6f-9fb4-2020f2480bb2
description: ReturnQueueEvents 元素表示运行任务的人员特权角色中。
ms.openlocfilehash: 02f4ca86ffa14117105ec186ae039065cb626670
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827233"
---
# <a name="returnqueueevents"></a><span data-ttu-id="e937d-103">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="e937d-103">ReturnQueueEvents</span></span>

<span data-ttu-id="e937d-104">**ReturnQueueEvents**元素表示运行任务的人员特权角色中。</span><span class="sxs-lookup"><span data-stu-id="e937d-104">The **ReturnQueueEvents** element indicates that the person who is running the task is in a privileged role.</span></span> 
  
```XML
<ReturnQueueEvents>true | false</ReturnQueueEvents>
```

 <span data-ttu-id="e937d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e937d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e937d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e937d-106">Attributes and elements</span></span>

<span data-ttu-id="e937d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e937d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e937d-108">属性</span><span class="sxs-lookup"><span data-stu-id="e937d-108">Attributes</span></span>

<span data-ttu-id="e937d-109">无。</span><span class="sxs-lookup"><span data-stu-id="e937d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e937d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e937d-110">Child elements</span></span>

<span data-ttu-id="e937d-111">无。</span><span class="sxs-lookup"><span data-stu-id="e937d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e937d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e937d-112">Parent elements</span></span>

|<span data-ttu-id="e937d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e937d-113">**Element**</span></span>|<span data-ttu-id="e937d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e937d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e937d-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="e937d-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="e937d-116">包含要检索完整的邮件跟踪报告的指定 ID 的[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求</span><span class="sxs-lookup"><span data-stu-id="e937d-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e937d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e937d-117">Text value</span></span>

<span data-ttu-id="e937d-118">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="e937d-118">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="e937d-119">值为**true**指示正在运行的任务的人员处于特权角色;如果值为**false**指示正在运行的任务的人员不在特权角色。</span><span class="sxs-lookup"><span data-stu-id="e937d-119">A value of **true** indicates that the person who is running the task is in a privileged role; a value of **false** indicates that the person who is running the task is not in a privileged role.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e937d-120">备注</span><span class="sxs-lookup"><span data-stu-id="e937d-120">Remarks</span></span>

<span data-ttu-id="e937d-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e937d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e937d-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="e937d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e937d-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="e937d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e937d-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="e937d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e937d-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="e937d-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e937d-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="e937d-126">Validation File</span></span>  <br/> |<span data-ttu-id="e937d-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e937d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e937d-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="e937d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e937d-129">False</span><span class="sxs-lookup"><span data-stu-id="e937d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e937d-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e937d-130">See also</span></span>



[<span data-ttu-id="e937d-131">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="e937d-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="e937d-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e937d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

