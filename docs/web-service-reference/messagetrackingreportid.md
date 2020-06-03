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
description: MessageTrackingReportId 元素表示邮件的邮件 ID、在其中找到邮件的组织、提交邮件的服务器以及唯一标识该邮件的内部 ID。
ms.openlocfilehash: d6e92593d55608e260634602c2aab694804d716d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460594"
---
# <a name="messagetrackingreportid"></a><span data-ttu-id="f9caa-103">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="f9caa-103">MessageTrackingReportId</span></span>

<span data-ttu-id="f9caa-104">**MessageTrackingReportId**元素表示邮件的邮件 ID、在其中找到邮件的组织、提交邮件的服务器以及唯一标识该邮件的内部 ID。</span><span class="sxs-lookup"><span data-stu-id="f9caa-104">The **MessageTrackingReportId** element represents the message by its message ID, the organization where the message was found, the server on which the message was submitted, and an internal ID that uniquely identifies the message.</span></span> 
  
```XML
<MessageTrackingReportId/>
```

 <span data-ttu-id="f9caa-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="f9caa-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9caa-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f9caa-106">Attributes and elements</span></span>

<span data-ttu-id="f9caa-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f9caa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9caa-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f9caa-108">Attributes</span></span>

<span data-ttu-id="f9caa-109">无。</span><span class="sxs-lookup"><span data-stu-id="f9caa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9caa-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f9caa-110">Child elements</span></span>

<span data-ttu-id="f9caa-111">无。</span><span class="sxs-lookup"><span data-stu-id="f9caa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f9caa-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f9caa-112">Parent elements</span></span>

|<span data-ttu-id="f9caa-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f9caa-113">**Element**</span></span>|<span data-ttu-id="f9caa-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f9caa-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9caa-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="f9caa-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="f9caa-116">包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求，以检索指定 ID 的完整邮件跟踪报告。</span><span class="sxs-lookup"><span data-stu-id="f9caa-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="f9caa-117">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="f9caa-117">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="f9caa-118">包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="f9caa-118">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f9caa-119">文本值</span><span class="sxs-lookup"><span data-stu-id="f9caa-119">Text value</span></span>

<span data-ttu-id="f9caa-120">如果使用此元素，则需要一个表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="f9caa-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9caa-121">说明</span><span class="sxs-lookup"><span data-stu-id="f9caa-121">Remarks</span></span>

<span data-ttu-id="f9caa-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f9caa-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9caa-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f9caa-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9caa-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f9caa-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f9caa-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f9caa-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f9caa-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="f9caa-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="f9caa-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f9caa-127">Validation File</span></span>  <br/> |<span data-ttu-id="f9caa-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f9caa-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f9caa-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f9caa-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="f9caa-130">False</span><span class="sxs-lookup"><span data-stu-id="f9caa-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9caa-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f9caa-131">See also</span></span>



[<span data-ttu-id="f9caa-132">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="f9caa-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="f9caa-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f9caa-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

