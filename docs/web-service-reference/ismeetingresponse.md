---
title: IsMeetingResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsMeetingResponse
api_type:
- schema
ms.assetid: 85090943-81c6-4fbe-a2db-007dced6a4cf
description: IsMeetngResponsequest 元素指示传入邮件是否必须是会议响应中的条件或例外应用的顺序。
ms.openlocfilehash: 9040859452a48916a969b6d8e4e370b5785c1c1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826053"
---
# <a name="ismeetingresponse"></a><span data-ttu-id="cf35f-103">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="cf35f-103">IsMeetingResponse</span></span>

<span data-ttu-id="cf35f-104">**IsMeetngResponsequest**元素指示传入邮件是否必须是会议响应中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="cf35f-104">The **IsMeetngResponsequest** element indicates whether incoming messages must be a meeting response in order for the condition or exception to apply.</span></span> 
  
```XML
<IsMeetingResponse/>true | false</IsMeetingResponse>
```

 <span data-ttu-id="cf35f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cf35f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf35f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cf35f-106">Attributes and elements</span></span>

<span data-ttu-id="cf35f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cf35f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf35f-108">属性</span><span class="sxs-lookup"><span data-stu-id="cf35f-108">Attributes</span></span>

<span data-ttu-id="cf35f-109">无。</span><span class="sxs-lookup"><span data-stu-id="cf35f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cf35f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cf35f-110">Child elements</span></span>

<span data-ttu-id="cf35f-111">无。</span><span class="sxs-lookup"><span data-stu-id="cf35f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cf35f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cf35f-112">Parent elements</span></span>

|<span data-ttu-id="cf35f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cf35f-113">**Element**</span></span>|<span data-ttu-id="cf35f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf35f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf35f-115">条件</span><span class="sxs-lookup"><span data-stu-id="cf35f-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="cf35f-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="cf35f-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="cf35f-117">异常</span><span class="sxs-lookup"><span data-stu-id="cf35f-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="cf35f-118">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="cf35f-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cf35f-119">文本值</span><span class="sxs-lookup"><span data-stu-id="cf35f-119">Text value</span></span>

<span data-ttu-id="cf35f-120">文本值为**true**指示邮件必须会议响应中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="cf35f-120">A text value of **true** indicates that the message must be a meeting response in order for the condition or exception to apply.</span></span> <span data-ttu-id="cf35f-121">文本值为**false**指示邮件不得会议响应中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="cf35f-121">A text value of **false** indicates that the message must not be a meeting response in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf35f-122">备注</span><span class="sxs-lookup"><span data-stu-id="cf35f-122">Remarks</span></span>

<span data-ttu-id="cf35f-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cf35f-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf35f-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="cf35f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf35f-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="cf35f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cf35f-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="cf35f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="cf35f-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="cf35f-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cf35f-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="cf35f-128">Validation File</span></span>  <br/> |<span data-ttu-id="cf35f-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cf35f-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf35f-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="cf35f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf35f-131">True</span><span class="sxs-lookup"><span data-stu-id="cf35f-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf35f-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cf35f-132">See also</span></span>



- [<span data-ttu-id="cf35f-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cf35f-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

