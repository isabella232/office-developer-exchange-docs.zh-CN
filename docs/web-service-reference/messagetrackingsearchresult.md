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
ms.openlocfilehash: ad4fb9d9e2266222303bd2015a7afba0bb46721b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826460"
---
# <a name="messagetrackingsearchresult"></a><span data-ttu-id="cb7ce-103">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="cb7ce-103">MessageTrackingSearchResult</span></span>

<span data-ttu-id="cb7ce-104">**MessageTrackingSearchResult**元素包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-104">The **MessageTrackingSearchResult** element contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span> 
  
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

 <span data-ttu-id="cb7ce-105">**FindMessageTrackingSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="cb7ce-105">**FindMessageTrackingSearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb7ce-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cb7ce-106">Attributes and elements</span></span>

<span data-ttu-id="cb7ce-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb7ce-108">属性</span><span class="sxs-lookup"><span data-stu-id="cb7ce-108">Attributes</span></span>

<span data-ttu-id="cb7ce-109">无。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb7ce-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cb7ce-110">Child elements</span></span>

|<span data-ttu-id="cb7ce-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb7ce-111">**Element**</span></span>|<span data-ttu-id="cb7ce-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb7ce-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb7ce-113">Subject</span><span class="sxs-lookup"><span data-stu-id="cb7ce-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="cb7ce-114">包含电子邮件主题。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-114">Contains the e-mail message subject.</span></span>  <br/> |
|[<span data-ttu-id="cb7ce-115">发件人 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cb7ce-115">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="cb7ce-116">包含电子邮件发件人的地址。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-116">Contains the e-mail message sender's address.</span></span>  <br/> |
|[<span data-ttu-id="cb7ce-117">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="cb7ce-117">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="cb7ce-118">包含声称的发件人的电子邮件的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-118">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="cb7ce-119">收件人 (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="cb7ce-119">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="cb7ce-120">包含的电子邮件地址收到此消息的列表。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-120">Contains a list of e-mail addresses that received this message.</span></span>  <br/> |
|[<span data-ttu-id="cb7ce-121">SubmittedTime</span><span class="sxs-lookup"><span data-stu-id="cb7ce-121">SubmittedTime</span></span>](submittedtime.md) <br/> |<span data-ttu-id="cb7ce-122">包含已提交提交邮件的时间。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-122">Contains the time that the message was submitted.</span></span>  <br/> |
|[<span data-ttu-id="cb7ce-123">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="cb7ce-123">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="cb7ce-124">包含内部 ID 标识的传输数据库中的消息。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-124">Contains an internal ID that identifies the message in the transport database.</span></span>  <br/> |
|[<span data-ttu-id="cb7ce-125">PreviousHopServer</span><span class="sxs-lookup"><span data-stu-id="cb7ce-125">PreviousHopServer</span></span>](previoushopserver.md) <br/> |<span data-ttu-id="cb7ce-126">包含林中的以前接受邮件服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-126">Contains the name of the server in the forest that previously accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="cb7ce-127">FirstHopServer</span><span class="sxs-lookup"><span data-stu-id="cb7ce-127">FirstHopServer</span></span>](firsthopserver.md) <br/> |<span data-ttu-id="cb7ce-128">包含林中的先接受邮件服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-128">Contains the name of the server in the forest that first accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="cb7ce-129">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="cb7ce-129">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="cb7ce-130">包含一个或多个跟踪属性的列表。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-130">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cb7ce-131">父元素</span><span class="sxs-lookup"><span data-stu-id="cb7ce-131">Parent elements</span></span>

|<span data-ttu-id="cb7ce-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb7ce-132">**Element**</span></span>|<span data-ttu-id="cb7ce-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb7ce-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb7ce-134">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="cb7ce-134">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="cb7ce-135">包含与搜索条件匹配的邮件的列表。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-135">Contains a list of messages that match the search criteria.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb7ce-136">文本值</span><span class="sxs-lookup"><span data-stu-id="cb7ce-136">Text value</span></span>

<span data-ttu-id="cb7ce-137">无。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb7ce-138">备注</span><span class="sxs-lookup"><span data-stu-id="cb7ce-138">Remarks</span></span>

<span data-ttu-id="cb7ce-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cb7ce-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb7ce-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="cb7ce-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb7ce-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="cb7ce-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cb7ce-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="cb7ce-142">Schema Name</span></span>  <br/> |<span data-ttu-id="cb7ce-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="cb7ce-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="cb7ce-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="cb7ce-144">Validation File</span></span>  <br/> |<span data-ttu-id="cb7ce-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cb7ce-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cb7ce-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="cb7ce-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb7ce-147">False</span><span class="sxs-lookup"><span data-stu-id="cb7ce-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb7ce-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb7ce-148">See also</span></span>



[<span data-ttu-id="cb7ce-149">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="cb7ce-149">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="cb7ce-150">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cb7ce-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

