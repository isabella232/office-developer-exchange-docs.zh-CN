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
description: InvalidRecipient 元素表示是否收件人无效。
ms.openlocfilehash: addb86ece2be3091ac55a52ee2f16f5c5f72ae41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825958"
---
# <a name="invalidrecipient-mailtips"></a><span data-ttu-id="bf202-103">InvalidRecipient （邮件提示）</span><span class="sxs-lookup"><span data-stu-id="bf202-103">InvalidRecipient (MailTips)</span></span>

<span data-ttu-id="bf202-104">**InvalidRecipient**元素表示是否收件人无效。</span><span class="sxs-lookup"><span data-stu-id="bf202-104">The **InvalidRecipient** element indicates whether the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>true | false</InvalidRecipient>
```

 <span data-ttu-id="bf202-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bf202-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bf202-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bf202-106">Attributes and elements</span></span>

<span data-ttu-id="bf202-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bf202-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf202-108">属性</span><span class="sxs-lookup"><span data-stu-id="bf202-108">Attributes</span></span>

<span data-ttu-id="bf202-109">无。</span><span class="sxs-lookup"><span data-stu-id="bf202-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf202-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bf202-110">Child elements</span></span>

<span data-ttu-id="bf202-111">无。</span><span class="sxs-lookup"><span data-stu-id="bf202-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bf202-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bf202-112">Parent elements</span></span>

|<span data-ttu-id="bf202-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="bf202-113">**Element**</span></span>|<span data-ttu-id="bf202-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="bf202-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf202-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="bf202-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="bf202-116">表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="bf202-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bf202-117">文本值</span><span class="sxs-lookup"><span data-stu-id="bf202-117">Text value</span></span>

<span data-ttu-id="bf202-118">如果收件人无效，此元素的文本值为**true** 。</span><span class="sxs-lookup"><span data-stu-id="bf202-118">The text value of this element is **true** if the recipient is invalid.</span></span> <span data-ttu-id="bf202-119">如果收件人不是无效，则值为**false** 。</span><span class="sxs-lookup"><span data-stu-id="bf202-119">The value is **false** if the recipient is not invalid.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bf202-120">备注</span><span class="sxs-lookup"><span data-stu-id="bf202-120">Remarks</span></span>

<span data-ttu-id="bf202-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bf202-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf202-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="bf202-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf202-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="bf202-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bf202-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="bf202-124">Schema Name</span></span>  <br/> |<span data-ttu-id="bf202-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="bf202-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="bf202-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="bf202-126">Validation File</span></span>  <br/> |<span data-ttu-id="bf202-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bf202-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bf202-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="bf202-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="bf202-129">False</span><span class="sxs-lookup"><span data-stu-id="bf202-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf202-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bf202-130">See also</span></span>



- [<span data-ttu-id="bf202-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bf202-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

