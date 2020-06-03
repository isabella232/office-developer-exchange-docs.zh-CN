---
title: SendSMSAlertToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendSMSAlertToRecipients
api_type:
- schema
ms.assetid: c4dd000b-11b6-4b7b-91e0-dbfeae11d770
description: SendSMSAlertToRecipients元素指示一条短消息服务 (SMS) 的警报将发送到移动电话号码。
ms.openlocfilehash: ed17bf9ad20a51cbead4b86f385a53d19562fa64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464845"
---
# <a name="sendsmsalerttorecipients"></a><span data-ttu-id="eb1bb-103">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="eb1bb-103">SendSMSAlertToRecipients</span></span>

<span data-ttu-id="eb1bb-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **SendSMSAlertToRecipients**元素指示一条短消息服务 (SMS) 的警报将发送到移动电话号码。</span><span class="sxs-lookup"><span data-stu-id="eb1bb-104">The **SendSMSAlertToRecipients** element indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span> 
  
```XML
<SendSMSAlertToRecipients>
   <Address/>
</SendSMSAlertToRecipients>
```

 <span data-ttu-id="eb1bb-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="eb1bb-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb1bb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eb1bb-106">Attributes and elements</span></span>

<span data-ttu-id="eb1bb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eb1bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb1bb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="eb1bb-108">Attributes</span></span>

<span data-ttu-id="eb1bb-109">无。</span><span class="sxs-lookup"><span data-stu-id="eb1bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb1bb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="eb1bb-110">Child elements</span></span>

|<span data-ttu-id="eb1bb-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="eb1bb-111">**Element**</span></span>|<span data-ttu-id="eb1bb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb1bb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb1bb-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="eb1bb-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="eb1bb-114">表示一个完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="eb1bb-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eb1bb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="eb1bb-115">Parent elements</span></span>

|<span data-ttu-id="eb1bb-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="eb1bb-116">**Element**</span></span>|<span data-ttu-id="eb1bb-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb1bb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb1bb-118">操作</span><span class="sxs-lookup"><span data-stu-id="eb1bb-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="eb1bb-119">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="eb1bb-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eb1bb-120">文本值</span><span class="sxs-lookup"><span data-stu-id="eb1bb-120">Text value</span></span>

<span data-ttu-id="eb1bb-121">无。</span><span class="sxs-lookup"><span data-stu-id="eb1bb-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb1bb-122">说明</span><span class="sxs-lookup"><span data-stu-id="eb1bb-122">Remarks</span></span>

<span data-ttu-id="eb1bb-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eb1bb-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb1bb-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="eb1bb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb1bb-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="eb1bb-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb1bb-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="eb1bb-126">Schema Name</span></span>  <br/> |<span data-ttu-id="eb1bb-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="eb1bb-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eb1bb-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="eb1bb-128">Validation File</span></span>  <br/> |<span data-ttu-id="eb1bb-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eb1bb-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb1bb-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="eb1bb-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb1bb-131">True</span><span class="sxs-lookup"><span data-stu-id="eb1bb-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb1bb-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb1bb-132">See also</span></span>



- [<span data-ttu-id="eb1bb-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="eb1bb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

