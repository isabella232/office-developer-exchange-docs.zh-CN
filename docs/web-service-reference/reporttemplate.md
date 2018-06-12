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
description: ReportTemplate 元素均表示要获取报告的类型。
ms.openlocfilehash: 70aab69f4d20ad9fd7e878c7fccd16e261c9b94c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827118"
---
# <a name="reporttemplate"></a><span data-ttu-id="15cdd-103">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="15cdd-103">ReportTemplate</span></span>

<span data-ttu-id="15cdd-104">**ReportTemplate**元素均表示要获取报告的类型。</span><span class="sxs-lookup"><span data-stu-id="15cdd-104">The **ReportTemplate** element represents the type of report to get.</span></span> 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 <span data-ttu-id="15cdd-105">**MessageTrackingReportTemplateType**</span><span class="sxs-lookup"><span data-stu-id="15cdd-105">**MessageTrackingReportTemplateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15cdd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="15cdd-106">Attributes and elements</span></span>

<span data-ttu-id="15cdd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="15cdd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15cdd-108">属性</span><span class="sxs-lookup"><span data-stu-id="15cdd-108">Attributes</span></span>

<span data-ttu-id="15cdd-109">无。</span><span class="sxs-lookup"><span data-stu-id="15cdd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15cdd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="15cdd-110">Child elements</span></span>

<span data-ttu-id="15cdd-111">无。</span><span class="sxs-lookup"><span data-stu-id="15cdd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="15cdd-112">父元素</span><span class="sxs-lookup"><span data-stu-id="15cdd-112">Parent elements</span></span>

|<span data-ttu-id="15cdd-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="15cdd-113">**Element**</span></span>|<span data-ttu-id="15cdd-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="15cdd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15cdd-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="15cdd-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="15cdd-116">包含要检索完整的邮件跟踪报告的指定 ID 的[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求</span><span class="sxs-lookup"><span data-stu-id="15cdd-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="15cdd-117">文本值</span><span class="sxs-lookup"><span data-stu-id="15cdd-117">Text value</span></span>

<span data-ttu-id="15cdd-118">下表列出了**ReportTemplate**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="15cdd-118">The following table lists the possible values for the **ReportTemplate** element.</span></span> 
  
<span data-ttu-id="15cdd-119">**ReportTemplate 元素的值**</span><span class="sxs-lookup"><span data-stu-id="15cdd-119">**ReportTemplate element values**</span></span>

|<span data-ttu-id="15cdd-120">**值**</span><span class="sxs-lookup"><span data-stu-id="15cdd-120">**Value**</span></span>|<span data-ttu-id="15cdd-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="15cdd-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15cdd-122">摘要</span><span class="sxs-lookup"><span data-stu-id="15cdd-122">Summary</span></span>  <br/> |<span data-ttu-id="15cdd-123">指定报表将每个收件人显示的邮件的所有收件人和邮件的传递状态。</span><span class="sxs-lookup"><span data-stu-id="15cdd-123">Specifies that the report will display all the recipients of the message and the delivery status of the message to each recipient.</span></span>  <br/> |
|<span data-ttu-id="15cdd-124">RecipientPath</span><span class="sxs-lookup"><span data-stu-id="15cdd-124">RecipientPath</span></span>  <br/> |<span data-ttu-id="15cdd-125">指定的单个收件人，报告将显示发生的事件的完整的历史记录。</span><span class="sxs-lookup"><span data-stu-id="15cdd-125">Specifies that for a single recipient, the report will display a full history of the events that occurred.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15cdd-126">备注</span><span class="sxs-lookup"><span data-stu-id="15cdd-126">Remarks</span></span>

<span data-ttu-id="15cdd-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="15cdd-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15cdd-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="15cdd-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15cdd-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="15cdd-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="15cdd-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="15cdd-130">Schema Name</span></span>  <br/> |<span data-ttu-id="15cdd-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="15cdd-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="15cdd-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="15cdd-132">Validation File</span></span>  <br/> |<span data-ttu-id="15cdd-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="15cdd-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="15cdd-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="15cdd-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="15cdd-135">False</span><span class="sxs-lookup"><span data-stu-id="15cdd-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15cdd-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15cdd-136">See also</span></span>



- [<span data-ttu-id="15cdd-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="15cdd-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

