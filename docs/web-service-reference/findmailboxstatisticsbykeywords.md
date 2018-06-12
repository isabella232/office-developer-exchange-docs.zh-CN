---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: FindMailboxStatisticsByKeywords 元素指定按关键字搜索的邮箱统计信息的请求。
ms.openlocfilehash: e667f13b66e439dca88d73a5e05d74846183928c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754343"
---
# <a name="findmailboxstatisticsbykeywords"></a><span data-ttu-id="2c002-103">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="2c002-103">FindMailboxStatisticsByKeywords</span></span>

<span data-ttu-id="2c002-104">**FindMailboxStatisticsByKeywords**元素指定按关键字搜索的邮箱统计信息的请求。</span><span class="sxs-lookup"><span data-stu-id="2c002-104">The **FindMailboxStatisticsByKeywords** element specifies a request to search for mailbox statistics by keyword.</span></span> 
  
```XML
<FindMailboxStatisticsByKeywords>
    <Mailboxes/>
    <Keywords/>
    <Language/>
    <Senders/>
    <Recipients/>
    <FromDate/>
    <ToDate/>
    <MessageTypes/>
    <SearchDumpster/>
    <IncludePersonalArchive/>
    <IncludeUnsearchableItems/>
</FindMailboxStatisticsByKeywords>
```

 <span data-ttu-id="2c002-105">**FindMailboxStatisticsByKeywordsType**</span><span class="sxs-lookup"><span data-stu-id="2c002-105">**FindMailboxStatisticsByKeywordsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c002-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2c002-106">Attributes and elements</span></span>

<span data-ttu-id="2c002-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2c002-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c002-108">属性</span><span class="sxs-lookup"><span data-stu-id="2c002-108">Attributes</span></span>

<span data-ttu-id="2c002-109">无。</span><span class="sxs-lookup"><span data-stu-id="2c002-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c002-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2c002-110">Child elements</span></span>

|<span data-ttu-id="2c002-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2c002-111">**Element**</span></span>|<span data-ttu-id="2c002-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2c002-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c002-113">邮箱 (ArrayOfUserMailboxesType)</span><span class="sxs-lookup"><span data-stu-id="2c002-113">Mailboxes (ArrayOfUserMailboxesType)</span></span>](mailboxes-arrayofusermailboxestype.md) <br/> |<span data-ttu-id="2c002-114">包含受保留的邮箱的数组。</span><span class="sxs-lookup"><span data-stu-id="2c002-114">Contains an array of mailboxes affected by the hold.</span></span>  <br/> |
|[<span data-ttu-id="2c002-115">Keywords</span><span class="sxs-lookup"><span data-stu-id="2c002-115">Keywords</span></span>](keywords-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2c002-116">指定搜索的关键字。</span><span class="sxs-lookup"><span data-stu-id="2c002-116">Specifies keywords for a search.</span></span>  <br/> |
|[<span data-ttu-id="2c002-117">Language</span><span class="sxs-lookup"><span data-stu-id="2c002-117">Language</span></span>](language.md) <br/> |<span data-ttu-id="2c002-118">包含用于搜索查询的语言。</span><span class="sxs-lookup"><span data-stu-id="2c002-118">Contains the language used for the search query.</span></span>  <br/> |
|[<span data-ttu-id="2c002-119">发件人</span><span class="sxs-lookup"><span data-stu-id="2c002-119">Senders</span></span>](senders.md) <br/> |<span data-ttu-id="2c002-120">指定 SMTP 地址的数组。</span><span class="sxs-lookup"><span data-stu-id="2c002-120">Specifies an array of SMTP addresses.</span></span>  <br/> |
|[<span data-ttu-id="2c002-121">收件人 (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="2c002-121">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="2c002-122">指定的邮件收件人的数组。</span><span class="sxs-lookup"><span data-stu-id="2c002-122">Specifies an array of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="2c002-123">FromDate</span><span class="sxs-lookup"><span data-stu-id="2c002-123">FromDate</span></span>](fromdate.md) <br/> |<span data-ttu-id="2c002-124">指定发送邮件的日期。</span><span class="sxs-lookup"><span data-stu-id="2c002-124">Specifies the date that the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="2c002-125">ToDate</span><span class="sxs-lookup"><span data-stu-id="2c002-125">ToDate</span></span>](todate.md) <br/> |<span data-ttu-id="2c002-126">指定收到邮件的日期。</span><span class="sxs-lookup"><span data-stu-id="2c002-126">Specifies the date that the message was received.</span></span>  <br/> |
|[<span data-ttu-id="2c002-127">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="2c002-127">MessageTypes</span></span>](messagetypes.md) <br/> |<span data-ttu-id="2c002-128">指定要搜索消息的的数组。</span><span class="sxs-lookup"><span data-stu-id="2c002-128">Specifies an array of messages to search.</span></span>  <br/> |
|[<span data-ttu-id="2c002-129">SearchDumpster</span><span class="sxs-lookup"><span data-stu-id="2c002-129">SearchDumpster</span></span>](searchdumpster.md) <br/> |<span data-ttu-id="2c002-130">指定是否在已删除项目中搜索。</span><span class="sxs-lookup"><span data-stu-id="2c002-130">Specifies whether to search in deleted items.</span></span>  <br/> |
|[<span data-ttu-id="2c002-131">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="2c002-131">IncludePersonalArchive</span></span>](includepersonalarchive.md) <br/> |<span data-ttu-id="2c002-132">指定是否在搜索中包括个人存档。</span><span class="sxs-lookup"><span data-stu-id="2c002-132">Specifies whether to include the personal archive in the search.</span></span>  <br/> |
|[<span data-ttu-id="2c002-133">IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="2c002-133">IncludeUnsearchableItems</span></span>](includeunsearchableitems.md) <br/> |<span data-ttu-id="2c002-134">指定是否包含无法搜索的项目。</span><span class="sxs-lookup"><span data-stu-id="2c002-134">Specifies whether to include items that cannot be searched.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c002-135">父元素</span><span class="sxs-lookup"><span data-stu-id="2c002-135">Parent elements</span></span>

<span data-ttu-id="2c002-136">无。</span><span class="sxs-lookup"><span data-stu-id="2c002-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c002-137">备注</span><span class="sxs-lookup"><span data-stu-id="2c002-137">Remarks</span></span>

<span data-ttu-id="2c002-138">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2c002-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c002-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="2c002-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c002-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="2c002-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2c002-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="2c002-141">Schema Name</span></span>  <br/> |<span data-ttu-id="2c002-142">消息架构</span><span class="sxs-lookup"><span data-stu-id="2c002-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="2c002-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="2c002-143">Validation File</span></span>  <br/> |<span data-ttu-id="2c002-144">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2c002-144">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2c002-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="2c002-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2c002-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c002-146">See also</span></span>



- [<span data-ttu-id="2c002-147">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2c002-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

