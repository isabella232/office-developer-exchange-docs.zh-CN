---
title: 规则 Id
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
ms.openlocfilehash: 4dfa71c9fb6ee362d776487952199f2430e5e4a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827260"
---
# <a name="ruleid"></a><span data-ttu-id="6eb46-103">规则 Id</span><span class="sxs-lookup"><span data-stu-id="6eb46-103">RuleId</span></span>

<span data-ttu-id="6eb46-104">**RuleId**元素指定规则标识符。</span><span class="sxs-lookup"><span data-stu-id="6eb46-104">The **RuleId** element specifies a rule identifier.</span></span> 
  
```XML
<RuleId/>
```

 <span data-ttu-id="6eb46-105">**string**</span><span class="sxs-lookup"><span data-stu-id="6eb46-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6eb46-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6eb46-106">Attributes and elements</span></span>

<span data-ttu-id="6eb46-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6eb46-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6eb46-108">属性</span><span class="sxs-lookup"><span data-stu-id="6eb46-108">Attributes</span></span>

<span data-ttu-id="6eb46-109">无。</span><span class="sxs-lookup"><span data-stu-id="6eb46-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6eb46-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6eb46-110">Child elements</span></span>

<span data-ttu-id="6eb46-111">无。</span><span class="sxs-lookup"><span data-stu-id="6eb46-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6eb46-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6eb46-112">Parent elements</span></span>

|<span data-ttu-id="6eb46-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6eb46-113">**Element**</span></span>|<span data-ttu-id="6eb46-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6eb46-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6eb46-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="6eb46-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="6eb46-116">表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="6eb46-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6eb46-117">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="6eb46-117">DeleteRuleOperation</span></span>](deleteruleoperation.md) <br/> |<span data-ttu-id="6eb46-118">代表要删除现有的收件箱规则操作。</span><span class="sxs-lookup"><span data-stu-id="6eb46-118">Represents the operation to delete an existing Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6eb46-119">文本值</span><span class="sxs-lookup"><span data-stu-id="6eb46-119">Text value</span></span>

<span data-ttu-id="6eb46-120">文本值是一个 string 值，该值代表规则。</span><span class="sxs-lookup"><span data-stu-id="6eb46-120">The text value is a string value that represents the rule.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6eb46-121">备注</span><span class="sxs-lookup"><span data-stu-id="6eb46-121">Remarks</span></span>

<span data-ttu-id="6eb46-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6eb46-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6eb46-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="6eb46-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6eb46-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="6eb46-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6eb46-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="6eb46-125">Schema Name</span></span>  <br/> |<span data-ttu-id="6eb46-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="6eb46-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6eb46-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="6eb46-127">Validation File</span></span>  <br/> |<span data-ttu-id="6eb46-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6eb46-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6eb46-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="6eb46-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="6eb46-130">True</span><span class="sxs-lookup"><span data-stu-id="6eb46-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6eb46-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6eb46-131">See also</span></span>



- [<span data-ttu-id="6eb46-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6eb46-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

