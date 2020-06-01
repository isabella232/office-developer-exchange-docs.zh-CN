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
description: IsMeetngResponsequest 元素指示传入的邮件是否必须是会议响应，以便条件或例外情况适用。
ms.openlocfilehash: 40714b7e926768f55207d870b79f21f07163bb37
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465931"
---
# <a name="ismeetingresponse"></a><span data-ttu-id="bbf89-103">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="bbf89-103">IsMeetingResponse</span></span>

<span data-ttu-id="bbf89-104">**IsMeetngResponsequest**元素指示传入的邮件是否必须是会议响应，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="bbf89-104">The **IsMeetngResponsequest** element indicates whether incoming messages must be a meeting response in order for the condition or exception to apply.</span></span> 
  
```XML
<IsMeetingResponse/>true | false</IsMeetingResponse>
```

 <span data-ttu-id="bbf89-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bbf89-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bbf89-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bbf89-106">Attributes and elements</span></span>

<span data-ttu-id="bbf89-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bbf89-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bbf89-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bbf89-108">Attributes</span></span>

<span data-ttu-id="bbf89-109">无。</span><span class="sxs-lookup"><span data-stu-id="bbf89-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bbf89-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bbf89-110">Child elements</span></span>

<span data-ttu-id="bbf89-111">无。</span><span class="sxs-lookup"><span data-stu-id="bbf89-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bbf89-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bbf89-112">Parent elements</span></span>

|<span data-ttu-id="bbf89-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="bbf89-113">**Element**</span></span>|<span data-ttu-id="bbf89-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="bbf89-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bbf89-115">条件</span><span class="sxs-lookup"><span data-stu-id="bbf89-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="bbf89-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="bbf89-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="bbf89-117">异常</span><span class="sxs-lookup"><span data-stu-id="bbf89-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="bbf89-118">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="bbf89-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bbf89-119">文本值</span><span class="sxs-lookup"><span data-stu-id="bbf89-119">Text value</span></span>

<span data-ttu-id="bbf89-120">如果文本值为**true** ，则表示邮件必须是会议响应，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="bbf89-120">A text value of **true** indicates that the message must be a meeting response in order for the condition or exception to apply.</span></span> <span data-ttu-id="bbf89-121">如果文本值为**false** ，则表示邮件必须不是会议响应，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="bbf89-121">A text value of **false** indicates that the message must not be a meeting response in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bbf89-122">说明</span><span class="sxs-lookup"><span data-stu-id="bbf89-122">Remarks</span></span>

<span data-ttu-id="bbf89-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bbf89-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bbf89-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="bbf89-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bbf89-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="bbf89-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bbf89-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="bbf89-126">Schema Name</span></span>  <br/> |<span data-ttu-id="bbf89-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="bbf89-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bbf89-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="bbf89-128">Validation File</span></span>  <br/> |<span data-ttu-id="bbf89-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bbf89-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bbf89-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="bbf89-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="bbf89-131">True</span><span class="sxs-lookup"><span data-stu-id="bbf89-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bbf89-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bbf89-132">See also</span></span>



- [<span data-ttu-id="bbf89-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bbf89-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

