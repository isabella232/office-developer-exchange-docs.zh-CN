---
title: MessageClassifications
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageClassifications
api_type:
- schema
ms.assetid: 041b3d48-8f43-47f3-869f-72b66bef372a
description: MessageClassifications 元素表示必须在传入邮件上标记的邮件分类，以便条件或例外情况适用。
ms.openlocfilehash: 63481aa8903c4e9637870130eb9154118471c3b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467968"
---
# <a name="messageclassifications"></a><span data-ttu-id="8dba0-103">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="8dba0-103">MessageClassifications</span></span>

<span data-ttu-id="8dba0-104">**MessageClassifications**元素表示必须在传入邮件上标记的邮件分类，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="8dba0-104">The **MessageClassifications** element represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<MessageClassifications>
    <String/>
</MessageClassifications>
```

 <span data-ttu-id="8dba0-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="8dba0-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8dba0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8dba0-106">Attributes and elements</span></span>

<span data-ttu-id="8dba0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8dba0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8dba0-108">属性</span><span class="sxs-lookup"><span data-stu-id="8dba0-108">Attributes</span></span>

<span data-ttu-id="8dba0-109">无</span><span class="sxs-lookup"><span data-stu-id="8dba0-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8dba0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8dba0-110">Child elements</span></span>

|<span data-ttu-id="8dba0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8dba0-111">**Element**</span></span>|<span data-ttu-id="8dba0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8dba0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8dba0-113">字符串</span><span class="sxs-lookup"><span data-stu-id="8dba0-113">String</span></span>](string.md) <br/> |<span data-ttu-id="8dba0-114">表示邮件分类。</span><span class="sxs-lookup"><span data-stu-id="8dba0-114">Represents a message classification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8dba0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="8dba0-115">Parent elements</span></span>

|<span data-ttu-id="8dba0-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="8dba0-116">**Element**</span></span>|<span data-ttu-id="8dba0-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="8dba0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8dba0-118">条件</span><span class="sxs-lookup"><span data-stu-id="8dba0-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="8dba0-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="8dba0-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="8dba0-120">异常</span><span class="sxs-lookup"><span data-stu-id="8dba0-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="8dba0-121">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="8dba0-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8dba0-122">文本值</span><span class="sxs-lookup"><span data-stu-id="8dba0-122">Text value</span></span>

<span data-ttu-id="8dba0-123">无。</span><span class="sxs-lookup"><span data-stu-id="8dba0-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8dba0-124">说明</span><span class="sxs-lookup"><span data-stu-id="8dba0-124">Remarks</span></span>

<span data-ttu-id="8dba0-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8dba0-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8dba0-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="8dba0-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8dba0-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="8dba0-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8dba0-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="8dba0-128">Schema Name</span></span>  <br/> |<span data-ttu-id="8dba0-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="8dba0-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8dba0-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="8dba0-130">Validation File</span></span>  <br/> |<span data-ttu-id="8dba0-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8dba0-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8dba0-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="8dba0-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="8dba0-133">True</span><span class="sxs-lookup"><span data-stu-id="8dba0-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8dba0-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8dba0-134">See also</span></span>



- [<span data-ttu-id="8dba0-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8dba0-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

