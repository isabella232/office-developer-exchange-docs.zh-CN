---
title: MessageTrackingSearchResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: MessageTrackingSearchResult 元素包含 FindMessageTrackingReportResponse 元素的单个邮件结果。
ms.openlocfilehash: 27e70cd9e11b480ab6bbb9b28275f142da7c76ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466680"
---
# <a name="messagetrackingsearchresult"></a><span data-ttu-id="4650f-103">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="4650f-103">MessageTrackingSearchResult</span></span>

<span data-ttu-id="4650f-104">**MessageTrackingSearchResult**元素包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="4650f-104">The **MessageTrackingSearchResult** element contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span> 
  
```xml
<MessageTrackingSearchResult>
   <Subject/>
   <Sender/>
   <PurportedSender/>
   <Recipients/>
   <SubmittedTime/>
   <MessageTrackingReportId/>
   <PreviousHopServer/>
   <FirstHopServer/>
   <Properties/>
</MessageTrackingSearchResult>
```

 <span data-ttu-id="4650f-105">**FindMessageTrackingSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="4650f-105">**FindMessageTrackingSearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4650f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4650f-106">Attributes and elements</span></span>

<span data-ttu-id="4650f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4650f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4650f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4650f-108">Attributes</span></span>

<span data-ttu-id="4650f-109">无。</span><span class="sxs-lookup"><span data-stu-id="4650f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4650f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4650f-110">Child elements</span></span>

|<span data-ttu-id="4650f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4650f-111">**Element**</span></span>|<span data-ttu-id="4650f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4650f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4650f-113">主题</span><span class="sxs-lookup"><span data-stu-id="4650f-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="4650f-114">包含电子邮件主题。</span><span class="sxs-lookup"><span data-stu-id="4650f-114">Contains the e-mail message subject.</span></span>  <br/> |
|[<span data-ttu-id="4650f-115">发件人（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="4650f-115">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="4650f-116">包含电子邮件发件人的地址。</span><span class="sxs-lookup"><span data-stu-id="4650f-116">Contains the e-mail message sender's address.</span></span>  <br/> |
|[<span data-ttu-id="4650f-117">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="4650f-117">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="4650f-118">包含所声称的电子邮件发件人的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="4650f-118">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="4650f-119">收件人（ArrayOfRecipientsType）</span><span class="sxs-lookup"><span data-stu-id="4650f-119">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="4650f-120">包含收到此邮件的电子邮件地址的列表。</span><span class="sxs-lookup"><span data-stu-id="4650f-120">Contains a list of e-mail addresses that received this message.</span></span>  <br/> |
|[<span data-ttu-id="4650f-121">SubmittedTime</span><span class="sxs-lookup"><span data-stu-id="4650f-121">SubmittedTime</span></span>](submittedtime.md) <br/> |<span data-ttu-id="4650f-122">包含提交邮件的时间。</span><span class="sxs-lookup"><span data-stu-id="4650f-122">Contains the time that the message was submitted.</span></span>  <br/> |
|[<span data-ttu-id="4650f-123">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="4650f-123">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="4650f-124">包含标识传输数据库中的邮件的内部 ID。</span><span class="sxs-lookup"><span data-stu-id="4650f-124">Contains an internal ID that identifies the message in the transport database.</span></span>  <br/> |
|[<span data-ttu-id="4650f-125">PreviousHopServer</span><span class="sxs-lookup"><span data-stu-id="4650f-125">PreviousHopServer</span></span>](previoushopserver.md) <br/> |<span data-ttu-id="4650f-126">包含之前接受邮件的林中的服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="4650f-126">Contains the name of the server in the forest that previously accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="4650f-127">FirstHopServer</span><span class="sxs-lookup"><span data-stu-id="4650f-127">FirstHopServer</span></span>](firsthopserver.md) <br/> |<span data-ttu-id="4650f-128">包含在林中第一次接受邮件的服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="4650f-128">Contains the name of the server in the forest that first accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="4650f-129">Properties （ArrayOfTrackingPropertiesType）</span><span class="sxs-lookup"><span data-stu-id="4650f-129">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="4650f-130">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="4650f-130">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4650f-131">父元素</span><span class="sxs-lookup"><span data-stu-id="4650f-131">Parent elements</span></span>

|<span data-ttu-id="4650f-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="4650f-132">**Element**</span></span>|<span data-ttu-id="4650f-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="4650f-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4650f-134">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="4650f-134">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="4650f-135">包含与搜索条件匹配的邮件的列表。</span><span class="sxs-lookup"><span data-stu-id="4650f-135">Contains a list of messages that match the search criteria.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4650f-136">文本值</span><span class="sxs-lookup"><span data-stu-id="4650f-136">Text value</span></span>

<span data-ttu-id="4650f-137">无。</span><span class="sxs-lookup"><span data-stu-id="4650f-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4650f-138">说明</span><span class="sxs-lookup"><span data-stu-id="4650f-138">Remarks</span></span>

<span data-ttu-id="4650f-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4650f-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4650f-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="4650f-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4650f-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="4650f-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4650f-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="4650f-142">Schema Name</span></span>  <br/> |<span data-ttu-id="4650f-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="4650f-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="4650f-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="4650f-144">Validation File</span></span>  <br/> |<span data-ttu-id="4650f-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4650f-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4650f-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="4650f-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="4650f-147">False</span><span class="sxs-lookup"><span data-stu-id="4650f-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4650f-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4650f-148">See also</span></span>



[<span data-ttu-id="4650f-149">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="4650f-149">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="4650f-150">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4650f-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

