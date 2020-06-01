---
title: MailboxType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: MailboxType 元素表示电子邮件地址所代表的邮箱的类型。
ms.openlocfilehash: 8c322ab8a87730832f5d199698a369656b058a9a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459796"
---
# <a name="mailboxtype"></a><span data-ttu-id="26fef-103">MailboxType</span><span class="sxs-lookup"><span data-stu-id="26fef-103">MailboxType</span></span>

<span data-ttu-id="26fef-104">**MailboxType**元素表示电子邮件地址所代表的邮箱的类型。</span><span class="sxs-lookup"><span data-stu-id="26fef-104">The **MailboxType** element represents the type of mailbox that is represented by the e-mail address.</span></span> 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

<span data-ttu-id="26fef-105">**MailboxTypeType**</span><span class="sxs-lookup"><span data-stu-id="26fef-105">**MailboxTypeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="26fef-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="26fef-106">Attributes and elements</span></span>

<span data-ttu-id="26fef-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="26fef-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26fef-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="26fef-108">Attributes</span></span>

<span data-ttu-id="26fef-109">无。</span><span class="sxs-lookup"><span data-stu-id="26fef-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26fef-110">子元素</span><span class="sxs-lookup"><span data-stu-id="26fef-110">Child elements</span></span>

<span data-ttu-id="26fef-111">无。</span><span class="sxs-lookup"><span data-stu-id="26fef-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26fef-112">父元素</span><span class="sxs-lookup"><span data-stu-id="26fef-112">Parent elements</span></span>

|<span data-ttu-id="26fef-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="26fef-113">**Element**</span></span>|<span data-ttu-id="26fef-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="26fef-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26fef-115">Mailbox</span><span class="sxs-lookup"><span data-stu-id="26fef-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="26fef-116">标识完全解析的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="26fef-116">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="26fef-117">RoomList</span><span class="sxs-lookup"><span data-stu-id="26fef-117">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="26fef-118">标识会议室列表。</span><span class="sxs-lookup"><span data-stu-id="26fef-118">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26fef-119">文本值</span><span class="sxs-lookup"><span data-stu-id="26fef-119">Text value</span></span>

<span data-ttu-id="26fef-120">下表列出了**MailboxType**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="26fef-120">The following table lists the possible values for the **MailboxType** element.</span></span> 
  
|<span data-ttu-id="26fef-121">**值**</span><span class="sxs-lookup"><span data-stu-id="26fef-121">**Value**</span></span>|<span data-ttu-id="26fef-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="26fef-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26fef-123">邮箱</span><span class="sxs-lookup"><span data-stu-id="26fef-123">Mailbox</span></span>  <br/> |<span data-ttu-id="26fef-124">表示启用邮件的 Active Directory 对象。</span><span class="sxs-lookup"><span data-stu-id="26fef-124">Represents a mail-enabled Active Directory object.</span></span>  <br/> |
|<span data-ttu-id="26fef-125">PublicDL</span><span class="sxs-lookup"><span data-stu-id="26fef-125">PublicDL</span></span>  <br/> |<span data-ttu-id="26fef-126">代表公共通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="26fef-126">Represents a public distribution list.</span></span>  <br/> |
|<span data-ttu-id="26fef-127">PrivateDL</span><span class="sxs-lookup"><span data-stu-id="26fef-127">PrivateDL</span></span>  <br/> |<span data-ttu-id="26fef-128">代表用户邮箱中的专用通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="26fef-128">Represents a private distribution list in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="26fef-129">Contact</span><span class="sxs-lookup"><span data-stu-id="26fef-129">Contact</span></span>  <br/> |<span data-ttu-id="26fef-130">表示用户邮箱中的联系人。</span><span class="sxs-lookup"><span data-stu-id="26fef-130">Represents a contact in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="26fef-131">Set-publicfolder</span><span class="sxs-lookup"><span data-stu-id="26fef-131">PublicFolder</span></span>  <br/> |<span data-ttu-id="26fef-132">表示公用文件夹。</span><span class="sxs-lookup"><span data-stu-id="26fef-132">Represents a public folder.</span></span>  <br/> |
|<span data-ttu-id="26fef-133">未知</span><span class="sxs-lookup"><span data-stu-id="26fef-133">Unknown</span></span>  <br/> |<span data-ttu-id="26fef-134">代表未知类型的邮箱。</span><span class="sxs-lookup"><span data-stu-id="26fef-134">Represents an unknown type of mailbox.</span></span>  <br/> |
|<span data-ttu-id="26fef-135">OneOff</span><span class="sxs-lookup"><span data-stu-id="26fef-135">OneOff</span></span>  <br/> |<span data-ttu-id="26fef-136">表示个人通讯组列表的一次性成员。</span><span class="sxs-lookup"><span data-stu-id="26fef-136">Represents a one-off member of a personal distribution list.</span></span>  <br/> |
|<span data-ttu-id="26fef-137">GroupMailbox</span><span class="sxs-lookup"><span data-stu-id="26fef-137">GroupMailbox</span></span>  <br/> |<span data-ttu-id="26fef-138">代表组邮箱。</span><span class="sxs-lookup"><span data-stu-id="26fef-138">Represents a group mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26fef-139">说明</span><span class="sxs-lookup"><span data-stu-id="26fef-139">Remarks</span></span>

<span data-ttu-id="26fef-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="26fef-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26fef-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="26fef-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26fef-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="26fef-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26fef-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="26fef-143">Schema Name</span></span>  <br/> |<span data-ttu-id="26fef-144">类型架构</span><span class="sxs-lookup"><span data-stu-id="26fef-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="26fef-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="26fef-145">Validation File</span></span>  <br/> |<span data-ttu-id="26fef-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="26fef-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="26fef-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="26fef-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="26fef-148">False</span><span class="sxs-lookup"><span data-stu-id="26fef-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26fef-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="26fef-149">See also</span></span>

- [<span data-ttu-id="26fef-150">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="26fef-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

