---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: FindMailboxStatisticsByKeywords 元素指定按关键字搜索邮箱统计信息的请求。
ms.openlocfilehash: e22c7d8dc849d3fd45d6cb158030cbd82119437e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462526"
---
# <a name="findmailboxstatisticsbykeywords"></a><span data-ttu-id="c4d2e-103">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="c4d2e-103">FindMailboxStatisticsByKeywords</span></span>

<span data-ttu-id="c4d2e-104">**FindMailboxStatisticsByKeywords**元素指定按关键字搜索邮箱统计信息的请求。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-104">The **FindMailboxStatisticsByKeywords** element specifies a request to search for mailbox statistics by keyword.</span></span> 
  
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

 <span data-ttu-id="c4d2e-105">**FindMailboxStatisticsByKeywordsType**</span><span class="sxs-lookup"><span data-stu-id="c4d2e-105">**FindMailboxStatisticsByKeywordsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4d2e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c4d2e-106">Attributes and elements</span></span>

<span data-ttu-id="c4d2e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4d2e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c4d2e-108">Attributes</span></span>

<span data-ttu-id="c4d2e-109">无。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4d2e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c4d2e-110">Child elements</span></span>

|<span data-ttu-id="c4d2e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c4d2e-111">**Element**</span></span>|<span data-ttu-id="c4d2e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4d2e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4d2e-113">邮箱（ArrayOfUserMailboxesType）</span><span class="sxs-lookup"><span data-stu-id="c4d2e-113">Mailboxes (ArrayOfUserMailboxesType)</span></span>](mailboxes-arrayofusermailboxestype.md) <br/> |<span data-ttu-id="c4d2e-114">包含受保留影响的邮箱数组。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-114">Contains an array of mailboxes affected by the hold.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-115">Keywords</span><span class="sxs-lookup"><span data-stu-id="c4d2e-115">Keywords</span></span>](keywords-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c4d2e-116">指定用于搜索的关键字。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-116">Specifies keywords for a search.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-117">Language</span><span class="sxs-lookup"><span data-stu-id="c4d2e-117">Language</span></span>](language.md) <br/> |<span data-ttu-id="c4d2e-118">包含用于搜索查询的语言。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-118">Contains the language used for the search query.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-119">发件人</span><span class="sxs-lookup"><span data-stu-id="c4d2e-119">Senders</span></span>](senders.md) <br/> |<span data-ttu-id="c4d2e-120">指定 SMTP 地址的数组。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-120">Specifies an array of SMTP addresses.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-121">收件人（ArrayOfSmtpAddressType）</span><span class="sxs-lookup"><span data-stu-id="c4d2e-121">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="c4d2e-122">指定邮件的收件人数组。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-122">Specifies an array of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-123">FromDate</span><span class="sxs-lookup"><span data-stu-id="c4d2e-123">FromDate</span></span>](fromdate.md) <br/> |<span data-ttu-id="c4d2e-124">指定发送邮件的日期。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-124">Specifies the date that the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-125">ToDate</span><span class="sxs-lookup"><span data-stu-id="c4d2e-125">ToDate</span></span>](todate.md) <br/> |<span data-ttu-id="c4d2e-126">指定接收邮件的日期。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-126">Specifies the date that the message was received.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-127">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="c4d2e-127">MessageTypes</span></span>](messagetypes.md) <br/> |<span data-ttu-id="c4d2e-128">指定要搜索的邮件数组。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-128">Specifies an array of messages to search.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-129">SearchDumpster</span><span class="sxs-lookup"><span data-stu-id="c4d2e-129">SearchDumpster</span></span>](searchdumpster.md) <br/> |<span data-ttu-id="c4d2e-130">指定是否在 "已删除邮件" 中搜索。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-130">Specifies whether to search in deleted items.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-131">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="c4d2e-131">IncludePersonalArchive</span></span>](includepersonalarchive.md) <br/> |<span data-ttu-id="c4d2e-132">指定是否在搜索中包含个人存档。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-132">Specifies whether to include the personal archive in the search.</span></span>  <br/> |
|[<span data-ttu-id="c4d2e-133">IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="c4d2e-133">IncludeUnsearchableItems</span></span>](includeunsearchableitems.md) <br/> |<span data-ttu-id="c4d2e-134">指定是否包括无法搜索的项目。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-134">Specifies whether to include items that cannot be searched.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4d2e-135">父元素</span><span class="sxs-lookup"><span data-stu-id="c4d2e-135">Parent elements</span></span>

<span data-ttu-id="c4d2e-136">无。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4d2e-137">说明</span><span class="sxs-lookup"><span data-stu-id="c4d2e-137">Remarks</span></span>

<span data-ttu-id="c4d2e-138">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c4d2e-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4d2e-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="c4d2e-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4d2e-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="c4d2e-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c4d2e-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="c4d2e-141">Schema Name</span></span>  <br/> |<span data-ttu-id="c4d2e-142">消息架构</span><span class="sxs-lookup"><span data-stu-id="c4d2e-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="c4d2e-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="c4d2e-143">Validation File</span></span>  <br/> |<span data-ttu-id="c4d2e-144">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="c4d2e-144">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c4d2e-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="c4d2e-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c4d2e-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4d2e-146">See also</span></span>



- [<span data-ttu-id="c4d2e-147">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c4d2e-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

