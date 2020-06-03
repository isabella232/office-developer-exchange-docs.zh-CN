---
title: InboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InboxRules
api_type:
- schema
ms.assetid: 7bb9896c-bd12-49ae-842a-a10b5f9a2ef6
description: InboxRules元素表示一个数组，该用户的邮箱中的规则。
ms.openlocfilehash: a3107c3c317a912d0bd3e60d03da4168f2f3a0a9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458269"
---
# <a name="inboxrules"></a><span data-ttu-id="4408d-103">InboxRules</span><span class="sxs-lookup"><span data-stu-id="4408d-103">InboxRules</span></span>

<span data-ttu-id="4408d-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **InboxRules**元素表示一个数组，该用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="4408d-104">The **InboxRules** element represents an array of rules in the user's mailbox.</span></span> 
  
[<span data-ttu-id="4408d-105">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="4408d-105">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
  
[<span data-ttu-id="4408d-106">InboxRules</span><span class="sxs-lookup"><span data-stu-id="4408d-106">InboxRules</span></span>](inboxrules.md)
  
```XML
<InboxRules>
   <Rule/>
</InboxRules>
```

 <span data-ttu-id="4408d-107">**ArrayOfRulesType**</span><span class="sxs-lookup"><span data-stu-id="4408d-107">**ArrayOfRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4408d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4408d-108">Attributes and elements</span></span>

<span data-ttu-id="4408d-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4408d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4408d-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="4408d-110">Attributes</span></span>

<span data-ttu-id="4408d-111">无。</span><span class="sxs-lookup"><span data-stu-id="4408d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4408d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="4408d-112">Child elements</span></span>

|<span data-ttu-id="4408d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4408d-113">**Element**</span></span>|<span data-ttu-id="4408d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4408d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4408d-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="4408d-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="4408d-116">包含一个规则并表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="4408d-116">Contains a single rule and represents a rule in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4408d-117">父元素</span><span class="sxs-lookup"><span data-stu-id="4408d-117">Parent elements</span></span>

|<span data-ttu-id="4408d-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="4408d-118">**Element**</span></span>|<span data-ttu-id="4408d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="4408d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4408d-120">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="4408d-120">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md) <br/> |<span data-ttu-id="4408d-121">定义一个[GetInboxRules 操作](getinboxrules-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="4408d-121">Defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4408d-122">文本值</span><span class="sxs-lookup"><span data-stu-id="4408d-122">Text value</span></span>

<span data-ttu-id="4408d-123">无。</span><span class="sxs-lookup"><span data-stu-id="4408d-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4408d-124">说明</span><span class="sxs-lookup"><span data-stu-id="4408d-124">Remarks</span></span>

<span data-ttu-id="4408d-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4408d-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4408d-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="4408d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4408d-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="4408d-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4408d-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="4408d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4408d-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="4408d-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4408d-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="4408d-130">Validation File</span></span>  <br/> |<span data-ttu-id="4408d-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4408d-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4408d-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="4408d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="4408d-133">True</span><span class="sxs-lookup"><span data-stu-id="4408d-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4408d-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4408d-134">See also</span></span>



[<span data-ttu-id="4408d-135">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="4408d-135">GetInboxRules</span></span>](getinboxrules.md)
  
[<span data-ttu-id="4408d-136">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="4408d-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)


- [<span data-ttu-id="4408d-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4408d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

