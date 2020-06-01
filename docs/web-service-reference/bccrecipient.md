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
description: BccRecipient 元素表示接收电子邮件的密件抄送（Bcc）的收件人。
ms.openlocfilehash: 8296af1d74338bdfb1f4cb7bc7449ad91a9cd531
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461525"
---
# <a name="bccrecipient"></a><span data-ttu-id="86cc1-103">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="86cc1-103">BccRecipient</span></span>

<span data-ttu-id="86cc1-104">**BccRecipient**元素表示接收电子邮件的密件抄送（Bcc）的收件人。</span><span class="sxs-lookup"><span data-stu-id="86cc1-104">The **BccRecipient** element represents a recipient to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```XML
<BccRecipient>true | false</BccRecipient>
```

 <span data-ttu-id="86cc1-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="86cc1-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86cc1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="86cc1-106">Attributes and elements</span></span>

<span data-ttu-id="86cc1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="86cc1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86cc1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="86cc1-108">Attributes</span></span>

<span data-ttu-id="86cc1-109">无。</span><span class="sxs-lookup"><span data-stu-id="86cc1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86cc1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="86cc1-110">Child elements</span></span>

<span data-ttu-id="86cc1-111">无。</span><span class="sxs-lookup"><span data-stu-id="86cc1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="86cc1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="86cc1-112">Parent elements</span></span>

|<span data-ttu-id="86cc1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="86cc1-113">**Element**</span></span>|<span data-ttu-id="86cc1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="86cc1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86cc1-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="86cc1-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="86cc1-116">包含收件人的单个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="86cc1-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="86cc1-117">文本值</span><span class="sxs-lookup"><span data-stu-id="86cc1-117">Text value</span></span>

<span data-ttu-id="86cc1-118">此元素可以是**true** ，也可以是**false**。</span><span class="sxs-lookup"><span data-stu-id="86cc1-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="86cc1-119">**如果值为 true** ，则表示收件人已复制密件抄送;**如果值为 false** ，则表示收件人不复制密件抄送。</span><span class="sxs-lookup"><span data-stu-id="86cc1-119">A value of **true** indicates that the recipient is blind carbon copied; a value of **false** indicates that the recipient is not blind carbon copied.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="86cc1-120">说明</span><span class="sxs-lookup"><span data-stu-id="86cc1-120">Remarks</span></span>

<span data-ttu-id="86cc1-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="86cc1-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86cc1-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="86cc1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86cc1-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="86cc1-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="86cc1-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="86cc1-124">Schema Name</span></span>  <br/> |<span data-ttu-id="86cc1-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="86cc1-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="86cc1-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="86cc1-126">Validation File</span></span>  <br/> |<span data-ttu-id="86cc1-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="86cc1-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="86cc1-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="86cc1-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="86cc1-129">False</span><span class="sxs-lookup"><span data-stu-id="86cc1-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86cc1-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="86cc1-130">See also</span></span>



- [<span data-ttu-id="86cc1-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="86cc1-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

