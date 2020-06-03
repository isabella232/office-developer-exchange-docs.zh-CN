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
description: MessageTrackingSearchResults 元素包含匹配搜索条件的记录的列表。
ms.openlocfilehash: 1e03cb135b7b2a125da1e29f7293d233f4e20ddb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468675"
---
# <a name="messagetrackingsearchresults"></a><span data-ttu-id="afffa-103">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="afffa-103">MessageTrackingSearchResults</span></span>

<span data-ttu-id="afffa-104">**MessageTrackingSearchResults**元素包含匹配搜索条件的记录的列表。</span><span class="sxs-lookup"><span data-stu-id="afffa-104">The **MessageTrackingSearchResults** element contains a list of records that match the search criteria.</span></span> 
  
```XML
<MessageTrackingSearchResults>
   <MessageTrackingSearchResult/>
</MessageTrackingSearchResults>
```

 <span data-ttu-id="afffa-105">**ArrayOfFindMessageTrackingSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="afffa-105">**ArrayOfFindMessageTrackingSearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="afffa-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="afffa-106">Attributes and elements</span></span>

<span data-ttu-id="afffa-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="afffa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afffa-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="afffa-108">Attributes</span></span>

<span data-ttu-id="afffa-109">无。</span><span class="sxs-lookup"><span data-stu-id="afffa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="afffa-110">子元素</span><span class="sxs-lookup"><span data-stu-id="afffa-110">Child elements</span></span>

|<span data-ttu-id="afffa-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="afffa-111">**Element**</span></span>|<span data-ttu-id="afffa-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="afffa-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afffa-113">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="afffa-113">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="afffa-114">包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="afffa-114">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="afffa-115">父元素</span><span class="sxs-lookup"><span data-stu-id="afffa-115">Parent elements</span></span>

|<span data-ttu-id="afffa-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="afffa-116">**Element**</span></span>|<span data-ttu-id="afffa-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="afffa-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afffa-118">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="afffa-118">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="afffa-119">包含单个[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="afffa-119">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="afffa-120">文本值</span><span class="sxs-lookup"><span data-stu-id="afffa-120">Text value</span></span>

<span data-ttu-id="afffa-121">无。</span><span class="sxs-lookup"><span data-stu-id="afffa-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afffa-122">说明</span><span class="sxs-lookup"><span data-stu-id="afffa-122">Remarks</span></span>

<span data-ttu-id="afffa-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="afffa-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afffa-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="afffa-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afffa-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="afffa-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="afffa-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="afffa-126">Schema Name</span></span>  <br/> |<span data-ttu-id="afffa-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="afffa-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="afffa-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="afffa-128">Validation File</span></span>  <br/> |<span data-ttu-id="afffa-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="afffa-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="afffa-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="afffa-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="afffa-131">False</span><span class="sxs-lookup"><span data-stu-id="afffa-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afffa-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="afffa-132">See also</span></span>



- [<span data-ttu-id="afffa-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="afffa-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

