---
title: IsNotSupported
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNotSupported
api_type:
- schema
ms.assetid: 4db469ae-1515-47ea-9905-6aabf199febd
description: IsNotSupported 元素指示是否不能使用托管代码 Api 修改规则。
ms.openlocfilehash: e2d0c506209978fd5e8702e0de6cddf2e9c4b7fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465833"
---
# <a name="isnotsupported"></a><span data-ttu-id="cac2e-103">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="cac2e-103">IsNotSupported</span></span>

<span data-ttu-id="cac2e-104">**IsNotSupported**元素指示是否不能使用托管代码 api 修改规则。</span><span class="sxs-lookup"><span data-stu-id="cac2e-104">The **IsNotSupported** element indicates whether the rule cannot be modified by using the managed code APIs.</span></span> 
  
```XML
<IsNotSupported/>
```

 <span data-ttu-id="cac2e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cac2e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cac2e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cac2e-106">Attributes and elements</span></span>

<span data-ttu-id="cac2e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cac2e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cac2e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cac2e-108">Attributes</span></span>

<span data-ttu-id="cac2e-109">无。</span><span class="sxs-lookup"><span data-stu-id="cac2e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cac2e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cac2e-110">Child elements</span></span>

<span data-ttu-id="cac2e-111">无。</span><span class="sxs-lookup"><span data-stu-id="cac2e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cac2e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cac2e-112">Parent elements</span></span>

|<span data-ttu-id="cac2e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cac2e-113">**Element**</span></span>|<span data-ttu-id="cac2e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cac2e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cac2e-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="cac2e-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="cac2e-116">表示用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="cac2e-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cac2e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="cac2e-117">Text value</span></span>

<span data-ttu-id="cac2e-118">如果文本值为**true** ，则表示无法使用托管代码 api 修改规则。</span><span class="sxs-lookup"><span data-stu-id="cac2e-118">A text value of **true** indicates that the rule cannot be modified by using the managed code APIs.</span></span> <span data-ttu-id="cac2e-119">**如果值为 false** ，则表示可以使用托管代码 api 修改规则。</span><span class="sxs-lookup"><span data-stu-id="cac2e-119">A value of **false** indicates that the rule can be modified by using the managed code APIs.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cac2e-120">说明</span><span class="sxs-lookup"><span data-stu-id="cac2e-120">Remarks</span></span>

<span data-ttu-id="cac2e-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cac2e-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cac2e-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="cac2e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cac2e-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="cac2e-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cac2e-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="cac2e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="cac2e-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="cac2e-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cac2e-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="cac2e-126">Validation File</span></span>  <br/> |<span data-ttu-id="cac2e-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cac2e-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cac2e-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="cac2e-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="cac2e-129">True</span><span class="sxs-lookup"><span data-stu-id="cac2e-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cac2e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cac2e-130">See also</span></span>



- [<span data-ttu-id="cac2e-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cac2e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

