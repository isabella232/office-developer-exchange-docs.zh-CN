---
title: FindMailboxStatisticsByKeywordsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d3835800-8887-43db-9a8a-fe3cfea7a863
description: FindMailboxStatisticsByKeywordsResponseMessage 元素指定 FindMailboxStatisticsByKeywords 请求的响应消息。
ms.openlocfilehash: 704eebbf82db2871ab36be8e5b30c88c6959baa5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44525974"
---
# <a name="findmailboxstatisticsbykeywordsresponsemessage"></a><span data-ttu-id="fa65c-103">FindMailboxStatisticsByKeywordsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fa65c-103">FindMailboxStatisticsByKeywordsResponseMessage</span></span>

<span data-ttu-id="fa65c-104">**FindMailboxStatisticsByKeywordsResponseMessage**元素指定**FindMailboxStatisticsByKeywords**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="fa65c-104">The **FindMailboxStatisticsByKeywordsResponseMessage** element specifies the response message for a **FindMailboxStatisticsByKeywords** request.</span></span> 
  
```XML
<FindMailboxStatisticsByKeywordsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxStatisticsSearchResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindMailboxStatisticsByKeywordsResponseMessage>
```

 <span data-ttu-id="fa65c-105">**FindMailboxStatisticsByKeywordsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="fa65c-105">**FindMailboxStatisticsByKeywordsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa65c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa65c-106">Attributes and elements</span></span>

<span data-ttu-id="fa65c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa65c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa65c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fa65c-108">Attributes</span></span>

|<span data-ttu-id="fa65c-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="fa65c-109">**Attribute**</span></span>|<span data-ttu-id="fa65c-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa65c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa65c-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="fa65c-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="fa65c-112">指定响应类。</span><span class="sxs-lookup"><span data-stu-id="fa65c-112">Specifies the response class.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="fa65c-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="fa65c-113">ResponseClass</span></span>

|<span data-ttu-id="fa65c-114">**值**</span><span class="sxs-lookup"><span data-stu-id="fa65c-114">**Value**</span></span>|<span data-ttu-id="fa65c-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa65c-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa65c-116">成功</span><span class="sxs-lookup"><span data-stu-id="fa65c-116">Success</span></span>  <br/> |<span data-ttu-id="fa65c-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="fa65c-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="fa65c-118">警告</span><span class="sxs-lookup"><span data-stu-id="fa65c-118">Warning</span></span>  <br/> |<span data-ttu-id="fa65c-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="fa65c-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="fa65c-120">错误</span><span class="sxs-lookup"><span data-stu-id="fa65c-120">Error</span></span>  <br/> |<span data-ttu-id="fa65c-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="fa65c-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fa65c-122">子元素</span><span class="sxs-lookup"><span data-stu-id="fa65c-122">Child elements</span></span>

|<span data-ttu-id="fa65c-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa65c-123">**Element**</span></span>|<span data-ttu-id="fa65c-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="fa65c-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa65c-125">MailboxStatisticsSearchResult</span><span class="sxs-lookup"><span data-stu-id="fa65c-125">MailboxStatisticsSearchResult</span></span>](mailboxstatisticssearchresult.md) <br/> |<span data-ttu-id="fa65c-126">指定邮箱搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="fa65c-126">Specifies the result of a mailbox search.</span></span>  <br/> |
|[<span data-ttu-id="fa65c-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="fa65c-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="fa65c-128">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="fa65c-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="fa65c-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fa65c-129">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="fa65c-130">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="fa65c-130">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="fa65c-131">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fa65c-131">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="fa65c-132">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="fa65c-132">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="fa65c-133">MessageXml</span><span class="sxs-lookup"><span data-stu-id="fa65c-133">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="fa65c-134">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="fa65c-134">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa65c-135">父元素</span><span class="sxs-lookup"><span data-stu-id="fa65c-135">Parent elements</span></span>

|<span data-ttu-id="fa65c-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa65c-136">**Element**</span></span>|<span data-ttu-id="fa65c-137">**描述**</span><span class="sxs-lookup"><span data-stu-id="fa65c-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa65c-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fa65c-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="fa65c-139">指定响应消息的数组。</span><span class="sxs-lookup"><span data-stu-id="fa65c-139">Specifies an array of response messages.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa65c-140">备注</span><span class="sxs-lookup"><span data-stu-id="fa65c-140">Remarks</span></span>

<span data-ttu-id="fa65c-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fa65c-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa65c-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fa65c-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa65c-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa65c-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa65c-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa65c-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fa65c-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa65c-145">Schema Name</span></span>  <br/> |<span data-ttu-id="fa65c-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="fa65c-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="fa65c-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa65c-147">Validation File</span></span>  <br/> |<span data-ttu-id="fa65c-148">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="fa65c-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fa65c-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa65c-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fa65c-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa65c-150">See also</span></span>



- [<span data-ttu-id="fa65c-151">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fa65c-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

