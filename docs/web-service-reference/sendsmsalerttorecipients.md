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
ms.openlocfilehash: b28202c71257fccca67879713d5d7df03f69b06d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827347"
---
# <a name="sendsmsalerttorecipients"></a><span data-ttu-id="ce04f-103">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="ce04f-103">SendSMSAlertToRecipients</span></span>

<span data-ttu-id="ce04f-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **SendSMSAlertToRecipients**元素指示一条短消息服务 (SMS) 的警报将发送到移动电话号码。</span><span class="sxs-lookup"><span data-stu-id="ce04f-104">The **SendSMSAlertToRecipients** element indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span> 
  
```XML
<SendSMSAlertToRecipients>
   <Address/>
</SendSMSAlertToRecipients>
```

 <span data-ttu-id="ce04f-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="ce04f-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce04f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ce04f-106">Attributes and elements</span></span>

<span data-ttu-id="ce04f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ce04f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce04f-108">属性</span><span class="sxs-lookup"><span data-stu-id="ce04f-108">Attributes</span></span>

<span data-ttu-id="ce04f-109">无。</span><span class="sxs-lookup"><span data-stu-id="ce04f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce04f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ce04f-110">Child elements</span></span>

|<span data-ttu-id="ce04f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ce04f-111">**Element**</span></span>|<span data-ttu-id="ce04f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce04f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce04f-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="ce04f-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="ce04f-114">表示一个完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="ce04f-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ce04f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ce04f-115">Parent elements</span></span>

|<span data-ttu-id="ce04f-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="ce04f-116">**Element**</span></span>|<span data-ttu-id="ce04f-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce04f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce04f-118">操作</span><span class="sxs-lookup"><span data-stu-id="ce04f-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="ce04f-119">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="ce04f-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ce04f-120">文本值</span><span class="sxs-lookup"><span data-stu-id="ce04f-120">Text value</span></span>

<span data-ttu-id="ce04f-121">无。</span><span class="sxs-lookup"><span data-stu-id="ce04f-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce04f-122">备注</span><span class="sxs-lookup"><span data-stu-id="ce04f-122">Remarks</span></span>

<span data-ttu-id="ce04f-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ce04f-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce04f-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="ce04f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce04f-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="ce04f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ce04f-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="ce04f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ce04f-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="ce04f-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ce04f-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="ce04f-128">Validation File</span></span>  <br/> |<span data-ttu-id="ce04f-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ce04f-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ce04f-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="ce04f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce04f-131">True</span><span class="sxs-lookup"><span data-stu-id="ce04f-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce04f-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ce04f-132">See also</span></span>



- [<span data-ttu-id="ce04f-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ce04f-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

