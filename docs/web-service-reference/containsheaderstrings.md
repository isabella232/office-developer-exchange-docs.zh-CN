---
title: ContainsHeaderStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsHeaderStrings
api_type:
- schema
ms.assetid: 5f68427b-990a-4a27-bfb3-fce3115b02d7
description: ContainsHeaderStrings 元素指示必须出现在传入邮件的标头中的字符串，以便条件或例外情况适用。
ms.openlocfilehash: 23e3d0e7cff9c78edbac10a6275514af93cab325
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458990"
---
# <a name="containsheaderstrings"></a><span data-ttu-id="41f3c-103">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="41f3c-103">ContainsHeaderStrings</span></span>

<span data-ttu-id="41f3c-104">**ContainsHeaderStrings**元素指示必须出现在传入邮件的标头中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="41f3c-104">The **ContainsHeaderStrings** element indicates the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsHeaderStrings>
    <String/>
</ContainsHeaderStrings>
```

 <span data-ttu-id="41f3c-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="41f3c-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41f3c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41f3c-106">Attributes and elements</span></span>

<span data-ttu-id="41f3c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41f3c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41f3c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="41f3c-108">Attributes</span></span>

<span data-ttu-id="41f3c-109">无。</span><span class="sxs-lookup"><span data-stu-id="41f3c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41f3c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="41f3c-110">Child elements</span></span>

|<span data-ttu-id="41f3c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="41f3c-111">**Element**</span></span>|<span data-ttu-id="41f3c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="41f3c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41f3c-113">字符串</span><span class="sxs-lookup"><span data-stu-id="41f3c-113">String</span></span>](string.md) <br/> |<span data-ttu-id="41f3c-114">表示必须出现在邮件头中的字符串，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="41f3c-114">Represents a string that must appear in message headers in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="41f3c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="41f3c-115">Parent elements</span></span>

|<span data-ttu-id="41f3c-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="41f3c-116">**Element**</span></span>|<span data-ttu-id="41f3c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="41f3c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41f3c-118">条件</span><span class="sxs-lookup"><span data-stu-id="41f3c-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="41f3c-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="41f3c-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="41f3c-120">异常</span><span class="sxs-lookup"><span data-stu-id="41f3c-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="41f3c-121">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="41f3c-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41f3c-122">文本值</span><span class="sxs-lookup"><span data-stu-id="41f3c-122">Text value</span></span>

<span data-ttu-id="41f3c-123">无。</span><span class="sxs-lookup"><span data-stu-id="41f3c-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41f3c-124">说明</span><span class="sxs-lookup"><span data-stu-id="41f3c-124">Remarks</span></span>

<span data-ttu-id="41f3c-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="41f3c-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41f3c-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="41f3c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41f3c-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="41f3c-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="41f3c-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="41f3c-128">Schema Name</span></span>  <br/> |<span data-ttu-id="41f3c-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="41f3c-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="41f3c-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="41f3c-130">Validation File</span></span>  <br/> |<span data-ttu-id="41f3c-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="41f3c-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="41f3c-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="41f3c-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="41f3c-133">True</span><span class="sxs-lookup"><span data-stu-id="41f3c-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41f3c-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41f3c-134">See also</span></span>



- [<span data-ttu-id="41f3c-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="41f3c-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

