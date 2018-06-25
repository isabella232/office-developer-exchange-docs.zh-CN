---
title: 位置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: 位置元素指定从一条消息中提取实体的位置。
ms.openlocfilehash: 4bd8f3088891e918e13d5ef1ec8e3e5217cb3fa1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826853"
---
# <a name="position"></a><span data-ttu-id="539a5-103">位置</span><span class="sxs-lookup"><span data-stu-id="539a5-103">Position</span></span>

<span data-ttu-id="539a5-104">**位置**元素指定从一条消息中提取实体的位置。</span><span class="sxs-lookup"><span data-stu-id="539a5-104">The **Position** element specifies the position of an entity extracted from a message.</span></span> 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 <span data-ttu-id="539a5-105">**EmailPositionType**</span><span class="sxs-lookup"><span data-stu-id="539a5-105">**EmailPositionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="539a5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="539a5-106">Attributes and elements</span></span>

<span data-ttu-id="539a5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="539a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="539a5-108">属性</span><span class="sxs-lookup"><span data-stu-id="539a5-108">Attributes</span></span>

<span data-ttu-id="539a5-109">无。</span><span class="sxs-lookup"><span data-stu-id="539a5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="539a5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="539a5-110">Child elements</span></span>

<span data-ttu-id="539a5-111">无。</span><span class="sxs-lookup"><span data-stu-id="539a5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="539a5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="539a5-112">Parent elements</span></span>

<span data-ttu-id="539a5-113">[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [联系人 (ContactType)](contact-contacttype.md) | [电话 (PhoneEntityType)](phone-phoneentitytype.md)  |  [TaskSuggestion](tasksuggestion.md)</span><span class="sxs-lookup"><span data-stu-id="539a5-113">[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [Contact (ContactType)](contact-contacttype.md) | [Phone (PhoneEntityType)](phone-phoneentitytype.md) | [TaskSuggestion](tasksuggestion.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="539a5-114">文本值</span><span class="sxs-lookup"><span data-stu-id="539a5-114">Text value</span></span>

<span data-ttu-id="539a5-115">**位置**元素的文本值是已提取的实体发起源邮件中的位置。</span><span class="sxs-lookup"><span data-stu-id="539a5-115">The text value of the **Position** element is the location where an extracted entity originated in the source message.</span></span> <span data-ttu-id="539a5-116">**位置**元素的文本值是：</span><span class="sxs-lookup"><span data-stu-id="539a5-116">The text values for the **Position** element are:</span></span> 
  
- <span data-ttu-id="539a5-117">**LatestReply** -提取的不是来自邮件的最新的答复。</span><span class="sxs-lookup"><span data-stu-id="539a5-117">**LatestReply** - the extracted entity originates from the latest reply to the message.</span></span> 
    
- <span data-ttu-id="539a5-118">**其他**-提取的源自消息的未定义的一部分。</span><span class="sxs-lookup"><span data-stu-id="539a5-118">**Other** - the extracted entity originates from an undefined part of the message.</span></span> 
    
- <span data-ttu-id="539a5-119">**主题**-提取的来自在邮件主题。</span><span class="sxs-lookup"><span data-stu-id="539a5-119">**Subject** - the extracted entity originates from the message subject.</span></span> 
    
- <span data-ttu-id="539a5-120">**签名**-提取的来自邮件签名。</span><span class="sxs-lookup"><span data-stu-id="539a5-120">**Signature** - the extracted entity originates from the message signature.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="539a5-121">备注</span><span class="sxs-lookup"><span data-stu-id="539a5-121">Remarks</span></span>

<span data-ttu-id="539a5-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="539a5-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="539a5-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="539a5-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="539a5-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="539a5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="539a5-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="539a5-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="539a5-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="539a5-126">Schema name</span></span>  <br/> |<span data-ttu-id="539a5-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="539a5-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="539a5-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="539a5-128">Validation file</span></span>  <br/> |<span data-ttu-id="539a5-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="539a5-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="539a5-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="539a5-130">Can be empty</span></span>  <br/> ||
   

