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
description: 操作元素包含可在收件箱中执行的一组规则操作。
ms.openlocfilehash: 4bbec4ad6424f802bb6781a870d65f23705e88c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462484"
---
# <a name="operations"></a><span data-ttu-id="60edd-103">操作</span><span class="sxs-lookup"><span data-stu-id="60edd-103">Operations</span></span>

<span data-ttu-id="60edd-104">**操作**元素包含可在收件箱中执行的一组规则操作。</span><span class="sxs-lookup"><span data-stu-id="60edd-104">The **Operations** element contains an array of rule operations that can be performed on an Inbox.</span></span> 
  
[<span data-ttu-id="60edd-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="60edd-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
```XML
<Operations>
    <CreateRuleOperation/>
    <SetRuleOperation/>
    <DeleteRuleOperation/>
</Operations>
```

 <span data-ttu-id="60edd-106">**ArrayOfRuleOperationsType**</span><span class="sxs-lookup"><span data-stu-id="60edd-106">**ArrayOfRuleOperationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60edd-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="60edd-107">Attributes and elements</span></span>

<span data-ttu-id="60edd-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="60edd-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60edd-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="60edd-109">Attributes</span></span>

<span data-ttu-id="60edd-110">无。</span><span class="sxs-lookup"><span data-stu-id="60edd-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60edd-111">子元素</span><span class="sxs-lookup"><span data-stu-id="60edd-111">Child elements</span></span>

|<span data-ttu-id="60edd-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="60edd-112">**Element**</span></span>|<span data-ttu-id="60edd-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="60edd-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60edd-114">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="60edd-114">CreateRuleOperation</span></span>](createruleoperation.md) <br/> |<span data-ttu-id="60edd-115">表示用于创建新的收件箱规则的操作。</span><span class="sxs-lookup"><span data-stu-id="60edd-115">Represents an operation to create a new Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="60edd-116">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="60edd-116">SetRuleOperation</span></span>](setruleoperation.md) <br/> |<span data-ttu-id="60edd-117">表示更新收件箱规则的操作。</span><span class="sxs-lookup"><span data-stu-id="60edd-117">Represents an operation to update an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="60edd-118">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="60edd-118">DeleteRuleOperation</span></span>](deleteruleoperation.md) <br/> |<span data-ttu-id="60edd-119">表示删除收件箱规则的操作。</span><span class="sxs-lookup"><span data-stu-id="60edd-119">Represents an operation to delete an Inbox rule.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="60edd-120">父元素</span><span class="sxs-lookup"><span data-stu-id="60edd-120">Parent elements</span></span>

|<span data-ttu-id="60edd-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="60edd-121">**Element**</span></span>|<span data-ttu-id="60edd-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="60edd-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60edd-123">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="60edd-123">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="60edd-124">定义更新服务器存储中的邮箱的收件箱规则的请求。</span><span class="sxs-lookup"><span data-stu-id="60edd-124">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60edd-125">说明</span><span class="sxs-lookup"><span data-stu-id="60edd-125">Remarks</span></span>

<span data-ttu-id="60edd-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="60edd-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60edd-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="60edd-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60edd-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="60edd-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60edd-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="60edd-129">Schema Name</span></span>  <br/> |<span data-ttu-id="60edd-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="60edd-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="60edd-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="60edd-131">Validation File</span></span>  <br/> |<span data-ttu-id="60edd-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60edd-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60edd-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="60edd-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="60edd-134">False</span><span class="sxs-lookup"><span data-stu-id="60edd-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60edd-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="60edd-135">See also</span></span>



[<span data-ttu-id="60edd-136">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="60edd-136">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="60edd-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="60edd-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

