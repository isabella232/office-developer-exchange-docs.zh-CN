---
title: IsReadReceipt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsReadReceipt
api_type:
- schema
ms.assetid: e60e525f-c136-469a-b68b-b3dc01f400a6
description: IsReadReceipt 元素指示传入的邮件是否必须为 "已读" 回执，以便条件或例外情况适用。
ms.openlocfilehash: e86a7776bc43204dae9fc92f21d4304255ddb888
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463900"
---
# <a name="isreadreceipt"></a><span data-ttu-id="b7171-103">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="b7171-103">IsReadReceipt</span></span>

<span data-ttu-id="b7171-104">**IsReadReceipt**元素指示传入的邮件是否必须为 "已读" 回执，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="b7171-104">The **IsReadReceipt** element indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span> 
  
```XML
<IsReadReceipt> true | false</IsReadReceipt>
```

 <span data-ttu-id="b7171-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b7171-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7171-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7171-106">Attributes and elements</span></span>

<span data-ttu-id="b7171-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7171-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7171-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b7171-108">Attributes</span></span>

<span data-ttu-id="b7171-109">无。</span><span class="sxs-lookup"><span data-stu-id="b7171-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7171-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b7171-110">Child elements</span></span>

<span data-ttu-id="b7171-111">无。</span><span class="sxs-lookup"><span data-stu-id="b7171-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7171-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b7171-112">Parent elements</span></span>

|<span data-ttu-id="b7171-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7171-113">**Element**</span></span>|<span data-ttu-id="b7171-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7171-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7171-115">条件</span><span class="sxs-lookup"><span data-stu-id="b7171-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="b7171-116">表示条件，履行时, 将触发该规则的规则操作。</span><span class="sxs-lookup"><span data-stu-id="b7171-116">Represents the conditions that, when fulfilled, will trigger the rule actions for that rule.</span></span>  <br/> |
|[<span data-ttu-id="b7171-117">异常</span><span class="sxs-lookup"><span data-stu-id="b7171-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="b7171-118">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="b7171-118">Represents all the available rule exception conditions for the Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b7171-119">文本值</span><span class="sxs-lookup"><span data-stu-id="b7171-119">Text value</span></span>

<span data-ttu-id="b7171-120">如果文本值为**true** ，则表示邮件必须为已读回执，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="b7171-120">A text value of **true** indicates that the message must be a read receipt in order for the condition or exception to apply.</span></span> <span data-ttu-id="b7171-121">如果该邮件不一定是要应用的条件或例外的已读回执，则该值为**false**。</span><span class="sxs-lookup"><span data-stu-id="b7171-121">If the message does not have to be a read receipt for the condition or exception to apply, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7171-122">说明</span><span class="sxs-lookup"><span data-stu-id="b7171-122">Remarks</span></span>

<span data-ttu-id="b7171-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b7171-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7171-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7171-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7171-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7171-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7171-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7171-126">Schema Name</span></span>  <br/> |<span data-ttu-id="b7171-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="b7171-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b7171-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7171-128">Validation File</span></span>  <br/> |<span data-ttu-id="b7171-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b7171-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7171-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7171-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="b7171-131">True</span><span class="sxs-lookup"><span data-stu-id="b7171-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7171-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7171-132">See also</span></span>



- [<span data-ttu-id="b7171-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b7171-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

