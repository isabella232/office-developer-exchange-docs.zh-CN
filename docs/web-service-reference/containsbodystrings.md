---
title: ContainsBodyStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsBodyStrings
api_type:
- schema
ms.assetid: 70639472-64bb-456a-8b40-dce727542443
description: ContainsBodyStrings 元素表示必须显示在正文中的条件或例外应用的顺序的传入消息的字符串。
ms.openlocfilehash: 5993bd4061298e82a2393768eccb051326564e98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753525"
---
# <a name="containsbodystrings"></a><span data-ttu-id="c0e79-103">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="c0e79-103">ContainsBodyStrings</span></span>

<span data-ttu-id="c0e79-104">**ContainsBodyStrings**元素表示必须显示在正文中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="c0e79-104">The **ContainsBodyStrings** element indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsBodyStrings>
    <String/>
</ContainsBodyStrings>
```

 <span data-ttu-id="c0e79-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="c0e79-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0e79-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c0e79-106">Attributes and elements</span></span>

<span data-ttu-id="c0e79-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c0e79-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0e79-108">属性</span><span class="sxs-lookup"><span data-stu-id="c0e79-108">Attributes</span></span>

<span data-ttu-id="c0e79-109">无。</span><span class="sxs-lookup"><span data-stu-id="c0e79-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0e79-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c0e79-110">Child elements</span></span>

|<span data-ttu-id="c0e79-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0e79-111">**Element**</span></span>|<span data-ttu-id="c0e79-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0e79-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0e79-113">字符串</span><span class="sxs-lookup"><span data-stu-id="c0e79-113">String</span></span>](string.md) <br/> |<span data-ttu-id="c0e79-114">表示必须显示在正文中的条件或例外应用的顺序的传入消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="c0e79-114">Represents a string that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0e79-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c0e79-115">Parent elements</span></span>

|<span data-ttu-id="c0e79-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0e79-116">**Element**</span></span>|<span data-ttu-id="c0e79-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0e79-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0e79-118">条件</span><span class="sxs-lookup"><span data-stu-id="c0e79-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="c0e79-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="c0e79-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="c0e79-120">异常</span><span class="sxs-lookup"><span data-stu-id="c0e79-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="c0e79-121">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="c0e79-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c0e79-122">文本值</span><span class="sxs-lookup"><span data-stu-id="c0e79-122">Text value</span></span>

<span data-ttu-id="c0e79-123">无。</span><span class="sxs-lookup"><span data-stu-id="c0e79-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0e79-124">备注</span><span class="sxs-lookup"><span data-stu-id="c0e79-124">Remarks</span></span>

<span data-ttu-id="c0e79-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c0e79-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0e79-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="c0e79-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0e79-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="c0e79-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c0e79-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="c0e79-128">Schema Name</span></span>  <br/> |<span data-ttu-id="c0e79-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="c0e79-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c0e79-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="c0e79-130">Validation File</span></span>  <br/> |<span data-ttu-id="c0e79-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c0e79-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0e79-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="c0e79-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0e79-133">True</span><span class="sxs-lookup"><span data-stu-id="c0e79-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0e79-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0e79-134">See also</span></span>



- [<span data-ttu-id="c0e79-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c0e79-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

