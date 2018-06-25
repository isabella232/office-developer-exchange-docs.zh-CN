---
title: IsSigned
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsSigned
api_type:
- schema
ms.assetid: a4f90fe5-2834-4621-9aa3-b561f74d4674
description: IsSigned 元素指示传入邮件是否必须登录的条件或例外应用的顺序。
ms.openlocfilehash: 33ff204260465490c701c6573ff4140967ac625a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826105"
---
# <a name="issigned"></a><span data-ttu-id="8a3da-103">IsSigned</span><span class="sxs-lookup"><span data-stu-id="8a3da-103">IsSigned</span></span>

<span data-ttu-id="8a3da-104">**IsSigned**元素指示传入邮件是否必须登录的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="8a3da-104">The **IsSigned** element indicates whether incoming messages must be signed in order for the condition or exception to apply.</span></span> 
  
```XML
<IsSigned>true | false</IsSigned>
```

 <span data-ttu-id="8a3da-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a3da-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a3da-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8a3da-106">Attributes and elements</span></span>

<span data-ttu-id="8a3da-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a3da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a3da-108">属性</span><span class="sxs-lookup"><span data-stu-id="8a3da-108">Attributes</span></span>

<span data-ttu-id="8a3da-109">无。</span><span class="sxs-lookup"><span data-stu-id="8a3da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a3da-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8a3da-110">Child elements</span></span>

<span data-ttu-id="8a3da-111">无。</span><span class="sxs-lookup"><span data-stu-id="8a3da-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a3da-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8a3da-112">Parent elements</span></span>

|<span data-ttu-id="8a3da-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8a3da-113">**Element**</span></span>|<span data-ttu-id="8a3da-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8a3da-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a3da-115">条件</span><span class="sxs-lookup"><span data-stu-id="8a3da-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="8a3da-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="8a3da-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="8a3da-117">异常</span><span class="sxs-lookup"><span data-stu-id="8a3da-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="8a3da-118">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="8a3da-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8a3da-119">文本值</span><span class="sxs-lookup"><span data-stu-id="8a3da-119">Text value</span></span>

<span data-ttu-id="8a3da-120">文本值为**true**指示邮件必须登录的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="8a3da-120">A text value of **true** indicates that the message must be signed in order for the condition or exception to apply.</span></span> <span data-ttu-id="8a3da-121">文本值为**false**指示邮件不需要进行签名的条件或例外应用。</span><span class="sxs-lookup"><span data-stu-id="8a3da-121">A text value of **false** indicates that the message does not have to be signed for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8a3da-122">备注</span><span class="sxs-lookup"><span data-stu-id="8a3da-122">Remarks</span></span>

<span data-ttu-id="8a3da-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8a3da-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a3da-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="8a3da-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a3da-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="8a3da-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a3da-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="8a3da-126">Schema Name</span></span>  <br/> |<span data-ttu-id="8a3da-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="8a3da-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8a3da-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="8a3da-128">Validation File</span></span>  <br/> |<span data-ttu-id="8a3da-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8a3da-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a3da-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="8a3da-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="8a3da-131">True</span><span class="sxs-lookup"><span data-stu-id="8a3da-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a3da-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a3da-132">See also</span></span>



- [<span data-ttu-id="8a3da-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8a3da-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

