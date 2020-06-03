---
title: Value （EmailAddressType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 24eaa473-0024-47e2-b7d2-051d5dd4f53c
description: Value 元素指定与归属数组相关联的 EmailAddress 的值。
ms.openlocfilehash: 45af2aaab7d2475ae46ae24ed13b1435f5b352c6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467597"
---
# <a name="value-emailaddresstype"></a><span data-ttu-id="687ff-103">Value （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="687ff-103">Value (EmailAddressType)</span></span>

<span data-ttu-id="687ff-104">**Value**元素指定与归属数组相关联的**EmailAddress**的值。</span><span class="sxs-lookup"><span data-stu-id="687ff-104">The **Value** element specifies the value of an **EmailAddress** associated with an attributions array.</span></span> 
  
```XML
<Value>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
   <OriginalDisplayName/>
</Value>
```

<span data-ttu-id="687ff-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="687ff-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="687ff-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="687ff-106">Attributes and elements</span></span>

<span data-ttu-id="687ff-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="687ff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="687ff-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="687ff-108">Attributes</span></span>

<span data-ttu-id="687ff-109">无。</span><span class="sxs-lookup"><span data-stu-id="687ff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="687ff-110">子元素</span><span class="sxs-lookup"><span data-stu-id="687ff-110">Child elements</span></span>

<span data-ttu-id="687ff-111">[名称（字符串）](name-string.md)  | [EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)  | [RoutingType （EmailAddressType）](routingtype-emailaddresstype.md)  | [MailboxType](mailboxtype.md)  | [ItemId](itemid.md)  | [OriginalDisplayName](originaldisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="687ff-111">[Name (string)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="687ff-112">父元素</span><span class="sxs-lookup"><span data-stu-id="687ff-112">Parent elements</span></span>

[<span data-ttu-id="687ff-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="687ff-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
  
## <a name="remarks"></a><span data-ttu-id="687ff-114">备注</span><span class="sxs-lookup"><span data-stu-id="687ff-114">Remarks</span></span>

<span data-ttu-id="687ff-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="687ff-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="687ff-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="687ff-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="687ff-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="687ff-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="687ff-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="687ff-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="687ff-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="687ff-119">Schema name</span></span>  <br/> |<span data-ttu-id="687ff-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="687ff-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="687ff-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="687ff-121">Validation file</span></span>  <br/> |<span data-ttu-id="687ff-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="687ff-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="687ff-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="687ff-123">Can be empty</span></span>  <br/> |<span data-ttu-id="687ff-124">false</span><span class="sxs-lookup"><span data-stu-id="687ff-124">false</span></span>  <br/> |
   

