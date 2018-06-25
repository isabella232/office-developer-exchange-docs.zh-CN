---
title: 值 (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 24eaa473-0024-47e2-b7d2-051d5dd4f53c
description: Value 元素指定的值的数组归属相关联的电子邮件地址。
ms.openlocfilehash: 097444d90e98e73b9e83912274ecf87249008116
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838509"
---
# <a name="value-emailaddresstype"></a><span data-ttu-id="4e46a-103">值 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="4e46a-103">Value (EmailAddressType)</span></span>

<span data-ttu-id="4e46a-104">**Value**元素指定与归属数组关联的**电子邮件地址**的值。</span><span class="sxs-lookup"><span data-stu-id="4e46a-104">The **Value** element specifies the value of an **EmailAddress** associated with an attributions array.</span></span> 
  
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

<span data-ttu-id="4e46a-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="4e46a-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4e46a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4e46a-106">Attributes and elements</span></span>

<span data-ttu-id="4e46a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4e46a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e46a-108">属性</span><span class="sxs-lookup"><span data-stu-id="4e46a-108">Attributes</span></span>

<span data-ttu-id="4e46a-109">无。</span><span class="sxs-lookup"><span data-stu-id="4e46a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e46a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4e46a-110">Child elements</span></span>

<span data-ttu-id="4e46a-111">[名称 （字符串）](name-string.md) | [电子邮件地址 (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="4e46a-111">[Name (string)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4e46a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4e46a-112">Parent elements</span></span>

[<span data-ttu-id="4e46a-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="4e46a-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
  
## <a name="remarks"></a><span data-ttu-id="4e46a-114">备注</span><span class="sxs-lookup"><span data-stu-id="4e46a-114">Remarks</span></span>

<span data-ttu-id="4e46a-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4e46a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4e46a-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4e46a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e46a-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="4e46a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e46a-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="4e46a-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e46a-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="4e46a-119">Schema name</span></span>  <br/> |<span data-ttu-id="4e46a-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="4e46a-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e46a-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="4e46a-121">Validation file</span></span>  <br/> |<span data-ttu-id="4e46a-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e46a-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e46a-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="4e46a-123">Can be empty</span></span>  <br/> |<span data-ttu-id="4e46a-124">false</span><span class="sxs-lookup"><span data-stu-id="4e46a-124">false</span></span>  <br/> |
   

