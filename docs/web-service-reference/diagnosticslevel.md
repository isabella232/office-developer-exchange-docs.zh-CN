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
description: DiagnosticsLevel 元素表示用于派生报表的计时和性能信息。
ms.openlocfilehash: 9205625bb6cf38e370e29d96770eb293ed9277f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753856"
---
# <a name="diagnosticslevel"></a><span data-ttu-id="63410-103">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="63410-103">DiagnosticsLevel</span></span>

<span data-ttu-id="63410-104">**DiagnosticsLevel**元素表示用于派生报表的计时和性能信息。</span><span class="sxs-lookup"><span data-stu-id="63410-104">The **DiagnosticsLevel** element represents timing and performance information that will be used to derive the report.</span></span> 
  
```XML
<DiagnosticsLevel/>
```

 <span data-ttu-id="63410-105">**string**</span><span class="sxs-lookup"><span data-stu-id="63410-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63410-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="63410-106">Attributes and elements</span></span>

<span data-ttu-id="63410-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="63410-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63410-108">属性</span><span class="sxs-lookup"><span data-stu-id="63410-108">Attributes</span></span>

<span data-ttu-id="63410-109">无。</span><span class="sxs-lookup"><span data-stu-id="63410-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63410-110">子元素</span><span class="sxs-lookup"><span data-stu-id="63410-110">Child elements</span></span>

<span data-ttu-id="63410-111">无。</span><span class="sxs-lookup"><span data-stu-id="63410-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="63410-112">父元素</span><span class="sxs-lookup"><span data-stu-id="63410-112">Parent elements</span></span>

|<span data-ttu-id="63410-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="63410-113">**Element**</span></span>|<span data-ttu-id="63410-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="63410-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63410-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="63410-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="63410-116">包含要查找的邮件的类型的条件。</span><span class="sxs-lookup"><span data-stu-id="63410-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="63410-117">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="63410-117">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="63410-118">包含要检索完整的邮件跟踪报告的指定 ID 的[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求</span><span class="sxs-lookup"><span data-stu-id="63410-118">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="63410-119">文本值</span><span class="sxs-lookup"><span data-stu-id="63410-119">Text value</span></span>

<span data-ttu-id="63410-120">如果使用此元素，则需要用于表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="63410-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63410-121">备注</span><span class="sxs-lookup"><span data-stu-id="63410-121">Remarks</span></span>

<span data-ttu-id="63410-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="63410-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63410-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="63410-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63410-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="63410-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="63410-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="63410-125">Schema Name</span></span>  <br/> |<span data-ttu-id="63410-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="63410-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="63410-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="63410-127">Validation File</span></span>  <br/> |<span data-ttu-id="63410-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="63410-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="63410-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="63410-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="63410-130">False</span><span class="sxs-lookup"><span data-stu-id="63410-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63410-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="63410-131">See also</span></span>

- [<span data-ttu-id="63410-132">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="63410-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="63410-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="63410-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

