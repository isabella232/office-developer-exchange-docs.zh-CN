---
title: ForwardToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ForwardToRecipients
api_type:
- schema
ms.assetid: dd58fd72-591d-4891-b226-465bcf12c19b
description: ForwardToRecipients元素指示邮件被转发的电子邮件地址。
ms.openlocfilehash: d565fa9f59794a4e10e91b05a507354a2f6ef0c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458318"
---
# <a name="forwardtorecipients"></a><span data-ttu-id="bc502-103">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="bc502-103">ForwardToRecipients</span></span>

<span data-ttu-id="bc502-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **ForwardToRecipients**元素指示邮件被转发的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="bc502-104">The **ForwardToRecipients** element indicates the e-mail addresses to which messages are to be forwarded.</span></span> 
  
```XML
<ForwardToRecipients>
   <Address/>
</ForwardToRecipients>
```

 <span data-ttu-id="bc502-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="bc502-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bc502-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bc502-106">Attributes and elements</span></span>

<span data-ttu-id="bc502-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bc502-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc502-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bc502-108">Attributes</span></span>

<span data-ttu-id="bc502-109">无。</span><span class="sxs-lookup"><span data-stu-id="bc502-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc502-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bc502-110">Child elements</span></span>

|<span data-ttu-id="bc502-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc502-111">**Element**</span></span>|<span data-ttu-id="bc502-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc502-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc502-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="bc502-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="bc502-114">表示一个完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="bc502-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bc502-115">父元素</span><span class="sxs-lookup"><span data-stu-id="bc502-115">Parent elements</span></span>

|<span data-ttu-id="bc502-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc502-116">**Element**</span></span>|<span data-ttu-id="bc502-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc502-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc502-118">操作</span><span class="sxs-lookup"><span data-stu-id="bc502-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="bc502-119">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="bc502-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bc502-120">文本值</span><span class="sxs-lookup"><span data-stu-id="bc502-120">Text value</span></span>

<span data-ttu-id="bc502-121">无。</span><span class="sxs-lookup"><span data-stu-id="bc502-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc502-122">说明</span><span class="sxs-lookup"><span data-stu-id="bc502-122">Remarks</span></span>

<span data-ttu-id="bc502-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bc502-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc502-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="bc502-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc502-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="bc502-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bc502-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="bc502-126">Schema Name</span></span>  <br/> |<span data-ttu-id="bc502-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="bc502-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bc502-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="bc502-128">Validation File</span></span>  <br/> |<span data-ttu-id="bc502-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bc502-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bc502-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="bc502-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="bc502-131">True</span><span class="sxs-lookup"><span data-stu-id="bc502-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc502-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bc502-132">See also</span></span>



- [<span data-ttu-id="bc502-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bc502-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

