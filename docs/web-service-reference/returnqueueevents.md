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
description: ReturnQueueEvents 元素指示正在运行该任务的人员处于特权角色中。
ms.openlocfilehash: 9d07bc8c3d32f1cd532febaf4ae04e4a2d31d243
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466589"
---
# <a name="returnqueueevents"></a><span data-ttu-id="dab2f-103">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="dab2f-103">ReturnQueueEvents</span></span>

<span data-ttu-id="dab2f-104">**ReturnQueueEvents**元素指示正在运行该任务的人员处于特权角色中。</span><span class="sxs-lookup"><span data-stu-id="dab2f-104">The **ReturnQueueEvents** element indicates that the person who is running the task is in a privileged role.</span></span> 
  
```XML
<ReturnQueueEvents>true | false</ReturnQueueEvents>
```

 <span data-ttu-id="dab2f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="dab2f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dab2f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dab2f-106">Attributes and elements</span></span>

<span data-ttu-id="dab2f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dab2f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dab2f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dab2f-108">Attributes</span></span>

<span data-ttu-id="dab2f-109">无。</span><span class="sxs-lookup"><span data-stu-id="dab2f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dab2f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dab2f-110">Child elements</span></span>

<span data-ttu-id="dab2f-111">无。</span><span class="sxs-lookup"><span data-stu-id="dab2f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dab2f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="dab2f-112">Parent elements</span></span>

|<span data-ttu-id="dab2f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="dab2f-113">**Element**</span></span>|<span data-ttu-id="dab2f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="dab2f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dab2f-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="dab2f-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="dab2f-116">包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求，以检索指定 ID 的完整邮件跟踪报告。</span><span class="sxs-lookup"><span data-stu-id="dab2f-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dab2f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="dab2f-117">Text value</span></span>

<span data-ttu-id="dab2f-118">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="dab2f-118">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="dab2f-119">**如果值为 true** ，则表示运行该任务的人员处于特权角色中;**如果值为 false** ，则表示运行该任务的人员不在特权角色中。</span><span class="sxs-lookup"><span data-stu-id="dab2f-119">A value of **true** indicates that the person who is running the task is in a privileged role; a value of **false** indicates that the person who is running the task is not in a privileged role.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dab2f-120">说明</span><span class="sxs-lookup"><span data-stu-id="dab2f-120">Remarks</span></span>

<span data-ttu-id="dab2f-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dab2f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dab2f-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="dab2f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dab2f-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="dab2f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dab2f-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="dab2f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="dab2f-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="dab2f-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dab2f-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="dab2f-126">Validation File</span></span>  <br/> |<span data-ttu-id="dab2f-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dab2f-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dab2f-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="dab2f-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="dab2f-129">False</span><span class="sxs-lookup"><span data-stu-id="dab2f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dab2f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dab2f-130">See also</span></span>



[<span data-ttu-id="dab2f-131">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="dab2f-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="dab2f-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dab2f-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

