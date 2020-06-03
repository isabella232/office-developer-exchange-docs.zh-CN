---
title: FailedMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d4c9816-54bb-4932-b4ba-f057c9173a1a
description: FailedMailbox元素指定搜索邮箱失败的错误消息。
ms.openlocfilehash: 404084bc342eb555db61c4216e936bee6ced9c36
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461959"
---
# <a name="failedmailbox"></a><span data-ttu-id="23707-103">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="23707-103">FailedMailbox</span></span>

<span data-ttu-id="23707-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **FailedMailbox**元素指定搜索邮箱失败的错误消息。</span><span class="sxs-lookup"><span data-stu-id="23707-104">The **FailedMailbox** element specifies the error message for a mailbox that failed on search.</span></span> 
  
```XML
<FailedMailbox>
    <Mailbox/>
    <ErrorCode/>
    <ErrorMessage/>
    <IsArchive/>
</FailedMailbox>
```

 <span data-ttu-id="23707-105">**FailedSearchMailboxType**</span><span class="sxs-lookup"><span data-stu-id="23707-105">**FailedSearchMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23707-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="23707-106">Attributes and elements</span></span>

<span data-ttu-id="23707-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="23707-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23707-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="23707-108">Attributes</span></span>

<span data-ttu-id="23707-109">无。</span><span class="sxs-lookup"><span data-stu-id="23707-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23707-110">子元素</span><span class="sxs-lookup"><span data-stu-id="23707-110">Child elements</span></span>

|<span data-ttu-id="23707-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="23707-111">**Element**</span></span>|<span data-ttu-id="23707-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="23707-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23707-113">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="23707-113">Mailbox (string)</span></span>](mailbox-string.md) <br/> |<span data-ttu-id="23707-114">包含邮箱的标识符。</span><span class="sxs-lookup"><span data-stu-id="23707-114">Contains an identifier for the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="23707-115">错误代码 (int)</span><span class="sxs-lookup"><span data-stu-id="23707-115">ErrorCode (int)</span></span>](errorcode-int.md) <br/> |<span data-ttu-id="23707-116">指定的邮箱，搜索失败的错误代码。</span><span class="sxs-lookup"><span data-stu-id="23707-116">Specifies the error code of the mailbox that failed the search.</span></span>  <br/> |
|[<span data-ttu-id="23707-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="23707-117">ErrorMessage</span></span>](errormessage.md) <br/> |<span data-ttu-id="23707-118">表示为验证错误的原因。</span><span class="sxs-lookup"><span data-stu-id="23707-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="23707-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="23707-119">IsArchive</span></span>](isarchive.md) <br/> |<span data-ttu-id="23707-120">指定一个布尔值，该值指示该邮箱是否存档。</span><span class="sxs-lookup"><span data-stu-id="23707-120">Specifies a Boolean value that indicates whether the mailbox is an archive.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23707-121">父元素</span><span class="sxs-lookup"><span data-stu-id="23707-121">Parent elements</span></span>

|<span data-ttu-id="23707-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="23707-122">**Element**</span></span>|<span data-ttu-id="23707-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="23707-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23707-124">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="23707-124">FailedMailboxes</span></span>](failedmailboxes.md) <br/> |<span data-ttu-id="23707-125">指定数组的邮箱失败。</span><span class="sxs-lookup"><span data-stu-id="23707-125">Specifies an array of failed mailboxes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23707-126">备注</span><span class="sxs-lookup"><span data-stu-id="23707-126">Remarks</span></span>

<span data-ttu-id="23707-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="23707-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="23707-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="23707-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23707-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="23707-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23707-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="23707-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23707-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="23707-131">Schema Name</span></span>  <br/> |<span data-ttu-id="23707-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="23707-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="23707-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="23707-133">Validation File</span></span>  <br/> |<span data-ttu-id="23707-134">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="23707-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="23707-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="23707-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="23707-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="23707-136">See also</span></span>



- [<span data-ttu-id="23707-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="23707-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

