---
title: 条目 （电子邮件地址）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: b028c5c7-3494-4ecd-96d1-78783daa660f
description: Entry 元素表示联系人的单个电子邮件地址。
ms.openlocfilehash: 1852584e507c38da030815c37f85f7c4af4e2ba4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754134"
---
# <a name="entry-emailaddress"></a><span data-ttu-id="38563-103">条目 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="38563-103">Entry (EmailAddress)</span></span>

<span data-ttu-id="38563-104">**Entry**元素表示联系人的单个电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="38563-104">The **Entry** element represents a single e-mail address for a contact.</span></span> 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

<span data-ttu-id="38563-105">**EmailAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="38563-105">**EmailAddressDictionaryEntryType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="38563-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="38563-106">Attributes and elements</span></span>

<span data-ttu-id="38563-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="38563-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38563-108">属性</span><span class="sxs-lookup"><span data-stu-id="38563-108">Attributes</span></span>

|<span data-ttu-id="38563-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="38563-109">**Attribute**</span></span>|<span data-ttu-id="38563-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="38563-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38563-111">**注册表项**</span><span class="sxs-lookup"><span data-stu-id="38563-111">**Key**</span></span> <br/> | <span data-ttu-id="38563-112">标识的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="38563-112">Identifies the e-mail address.</span></span><br/><br/><span data-ttu-id="38563-113">以下是该属性可能的值：</span><span class="sxs-lookup"><span data-stu-id="38563-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="38563-114">-EmailAddress1</span><span class="sxs-lookup"><span data-stu-id="38563-114">-  EmailAddress1</span></span>  <br/><span data-ttu-id="38563-115">-EmailAddress2</span><span class="sxs-lookup"><span data-stu-id="38563-115">-  EmailAddress2</span></span>  <br/><span data-ttu-id="38563-116">-EmailAddress3</span><span class="sxs-lookup"><span data-stu-id="38563-116">-  EmailAddress3</span></span> <br/><br/>  <span data-ttu-id="38563-117">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="38563-117">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="38563-118">**名称**</span><span class="sxs-lookup"><span data-stu-id="38563-118">**Name**</span></span> <br/> |<span data-ttu-id="38563-119">定义邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="38563-119">Defines the name of the mailbox user.</span></span> <span data-ttu-id="38563-120">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="38563-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="38563-121">**RoutingType**</span><span class="sxs-lookup"><span data-stu-id="38563-121">**RoutingType**</span></span> <br/> |<span data-ttu-id="38563-122">定义用于邮箱路由。</span><span class="sxs-lookup"><span data-stu-id="38563-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="38563-123">默认值为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="38563-123">The default is SMTP.</span></span> <span data-ttu-id="38563-124">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="38563-124">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="38563-125">**MailboxType**</span><span class="sxs-lookup"><span data-stu-id="38563-125">**MailboxType**</span></span> <br/> |<span data-ttu-id="38563-126">定义邮箱用户的邮箱类型。</span><span class="sxs-lookup"><span data-stu-id="38563-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="38563-127">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="38563-127">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="38563-128">子元素</span><span class="sxs-lookup"><span data-stu-id="38563-128">Child elements</span></span>

<span data-ttu-id="38563-129">无。</span><span class="sxs-lookup"><span data-stu-id="38563-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="38563-130">父元素</span><span class="sxs-lookup"><span data-stu-id="38563-130">Parent elements</span></span>

|<span data-ttu-id="38563-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="38563-131">**Element**</span></span>|<span data-ttu-id="38563-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="38563-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38563-133">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="38563-133">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="38563-134">表示一个联系人的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="38563-134">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38563-135">备注</span><span class="sxs-lookup"><span data-stu-id="38563-135">Remarks</span></span>

<span data-ttu-id="38563-136">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="38563-136">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="38563-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="38563-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38563-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="38563-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38563-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="38563-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="38563-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="38563-140">Schema name</span></span>  <br/> |<span data-ttu-id="38563-141">类型架构</span><span class="sxs-lookup"><span data-stu-id="38563-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="38563-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="38563-142">Validation file</span></span>  <br/> |<span data-ttu-id="38563-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="38563-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="38563-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="38563-144">Can be empty</span></span>  <br/> |<span data-ttu-id="38563-145">False</span><span class="sxs-lookup"><span data-stu-id="38563-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38563-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="38563-146">See also</span></span>

- [<span data-ttu-id="38563-147">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="38563-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

