---
title: UserMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1d47141c-3c3f-45b8-90c5-33a44adb34b2
description: UserMailbox元素标识用户邮箱。
ms.openlocfilehash: 9bb1b08320f5e6f4843383a8e3aff96fc3dcccad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465315"
---
# <a name="usermailbox"></a><span data-ttu-id="1beac-103">UserMailbox</span><span class="sxs-lookup"><span data-stu-id="1beac-103">UserMailbox</span></span>

<span data-ttu-id="1beac-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **UserMailbox**元素标识用户邮箱。</span><span class="sxs-lookup"><span data-stu-id="1beac-104">The **UserMailbox** element identifies a user mailbox.</span></span> 
  
```XML
<UserMailbox Id="" IsArchive=""/>
```

 <span data-ttu-id="1beac-105">**UserMailboxType**</span><span class="sxs-lookup"><span data-stu-id="1beac-105">**UserMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1beac-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1beac-106">Attributes and elements</span></span>

<span data-ttu-id="1beac-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1beac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1beac-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1beac-108">Attributes</span></span>

|<span data-ttu-id="1beac-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="1beac-109">**Attribute**</span></span>|<span data-ttu-id="1beac-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="1beac-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1beac-111">Id</span><span class="sxs-lookup"><span data-stu-id="1beac-111">Id</span></span>  <br/> |<span data-ttu-id="1beac-112">**Id**属性的文本值是邮箱的标识符。</span><span class="sxs-lookup"><span data-stu-id="1beac-112">The text value of the **Id** attribute is the identifier of the mailbox.</span></span>  <br/> |
|<span data-ttu-id="1beac-113">IsArchive</span><span class="sxs-lookup"><span data-stu-id="1beac-113">IsArchive</span></span>  <br/> |<span data-ttu-id="1beac-p101">**IsArchive**属性的文本值指示该邮箱是否存档邮箱。 **true** **IsArchive**属性的文本值表示邮箱存档邮箱。 **false** **IsArchive**属性的值表示邮箱是一个主邮箱。 </span><span class="sxs-lookup"><span data-stu-id="1beac-p101">The text value of the **IsArchive** attribute indicates whether the mailbox is an archive mailbox. A text value of **true** for the **IsArchive** attribute indicates that the mailbox is an archive mailbox. A value of **false** for the **IsArchive** attribute indicates that the mailbox is a primary mailbox.  </span></span><br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1beac-117">子元素</span><span class="sxs-lookup"><span data-stu-id="1beac-117">Child elements</span></span>

<span data-ttu-id="1beac-118">无。</span><span class="sxs-lookup"><span data-stu-id="1beac-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1beac-119">父元素</span><span class="sxs-lookup"><span data-stu-id="1beac-119">Parent elements</span></span>

<span data-ttu-id="1beac-120">[邮箱 (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span><span class="sxs-lookup"><span data-stu-id="1beac-120">[Mailboxes (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1beac-121">备注</span><span class="sxs-lookup"><span data-stu-id="1beac-121">Remarks</span></span>

<span data-ttu-id="1beac-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1beac-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1beac-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1beac-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1beac-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="1beac-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1beac-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="1beac-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1beac-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="1beac-126">Schema name</span></span>  <br/> |<span data-ttu-id="1beac-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="1beac-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="1beac-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="1beac-128">Validation file</span></span>  <br/> |<span data-ttu-id="1beac-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1beac-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1beac-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="1beac-130">Can be empty</span></span>  <br/> |<span data-ttu-id="1beac-131">True</span><span class="sxs-lookup"><span data-stu-id="1beac-131">true</span></span>  <br/> |
   

