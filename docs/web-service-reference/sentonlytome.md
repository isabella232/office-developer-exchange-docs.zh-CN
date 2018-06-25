---
title: SentOnlyToMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentOnlyToMe
api_type:
- schema
ms.assetid: b6d4dea5-812d-4b29-917d-071ebd7ddd92
description: SentOnlyToMe 元素指示是否邮箱所有者必须是唯一的条件或例外应用的顺序中的传入消息的 ToRecipients 属性中。
ms.openlocfilehash: 91c31069652a35dc7a38ad6b6e1512cc07d67a98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827353"
---
# <a name="sentonlytome"></a><span data-ttu-id="ae45f-103">SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="ae45f-103">SentOnlyToMe</span></span>

<span data-ttu-id="ae45f-104">**SentOnlyToMe**元素指示是否邮箱所有者必须是唯一的条件或例外应用的顺序中的传入消息的**ToRecipients**属性中。</span><span class="sxs-lookup"><span data-stu-id="ae45f-104">The **SentOnlyToMe** element indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentOnlyToMe/>true | false</SentOnlyToMe>
```

 <span data-ttu-id="ae45f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae45f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae45f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ae45f-106">Attributes and elements</span></span>

<span data-ttu-id="ae45f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ae45f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae45f-108">属性</span><span class="sxs-lookup"><span data-stu-id="ae45f-108">Attributes</span></span>

<span data-ttu-id="ae45f-109">无。</span><span class="sxs-lookup"><span data-stu-id="ae45f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae45f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ae45f-110">Child elements</span></span>

<span data-ttu-id="ae45f-111">无。</span><span class="sxs-lookup"><span data-stu-id="ae45f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae45f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ae45f-112">Parent elements</span></span>

|<span data-ttu-id="ae45f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae45f-113">**Element**</span></span>|<span data-ttu-id="ae45f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae45f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae45f-115">条件</span><span class="sxs-lookup"><span data-stu-id="ae45f-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="ae45f-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="ae45f-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="ae45f-117">异常</span><span class="sxs-lookup"><span data-stu-id="ae45f-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="ae45f-118">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="ae45f-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ae45f-119">文本值</span><span class="sxs-lookup"><span data-stu-id="ae45f-119">Text value</span></span>

<span data-ttu-id="ae45f-120">文本值为**true**指示邮箱的所有者必须是中的条件或例外应用的顺序的传入消息的**ToRecipients**属性中只能有一个。</span><span class="sxs-lookup"><span data-stu-id="ae45f-120">A text value of **true** indicates that the owner of the mailbox must be the only one in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="ae45f-121">如果值为**false**指示邮箱所有者不得中的条件或例外应用的顺序的传入消息的**ToRecipients**属性中只能有一个。</span><span class="sxs-lookup"><span data-stu-id="ae45f-121">A value of **false** indicates that the owner of the mailbox must not be the only one in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ae45f-122">备注</span><span class="sxs-lookup"><span data-stu-id="ae45f-122">Remarks</span></span>

<span data-ttu-id="ae45f-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ae45f-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae45f-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="ae45f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae45f-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="ae45f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ae45f-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="ae45f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ae45f-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="ae45f-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ae45f-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="ae45f-128">Validation File</span></span>  <br/> |<span data-ttu-id="ae45f-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ae45f-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ae45f-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="ae45f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae45f-131">True</span><span class="sxs-lookup"><span data-stu-id="ae45f-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae45f-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae45f-132">See also</span></span>



- [<span data-ttu-id="ae45f-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ae45f-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

