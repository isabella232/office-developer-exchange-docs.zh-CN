---
title: DiagnosticsLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DiagnosticsLevel
api_type:
- schema
ms.assetid: 66794226-f5e0-44f0-8a0e-1f194bb0ba0f
description: DiagnosticsLevel 元素表示将用于派生报表的计时和性能信息。
ms.openlocfilehash: 3060d4f1b8449a5870d964bdfcdbf0d503905abc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467828"
---
# <a name="diagnosticslevel"></a><span data-ttu-id="76a59-103">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="76a59-103">DiagnosticsLevel</span></span>

<span data-ttu-id="76a59-104">**DiagnosticsLevel**元素表示将用于派生报表的计时和性能信息。</span><span class="sxs-lookup"><span data-stu-id="76a59-104">The **DiagnosticsLevel** element represents timing and performance information that will be used to derive the report.</span></span> 
  
```XML
<DiagnosticsLevel/>
```

 <span data-ttu-id="76a59-105">**string**</span><span class="sxs-lookup"><span data-stu-id="76a59-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76a59-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="76a59-106">Attributes and elements</span></span>

<span data-ttu-id="76a59-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="76a59-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76a59-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="76a59-108">Attributes</span></span>

<span data-ttu-id="76a59-109">无。</span><span class="sxs-lookup"><span data-stu-id="76a59-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76a59-110">子元素</span><span class="sxs-lookup"><span data-stu-id="76a59-110">Child elements</span></span>

<span data-ttu-id="76a59-111">无。</span><span class="sxs-lookup"><span data-stu-id="76a59-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="76a59-112">父元素</span><span class="sxs-lookup"><span data-stu-id="76a59-112">Parent elements</span></span>

|<span data-ttu-id="76a59-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="76a59-113">**Element**</span></span>|<span data-ttu-id="76a59-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="76a59-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76a59-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="76a59-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="76a59-116">包含要查找的邮件的类型的条件。</span><span class="sxs-lookup"><span data-stu-id="76a59-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="76a59-117">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="76a59-117">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="76a59-118">包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求，以检索指定 ID 的完整邮件跟踪报告。</span><span class="sxs-lookup"><span data-stu-id="76a59-118">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="76a59-119">文本值</span><span class="sxs-lookup"><span data-stu-id="76a59-119">Text value</span></span>

<span data-ttu-id="76a59-120">如果使用此元素，则需要一个表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="76a59-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76a59-121">说明</span><span class="sxs-lookup"><span data-stu-id="76a59-121">Remarks</span></span>

<span data-ttu-id="76a59-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="76a59-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76a59-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="76a59-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76a59-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="76a59-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="76a59-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="76a59-125">Schema Name</span></span>  <br/> |<span data-ttu-id="76a59-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="76a59-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="76a59-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="76a59-127">Validation File</span></span>  <br/> |<span data-ttu-id="76a59-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="76a59-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="76a59-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="76a59-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="76a59-130">False</span><span class="sxs-lookup"><span data-stu-id="76a59-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76a59-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="76a59-131">See also</span></span>

- [<span data-ttu-id="76a59-132">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="76a59-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="76a59-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="76a59-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

