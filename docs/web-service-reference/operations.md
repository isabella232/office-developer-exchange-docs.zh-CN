---
title: 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Operations
api_type:
- schema
ms.assetid: d8cd41b1-28ae-4c95-9ff6-8b25c8e18306
description: 操作元素包含数组的可执行在收件箱规则操作。
ms.openlocfilehash: 1030703d5e496be391d557e99e1420f9fddfdb36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826655"
---
# <a name="operations"></a><span data-ttu-id="da1ec-103">操作</span><span class="sxs-lookup"><span data-stu-id="da1ec-103">Operations</span></span>

<span data-ttu-id="da1ec-104">**操作**元素包含数组的可执行在收件箱规则操作。</span><span class="sxs-lookup"><span data-stu-id="da1ec-104">The **Operations** element contains an array of rule operations that can be performed on an Inbox.</span></span> 
  
[<span data-ttu-id="da1ec-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="da1ec-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
```XML
<Operations>
    <CreateRuleOperation/>
    <SetRuleOperation/>
    <DeleteRuleOperation/>
</Operations>
```

 <span data-ttu-id="da1ec-106">**ArrayOfRuleOperationsType**</span><span class="sxs-lookup"><span data-stu-id="da1ec-106">**ArrayOfRuleOperationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da1ec-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="da1ec-107">Attributes and elements</span></span>

<span data-ttu-id="da1ec-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="da1ec-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da1ec-109">属性</span><span class="sxs-lookup"><span data-stu-id="da1ec-109">Attributes</span></span>

<span data-ttu-id="da1ec-110">无。</span><span class="sxs-lookup"><span data-stu-id="da1ec-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da1ec-111">子元素</span><span class="sxs-lookup"><span data-stu-id="da1ec-111">Child elements</span></span>

|<span data-ttu-id="da1ec-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="da1ec-112">**Element**</span></span>|<span data-ttu-id="da1ec-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="da1ec-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da1ec-114">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="da1ec-114">CreateRuleOperation</span></span>](createruleoperation.md) <br/> |<span data-ttu-id="da1ec-115">代表要创建新的收件箱规则操作。</span><span class="sxs-lookup"><span data-stu-id="da1ec-115">Represents an operation to create a new Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="da1ec-116">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="da1ec-116">SetRuleOperation</span></span>](setruleoperation.md) <br/> |<span data-ttu-id="da1ec-117">代表要更新的收件箱规则操作。</span><span class="sxs-lookup"><span data-stu-id="da1ec-117">Represents an operation to update an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="da1ec-118">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="da1ec-118">DeleteRuleOperation</span></span>](deleteruleoperation.md) <br/> |<span data-ttu-id="da1ec-119">代表要删除收件箱规则操作。</span><span class="sxs-lookup"><span data-stu-id="da1ec-119">Represents an operation to delete an Inbox rule.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da1ec-120">父元素</span><span class="sxs-lookup"><span data-stu-id="da1ec-120">Parent elements</span></span>

|<span data-ttu-id="da1ec-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="da1ec-121">**Element**</span></span>|<span data-ttu-id="da1ec-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="da1ec-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da1ec-123">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="da1ec-123">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="da1ec-124">定义更新中的邮箱服务器存储区中的收件箱规则的请求。</span><span class="sxs-lookup"><span data-stu-id="da1ec-124">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da1ec-125">备注</span><span class="sxs-lookup"><span data-stu-id="da1ec-125">Remarks</span></span>

<span data-ttu-id="da1ec-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="da1ec-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da1ec-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="da1ec-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da1ec-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="da1ec-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da1ec-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="da1ec-129">Schema Name</span></span>  <br/> |<span data-ttu-id="da1ec-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="da1ec-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="da1ec-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="da1ec-131">Validation File</span></span>  <br/> |<span data-ttu-id="da1ec-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="da1ec-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="da1ec-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="da1ec-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="da1ec-134">False</span><span class="sxs-lookup"><span data-stu-id="da1ec-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da1ec-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="da1ec-135">See also</span></span>



[<span data-ttu-id="da1ec-136">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="da1ec-136">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="da1ec-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="da1ec-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

