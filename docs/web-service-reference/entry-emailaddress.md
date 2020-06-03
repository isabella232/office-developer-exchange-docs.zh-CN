---
title: 条目（EmailAddress）
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
ms.openlocfilehash: 766d67cda10b02c07a7677e541fddfc38a4285cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459642"
---
# <a name="entry-emailaddress"></a><span data-ttu-id="defac-103">条目（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="defac-103">Entry (EmailAddress)</span></span>

<span data-ttu-id="defac-104">**Entry**元素表示联系人的单个电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="defac-104">The **Entry** element represents a single e-mail address for a contact.</span></span> 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

<span data-ttu-id="defac-105">**EmailAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="defac-105">**EmailAddressDictionaryEntryType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="defac-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="defac-106">Attributes and elements</span></span>

<span data-ttu-id="defac-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="defac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="defac-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="defac-108">Attributes</span></span>

|<span data-ttu-id="defac-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="defac-109">**Attribute**</span></span>|<span data-ttu-id="defac-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="defac-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="defac-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="defac-111">**Key**</span></span> <br/> | <span data-ttu-id="defac-112">标识电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="defac-112">Identifies the e-mail address.</span></span><br/><br/><span data-ttu-id="defac-113">以下是该属性可能的值：</span><span class="sxs-lookup"><span data-stu-id="defac-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="defac-114">- EmailAddress1</span><span class="sxs-lookup"><span data-stu-id="defac-114">-  EmailAddress1</span></span>  <br/><span data-ttu-id="defac-115">- EmailAddress2</span><span class="sxs-lookup"><span data-stu-id="defac-115">-  EmailAddress2</span></span>  <br/><span data-ttu-id="defac-116">- EmailAddress3</span><span class="sxs-lookup"><span data-stu-id="defac-116">-  EmailAddress3</span></span> <br/><br/>  <span data-ttu-id="defac-117">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="defac-117">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="defac-118">**名称**</span><span class="sxs-lookup"><span data-stu-id="defac-118">**Name**</span></span> <br/> |<span data-ttu-id="defac-119">定义邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="defac-119">Defines the name of the mailbox user.</span></span> <span data-ttu-id="defac-120">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="defac-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="defac-121">**RoutingType**</span><span class="sxs-lookup"><span data-stu-id="defac-121">**RoutingType**</span></span> <br/> |<span data-ttu-id="defac-122">定义供邮箱使用的路由。</span><span class="sxs-lookup"><span data-stu-id="defac-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="defac-123">默认为 SMTP。</span><span class="sxs-lookup"><span data-stu-id="defac-123">The default is SMTP.</span></span> <span data-ttu-id="defac-124">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="defac-124">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="defac-125">**MailboxType**</span><span class="sxs-lookup"><span data-stu-id="defac-125">**MailboxType**</span></span> <br/> |<span data-ttu-id="defac-126">定义邮箱用户的类型。</span><span class="sxs-lookup"><span data-stu-id="defac-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="defac-127">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="defac-127">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="defac-128">子元素</span><span class="sxs-lookup"><span data-stu-id="defac-128">Child elements</span></span>

<span data-ttu-id="defac-129">无。</span><span class="sxs-lookup"><span data-stu-id="defac-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="defac-130">父元素</span><span class="sxs-lookup"><span data-stu-id="defac-130">Parent elements</span></span>

|<span data-ttu-id="defac-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="defac-131">**Element**</span></span>|<span data-ttu-id="defac-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="defac-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="defac-133">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="defac-133">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="defac-134">表示联系人的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="defac-134">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="defac-135">备注</span><span class="sxs-lookup"><span data-stu-id="defac-135">Remarks</span></span>

<span data-ttu-id="defac-136">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="defac-136">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="defac-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="defac-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="defac-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="defac-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="defac-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="defac-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="defac-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="defac-140">Schema name</span></span>  <br/> |<span data-ttu-id="defac-141">类型架构</span><span class="sxs-lookup"><span data-stu-id="defac-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="defac-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="defac-142">Validation file</span></span>  <br/> |<span data-ttu-id="defac-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="defac-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="defac-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="defac-144">Can be empty</span></span>  <br/> |<span data-ttu-id="defac-145">False</span><span class="sxs-lookup"><span data-stu-id="defac-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="defac-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="defac-146">See also</span></span>

- [<span data-ttu-id="defac-147">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="defac-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

