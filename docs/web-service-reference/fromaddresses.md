---
title: FromAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FromAddresses
api_type:
- schema
ms.assetid: b219f315-c20a-4633-af3e-94bd3e4526b6
description: FromAddresses 元素表示必须从其发送传入消息的条件或例外的顺序应用中的电子邮件地址。
ms.openlocfilehash: 40ecb1f3e16ad961b8e4c38d5aa9d15f4f74469a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754432"
---
# <a name="fromaddresses"></a><span data-ttu-id="850eb-103">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="850eb-103">FromAddresses</span></span>

<span data-ttu-id="850eb-104">**FromAddresses**元素表示必须从其发送传入消息的条件或例外的顺序应用中的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="850eb-104">The **FromAddresses** element indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span> 
  
```XML
<FromAddresses>
   <Address/>
</FromAddresses>
```

 <span data-ttu-id="850eb-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="850eb-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="850eb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="850eb-106">Attributes and elements</span></span>

<span data-ttu-id="850eb-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="850eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="850eb-108">属性</span><span class="sxs-lookup"><span data-stu-id="850eb-108">Attributes</span></span>

<span data-ttu-id="850eb-109">无。</span><span class="sxs-lookup"><span data-stu-id="850eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="850eb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="850eb-110">Child elements</span></span>

|<span data-ttu-id="850eb-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="850eb-111">**Element**</span></span>|<span data-ttu-id="850eb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="850eb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="850eb-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="850eb-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="850eb-114">表示一个完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="850eb-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="850eb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="850eb-115">Parent elements</span></span>

|<span data-ttu-id="850eb-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="850eb-116">**Element**</span></span>|<span data-ttu-id="850eb-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="850eb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="850eb-118">条件</span><span class="sxs-lookup"><span data-stu-id="850eb-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="850eb-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="850eb-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="850eb-120">异常</span><span class="sxs-lookup"><span data-stu-id="850eb-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="850eb-121">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="850eb-121">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="850eb-122">文本值</span><span class="sxs-lookup"><span data-stu-id="850eb-122">Text value</span></span>

<span data-ttu-id="850eb-123">无。</span><span class="sxs-lookup"><span data-stu-id="850eb-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="850eb-124">备注</span><span class="sxs-lookup"><span data-stu-id="850eb-124">Remarks</span></span>

<span data-ttu-id="850eb-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="850eb-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="850eb-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="850eb-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="850eb-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="850eb-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="850eb-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="850eb-128">Schema Name</span></span>  <br/> |<span data-ttu-id="850eb-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="850eb-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="850eb-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="850eb-130">Validation File</span></span>  <br/> |<span data-ttu-id="850eb-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="850eb-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="850eb-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="850eb-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="850eb-133">True</span><span class="sxs-lookup"><span data-stu-id="850eb-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="850eb-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="850eb-134">See also</span></span>



- [<span data-ttu-id="850eb-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="850eb-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

