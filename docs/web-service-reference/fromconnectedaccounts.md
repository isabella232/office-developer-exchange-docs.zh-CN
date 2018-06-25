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
ms.openlocfilehash: 426e81bbbe96fb5fb4b36506438dc4af4f560eef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754430"
---
# <a name="fromconnectedaccounts"></a><span data-ttu-id="99ade-103">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="99ade-103">FromConnectedAccounts</span></span>

<span data-ttu-id="99ade-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **FromConnectedAccounts**元素表示已有已聚合中应用的条件或例外顺序传入邮件的电子邮件帐户名称。</span><span class="sxs-lookup"><span data-stu-id="99ade-104">The **FromConnectedAccounts** element represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span> 
  
```XML
<FromConnectedAccounts>
    <String/>
</FromConnectedAccounts>
```

 <span data-ttu-id="99ade-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="99ade-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99ade-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="99ade-106">Attributes and elements</span></span>

<span data-ttu-id="99ade-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="99ade-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99ade-108">属性</span><span class="sxs-lookup"><span data-stu-id="99ade-108">Attributes</span></span>

<span data-ttu-id="99ade-109">无。</span><span class="sxs-lookup"><span data-stu-id="99ade-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99ade-110">子元素</span><span class="sxs-lookup"><span data-stu-id="99ade-110">Child elements</span></span>

|<span data-ttu-id="99ade-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="99ade-111">**Element**</span></span>|<span data-ttu-id="99ade-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="99ade-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99ade-113">字符串</span><span class="sxs-lookup"><span data-stu-id="99ade-113">String</span></span>](string.md) <br/> |<span data-ttu-id="99ade-114">表示已有已聚合中应用的条件或例外顺序传入邮件的电子邮件帐户名。</span><span class="sxs-lookup"><span data-stu-id="99ade-114">Represents an e-mail account name from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99ade-115">父元素</span><span class="sxs-lookup"><span data-stu-id="99ade-115">Parent elements</span></span>

|<span data-ttu-id="99ade-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="99ade-116">**Element**</span></span>|<span data-ttu-id="99ade-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="99ade-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99ade-118">条件</span><span class="sxs-lookup"><span data-stu-id="99ade-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="99ade-119">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="99ade-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="99ade-120">异常</span><span class="sxs-lookup"><span data-stu-id="99ade-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="99ade-121">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="99ade-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="99ade-122">文本值</span><span class="sxs-lookup"><span data-stu-id="99ade-122">Text value</span></span>

<span data-ttu-id="99ade-123">无。</span><span class="sxs-lookup"><span data-stu-id="99ade-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="99ade-124">备注</span><span class="sxs-lookup"><span data-stu-id="99ade-124">Remarks</span></span>

<span data-ttu-id="99ade-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="99ade-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99ade-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="99ade-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99ade-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="99ade-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="99ade-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="99ade-128">Schema Name</span></span>  <br/> |<span data-ttu-id="99ade-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="99ade-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="99ade-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="99ade-130">Validation File</span></span>  <br/> |<span data-ttu-id="99ade-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="99ade-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="99ade-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="99ade-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="99ade-133">True</span><span class="sxs-lookup"><span data-stu-id="99ade-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99ade-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="99ade-134">See also</span></span>



- [<span data-ttu-id="99ade-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="99ade-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

