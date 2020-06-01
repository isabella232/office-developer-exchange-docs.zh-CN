---
title: SentToAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToAddresses
api_type:
- schema
ms.assetid: 086130d2-93b1-4de1-9553-10ec10322a0c
description: SentToAddresses 元素指示传入邮件必须发送到的电子邮件地址，以便条件或例外情况适用。
ms.openlocfilehash: 9a901a93b666144092bf9cc8ebbf03222ac7bf6b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457415"
---
# <a name="senttoaddresses"></a><span data-ttu-id="cb023-103">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="cb023-103">SentToAddresses</span></span>

<span data-ttu-id="cb023-104">**SentToAddresses**元素指示传入邮件必须发送到的电子邮件地址，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="cb023-104">The **SentToAddresses** element indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToAddresses>
   <Address/>
</SentToAddresses>
```

 <span data-ttu-id="cb023-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="cb023-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb023-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cb023-106">Attributes and elements</span></span>

<span data-ttu-id="cb023-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cb023-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb023-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cb023-108">Attributes</span></span>

<span data-ttu-id="cb023-109">无。</span><span class="sxs-lookup"><span data-stu-id="cb023-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb023-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cb023-110">Child elements</span></span>

|<span data-ttu-id="cb023-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb023-111">**Element**</span></span>|<span data-ttu-id="cb023-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb023-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb023-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cb023-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="cb023-114">表示一个完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="cb023-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cb023-115">父元素</span><span class="sxs-lookup"><span data-stu-id="cb023-115">Parent elements</span></span>

|<span data-ttu-id="cb023-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb023-116">**Element**</span></span>|<span data-ttu-id="cb023-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb023-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb023-118">条件</span><span class="sxs-lookup"><span data-stu-id="cb023-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="cb023-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="cb023-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="cb023-120">异常</span><span class="sxs-lookup"><span data-stu-id="cb023-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="cb023-121">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="cb023-121">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb023-122">文本值</span><span class="sxs-lookup"><span data-stu-id="cb023-122">Text value</span></span>

<span data-ttu-id="cb023-123">无。</span><span class="sxs-lookup"><span data-stu-id="cb023-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb023-124">说明</span><span class="sxs-lookup"><span data-stu-id="cb023-124">Remarks</span></span>

<span data-ttu-id="cb023-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cb023-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb023-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="cb023-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb023-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="cb023-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cb023-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="cb023-128">Schema Name</span></span>  <br/> |<span data-ttu-id="cb023-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="cb023-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cb023-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="cb023-130">Validation File</span></span>  <br/> |<span data-ttu-id="cb023-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cb023-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cb023-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="cb023-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb023-133">True</span><span class="sxs-lookup"><span data-stu-id="cb023-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb023-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb023-134">See also</span></span>



- [<span data-ttu-id="cb023-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cb023-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

