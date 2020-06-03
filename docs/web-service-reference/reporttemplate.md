---
title: ReportTemplate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReportTemplate
api_type:
- schema
ms.assetid: f528eee6-d5af-4745-8b00-a9834bf34be6
description: ReportTemplate 元素表示要获取的报告类型。
ms.openlocfilehash: 22f14d326032a30e5cb4c2c9e1aff390d98e95e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528697"
---
# <a name="reporttemplate"></a><span data-ttu-id="7dd8d-103">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="7dd8d-103">ReportTemplate</span></span>

<span data-ttu-id="7dd8d-104">**ReportTemplate**元素表示要获取的报告类型。</span><span class="sxs-lookup"><span data-stu-id="7dd8d-104">The **ReportTemplate** element represents the type of report to get.</span></span> 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 <span data-ttu-id="7dd8d-105">**MessageTrackingReportTemplateType**</span><span class="sxs-lookup"><span data-stu-id="7dd8d-105">**MessageTrackingReportTemplateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7dd8d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7dd8d-106">Attributes and elements</span></span>

<span data-ttu-id="7dd8d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7dd8d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7dd8d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7dd8d-108">Attributes</span></span>

<span data-ttu-id="7dd8d-109">无。</span><span class="sxs-lookup"><span data-stu-id="7dd8d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7dd8d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7dd8d-110">Child elements</span></span>

<span data-ttu-id="7dd8d-111">无。</span><span class="sxs-lookup"><span data-stu-id="7dd8d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7dd8d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7dd8d-112">Parent elements</span></span>

|<span data-ttu-id="7dd8d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7dd8d-113">**Element**</span></span>|<span data-ttu-id="7dd8d-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="7dd8d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7dd8d-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="7dd8d-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="7dd8d-116">包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求，以检索指定 ID 的完整邮件跟踪报告。</span><span class="sxs-lookup"><span data-stu-id="7dd8d-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7dd8d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="7dd8d-117">Text value</span></span>

<span data-ttu-id="7dd8d-118">下表列出了**ReportTemplate**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="7dd8d-118">The following table lists the possible values for the **ReportTemplate** element.</span></span> 
  
<span data-ttu-id="7dd8d-119">**ReportTemplate 元素值**</span><span class="sxs-lookup"><span data-stu-id="7dd8d-119">**ReportTemplate element values**</span></span>

|<span data-ttu-id="7dd8d-120">**值**</span><span class="sxs-lookup"><span data-stu-id="7dd8d-120">**Value**</span></span>|<span data-ttu-id="7dd8d-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="7dd8d-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7dd8d-122">总结</span><span class="sxs-lookup"><span data-stu-id="7dd8d-122">Summary</span></span>  <br/> |<span data-ttu-id="7dd8d-123">指定报告将显示邮件的所有收件人以及邮件到每个收件人的传递状态。</span><span class="sxs-lookup"><span data-stu-id="7dd8d-123">Specifies that the report will display all the recipients of the message and the delivery status of the message to each recipient.</span></span>  <br/> |
|<span data-ttu-id="7dd8d-124">RecipientPath</span><span class="sxs-lookup"><span data-stu-id="7dd8d-124">RecipientPath</span></span>  <br/> |<span data-ttu-id="7dd8d-125">指定对于单个收件人，报告将显示所发生事件的完整历史记录。</span><span class="sxs-lookup"><span data-stu-id="7dd8d-125">Specifies that for a single recipient, the report will display a full history of the events that occurred.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7dd8d-126">备注</span><span class="sxs-lookup"><span data-stu-id="7dd8d-126">Remarks</span></span>

<span data-ttu-id="7dd8d-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7dd8d-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7dd8d-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="7dd8d-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7dd8d-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="7dd8d-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7dd8d-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="7dd8d-130">Schema Name</span></span>  <br/> |<span data-ttu-id="7dd8d-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="7dd8d-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7dd8d-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="7dd8d-132">Validation File</span></span>  <br/> |<span data-ttu-id="7dd8d-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7dd8d-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7dd8d-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="7dd8d-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="7dd8d-135">False</span><span class="sxs-lookup"><span data-stu-id="7dd8d-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7dd8d-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7dd8d-136">See also</span></span>



- [<span data-ttu-id="7dd8d-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7dd8d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

