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
description: IsReadReceipt 元素指示是否必须读取传入消息中的条件或例外应用的顺序的回执。
ms.openlocfilehash: 78714aafb116a609a69d77b3b4f0fd15695bda34
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826094"
---
# <a name="isreadreceipt"></a><span data-ttu-id="94911-103">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="94911-103">IsReadReceipt</span></span>

<span data-ttu-id="94911-104">**IsReadReceipt**元素指示是否必须读取传入消息中的条件或例外应用的顺序的回执。</span><span class="sxs-lookup"><span data-stu-id="94911-104">The **IsReadReceipt** element indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span> 
  
```XML
<IsReadReceipt> true | false</IsReadReceipt>
```

 <span data-ttu-id="94911-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="94911-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="94911-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="94911-106">Attributes and elements</span></span>

<span data-ttu-id="94911-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="94911-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94911-108">属性</span><span class="sxs-lookup"><span data-stu-id="94911-108">Attributes</span></span>

<span data-ttu-id="94911-109">无。</span><span class="sxs-lookup"><span data-stu-id="94911-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="94911-110">子元素</span><span class="sxs-lookup"><span data-stu-id="94911-110">Child elements</span></span>

<span data-ttu-id="94911-111">无。</span><span class="sxs-lookup"><span data-stu-id="94911-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="94911-112">父元素</span><span class="sxs-lookup"><span data-stu-id="94911-112">Parent elements</span></span>

|<span data-ttu-id="94911-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="94911-113">**Element**</span></span>|<span data-ttu-id="94911-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="94911-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94911-115">条件</span><span class="sxs-lookup"><span data-stu-id="94911-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="94911-116">表示条件，履行时, 将触发该规则的规则操作。</span><span class="sxs-lookup"><span data-stu-id="94911-116">Represents the conditions that, when fulfilled, will trigger the rule actions for that rule.</span></span>  <br/> |
|[<span data-ttu-id="94911-117">异常</span><span class="sxs-lookup"><span data-stu-id="94911-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="94911-118">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="94911-118">Represents all the available rule exception conditions for the Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="94911-119">文本值</span><span class="sxs-lookup"><span data-stu-id="94911-119">Text value</span></span>

<span data-ttu-id="94911-120">文本值为**true**指示邮件必须按条件或例外的顺序应用已读的回执。</span><span class="sxs-lookup"><span data-stu-id="94911-120">A text value of **true** indicates that the message must be a read receipt in order for the condition or exception to apply.</span></span> <span data-ttu-id="94911-121">如果邮件没有为已读的回执的条件或例外以应用，值为**false**。</span><span class="sxs-lookup"><span data-stu-id="94911-121">If the message does not have to be a read receipt for the condition or exception to apply, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94911-122">备注</span><span class="sxs-lookup"><span data-stu-id="94911-122">Remarks</span></span>

<span data-ttu-id="94911-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="94911-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94911-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="94911-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94911-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="94911-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="94911-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="94911-126">Schema Name</span></span>  <br/> |<span data-ttu-id="94911-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="94911-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="94911-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="94911-128">Validation File</span></span>  <br/> |<span data-ttu-id="94911-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="94911-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="94911-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="94911-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="94911-131">True</span><span class="sxs-lookup"><span data-stu-id="94911-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94911-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="94911-132">See also</span></span>



- [<span data-ttu-id="94911-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="94911-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

