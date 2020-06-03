---
title: FromConnectedAccounts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FromConnectedAccounts
api_type:
- schema
ms.assetid: d4d7ddd7-078d-4f1a-a26b-22dce0c49f3a
description: FromConnectedAccounts元素表示已有已聚合中应用的条件或例外顺序传入邮件的电子邮件帐户名称。
ms.openlocfilehash: 159ae064827c2f9c2b470580ad5457264e8dae93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464047"
---
# <a name="fromconnectedaccounts"></a><span data-ttu-id="15e34-103">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="15e34-103">FromConnectedAccounts</span></span>

<span data-ttu-id="15e34-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **FromConnectedAccounts**元素表示已有已聚合中应用的条件或例外顺序传入邮件的电子邮件帐户名称。</span><span class="sxs-lookup"><span data-stu-id="15e34-104">The **FromConnectedAccounts** element represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span> 
  
```XML
<FromConnectedAccounts>
    <String/>
</FromConnectedAccounts>
```

 <span data-ttu-id="15e34-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="15e34-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15e34-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="15e34-106">Attributes and elements</span></span>

<span data-ttu-id="15e34-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="15e34-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15e34-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="15e34-108">Attributes</span></span>

<span data-ttu-id="15e34-109">无。</span><span class="sxs-lookup"><span data-stu-id="15e34-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15e34-110">子元素</span><span class="sxs-lookup"><span data-stu-id="15e34-110">Child elements</span></span>

|<span data-ttu-id="15e34-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="15e34-111">**Element**</span></span>|<span data-ttu-id="15e34-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="15e34-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15e34-113">字符串</span><span class="sxs-lookup"><span data-stu-id="15e34-113">String</span></span>](string.md) <br/> |<span data-ttu-id="15e34-114">表示已有已聚合中应用的条件或例外顺序传入邮件的电子邮件帐户名。</span><span class="sxs-lookup"><span data-stu-id="15e34-114">Represents an e-mail account name from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15e34-115">父元素</span><span class="sxs-lookup"><span data-stu-id="15e34-115">Parent elements</span></span>

|<span data-ttu-id="15e34-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="15e34-116">**Element**</span></span>|<span data-ttu-id="15e34-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="15e34-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15e34-118">条件</span><span class="sxs-lookup"><span data-stu-id="15e34-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="15e34-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="15e34-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="15e34-120">异常</span><span class="sxs-lookup"><span data-stu-id="15e34-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="15e34-121">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="15e34-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="15e34-122">文本值</span><span class="sxs-lookup"><span data-stu-id="15e34-122">Text value</span></span>

<span data-ttu-id="15e34-123">无。</span><span class="sxs-lookup"><span data-stu-id="15e34-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15e34-124">说明</span><span class="sxs-lookup"><span data-stu-id="15e34-124">Remarks</span></span>

<span data-ttu-id="15e34-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="15e34-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15e34-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="15e34-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15e34-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="15e34-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="15e34-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="15e34-128">Schema Name</span></span>  <br/> |<span data-ttu-id="15e34-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="15e34-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="15e34-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="15e34-130">Validation File</span></span>  <br/> |<span data-ttu-id="15e34-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="15e34-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="15e34-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="15e34-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="15e34-133">True</span><span class="sxs-lookup"><span data-stu-id="15e34-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15e34-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15e34-134">See also</span></span>



- [<span data-ttu-id="15e34-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="15e34-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

