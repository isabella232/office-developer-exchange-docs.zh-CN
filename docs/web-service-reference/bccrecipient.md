---
title: BccRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BccRecipient
api_type:
- schema
ms.assetid: 4ef0cff5-8a5a-4d76-9d2b-938774d8fc1b
description: BccRecipient 元素均表示接收的电子邮件的密件抄送 (Bcc) 收件人。
ms.openlocfilehash: bed58536263196a61651493e92a4dcd1df3f5ec9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753318"
---
# <a name="bccrecipient"></a><span data-ttu-id="7aae5-103">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="7aae5-103">BccRecipient</span></span>

<span data-ttu-id="7aae5-104">**BccRecipient**元素均表示接收的电子邮件的密件抄送 (Bcc) 收件人。</span><span class="sxs-lookup"><span data-stu-id="7aae5-104">The **BccRecipient** element represents a recipient to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```XML
<BccRecipient>true | false</BccRecipient>
```

 <span data-ttu-id="7aae5-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7aae5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7aae5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7aae5-106">Attributes and elements</span></span>

<span data-ttu-id="7aae5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7aae5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7aae5-108">属性</span><span class="sxs-lookup"><span data-stu-id="7aae5-108">Attributes</span></span>

<span data-ttu-id="7aae5-109">无。</span><span class="sxs-lookup"><span data-stu-id="7aae5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7aae5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7aae5-110">Child elements</span></span>

<span data-ttu-id="7aae5-111">无。</span><span class="sxs-lookup"><span data-stu-id="7aae5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7aae5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7aae5-112">Parent elements</span></span>

|<span data-ttu-id="7aae5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7aae5-113">**Element**</span></span>|<span data-ttu-id="7aae5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7aae5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7aae5-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="7aae5-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="7aae5-116">包含收件人为一个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="7aae5-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7aae5-117">文本值</span><span class="sxs-lookup"><span data-stu-id="7aae5-117">Text value</span></span>

<span data-ttu-id="7aae5-118">此元素可以是**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="7aae5-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="7aae5-119">值为**true**指示收件人是密件抄送复制;如果值为**false**指示收件人不是复制的密件抄送。</span><span class="sxs-lookup"><span data-stu-id="7aae5-119">A value of **true** indicates that the recipient is blind carbon copied; a value of **false** indicates that the recipient is not blind carbon copied.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7aae5-120">备注</span><span class="sxs-lookup"><span data-stu-id="7aae5-120">Remarks</span></span>

<span data-ttu-id="7aae5-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7aae5-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7aae5-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="7aae5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7aae5-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="7aae5-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7aae5-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="7aae5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7aae5-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="7aae5-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="7aae5-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="7aae5-126">Validation File</span></span>  <br/> |<span data-ttu-id="7aae5-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7aae5-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7aae5-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="7aae5-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="7aae5-129">False</span><span class="sxs-lookup"><span data-stu-id="7aae5-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7aae5-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7aae5-130">See also</span></span>



- [<span data-ttu-id="7aae5-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7aae5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

