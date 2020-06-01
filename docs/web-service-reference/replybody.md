---
title: ReplyBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyBody
api_type:
- schema
ms.assetid: bb184144-3e4b-4419-a883-cc9fab1085e6
description: ReplyBody 元素包含一个外出（OOF）邮件和用于邮件的语言。
ms.openlocfilehash: 496d336d1f87d9ea493ba7da362eef5a416fd899
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465301"
---
# <a name="replybody"></a><span data-ttu-id="2a72d-103">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="2a72d-103">ReplyBody</span></span>

<span data-ttu-id="2a72d-104">**ReplyBody**元素包含一个外出（OOF）邮件和用于邮件的语言。</span><span class="sxs-lookup"><span data-stu-id="2a72d-104">The **ReplyBody** element contains an Out of Office (OOF) message and the language used for the message.</span></span> 
  
```XML
<ReplyBody xml:lang="">
   <Message/>
</ReplyBody>
```

 <span data-ttu-id="2a72d-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="2a72d-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a72d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2a72d-106">Attributes and elements</span></span>

<span data-ttu-id="2a72d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2a72d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a72d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2a72d-108">Attributes</span></span>

|<span data-ttu-id="2a72d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="2a72d-109">**Attribute**</span></span>|<span data-ttu-id="2a72d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a72d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a72d-111">xml： lang</span><span class="sxs-lookup"><span data-stu-id="2a72d-111">xml:lang</span></span>  <br/> |<span data-ttu-id="2a72d-112">指定在**ReplyBody**内容中使用的语言。</span><span class="sxs-lookup"><span data-stu-id="2a72d-112">Specifies the language used in the **ReplyBody** contents.</span></span> <span data-ttu-id="2a72d-113">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="2a72d-113">This attribute is optional.</span></span> <span data-ttu-id="2a72d-114">此属性的可能值由 IETF RFC 3066 定义。</span><span class="sxs-lookup"><span data-stu-id="2a72d-114">The possible values of this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2a72d-115">子元素</span><span class="sxs-lookup"><span data-stu-id="2a72d-115">Child elements</span></span>

|<span data-ttu-id="2a72d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a72d-116">**Element**</span></span>|<span data-ttu-id="2a72d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a72d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a72d-118">邮件（可用性）</span><span class="sxs-lookup"><span data-stu-id="2a72d-118">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="2a72d-119">包含外出（OOF）响应。</span><span class="sxs-lookup"><span data-stu-id="2a72d-119">Contains the out of office (OOF) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a72d-120">父元素</span><span class="sxs-lookup"><span data-stu-id="2a72d-120">Parent elements</span></span>

|<span data-ttu-id="2a72d-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a72d-121">**Element**</span></span>|<span data-ttu-id="2a72d-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a72d-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a72d-123">外出</span><span class="sxs-lookup"><span data-stu-id="2a72d-123">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="2a72d-124">定义 OOF 响应消息和发送邮箱的响应邮件的持续时间。</span><span class="sxs-lookup"><span data-stu-id="2a72d-124">Defines the OOF response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2a72d-125">文本值</span><span class="sxs-lookup"><span data-stu-id="2a72d-125">Text value</span></span>

<span data-ttu-id="2a72d-126">无。</span><span class="sxs-lookup"><span data-stu-id="2a72d-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a72d-127">说明</span><span class="sxs-lookup"><span data-stu-id="2a72d-127">Remarks</span></span>

<span data-ttu-id="2a72d-128">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="2a72d-128">This element is required.</span></span>
  
<span data-ttu-id="2a72d-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2a72d-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a72d-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="2a72d-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a72d-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="2a72d-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2a72d-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="2a72d-132">Schema Name</span></span>  <br/> |<span data-ttu-id="2a72d-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="2a72d-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="2a72d-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="2a72d-134">Validation File</span></span>  <br/> |<span data-ttu-id="2a72d-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2a72d-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2a72d-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="2a72d-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="2a72d-137">False</span><span class="sxs-lookup"><span data-stu-id="2a72d-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a72d-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2a72d-138">See also</span></span>



- [<span data-ttu-id="2a72d-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2a72d-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

