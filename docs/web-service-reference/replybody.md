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
description: ReplyBody 元素包含外出 (OOF) 邮件和消息所使用的语言。
ms.openlocfilehash: 8400dda1ee810781e129fcc44fd3cd5d6c15cbbe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827116"
---
# <a name="replybody"></a><span data-ttu-id="9ff46-103">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="9ff46-103">ReplyBody</span></span>

<span data-ttu-id="9ff46-104">**ReplyBody**元素包含外出 (OOF) 邮件和消息所使用的语言。</span><span class="sxs-lookup"><span data-stu-id="9ff46-104">The **ReplyBody** element contains an Out of Office (OOF) message and the language used for the message.</span></span> 
  
```XML
<ReplyBody xml:lang="">
   <Message/>
</ReplyBody>
```

 <span data-ttu-id="9ff46-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="9ff46-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9ff46-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9ff46-106">Attributes and elements</span></span>

<span data-ttu-id="9ff46-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9ff46-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ff46-108">属性</span><span class="sxs-lookup"><span data-stu-id="9ff46-108">Attributes</span></span>

|<span data-ttu-id="9ff46-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="9ff46-109">**Attribute**</span></span>|<span data-ttu-id="9ff46-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ff46-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ff46-111">xml: lang</span><span class="sxs-lookup"><span data-stu-id="9ff46-111">xml:lang</span></span>  <br/> |<span data-ttu-id="9ff46-112">指定**ReplyBody**内容中使用的语言。</span><span class="sxs-lookup"><span data-stu-id="9ff46-112">Specifies the language used in the **ReplyBody** contents.</span></span> <span data-ttu-id="9ff46-113">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="9ff46-113">This attribute is optional.</span></span> <span data-ttu-id="9ff46-114">此属性的可能值由 IETF RFC 3066 定义。</span><span class="sxs-lookup"><span data-stu-id="9ff46-114">The possible values of this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9ff46-115">子元素</span><span class="sxs-lookup"><span data-stu-id="9ff46-115">Child elements</span></span>

|<span data-ttu-id="9ff46-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ff46-116">**Element**</span></span>|<span data-ttu-id="9ff46-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ff46-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ff46-118">消息 （可用性）</span><span class="sxs-lookup"><span data-stu-id="9ff46-118">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="9ff46-119">包含外出 (oof) 响应。</span><span class="sxs-lookup"><span data-stu-id="9ff46-119">Contains the out of office (OOF) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9ff46-120">父元素</span><span class="sxs-lookup"><span data-stu-id="9ff46-120">Parent elements</span></span>

|<span data-ttu-id="9ff46-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ff46-121">**Element**</span></span>|<span data-ttu-id="9ff46-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ff46-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ff46-123">外出</span><span class="sxs-lookup"><span data-stu-id="9ff46-123">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="9ff46-124">定义 OOF 响应消息和发送响应消息邮箱的持续时间。</span><span class="sxs-lookup"><span data-stu-id="9ff46-124">Defines the OOF response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9ff46-125">文本值</span><span class="sxs-lookup"><span data-stu-id="9ff46-125">Text value</span></span>

<span data-ttu-id="9ff46-126">无。</span><span class="sxs-lookup"><span data-stu-id="9ff46-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9ff46-127">备注</span><span class="sxs-lookup"><span data-stu-id="9ff46-127">Remarks</span></span>

<span data-ttu-id="9ff46-128">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="9ff46-128">This element is required.</span></span>
  
<span data-ttu-id="9ff46-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9ff46-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ff46-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="9ff46-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ff46-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="9ff46-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9ff46-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="9ff46-132">Schema Name</span></span>  <br/> |<span data-ttu-id="9ff46-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="9ff46-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="9ff46-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="9ff46-134">Validation File</span></span>  <br/> |<span data-ttu-id="9ff46-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9ff46-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9ff46-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="9ff46-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="9ff46-137">False</span><span class="sxs-lookup"><span data-stu-id="9ff46-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ff46-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9ff46-138">See also</span></span>



- [<span data-ttu-id="9ff46-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9ff46-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

