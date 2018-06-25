---
title: MessageTrackingReportId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingReportId
api_type:
- schema
ms.assetid: 9c604ca3-10fe-4760-b7fd-8b52f1a0c712
description: MessageTrackingReportId 元素表示通过其邮件 ID、 组织邮件找、 在其已提交提交邮件，服务器和内部 ID 的唯一标识消息的消息。
ms.openlocfilehash: 8e0d85b203b8a34acedb5f6b9fe46359d5e0b97c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826456"
---
# <a name="messagetrackingreportid"></a><span data-ttu-id="1da98-103">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="1da98-103">MessageTrackingReportId</span></span>

<span data-ttu-id="1da98-104">**MessageTrackingReportId**元素表示通过其邮件 ID、 组织邮件找、 在其已提交提交邮件，服务器和内部 ID 的唯一标识消息的消息。</span><span class="sxs-lookup"><span data-stu-id="1da98-104">The **MessageTrackingReportId** element represents the message by its message ID, the organization where the message was found, the server on which the message was submitted, and an internal ID that uniquely identifies the message.</span></span> 
  
```XML
<MessageTrackingReportId/>
```

 <span data-ttu-id="1da98-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="1da98-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1da98-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1da98-106">Attributes and elements</span></span>

<span data-ttu-id="1da98-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1da98-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1da98-108">属性</span><span class="sxs-lookup"><span data-stu-id="1da98-108">Attributes</span></span>

<span data-ttu-id="1da98-109">无。</span><span class="sxs-lookup"><span data-stu-id="1da98-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1da98-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1da98-110">Child elements</span></span>

<span data-ttu-id="1da98-111">无。</span><span class="sxs-lookup"><span data-stu-id="1da98-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1da98-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1da98-112">Parent elements</span></span>

|<span data-ttu-id="1da98-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1da98-113">**Element**</span></span>|<span data-ttu-id="1da98-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1da98-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1da98-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1da98-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="1da98-116">包含要检索完整的邮件跟踪报告的指定 ID 的[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求</span><span class="sxs-lookup"><span data-stu-id="1da98-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="1da98-117">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="1da98-117">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="1da98-118">包含单个邮件结果[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="1da98-118">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1da98-119">文本值</span><span class="sxs-lookup"><span data-stu-id="1da98-119">Text value</span></span>

<span data-ttu-id="1da98-120">如果使用此元素，则需要用于表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="1da98-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1da98-121">备注</span><span class="sxs-lookup"><span data-stu-id="1da98-121">Remarks</span></span>

<span data-ttu-id="1da98-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1da98-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1da98-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="1da98-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1da98-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="1da98-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1da98-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="1da98-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1da98-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="1da98-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="1da98-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="1da98-127">Validation File</span></span>  <br/> |<span data-ttu-id="1da98-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1da98-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1da98-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="1da98-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="1da98-130">False</span><span class="sxs-lookup"><span data-stu-id="1da98-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1da98-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1da98-131">See also</span></span>



[<span data-ttu-id="1da98-132">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="1da98-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="1da98-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1da98-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

