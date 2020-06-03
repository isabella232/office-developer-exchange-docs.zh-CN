---
title: RuleId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RuleId
api_type:
- schema
ms.assetid: 456e3c34-e536-456a-ac40-7fd4f94c0bad
description: RuleId 元素指定规则标识符。
ms.openlocfilehash: 28fda7abbbbfd43be38d1ac4e5c37d37037993bc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464992"
---
# <a name="ruleid"></a><span data-ttu-id="a44eb-103">RuleId</span><span class="sxs-lookup"><span data-stu-id="a44eb-103">RuleId</span></span>

<span data-ttu-id="a44eb-104">**RuleId**元素指定规则标识符。</span><span class="sxs-lookup"><span data-stu-id="a44eb-104">The **RuleId** element specifies a rule identifier.</span></span> 
  
```XML
<RuleId/>
```

 <span data-ttu-id="a44eb-105">**string**</span><span class="sxs-lookup"><span data-stu-id="a44eb-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a44eb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a44eb-106">Attributes and elements</span></span>

<span data-ttu-id="a44eb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a44eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a44eb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a44eb-108">Attributes</span></span>

<span data-ttu-id="a44eb-109">无。</span><span class="sxs-lookup"><span data-stu-id="a44eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a44eb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a44eb-110">Child elements</span></span>

<span data-ttu-id="a44eb-111">无。</span><span class="sxs-lookup"><span data-stu-id="a44eb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a44eb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a44eb-112">Parent elements</span></span>

|<span data-ttu-id="a44eb-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a44eb-113">**Element**</span></span>|<span data-ttu-id="a44eb-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a44eb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a44eb-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="a44eb-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="a44eb-116">表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="a44eb-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a44eb-117">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="a44eb-117">DeleteRuleOperation</span></span>](deleteruleoperation.md) <br/> |<span data-ttu-id="a44eb-118">表示删除现有收件箱规则的操作。</span><span class="sxs-lookup"><span data-stu-id="a44eb-118">Represents the operation to delete an existing Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a44eb-119">文本值</span><span class="sxs-lookup"><span data-stu-id="a44eb-119">Text value</span></span>

<span data-ttu-id="a44eb-120">Text 值是表示该规则的字符串值。</span><span class="sxs-lookup"><span data-stu-id="a44eb-120">The text value is a string value that represents the rule.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a44eb-121">说明</span><span class="sxs-lookup"><span data-stu-id="a44eb-121">Remarks</span></span>

<span data-ttu-id="a44eb-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a44eb-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a44eb-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="a44eb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a44eb-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="a44eb-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a44eb-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="a44eb-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a44eb-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="a44eb-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a44eb-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="a44eb-127">Validation File</span></span>  <br/> |<span data-ttu-id="a44eb-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a44eb-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a44eb-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="a44eb-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="a44eb-130">True</span><span class="sxs-lookup"><span data-stu-id="a44eb-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a44eb-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a44eb-131">See also</span></span>



- [<span data-ttu-id="a44eb-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a44eb-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

