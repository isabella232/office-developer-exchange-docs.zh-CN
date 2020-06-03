---
title: 收件人是
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
description: 收件人是元素指定电子邮件的任何收件人与子值（ProtectionRuleValueType）元素中的任何指定收件人相匹配。
ms.openlocfilehash: 8f27c4484ce310c62f9bab0e6ffeea2bfac1d3ef
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463879"
---
# <a name="recipientis"></a><span data-ttu-id="df321-103">收件人是</span><span class="sxs-lookup"><span data-stu-id="df321-103">RecipientIs</span></span>

<span data-ttu-id="df321-104">**收件人是**元素指定电子邮件的任何收件人与子[值（ProtectionRuleValueType）](value-protectionrulevaluetype.md)元素中的任何指定收件人相匹配。</span><span class="sxs-lookup"><span data-stu-id="df321-104">The **RecipientIs** element specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span> 
  
```xml
<RecipientIs>   <Value/></RecipientIs>
```

 <span data-ttu-id="df321-105">**ProtectionRuleRecipientIsType**</span><span class="sxs-lookup"><span data-stu-id="df321-105">**ProtectionRuleRecipientIsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df321-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="df321-106">Attributes and elements</span></span>

<span data-ttu-id="df321-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="df321-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df321-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="df321-108">Attributes</span></span>

<span data-ttu-id="df321-109">无。</span><span class="sxs-lookup"><span data-stu-id="df321-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="df321-110">子元素</span><span class="sxs-lookup"><span data-stu-id="df321-110">Child elements</span></span>

|<span data-ttu-id="df321-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="df321-111">**Element**</span></span>|<span data-ttu-id="df321-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="df321-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df321-113">Value （ProtectionRuleValueType）</span><span class="sxs-lookup"><span data-stu-id="df321-113">Value (ProtectionRuleValueType)</span></span>](value-protectionrulevaluetype.md) <br/> |<span data-ttu-id="df321-114">标识收件人。</span><span class="sxs-lookup"><span data-stu-id="df321-114">Identifies a recipient.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="df321-115">父元素</span><span class="sxs-lookup"><span data-stu-id="df321-115">Parent elements</span></span>

|<span data-ttu-id="df321-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="df321-116">**Element**</span></span>|<span data-ttu-id="df321-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="df321-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df321-118">条件</span><span class="sxs-lookup"><span data-stu-id="df321-118">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="df321-119">确定要执行该规则的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="df321-119">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="df321-120">和 (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="df321-120">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="df321-121">指示所有子元素都必须匹配以求值为**true**。</span><span class="sxs-lookup"><span data-stu-id="df321-121">Indicates that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df321-122">备注</span><span class="sxs-lookup"><span data-stu-id="df321-122">Remarks</span></span>

<span data-ttu-id="df321-123">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="df321-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df321-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="df321-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df321-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="df321-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="df321-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="df321-126">Schema Name</span></span>  <br/> |<span data-ttu-id="df321-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="df321-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="df321-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="df321-128">Validation File</span></span>  <br/> |<span data-ttu-id="df321-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="df321-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="df321-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="df321-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="df321-131">False</span><span class="sxs-lookup"><span data-stu-id="df321-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df321-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="df321-132">See also</span></span>



- [<span data-ttu-id="df321-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="df321-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

