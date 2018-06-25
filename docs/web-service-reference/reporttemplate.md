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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827118"
---
# <a name="reporttemplate"></a><span data-ttu-id="57877-103">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="57877-103">ReportTemplate</span></span>

<span data-ttu-id="57877-104">**ReportTemplate**元素均表示要获取报告的类型。</span><span class="sxs-lookup"><span data-stu-id="57877-104">The **ReportTemplate** element represents the type of report to get.</span></span> 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 <span data-ttu-id="57877-105">**MessageTrackingReportTemplateType**</span><span class="sxs-lookup"><span data-stu-id="57877-105">**MessageTrackingReportTemplateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="57877-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="57877-106">Attributes and elements</span></span>

<span data-ttu-id="57877-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="57877-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57877-108">属性</span><span class="sxs-lookup"><span data-stu-id="57877-108">Attributes</span></span>

<span data-ttu-id="57877-109">无。</span><span class="sxs-lookup"><span data-stu-id="57877-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57877-110">子元素</span><span class="sxs-lookup"><span data-stu-id="57877-110">Child elements</span></span>

<span data-ttu-id="57877-111">无。</span><span class="sxs-lookup"><span data-stu-id="57877-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="57877-112">父元素</span><span class="sxs-lookup"><span data-stu-id="57877-112">Parent elements</span></span>

|<span data-ttu-id="57877-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="57877-113">**Element**</span></span>|<span data-ttu-id="57877-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="57877-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57877-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="57877-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="57877-116">包含要检索完整的邮件跟踪报告的指定 ID 的[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求</span><span class="sxs-lookup"><span data-stu-id="57877-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="57877-117">文本值</span><span class="sxs-lookup"><span data-stu-id="57877-117">Text value</span></span>

<span data-ttu-id="57877-118">下表列出了**ReportTemplate**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="57877-118">The following table lists the possible values for the **ReportTemplate** element.</span></span> 
  
<span data-ttu-id="57877-119">**ReportTemplate 元素的值**</span><span class="sxs-lookup"><span data-stu-id="57877-119">**ReportTemplate element values**</span></span>

|<span data-ttu-id="57877-120">**值**</span><span class="sxs-lookup"><span data-stu-id="57877-120">**Value**</span></span>|<span data-ttu-id="57877-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="57877-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57877-122">摘要</span><span class="sxs-lookup"><span data-stu-id="57877-122">Summary</span></span>  <br/> |<span data-ttu-id="57877-123">指定报表将每个收件人显示的邮件的所有收件人和邮件的传递状态。</span><span class="sxs-lookup"><span data-stu-id="57877-123">Specifies that the report will display all the recipients of the message and the delivery status of the message to each recipient.</span></span>  <br/> |
|<span data-ttu-id="57877-124">RecipientPath</span><span class="sxs-lookup"><span data-stu-id="57877-124">RecipientPath</span></span>  <br/> |<span data-ttu-id="57877-125">指定的单个收件人，报告将显示发生的事件的完整的历史记录。</span><span class="sxs-lookup"><span data-stu-id="57877-125">Specifies that for a single recipient, the report will display a full history of the events that occurred.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57877-126">注解</span><span class="sxs-lookup"><span data-stu-id="57877-126">Remarks</span></span>

<span data-ttu-id="57877-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="57877-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57877-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="57877-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57877-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="57877-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="57877-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="57877-130">Schema Name</span></span>  <br/> |<span data-ttu-id="57877-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="57877-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="57877-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="57877-132">Validation File</span></span>  <br/> |<span data-ttu-id="57877-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="57877-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="57877-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="57877-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="57877-135">False</span><span class="sxs-lookup"><span data-stu-id="57877-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57877-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="57877-136">See also</span></span>



- [<span data-ttu-id="57877-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="57877-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

