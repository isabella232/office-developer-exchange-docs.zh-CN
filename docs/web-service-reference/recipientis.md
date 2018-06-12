---
title: RecipientIs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientIs
api_type:
- schema
ms.assetid: 5d2fd7ce-6137-4b3c-a716-c0218dcc8a09
description: RecipientIs 元素指定任何收件人的电子邮件匹配的任何子值 (ProtectionRuleValueType) 元素中指定的收件人。
ms.openlocfilehash: b6d5c150cd874d1aced7f2d83ff36409e0738728
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826975"
---
# <a name="recipientis"></a><span data-ttu-id="95d42-103">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="95d42-103">RecipientIs</span></span>

<span data-ttu-id="95d42-104">**RecipientIs**元素指定任何收件人的电子邮件匹配的任何子[值 (ProtectionRuleValueType)](value-protectionrulevaluetype.md)元素中指定的收件人。</span><span class="sxs-lookup"><span data-stu-id="95d42-104">The **RecipientIs** element specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span> 
  
```xml
<RecipientIs>   <Value/></RecipientIs>
```

 <span data-ttu-id="95d42-105">**ProtectionRuleRecipientIsType**</span><span class="sxs-lookup"><span data-stu-id="95d42-105">**ProtectionRuleRecipientIsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95d42-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="95d42-106">Attributes and elements</span></span>

<span data-ttu-id="95d42-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="95d42-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95d42-108">属性</span><span class="sxs-lookup"><span data-stu-id="95d42-108">Attributes</span></span>

<span data-ttu-id="95d42-109">无。</span><span class="sxs-lookup"><span data-stu-id="95d42-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95d42-110">子元素</span><span class="sxs-lookup"><span data-stu-id="95d42-110">Child elements</span></span>

|<span data-ttu-id="95d42-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="95d42-111">**Element**</span></span>|<span data-ttu-id="95d42-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="95d42-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95d42-113">值 (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="95d42-113">Value (ProtectionRuleValueType)</span></span>](value-protectionrulevaluetype.md) <br/> |<span data-ttu-id="95d42-114">标识收件人。</span><span class="sxs-lookup"><span data-stu-id="95d42-114">Identifies a recipient.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="95d42-115">父元素</span><span class="sxs-lookup"><span data-stu-id="95d42-115">Parent elements</span></span>

|<span data-ttu-id="95d42-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="95d42-116">**Element**</span></span>|<span data-ttu-id="95d42-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="95d42-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95d42-118">条件</span><span class="sxs-lookup"><span data-stu-id="95d42-118">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="95d42-119">确定要执行该规则的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="95d42-119">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="95d42-120">和 (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="95d42-120">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="95d42-121">指示所有子元素必须都匹配计算结果为**true**。</span><span class="sxs-lookup"><span data-stu-id="95d42-121">Indicates that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95d42-122">备注</span><span class="sxs-lookup"><span data-stu-id="95d42-122">Remarks</span></span>

<span data-ttu-id="95d42-123">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="95d42-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95d42-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="95d42-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95d42-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="95d42-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95d42-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="95d42-126">Schema Name</span></span>  <br/> |<span data-ttu-id="95d42-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="95d42-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="95d42-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="95d42-128">Validation File</span></span>  <br/> |<span data-ttu-id="95d42-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="95d42-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95d42-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="95d42-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="95d42-131">False</span><span class="sxs-lookup"><span data-stu-id="95d42-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95d42-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95d42-132">See also</span></span>



- [<span data-ttu-id="95d42-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="95d42-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

