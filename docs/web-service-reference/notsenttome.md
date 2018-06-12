---
title: NotSentToMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NotSentToMe
api_type:
- schema
ms.assetid: 7cb63269-622c-4198-9a21-f5a021bf6901
description: NotSentToMe 元素指示是否中的条件或例外应用的顺序的传入消息的 ToRecipients 属性中不能邮箱的所有者。
ms.openlocfilehash: 917648f811855961877d1aba4924573e95e3962a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826555"
---
# <a name="notsenttome"></a><span data-ttu-id="bc5eb-103">NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="bc5eb-103">NotSentToMe</span></span>

<span data-ttu-id="bc5eb-104">**NotSentToMe**元素指示是否中的条件或例外应用的顺序的传入消息的**ToRecipients**属性中不能邮箱的所有者。</span><span class="sxs-lookup"><span data-stu-id="bc5eb-104">The **NotSentToMe** element indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
```xml
<NotSentToMe>true | false</NotSentToMe>
```

 <span data-ttu-id="bc5eb-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc5eb-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bc5eb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bc5eb-106">Attributes and elements</span></span>

<span data-ttu-id="bc5eb-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bc5eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc5eb-108">属性</span><span class="sxs-lookup"><span data-stu-id="bc5eb-108">Attributes</span></span>

<span data-ttu-id="bc5eb-109">无。</span><span class="sxs-lookup"><span data-stu-id="bc5eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc5eb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bc5eb-110">Child elements</span></span>

<span data-ttu-id="bc5eb-111">无。</span><span class="sxs-lookup"><span data-stu-id="bc5eb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bc5eb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bc5eb-112">Parent elements</span></span>

|<span data-ttu-id="bc5eb-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc5eb-113">**Element**</span></span>|<span data-ttu-id="bc5eb-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc5eb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc5eb-115">条件</span><span class="sxs-lookup"><span data-stu-id="bc5eb-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="bc5eb-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="bc5eb-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="bc5eb-117">异常</span><span class="sxs-lookup"><span data-stu-id="bc5eb-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="bc5eb-118">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="bc5eb-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bc5eb-119">文本值</span><span class="sxs-lookup"><span data-stu-id="bc5eb-119">Text value</span></span>

<span data-ttu-id="bc5eb-120">文本值为**true**指示邮箱所有者不得中的条件或例外应用的顺序的传入消息的**ToRecipients**属性中。</span><span class="sxs-lookup"><span data-stu-id="bc5eb-120">A text value of **true** indicates that the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="bc5eb-121">如果值为**false**指示邮箱的所有者必须是中的条件或例外应用的顺序的传入消息的**ToRecipients**属性中。</span><span class="sxs-lookup"><span data-stu-id="bc5eb-121">A value of **false** indicates that the owner of the mailbox must be in the **ToRecipients** property of the incoming message in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bc5eb-122">备注</span><span class="sxs-lookup"><span data-stu-id="bc5eb-122">Remarks</span></span>

<span data-ttu-id="bc5eb-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bc5eb-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc5eb-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="bc5eb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc5eb-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="bc5eb-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bc5eb-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="bc5eb-126">Schema Name</span></span>  <br/> |<span data-ttu-id="bc5eb-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="bc5eb-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bc5eb-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="bc5eb-128">Validation File</span></span>  <br/> |<span data-ttu-id="bc5eb-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bc5eb-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bc5eb-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="bc5eb-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="bc5eb-131">True</span><span class="sxs-lookup"><span data-stu-id="bc5eb-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc5eb-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bc5eb-132">See also</span></span>



- [<span data-ttu-id="bc5eb-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bc5eb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

