---
title: EmailAddress (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: EmailAddress 元素定义邮箱用户的主 SMTP 地址。
ms.openlocfilehash: fcc3e650d5fc32344022ed6f015d4096a4461f63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463130"
---
# <a name="emailaddress-nonemptystringtype"></a><span data-ttu-id="6bc8b-103">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-103">EmailAddress (NonEmptyStringType)</span></span>

<span data-ttu-id="6bc8b-104">**EmailAddress**元素定义邮箱用户的主 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-104">The **EmailAddress** element defines the primary SMTP address of a mailbox user.</span></span> 
  
```XML
<EmailAddress/>
```

 <span data-ttu-id="6bc8b-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="6bc8b-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6bc8b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6bc8b-106">Attributes and elements</span></span>

<span data-ttu-id="6bc8b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6bc8b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6bc8b-108">Attributes</span></span>

<span data-ttu-id="6bc8b-109">无。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6bc8b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6bc8b-110">Child elements</span></span>

<span data-ttu-id="6bc8b-111">无。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6bc8b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6bc8b-112">Parent elements</span></span>

|<span data-ttu-id="6bc8b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6bc8b-113">**Element**</span></span>|<span data-ttu-id="6bc8b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6bc8b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6bc8b-115">ActingAs</span><span class="sxs-lookup"><span data-stu-id="6bc8b-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="6bc8b-116">标识呼叫者发送的人。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="6bc8b-117">邮箱</span><span class="sxs-lookup"><span data-stu-id="6bc8b-117">Mailbox</span></span>](mailbox.md) <br/> | <span data-ttu-id="6bc8b-118">标识完全解析的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-118">Identifies a fully resolved e-mail address.</span></span>  <br/><br/><span data-ttu-id="6bc8b-119">以下是此元素的一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="6bc8b-119">The following are some XPath expressions to this element:</span></span><br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/><span data-ttu-id="6bc8b-120">以下是邮箱元素的其他父元素：</span><span class="sxs-lookup"><span data-stu-id="6bc8b-120">The following are additional parent elements of the Mailbox element:</span></span><br/><br/><span data-ttu-id="6bc8b-121">- [BccRecipients](bccrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-121">- [BccRecipients](bccrecipients.md)</span></span> <br/><span data-ttu-id="6bc8b-122">- [ReplyTo](replyto.md)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-122">- [ReplyTo](replyto.md)</span></span> <br/><span data-ttu-id="6bc8b-123">- [给](sender.md)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-123">- [Sender](sender.md)</span></span> <br/><span data-ttu-id="6bc8b-124">- [从](from.md)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-124">- [From](from.md)</span></span> <br/><span data-ttu-id="6bc8b-125">- [组织者](organizer.md)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-125">- [Organizer](organizer.md)</span></span> <br/><span data-ttu-id="6bc8b-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span></span> <br/><span data-ttu-id="6bc8b-127">- [办法](resolution.md)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-127">- [Resolution](resolution.md)</span></span> <br/><span data-ttu-id="6bc8b-128">- [DLExpansion](dlexpansion.md)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-128">- [DLExpansion](dlexpansion.md)</span></span> <br/><span data-ttu-id="6bc8b-129">- [与会](attendee.md)</span><span class="sxs-lookup"><span data-stu-id="6bc8b-129">- [Attendee](attendee.md)</span></span> <br/> |
|[<span data-ttu-id="6bc8b-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="6bc8b-130">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="6bc8b-131">通过电子邮件地址标识会议室列表。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-131">Identifies a list of meeting rooms by email address.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6bc8b-132">文本值</span><span class="sxs-lookup"><span data-stu-id="6bc8b-132">Text value</span></span>

<span data-ttu-id="6bc8b-133">需要一个代表 SMTP 地址的文本值。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-133">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6bc8b-134">备注</span><span class="sxs-lookup"><span data-stu-id="6bc8b-134">Remarks</span></span>

<span data-ttu-id="6bc8b-135">**EmailAddress**元素可以表示 SMTP 或旧版 Exchange 可分辨名称（也称为 DN）地址。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-135">The **EmailAddress** element can represent SMTP or legacy Exchange distinguished name (also known as DN) addresses.</span></span> <span data-ttu-id="6bc8b-136">**EmailAddress**元素是唯一一个必需的[邮箱](mailbox.md)元素。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-136">The **EmailAddress** element is the only required [Mailbox](mailbox.md) element.</span></span> 
  
<span data-ttu-id="6bc8b-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6bc8b-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6bc8b-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="6bc8b-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6bc8b-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="6bc8b-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6bc8b-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="6bc8b-140">Schema Name</span></span>  <br/> |<span data-ttu-id="6bc8b-141">类型架构</span><span class="sxs-lookup"><span data-stu-id="6bc8b-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="6bc8b-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="6bc8b-142">Validation File</span></span>  <br/> |<span data-ttu-id="6bc8b-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6bc8b-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6bc8b-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="6bc8b-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="6bc8b-145">False</span><span class="sxs-lookup"><span data-stu-id="6bc8b-145">False</span></span>  <br/> |
   

