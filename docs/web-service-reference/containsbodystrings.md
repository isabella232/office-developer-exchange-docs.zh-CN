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
description: ContainsBodyStrings 元素指示必须出现在传入邮件正文中的字符串，以便条件或例外情况适用。
ms.openlocfilehash: 008261ab94b1bed33cc72cacf7abe7aa58927d1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463802"
---
# <a name="containsbodystrings"></a><span data-ttu-id="43a94-103">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="43a94-103">ContainsBodyStrings</span></span>

<span data-ttu-id="43a94-104">**ContainsBodyStrings**元素指示必须出现在传入邮件正文中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="43a94-104">The **ContainsBodyStrings** element indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsBodyStrings>
    <String/>
</ContainsBodyStrings>
```

 <span data-ttu-id="43a94-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="43a94-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43a94-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="43a94-106">Attributes and elements</span></span>

<span data-ttu-id="43a94-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="43a94-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43a94-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="43a94-108">Attributes</span></span>

<span data-ttu-id="43a94-109">无。</span><span class="sxs-lookup"><span data-stu-id="43a94-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43a94-110">子元素</span><span class="sxs-lookup"><span data-stu-id="43a94-110">Child elements</span></span>

|<span data-ttu-id="43a94-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="43a94-111">**Element**</span></span>|<span data-ttu-id="43a94-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="43a94-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43a94-113">字符串</span><span class="sxs-lookup"><span data-stu-id="43a94-113">String</span></span>](string.md) <br/> |<span data-ttu-id="43a94-114">表示必须出现在传入邮件正文中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="43a94-114">Represents a string that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="43a94-115">父元素</span><span class="sxs-lookup"><span data-stu-id="43a94-115">Parent elements</span></span>

|<span data-ttu-id="43a94-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="43a94-116">**Element**</span></span>|<span data-ttu-id="43a94-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="43a94-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43a94-118">条件</span><span class="sxs-lookup"><span data-stu-id="43a94-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="43a94-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="43a94-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="43a94-120">异常</span><span class="sxs-lookup"><span data-stu-id="43a94-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="43a94-121">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="43a94-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="43a94-122">文本值</span><span class="sxs-lookup"><span data-stu-id="43a94-122">Text value</span></span>

<span data-ttu-id="43a94-123">无。</span><span class="sxs-lookup"><span data-stu-id="43a94-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43a94-124">说明</span><span class="sxs-lookup"><span data-stu-id="43a94-124">Remarks</span></span>

<span data-ttu-id="43a94-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="43a94-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43a94-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="43a94-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43a94-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="43a94-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="43a94-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="43a94-128">Schema Name</span></span>  <br/> |<span data-ttu-id="43a94-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="43a94-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="43a94-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="43a94-130">Validation File</span></span>  <br/> |<span data-ttu-id="43a94-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="43a94-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="43a94-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="43a94-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="43a94-133">True</span><span class="sxs-lookup"><span data-stu-id="43a94-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43a94-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43a94-134">See also</span></span>



- [<span data-ttu-id="43a94-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="43a94-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

