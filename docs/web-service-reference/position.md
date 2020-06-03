---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: Position 元素指定从邮件提取的实体的位置。
ms.openlocfilehash: 9acd965c3e0c29f3fa91df338c0671749192b38b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465420"
---
# <a name="position"></a><span data-ttu-id="0b3c6-103">Position</span><span class="sxs-lookup"><span data-stu-id="0b3c6-103">Position</span></span>

<span data-ttu-id="0b3c6-104">**Position**元素指定从邮件提取的实体的位置。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-104">The **Position** element specifies the position of an entity extracted from a message.</span></span> 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 <span data-ttu-id="0b3c6-105">**EmailPositionType**</span><span class="sxs-lookup"><span data-stu-id="0b3c6-105">**EmailPositionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b3c6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0b3c6-106">Attributes and elements</span></span>

<span data-ttu-id="0b3c6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b3c6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0b3c6-108">Attributes</span></span>

<span data-ttu-id="0b3c6-109">无。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b3c6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0b3c6-110">Child elements</span></span>

<span data-ttu-id="0b3c6-111">无。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0b3c6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0b3c6-112">Parent elements</span></span>

<span data-ttu-id="0b3c6-113">[UrlEntity](urlentity.md)  | [AddressEntity](addressentity.md)  | [EmailAddressEntity](emailaddressentity.md)  | [MeetingSuggestion](meetingsuggestion.md)  | [Contact （ContactType）](contact-contacttype.md)  | [电话（PhoneEntityType）](phone-phoneentitytype.md)  | [TaskSuggestion](tasksuggestion.md)</span><span class="sxs-lookup"><span data-stu-id="0b3c6-113">[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [Contact (ContactType)](contact-contacttype.md) | [Phone (PhoneEntityType)](phone-phoneentitytype.md) | [TaskSuggestion](tasksuggestion.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0b3c6-114">文本值</span><span class="sxs-lookup"><span data-stu-id="0b3c6-114">Text value</span></span>

<span data-ttu-id="0b3c6-115">**Position**元素的文本值是提取的实体在源消息中产生的位置。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-115">The text value of the **Position** element is the location where an extracted entity originated in the source message.</span></span> <span data-ttu-id="0b3c6-116">**Position**元素的文本值为：</span><span class="sxs-lookup"><span data-stu-id="0b3c6-116">The text values for the **Position** element are:</span></span> 
  
- <span data-ttu-id="0b3c6-117">**LatestReply** -提取的实体源自最新的邮件答复。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-117">**LatestReply** - the extracted entity originates from the latest reply to the message.</span></span> 
    
- <span data-ttu-id="0b3c6-118">**其他**-提取的实体来自未定义的邮件部分。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-118">**Other** - the extracted entity originates from an undefined part of the message.</span></span> 
    
- <span data-ttu-id="0b3c6-119">**Subject** -提取的实体来自邮件主题。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-119">**Subject** - the extracted entity originates from the message subject.</span></span> 
    
- <span data-ttu-id="0b3c6-120">**签名**-提取的实体源于邮件签名。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-120">**Signature** - the extracted entity originates from the message signature.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0b3c6-121">备注</span><span class="sxs-lookup"><span data-stu-id="0b3c6-121">Remarks</span></span>

<span data-ttu-id="0b3c6-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0b3c6-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0b3c6-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b3c6-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="0b3c6-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b3c6-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="0b3c6-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0b3c6-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="0b3c6-126">Schema name</span></span>  <br/> |<span data-ttu-id="0b3c6-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="0b3c6-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="0b3c6-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="0b3c6-128">Validation file</span></span>  <br/> |<span data-ttu-id="0b3c6-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0b3c6-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0b3c6-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="0b3c6-130">Can be empty</span></span>  <br/> ||
   

