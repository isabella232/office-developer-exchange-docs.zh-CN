---
title: IsInError
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsInError
api_type:
- schema
ms.assetid: f56e6c31-a566-4761-8755-d90ffe6fe790
description: IsInError元素指示该规则是否处于出错状态。
ms.openlocfilehash: 9e642c9f89434bdcad97b0c16dc35f99196051d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464215"
---
# <a name="isinerror"></a><span data-ttu-id="f3299-103">IsInError</span><span class="sxs-lookup"><span data-stu-id="f3299-103">IsInError</span></span>

<span data-ttu-id="f3299-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **IsInError**元素指示该规则是否处于出错状态。</span><span class="sxs-lookup"><span data-stu-id="f3299-104">The **IsInError** element indicates whether the rule is in an error condition.</span></span> 
  
```XML
<IsInError/>
```

 <span data-ttu-id="f3299-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3299-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f3299-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f3299-106">Attributes and elements</span></span>

<span data-ttu-id="f3299-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f3299-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3299-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f3299-108">Attributes</span></span>

<span data-ttu-id="f3299-109">无。</span><span class="sxs-lookup"><span data-stu-id="f3299-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3299-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f3299-110">Child elements</span></span>

<span data-ttu-id="f3299-111">无。</span><span class="sxs-lookup"><span data-stu-id="f3299-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f3299-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f3299-112">Parent elements</span></span>

|<span data-ttu-id="f3299-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f3299-113">**Element**</span></span>|<span data-ttu-id="f3299-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3299-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3299-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="f3299-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="f3299-116">表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="f3299-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f3299-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f3299-117">Text value</span></span>

<span data-ttu-id="f3299-p101">文本值 **true**表示规则是在错误条件。 **false**表示规则不处于错误状态。</span><span class="sxs-lookup"><span data-stu-id="f3299-p101">A text value of **true** indicates that the rule is in an error condition. A value of **false** indicates that the rule is not in an error condition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f3299-120">说明</span><span class="sxs-lookup"><span data-stu-id="f3299-120">Remarks</span></span>

<span data-ttu-id="f3299-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f3299-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3299-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="f3299-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3299-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="f3299-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f3299-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="f3299-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f3299-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="f3299-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f3299-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="f3299-126">Validation File</span></span>  <br/> |<span data-ttu-id="f3299-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f3299-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f3299-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="f3299-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f3299-129">True</span><span class="sxs-lookup"><span data-stu-id="f3299-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3299-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f3299-130">See also</span></span>



- [<span data-ttu-id="f3299-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f3299-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

