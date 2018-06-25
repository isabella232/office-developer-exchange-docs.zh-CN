---
title: 收件人 (ArrayOfRecipientsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipients
api_type:
- schema
ms.assetid: f4b71403-cbae-4176-8b2e-3597048c057b
description: 收件人元素均表示接收邮件的副本的收件人的集合。
ms.openlocfilehash: b24a029bfacd6cc40e85a201b8ca90efd7790e9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826991"
---
# <a name="recipients-arrayofrecipientstype"></a><span data-ttu-id="35e92-103">收件人 (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="35e92-103">Recipients (ArrayOfRecipientsType)</span></span>

<span data-ttu-id="35e92-104">**收件人**元素均表示接收邮件的副本的收件人的集合。</span><span class="sxs-lookup"><span data-stu-id="35e92-104">The **Recipients** element represents a collection of recipients that receive a copy of the message.</span></span> 
  
```XML
<Recipients>
   <Mailbox/>
</Recipients>
```

 <span data-ttu-id="35e92-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="35e92-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35e92-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="35e92-106">Attributes and elements</span></span>

<span data-ttu-id="35e92-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="35e92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35e92-108">属性</span><span class="sxs-lookup"><span data-stu-id="35e92-108">Attributes</span></span>

<span data-ttu-id="35e92-109">无。</span><span class="sxs-lookup"><span data-stu-id="35e92-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35e92-110">子元素</span><span class="sxs-lookup"><span data-stu-id="35e92-110">Child elements</span></span>

|<span data-ttu-id="35e92-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="35e92-111">**Element**</span></span>|<span data-ttu-id="35e92-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="35e92-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35e92-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="35e92-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="35e92-114">标识已启用邮件的 Active Directory 对象。</span><span class="sxs-lookup"><span data-stu-id="35e92-114">Identifies a mail-enabled Active Directory object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="35e92-115">父元素</span><span class="sxs-lookup"><span data-stu-id="35e92-115">Parent elements</span></span>

|<span data-ttu-id="35e92-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="35e92-116">**Element**</span></span>|<span data-ttu-id="35e92-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="35e92-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35e92-118">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="35e92-118">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="35e92-119">包含要检索的收件人和类型的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="35e92-119">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="35e92-120">文本值</span><span class="sxs-lookup"><span data-stu-id="35e92-120">Text value</span></span>

<span data-ttu-id="35e92-121">无。</span><span class="sxs-lookup"><span data-stu-id="35e92-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35e92-122">备注</span><span class="sxs-lookup"><span data-stu-id="35e92-122">Remarks</span></span>

<span data-ttu-id="35e92-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="35e92-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35e92-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="35e92-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35e92-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="35e92-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35e92-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="35e92-126">Schema Name</span></span>  <br/> |<span data-ttu-id="35e92-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="35e92-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="35e92-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="35e92-128">Validation File</span></span>  <br/> |<span data-ttu-id="35e92-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="35e92-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="35e92-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="35e92-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="35e92-131">False</span><span class="sxs-lookup"><span data-stu-id="35e92-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35e92-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35e92-132">See also</span></span>



- [<span data-ttu-id="35e92-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="35e92-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

