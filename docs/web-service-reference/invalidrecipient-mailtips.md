---
title: InvalidRecipient （邮件提示）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipient
api_type:
- schema
ms.assetid: 48959a99-bb0d-4004-963e-5a5baaa96476
description: InvalidRecipient 元素指示收件人是否无效。
ms.openlocfilehash: fddd75beb2228c50084bd38b4f4745064cc281dc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530000"
---
# <a name="invalidrecipient-mailtips"></a><span data-ttu-id="b0da5-103">InvalidRecipient （邮件提示）</span><span class="sxs-lookup"><span data-stu-id="b0da5-103">InvalidRecipient (MailTips)</span></span>

<span data-ttu-id="b0da5-104">**InvalidRecipient**元素指示收件人是否无效。</span><span class="sxs-lookup"><span data-stu-id="b0da5-104">The **InvalidRecipient** element indicates whether the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>true | false</InvalidRecipient>
```

 <span data-ttu-id="b0da5-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b0da5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0da5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b0da5-106">Attributes and elements</span></span>

<span data-ttu-id="b0da5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b0da5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0da5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b0da5-108">Attributes</span></span>

<span data-ttu-id="b0da5-109">无。</span><span class="sxs-lookup"><span data-stu-id="b0da5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0da5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b0da5-110">Child elements</span></span>

<span data-ttu-id="b0da5-111">无。</span><span class="sxs-lookup"><span data-stu-id="b0da5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0da5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b0da5-112">Parent elements</span></span>

|<span data-ttu-id="b0da5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0da5-113">**Element**</span></span>|<span data-ttu-id="b0da5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0da5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0da5-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="b0da5-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="b0da5-116">表示各种邮件提示类型的值。</span><span class="sxs-lookup"><span data-stu-id="b0da5-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b0da5-117">文本值</span><span class="sxs-lookup"><span data-stu-id="b0da5-117">Text value</span></span>

<span data-ttu-id="b0da5-118">如果收件人无效，则此元素的文本值为**true** 。</span><span class="sxs-lookup"><span data-stu-id="b0da5-118">The text value of this element is **true** if the recipient is invalid.</span></span> <span data-ttu-id="b0da5-119">如果收件人无效，则该值为**false** 。</span><span class="sxs-lookup"><span data-stu-id="b0da5-119">The value is **false** if the recipient is not invalid.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b0da5-120">说明</span><span class="sxs-lookup"><span data-stu-id="b0da5-120">Remarks</span></span>

<span data-ttu-id="b0da5-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b0da5-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0da5-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="b0da5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0da5-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="b0da5-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0da5-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="b0da5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="b0da5-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="b0da5-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="b0da5-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="b0da5-126">Validation File</span></span>  <br/> |<span data-ttu-id="b0da5-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b0da5-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0da5-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="b0da5-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="b0da5-129">False</span><span class="sxs-lookup"><span data-stu-id="b0da5-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0da5-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b0da5-130">See also</span></span>



- [<span data-ttu-id="b0da5-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b0da5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

