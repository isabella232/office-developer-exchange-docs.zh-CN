---
title: MailboxHoldStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92608b77-8aa4-403b-a4de-01e3a60af3e0
description: MailboxHoldStatus 元素指定邮箱的保留状态。
ms.openlocfilehash: 6703c909d0a7b4e83e190807fc3202ecd4699e7f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826288"
---
# <a name="mailboxholdstatus"></a><span data-ttu-id="7d8e0-103">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="7d8e0-103">MailboxHoldStatus</span></span>

<span data-ttu-id="7d8e0-104">**MailboxHoldStatus**元素指定邮箱的保留状态。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-104">The **MailboxHoldStatus** element specifies the hold status of the mailbox.</span></span> 
  
```XML
<MailboxHoldStatus>
   <Mailbox/>
   <Status/>
   <AdditionalInfo/>
</MailboxHoldStatus>
```

<span data-ttu-id="7d8e0-105">**MailboxHoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="7d8e0-105">**MailboxHoldStatusType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7d8e0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7d8e0-106">Attributes and elements</span></span>

<span data-ttu-id="7d8e0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d8e0-108">属性</span><span class="sxs-lookup"><span data-stu-id="7d8e0-108">Attributes</span></span>

<span data-ttu-id="7d8e0-109">无。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7d8e0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7d8e0-110">Child elements</span></span>

<span data-ttu-id="7d8e0-111">[邮箱 （字符串）](mailbox-string.md) | [状态 (HoldStatusType)](status-holdstatustype.md) | [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="7d8e0-111">[Mailbox (string)](mailbox-string.md) | [Status (HoldStatusType)](status-holdstatustype.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7d8e0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7d8e0-112">Parent elements</span></span>

[<span data-ttu-id="7d8e0-113">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="7d8e0-113">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
  
## <a name="remarks"></a><span data-ttu-id="7d8e0-114">备注</span><span class="sxs-lookup"><span data-stu-id="7d8e0-114">Remarks</span></span>

<span data-ttu-id="7d8e0-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7d8e0-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d8e0-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="7d8e0-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d8e0-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="7d8e0-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7d8e0-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="7d8e0-119">Schema name</span></span>  <br/> |<span data-ttu-id="7d8e0-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="7d8e0-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="7d8e0-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="7d8e0-121">Validation file</span></span>  <br/> |<span data-ttu-id="7d8e0-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7d8e0-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7d8e0-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="7d8e0-123">Can be empty</span></span>  <br/> ||
   

