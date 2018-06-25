---
title: Diagnostics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Diagnostics
api_type:
- schema
ms.assetid: fecea440-970a-49da-9796-534ca470cbd6
description: 诊断元素提供用于报告数据中心中的计时和性能信息。
ms.openlocfilehash: 2b9cac54a683967ec274b8681fb9a0c8a844205e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753854"
---
# <a name="diagnostics"></a><span data-ttu-id="69873-103">Diagnostics</span><span class="sxs-lookup"><span data-stu-id="69873-103">Diagnostics</span></span>

<span data-ttu-id="69873-104">**诊断**元素提供用于报告数据中心中的计时和性能信息。</span><span class="sxs-lookup"><span data-stu-id="69873-104">The **Diagnostics** element provides timing and performance information that is used for reporting in a DataCenter.</span></span> 
  
```XML
<Diagnostics>
   <String/>
</Diagnostics>

```

 <span data-ttu-id="69873-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="69873-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69873-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="69873-106">Attributes and elements</span></span>

<span data-ttu-id="69873-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="69873-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69873-108">属性</span><span class="sxs-lookup"><span data-stu-id="69873-108">Attributes</span></span>

<span data-ttu-id="69873-109">无。</span><span class="sxs-lookup"><span data-stu-id="69873-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69873-110">子元素</span><span class="sxs-lookup"><span data-stu-id="69873-110">Child elements</span></span>

|<span data-ttu-id="69873-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="69873-111">**Element**</span></span>|<span data-ttu-id="69873-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="69873-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69873-113">字符串</span><span class="sxs-lookup"><span data-stu-id="69873-113">String</span></span>](string.md) <br/> |<span data-ttu-id="69873-114">包含一个字符串，由项目、 联系人、 任务和对话。</span><span class="sxs-lookup"><span data-stu-id="69873-114">Contains a string that is used by items, contacts, tasks, and conversations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69873-115">父元素</span><span class="sxs-lookup"><span data-stu-id="69873-115">Parent elements</span></span>

|<span data-ttu-id="69873-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="69873-116">**Element**</span></span>|<span data-ttu-id="69873-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="69873-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69873-118">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="69873-118">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="69873-119">包含状态和的单个结果[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="69873-119">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="69873-120">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="69873-120">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="69873-121">包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="69873-121">Contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="69873-122">文本值</span><span class="sxs-lookup"><span data-stu-id="69873-122">Text value</span></span>

<span data-ttu-id="69873-123">无。</span><span class="sxs-lookup"><span data-stu-id="69873-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69873-124">备注</span><span class="sxs-lookup"><span data-stu-id="69873-124">Remarks</span></span>

<span data-ttu-id="69873-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="69873-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69873-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="69873-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69873-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="69873-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="69873-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="69873-128">Schema Name</span></span>  <br/> |<span data-ttu-id="69873-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="69873-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="69873-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="69873-130">Validation File</span></span>  <br/> |<span data-ttu-id="69873-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="69873-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="69873-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="69873-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="69873-133">False</span><span class="sxs-lookup"><span data-stu-id="69873-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69873-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69873-134">See also</span></span>

- [<span data-ttu-id="69873-135">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="69873-135">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="69873-136">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="69873-136">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="69873-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="69873-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

