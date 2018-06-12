---
title: IsPermissionControlled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsPermissionControlled
api_type:
- schema
ms.assetid: a2fd0340-f31f-4389-a1cd-7e93b40bb3c6
description: IsPermissionControlled 元素指示传入邮件是否必须以控制权限 (受 RMS 保护) 中的条件或例外应用的顺序。
ms.openlocfilehash: fdd9910b8c35d9d57e724d6fec57d203f38f0359
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826088"
---
# <a name="ispermissioncontrolled"></a><span data-ttu-id="e99b4-103">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="e99b4-103">IsPermissionControlled</span></span>

<span data-ttu-id="e99b4-104">**IsPermissionControlled**元素指示传入邮件是否必须以控制权限 (受 RMS 保护) 中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="e99b4-104">The **IsPermissionControlled** element indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsPermissionControlled>true | false</IsPermissionControlled>
```

 <span data-ttu-id="e99b4-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e99b4-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e99b4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e99b4-106">Attributes and elements</span></span>

<span data-ttu-id="e99b4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e99b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e99b4-108">属性</span><span class="sxs-lookup"><span data-stu-id="e99b4-108">Attributes</span></span>

<span data-ttu-id="e99b4-109">无。</span><span class="sxs-lookup"><span data-stu-id="e99b4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e99b4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e99b4-110">Child elements</span></span>

<span data-ttu-id="e99b4-111">无。</span><span class="sxs-lookup"><span data-stu-id="e99b4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e99b4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e99b4-112">Parent elements</span></span>

|<span data-ttu-id="e99b4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e99b4-113">**Element**</span></span>|<span data-ttu-id="e99b4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e99b4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e99b4-115">条件</span><span class="sxs-lookup"><span data-stu-id="e99b4-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="e99b4-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="e99b4-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="e99b4-117">异常</span><span class="sxs-lookup"><span data-stu-id="e99b4-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="e99b4-118">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="e99b4-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e99b4-119">文本值</span><span class="sxs-lookup"><span data-stu-id="e99b4-119">Text value</span></span>

<span data-ttu-id="e99b4-120">文本值为**true**指示邮件必须受 RMS 保护的条件或例外的顺序应用。</span><span class="sxs-lookup"><span data-stu-id="e99b4-120">A text value of **true** indicates that the message must be RMS protected in order for the condition or exception to apply.</span></span> <span data-ttu-id="e99b4-121">如果值为**false**指示邮件不得受 RMS 保护的条件或例外的顺序应用。</span><span class="sxs-lookup"><span data-stu-id="e99b4-121">A value of **false** indicates that the message must not be RMS protected in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e99b4-122">备注</span><span class="sxs-lookup"><span data-stu-id="e99b4-122">Remarks</span></span>

<span data-ttu-id="e99b4-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e99b4-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e99b4-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="e99b4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e99b4-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="e99b4-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e99b4-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="e99b4-126">Schema Name</span></span>  <br/> |<span data-ttu-id="e99b4-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="e99b4-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e99b4-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="e99b4-128">Validation File</span></span>  <br/> |<span data-ttu-id="e99b4-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e99b4-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e99b4-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="e99b4-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="e99b4-131">True</span><span class="sxs-lookup"><span data-stu-id="e99b4-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e99b4-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e99b4-132">See also</span></span>



- [<span data-ttu-id="e99b4-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e99b4-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

