---
title: IsVoicemail
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsVoicemail
api_type:
- schema
ms.assetid: 96d81d6e-4b75-43ad-b151-2dd4fd57db94
description: IsVoicemail元素指示传入的邮件是否必须是为了让情况或异常的应用的语音邮件。
ms.openlocfilehash: 513498301aa65eaf0cac5769c940eeedf5c9e629
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826136"
---
# <a name="isvoicemail"></a><span data-ttu-id="9250b-103">IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="9250b-103">IsVoicemail</span></span>

<span data-ttu-id="9250b-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **IsVoicemail**元素指示传入的邮件是否必须是为了让情况或异常的应用的语音邮件。</span><span class="sxs-lookup"><span data-stu-id="9250b-104">The **IsVoicemail** element indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.</span></span> 
  
```XML
<IsVoicemail>true | false</IsVoicemail>
```

 <span data-ttu-id="9250b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9250b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9250b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9250b-106">Attributes and elements</span></span>

<span data-ttu-id="9250b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9250b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9250b-108">属性</span><span class="sxs-lookup"><span data-stu-id="9250b-108">Attributes</span></span>

<span data-ttu-id="9250b-109">无。</span><span class="sxs-lookup"><span data-stu-id="9250b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9250b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9250b-110">Child elements</span></span>

<span data-ttu-id="9250b-111">无。</span><span class="sxs-lookup"><span data-stu-id="9250b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9250b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9250b-112">Parent elements</span></span>

|<span data-ttu-id="9250b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9250b-113">**Element**</span></span>|<span data-ttu-id="9250b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9250b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9250b-115">条件</span><span class="sxs-lookup"><span data-stu-id="9250b-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="9250b-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="9250b-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="9250b-117">异常</span><span class="sxs-lookup"><span data-stu-id="9250b-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="9250b-118">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="9250b-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9250b-119">文本值</span><span class="sxs-lookup"><span data-stu-id="9250b-119">Text value</span></span>

<span data-ttu-id="9250b-p101">**true**的一个文字值指示消息必须语音邮件信息中的条件或例外的顺序应用。 **false**表示该消息必须不让中的条件或例外应用语音邮件。</span><span class="sxs-lookup"><span data-stu-id="9250b-p101">A text value of **true** indicates that the message must be a voice mail message in order for the condition or exception to apply. A value of **false** indicates that the message must not be a voice mail message in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9250b-122">备注</span><span class="sxs-lookup"><span data-stu-id="9250b-122">Remarks</span></span>

<span data-ttu-id="9250b-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9250b-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9250b-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="9250b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9250b-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="9250b-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9250b-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="9250b-126">Schema Name</span></span>  <br/> |<span data-ttu-id="9250b-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="9250b-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9250b-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="9250b-128">Validation File</span></span>  <br/> |<span data-ttu-id="9250b-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9250b-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9250b-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="9250b-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="9250b-131">True</span><span class="sxs-lookup"><span data-stu-id="9250b-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9250b-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9250b-132">See also</span></span>



- [<span data-ttu-id="9250b-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9250b-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
