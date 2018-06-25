---
title: ContainsSenderStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsSenderStrings
api_type:
- schema
ms.assetid: 3e16163f-cffe-4c4e-9a2a-00245d25ba96
description: ContainsSenderStrings 元素表示必须出现在 From 属性中的条件或例外应用的顺序的传入消息的字符串。
ms.openlocfilehash: d174c0d7e2cbfd5b671a825a867d3ee7e24c2f2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753539"
---
# <a name="containssenderstrings"></a><span data-ttu-id="67563-103">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="67563-103">ContainsSenderStrings</span></span>

<span data-ttu-id="67563-104">**ContainsSenderStrings**元素表示必须出现在**From**属性中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="67563-104">The **ContainsSenderStrings** element indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsSenderStrings>
    <String/>
</ContainsSenderStrings>
```

 <span data-ttu-id="67563-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="67563-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67563-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="67563-106">Attributes and elements</span></span>

<span data-ttu-id="67563-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="67563-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67563-108">属性</span><span class="sxs-lookup"><span data-stu-id="67563-108">Attributes</span></span>

<span data-ttu-id="67563-109">无。</span><span class="sxs-lookup"><span data-stu-id="67563-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67563-110">子元素</span><span class="sxs-lookup"><span data-stu-id="67563-110">Child elements</span></span>

|<span data-ttu-id="67563-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="67563-111">**Element**</span></span>|<span data-ttu-id="67563-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="67563-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67563-113">字符串</span><span class="sxs-lookup"><span data-stu-id="67563-113">String</span></span>](string.md) <br/> |<span data-ttu-id="67563-114">表示必须出现在**From**属性中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="67563-114">Represents a string that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67563-115">父元素</span><span class="sxs-lookup"><span data-stu-id="67563-115">Parent elements</span></span>

|<span data-ttu-id="67563-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="67563-116">**Element**</span></span>|<span data-ttu-id="67563-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="67563-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67563-118">条件</span><span class="sxs-lookup"><span data-stu-id="67563-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="67563-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="67563-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="67563-120">异常</span><span class="sxs-lookup"><span data-stu-id="67563-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="67563-121">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="67563-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="67563-122">文本值</span><span class="sxs-lookup"><span data-stu-id="67563-122">Text value</span></span>

<span data-ttu-id="67563-123">无。</span><span class="sxs-lookup"><span data-stu-id="67563-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67563-124">备注</span><span class="sxs-lookup"><span data-stu-id="67563-124">Remarks</span></span>

<span data-ttu-id="67563-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="67563-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67563-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="67563-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67563-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="67563-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="67563-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="67563-128">Schema Name</span></span>  <br/> |<span data-ttu-id="67563-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="67563-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="67563-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="67563-130">Validation File</span></span>  <br/> |<span data-ttu-id="67563-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="67563-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="67563-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="67563-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="67563-133">True</span><span class="sxs-lookup"><span data-stu-id="67563-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67563-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67563-134">See also</span></span>



- [<span data-ttu-id="67563-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="67563-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

