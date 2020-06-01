---
title: SentToOrCcMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToOrCcMe
api_type:
- schema
ms.assetid: ca43e05d-df37-485b-9276-34678025f2b7
description: SentToOrCcMe 元素指示邮箱的所有者是否必须位于传入邮件的 ToRecipients 或 CcRecipients 属性中，以便条件或例外情况适用。
ms.openlocfilehash: 906e5d9fd405b9aa6f772bcedbd1869b5023a05e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462078"
---
# <a name="senttoorccme"></a><span data-ttu-id="0cb79-103">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="0cb79-103">SentToOrCcMe</span></span>

<span data-ttu-id="0cb79-104">**SentToOrCcMe**元素指示邮箱的所有者是否必须位于传入邮件的**ToRecipients**或**CcRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="0cb79-104">The **SentToOrCcMe** element indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToOrCcMe>true | false</SentToOrCcMe>
```

 <span data-ttu-id="0cb79-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0cb79-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0cb79-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0cb79-106">Attributes and elements</span></span>

<span data-ttu-id="0cb79-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0cb79-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0cb79-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0cb79-108">Attributes</span></span>

<span data-ttu-id="0cb79-109">无。</span><span class="sxs-lookup"><span data-stu-id="0cb79-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0cb79-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0cb79-110">Child elements</span></span>

<span data-ttu-id="0cb79-111">无。</span><span class="sxs-lookup"><span data-stu-id="0cb79-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0cb79-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0cb79-112">Parent elements</span></span>

|<span data-ttu-id="0cb79-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0cb79-113">**Element**</span></span>|<span data-ttu-id="0cb79-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0cb79-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cb79-115">条件</span><span class="sxs-lookup"><span data-stu-id="0cb79-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="0cb79-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="0cb79-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="0cb79-117">异常</span><span class="sxs-lookup"><span data-stu-id="0cb79-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="0cb79-118">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="0cb79-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0cb79-119">文本值</span><span class="sxs-lookup"><span data-stu-id="0cb79-119">Text value</span></span>

<span data-ttu-id="0cb79-120">如果文本值为**true** ，则表示邮箱的所有者必须位于传入邮件的**ToRecipients**或**CcRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="0cb79-120">A text value of **true** indicates that the owner of the mailbox must be in the **ToRecipients** or **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="0cb79-121">如果值为**false** ，则表示邮箱的所有者不得在传入邮件的**ToRecipients**或**CcRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="0cb79-121">A value of **false** indicates that the owner of the mailbox must not be in the **ToRecipients** or **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0cb79-122">说明</span><span class="sxs-lookup"><span data-stu-id="0cb79-122">Remarks</span></span>

<span data-ttu-id="0cb79-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0cb79-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0cb79-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="0cb79-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cb79-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="0cb79-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0cb79-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="0cb79-126">Schema Name</span></span>  <br/> |<span data-ttu-id="0cb79-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="0cb79-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0cb79-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="0cb79-128">Validation File</span></span>  <br/> |<span data-ttu-id="0cb79-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0cb79-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0cb79-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="0cb79-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="0cb79-131">True</span><span class="sxs-lookup"><span data-stu-id="0cb79-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0cb79-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0cb79-132">See also</span></span>



- [<span data-ttu-id="0cb79-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0cb79-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

