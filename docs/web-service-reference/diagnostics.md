---
title: 过程
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
description: Diagnostics 元素提供用于在数据中心中进行报告的计时和性能信息。
ms.openlocfilehash: 9eb46ef7ceb877372aff9b029190af8c8d8115cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467835"
---
# <a name="diagnostics"></a><span data-ttu-id="264a1-103">过程</span><span class="sxs-lookup"><span data-stu-id="264a1-103">Diagnostics</span></span>

<span data-ttu-id="264a1-104">**Diagnostics**元素提供用于在数据中心中进行报告的计时和性能信息。</span><span class="sxs-lookup"><span data-stu-id="264a1-104">The **Diagnostics** element provides timing and performance information that is used for reporting in a DataCenter.</span></span> 
  
```XML
<Diagnostics>
   <String/>
</Diagnostics>

```

 <span data-ttu-id="264a1-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="264a1-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="264a1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="264a1-106">Attributes and elements</span></span>

<span data-ttu-id="264a1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="264a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="264a1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="264a1-108">Attributes</span></span>

<span data-ttu-id="264a1-109">无。</span><span class="sxs-lookup"><span data-stu-id="264a1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="264a1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="264a1-110">Child elements</span></span>

|<span data-ttu-id="264a1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="264a1-111">**Element**</span></span>|<span data-ttu-id="264a1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="264a1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="264a1-113">字符串</span><span class="sxs-lookup"><span data-stu-id="264a1-113">String</span></span>](string.md) <br/> |<span data-ttu-id="264a1-114">包含项目、联系人、任务和对话使用的字符串。</span><span class="sxs-lookup"><span data-stu-id="264a1-114">Contains a string that is used by items, contacts, tasks, and conversations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="264a1-115">父元素</span><span class="sxs-lookup"><span data-stu-id="264a1-115">Parent elements</span></span>

|<span data-ttu-id="264a1-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="264a1-116">**Element**</span></span>|<span data-ttu-id="264a1-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="264a1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="264a1-118">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="264a1-118">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="264a1-119">包含单个[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="264a1-119">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="264a1-120">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="264a1-120">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="264a1-121">包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="264a1-121">Contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="264a1-122">文本值</span><span class="sxs-lookup"><span data-stu-id="264a1-122">Text value</span></span>

<span data-ttu-id="264a1-123">无。</span><span class="sxs-lookup"><span data-stu-id="264a1-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="264a1-124">说明</span><span class="sxs-lookup"><span data-stu-id="264a1-124">Remarks</span></span>

<span data-ttu-id="264a1-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="264a1-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="264a1-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="264a1-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="264a1-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="264a1-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="264a1-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="264a1-128">Schema Name</span></span>  <br/> |<span data-ttu-id="264a1-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="264a1-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="264a1-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="264a1-130">Validation File</span></span>  <br/> |<span data-ttu-id="264a1-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="264a1-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="264a1-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="264a1-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="264a1-133">False</span><span class="sxs-lookup"><span data-stu-id="264a1-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="264a1-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="264a1-134">See also</span></span>

- [<span data-ttu-id="264a1-135">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="264a1-135">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="264a1-136">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="264a1-136">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="264a1-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="264a1-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

