---
title: SentToMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToMe
api_type:
- schema
ms.assetid: f18aecd1-ad33-41c3-b275-4ca648ce1da0
description: SentToMe 元素指示邮箱的所有者是否必须在传入邮件的 ToRecipients 属性中，以便条件或例外情况适用。
ms.openlocfilehash: 830125f03ad91a3e6f2beaf11e41be5e940ed48b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44439922"
---
# <a name="senttome"></a><span data-ttu-id="77439-103">SentToMe</span><span class="sxs-lookup"><span data-stu-id="77439-103">SentToMe</span></span>

<span data-ttu-id="77439-104">**SentToMe**元素指示邮箱的所有者是否必须在传入邮件的**ToRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="77439-104">The **SentToMe** element indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToMe>true | false</SentToMe>
```

 <span data-ttu-id="77439-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="77439-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77439-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="77439-106">Attributes and elements</span></span>

<span data-ttu-id="77439-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="77439-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77439-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="77439-108">Attributes</span></span>

<span data-ttu-id="77439-109">无。</span><span class="sxs-lookup"><span data-stu-id="77439-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77439-110">子元素</span><span class="sxs-lookup"><span data-stu-id="77439-110">Child elements</span></span>

<span data-ttu-id="77439-111">无。</span><span class="sxs-lookup"><span data-stu-id="77439-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="77439-112">父元素</span><span class="sxs-lookup"><span data-stu-id="77439-112">Parent elements</span></span>

|<span data-ttu-id="77439-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="77439-113">**Element**</span></span>|<span data-ttu-id="77439-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="77439-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77439-115">条件</span><span class="sxs-lookup"><span data-stu-id="77439-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="77439-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="77439-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="77439-117">异常</span><span class="sxs-lookup"><span data-stu-id="77439-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="77439-118">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="77439-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="77439-119">文本值</span><span class="sxs-lookup"><span data-stu-id="77439-119">Text value</span></span>

<span data-ttu-id="77439-120">如果文本值为**true** ，则表示邮箱的所有者必须位于传入邮件的**ToRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="77439-120">A text value of **true** indicates that the owner of the mailbox must be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="77439-121">如果值为**false** ，则表示邮箱的所有者不得在传入邮件的**ToRecipients**属性中，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="77439-121">A value of **false** indicates that the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="77439-122">说明</span><span class="sxs-lookup"><span data-stu-id="77439-122">Remarks</span></span>

<span data-ttu-id="77439-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="77439-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77439-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="77439-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77439-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="77439-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="77439-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="77439-126">Schema Name</span></span>  <br/> |<span data-ttu-id="77439-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="77439-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="77439-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="77439-128">Validation File</span></span>  <br/> |<span data-ttu-id="77439-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="77439-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="77439-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="77439-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="77439-131">True</span><span class="sxs-lookup"><span data-stu-id="77439-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77439-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77439-132">See also</span></span>



- [<span data-ttu-id="77439-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="77439-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

