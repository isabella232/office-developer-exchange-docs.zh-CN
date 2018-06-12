---
title: MessageTrackingSearchResults
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingSearchResults
api_type:
- schema
ms.assetid: 6bf36f37-c2b3-40c1-a4df-31573ed8642a
description: MessageTrackingSearchResults 元素包含与搜索条件匹配的记录的列表。
ms.openlocfilehash: 866cc8d4e9afa8347eb7bd0d9e9acaddc616c396
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826454"
---
# <a name="messagetrackingsearchresults"></a><span data-ttu-id="d3509-103">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="d3509-103">MessageTrackingSearchResults</span></span>

<span data-ttu-id="d3509-104">**MessageTrackingSearchResults**元素包含与搜索条件匹配的记录的列表。</span><span class="sxs-lookup"><span data-stu-id="d3509-104">The **MessageTrackingSearchResults** element contains a list of records that match the search criteria.</span></span> 
  
```XML
<MessageTrackingSearchResults>
   <MessageTrackingSearchResult/>
</MessageTrackingSearchResults>
```

 <span data-ttu-id="d3509-105">**ArrayOfFindMessageTrackingSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="d3509-105">**ArrayOfFindMessageTrackingSearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3509-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d3509-106">Attributes and elements</span></span>

<span data-ttu-id="d3509-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d3509-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3509-108">属性</span><span class="sxs-lookup"><span data-stu-id="d3509-108">Attributes</span></span>

<span data-ttu-id="d3509-109">无。</span><span class="sxs-lookup"><span data-stu-id="d3509-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3509-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d3509-110">Child elements</span></span>

|<span data-ttu-id="d3509-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d3509-111">**Element**</span></span>|<span data-ttu-id="d3509-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d3509-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3509-113">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="d3509-113">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="d3509-114">包含单个邮件结果[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="d3509-114">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3509-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d3509-115">Parent elements</span></span>

|<span data-ttu-id="d3509-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="d3509-116">**Element**</span></span>|<span data-ttu-id="d3509-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="d3509-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3509-118">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="d3509-118">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="d3509-119">包含状态和的单个结果[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="d3509-119">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d3509-120">文本值</span><span class="sxs-lookup"><span data-stu-id="d3509-120">Text value</span></span>

<span data-ttu-id="d3509-121">无。</span><span class="sxs-lookup"><span data-stu-id="d3509-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d3509-122">备注</span><span class="sxs-lookup"><span data-stu-id="d3509-122">Remarks</span></span>

<span data-ttu-id="d3509-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d3509-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3509-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="d3509-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3509-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="d3509-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d3509-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="d3509-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d3509-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="d3509-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d3509-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="d3509-128">Validation File</span></span>  <br/> |<span data-ttu-id="d3509-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d3509-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d3509-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="d3509-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3509-131">False</span><span class="sxs-lookup"><span data-stu-id="d3509-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3509-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d3509-132">See also</span></span>



- [<span data-ttu-id="d3509-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d3509-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

