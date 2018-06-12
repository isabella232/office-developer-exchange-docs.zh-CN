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
description: EmailAddress 元素定义邮箱用户的主 SMTP 的地址。
ms.openlocfilehash: fcf2839c1e2e40a22d6b6a856608f52f2c9c2a1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754049"
---
# <a name="emailaddress-nonemptystringtype"></a><span data-ttu-id="214d1-103">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="214d1-103">EmailAddress (NonEmptyStringType)</span></span>

<span data-ttu-id="214d1-104">**EmailAddress**元素定义邮箱用户的主 SMTP 的地址。</span><span class="sxs-lookup"><span data-stu-id="214d1-104">The **EmailAddress** element defines the primary SMTP address of a mailbox user.</span></span> 
  
```XML
<EmailAddress/>
```

 <span data-ttu-id="214d1-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="214d1-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="214d1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="214d1-106">Attributes and elements</span></span>

<span data-ttu-id="214d1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="214d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="214d1-108">属性</span><span class="sxs-lookup"><span data-stu-id="214d1-108">Attributes</span></span>

<span data-ttu-id="214d1-109">无。</span><span class="sxs-lookup"><span data-stu-id="214d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="214d1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="214d1-110">Child elements</span></span>

<span data-ttu-id="214d1-111">无。</span><span class="sxs-lookup"><span data-stu-id="214d1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="214d1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="214d1-112">Parent elements</span></span>

|<span data-ttu-id="214d1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="214d1-113">**Element**</span></span>|<span data-ttu-id="214d1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="214d1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="214d1-115">ActingAs</span><span class="sxs-lookup"><span data-stu-id="214d1-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="214d1-116">标识用户呼叫者发送为。</span><span class="sxs-lookup"><span data-stu-id="214d1-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="214d1-117">Mailbox</span><span class="sxs-lookup"><span data-stu-id="214d1-117">Mailbox</span></span>](mailbox.md) <br/> | <span data-ttu-id="214d1-118">标识完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="214d1-118">Identifies a fully resolved e-mail address.</span></span>  <br/><br/><span data-ttu-id="214d1-119">以下是此元素一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="214d1-119">The following are some XPath expressions to this element:</span></span><br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/><span data-ttu-id="214d1-120">邮箱元素的其他父元素如下：</span><span class="sxs-lookup"><span data-stu-id="214d1-120">The following are additional parent elements of the Mailbox element:</span></span><br/><br/><span data-ttu-id="214d1-121">- [BccRecipients](bccrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="214d1-121">- [BccRecipients](bccrecipients.md)</span></span> <br/><span data-ttu-id="214d1-122">- [回复](replyto.md)</span><span class="sxs-lookup"><span data-stu-id="214d1-122">- [ReplyTo](replyto.md)</span></span> <br/><span data-ttu-id="214d1-123">- [发件人](sender.md)</span><span class="sxs-lookup"><span data-stu-id="214d1-123">- [Sender](sender.md)</span></span> <br/><span data-ttu-id="214d1-124">- [从](from.md)</span><span class="sxs-lookup"><span data-stu-id="214d1-124">- [From](from.md)</span></span> <br/><span data-ttu-id="214d1-125">- [组织者](organizer.md)</span><span class="sxs-lookup"><span data-stu-id="214d1-125">- [Organizer](organizer.md)</span></span> <br/><span data-ttu-id="214d1-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="214d1-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span></span> <br/><span data-ttu-id="214d1-127">- [解决方案](resolution.md)</span><span class="sxs-lookup"><span data-stu-id="214d1-127">- [Resolution](resolution.md)</span></span> <br/><span data-ttu-id="214d1-128">- [DLExpansion](dlexpansion.md)</span><span class="sxs-lookup"><span data-stu-id="214d1-128">- [DLExpansion](dlexpansion.md)</span></span> <br/><span data-ttu-id="214d1-129">- [与会者](attendee.md)</span><span class="sxs-lookup"><span data-stu-id="214d1-129">- [Attendee](attendee.md)</span></span> <br/> |
|[<span data-ttu-id="214d1-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="214d1-130">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="214d1-131">标识会议室按电子邮件地址的列表。</span><span class="sxs-lookup"><span data-stu-id="214d1-131">Identifies a list of meeting rooms by email address.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="214d1-132">文本值</span><span class="sxs-lookup"><span data-stu-id="214d1-132">Text value</span></span>

<span data-ttu-id="214d1-133">需要安装一个代表 SMTP 地址的文本值。</span><span class="sxs-lookup"><span data-stu-id="214d1-133">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="214d1-134">备注</span><span class="sxs-lookup"><span data-stu-id="214d1-134">Remarks</span></span>

<span data-ttu-id="214d1-135">**EmailAddress**元素可以表示 SMTP 或旧版 Exchange 可分辨名称 (也称为 DN) 地址。</span><span class="sxs-lookup"><span data-stu-id="214d1-135">The **EmailAddress** element can represent SMTP or legacy Exchange distinguished name (also known as DN) addresses.</span></span> <span data-ttu-id="214d1-136">**EmailAddress**元素是唯一的必需的[邮箱](mailbox.md)元素。</span><span class="sxs-lookup"><span data-stu-id="214d1-136">The **EmailAddress** element is the only required [Mailbox](mailbox.md) element.</span></span> 
  
<span data-ttu-id="214d1-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="214d1-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="214d1-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="214d1-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="214d1-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="214d1-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="214d1-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="214d1-140">Schema Name</span></span>  <br/> |<span data-ttu-id="214d1-141">类型架构</span><span class="sxs-lookup"><span data-stu-id="214d1-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="214d1-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="214d1-142">Validation File</span></span>  <br/> |<span data-ttu-id="214d1-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="214d1-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="214d1-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="214d1-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="214d1-145">False</span><span class="sxs-lookup"><span data-stu-id="214d1-145">False</span></span>  <br/> |
   
