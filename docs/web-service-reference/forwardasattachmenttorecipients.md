---
title: ForwardAsAttachmentToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ForwardAsAttachmentToRecipients
api_type:
- schema
ms.assetid: 8649ea14-672f-43c9-b10a-a2b02efd5867
description: ForwardAsAttachmentToRecipients元素指示消息是以附件形式转发电子邮件地址。
ms.openlocfilehash: bf8c3563460eea811602074bf16f9253b4610832
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44453334"
---
# <a name="forwardasattachmenttorecipients"></a><span data-ttu-id="1bba1-103">ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="1bba1-103">ForwardAsAttachmentToRecipients</span></span>

<span data-ttu-id="1bba1-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **ForwardAsAttachmentToRecipients**元素指示消息是以附件形式转发电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="1bba1-104">The **ForwardAsAttachmentToRecipients** element indicates the e-mail addresses to which messages are to be forwarded as attachments.</span></span> 
  
```XML
<ForwardAsAttachmentToRecipients>
   <Address/>
</ForwardAsAttachmentToRecipients>
```

 <span data-ttu-id="1bba1-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="1bba1-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1bba1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1bba1-106">Attributes and elements</span></span>

<span data-ttu-id="1bba1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1bba1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1bba1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1bba1-108">Attributes</span></span>

<span data-ttu-id="1bba1-109">无。</span><span class="sxs-lookup"><span data-stu-id="1bba1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1bba1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1bba1-110">Child elements</span></span>

|<span data-ttu-id="1bba1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1bba1-111">**Element**</span></span>|<span data-ttu-id="1bba1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1bba1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bba1-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="1bba1-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="1bba1-114">表示一个完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="1bba1-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1bba1-115">父元素</span><span class="sxs-lookup"><span data-stu-id="1bba1-115">Parent elements</span></span>

|<span data-ttu-id="1bba1-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="1bba1-116">**Element**</span></span>|<span data-ttu-id="1bba1-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="1bba1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bba1-118">操作</span><span class="sxs-lookup"><span data-stu-id="1bba1-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="1bba1-119">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="1bba1-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1bba1-120">文本值</span><span class="sxs-lookup"><span data-stu-id="1bba1-120">Text value</span></span>

<span data-ttu-id="1bba1-121">无。</span><span class="sxs-lookup"><span data-stu-id="1bba1-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1bba1-122">说明</span><span class="sxs-lookup"><span data-stu-id="1bba1-122">Remarks</span></span>

<span data-ttu-id="1bba1-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1bba1-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1bba1-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="1bba1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bba1-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="1bba1-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1bba1-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="1bba1-126">Schema Name</span></span>  <br/> |<span data-ttu-id="1bba1-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="1bba1-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1bba1-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="1bba1-128">Validation File</span></span>  <br/> |<span data-ttu-id="1bba1-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1bba1-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1bba1-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="1bba1-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="1bba1-131">True</span><span class="sxs-lookup"><span data-stu-id="1bba1-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bba1-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1bba1-132">See also</span></span>



- [<span data-ttu-id="1bba1-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1bba1-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

