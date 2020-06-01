---
title: 收件人（ArrayOfRecipientsType）
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
description: 收件人元素表示接收邮件副本的收件人的集合。
ms.openlocfilehash: 0e18152a8143b888ad27f48137c06613694f5713
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463872"
---
# <a name="recipients-arrayofrecipientstype"></a><span data-ttu-id="6f768-103">收件人（ArrayOfRecipientsType）</span><span class="sxs-lookup"><span data-stu-id="6f768-103">Recipients (ArrayOfRecipientsType)</span></span>

<span data-ttu-id="6f768-104">**收件人**元素表示接收邮件副本的收件人的集合。</span><span class="sxs-lookup"><span data-stu-id="6f768-104">The **Recipients** element represents a collection of recipients that receive a copy of the message.</span></span> 
  
```XML
<Recipients>
   <Mailbox/>
</Recipients>
```

 <span data-ttu-id="6f768-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="6f768-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f768-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f768-106">Attributes and elements</span></span>

<span data-ttu-id="6f768-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f768-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f768-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6f768-108">Attributes</span></span>

<span data-ttu-id="6f768-109">无。</span><span class="sxs-lookup"><span data-stu-id="6f768-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f768-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6f768-110">Child elements</span></span>

|<span data-ttu-id="6f768-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f768-111">**Element**</span></span>|<span data-ttu-id="6f768-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f768-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f768-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="6f768-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="6f768-114">标识已启用邮件的 Active Directory 对象。</span><span class="sxs-lookup"><span data-stu-id="6f768-114">Identifies a mail-enabled Active Directory object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f768-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6f768-115">Parent elements</span></span>

|<span data-ttu-id="6f768-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f768-116">**Element**</span></span>|<span data-ttu-id="6f768-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f768-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f768-118">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="6f768-118">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="6f768-119">包含要检索的邮件提示的收件人和类型。</span><span class="sxs-lookup"><span data-stu-id="6f768-119">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6f768-120">文本值</span><span class="sxs-lookup"><span data-stu-id="6f768-120">Text value</span></span>

<span data-ttu-id="6f768-121">无。</span><span class="sxs-lookup"><span data-stu-id="6f768-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f768-122">说明</span><span class="sxs-lookup"><span data-stu-id="6f768-122">Remarks</span></span>

<span data-ttu-id="6f768-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6f768-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f768-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f768-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f768-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f768-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f768-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f768-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6f768-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="6f768-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f768-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f768-128">Validation File</span></span>  <br/> |<span data-ttu-id="6f768-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6f768-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f768-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f768-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f768-131">False</span><span class="sxs-lookup"><span data-stu-id="6f768-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f768-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f768-132">See also</span></span>



- [<span data-ttu-id="6f768-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6f768-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

