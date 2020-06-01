---
title: DeliveryRestricted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryRestricted
api_type:
- schema
ms.assetid: 05989915-121c-4f26-93cc-af8d454ab442
description: DeliveryRestricted 元素指示传递限制是否将阻止发件人的邮件到达收件人。
ms.openlocfilehash: 58fc85873326179d7745db4ba7d4854a76ced6a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462687"
---
# <a name="deliveryrestricted"></a><span data-ttu-id="e3b2a-103">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="e3b2a-103">DeliveryRestricted</span></span>

<span data-ttu-id="e3b2a-104">**DeliveryRestricted**元素指示传递限制是否将阻止发件人的邮件到达收件人。</span><span class="sxs-lookup"><span data-stu-id="e3b2a-104">The **DeliveryRestricted** element indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> 
  
```XML
<DeliveryRestricted>true | false</DeliveryRestricted>
```

 <span data-ttu-id="e3b2a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e3b2a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3b2a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e3b2a-106">Attributes and elements</span></span>

<span data-ttu-id="e3b2a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e3b2a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3b2a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e3b2a-108">Attributes</span></span>

<span data-ttu-id="e3b2a-109">无。</span><span class="sxs-lookup"><span data-stu-id="e3b2a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3b2a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e3b2a-110">Child elements</span></span>

<span data-ttu-id="e3b2a-111">无。</span><span class="sxs-lookup"><span data-stu-id="e3b2a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3b2a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e3b2a-112">Parent elements</span></span>

|<span data-ttu-id="e3b2a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e3b2a-113">**Element**</span></span>|<span data-ttu-id="e3b2a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3b2a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3b2a-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="e3b2a-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="e3b2a-116">表示各种邮件提示类型的值。</span><span class="sxs-lookup"><span data-stu-id="e3b2a-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3b2a-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e3b2a-117">Text value</span></span>

<span data-ttu-id="e3b2a-118">如果传递限制将阻止发件人的邮件到达收件人，则此元素的文本值为**true** 。</span><span class="sxs-lookup"><span data-stu-id="e3b2a-118">The text value of this element is **true** if delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> <span data-ttu-id="e3b2a-119">如果传递限制不会阻止发件人的邮件到达收件人，则该值为**false** 。</span><span class="sxs-lookup"><span data-stu-id="e3b2a-119">The value is **false** if delivery restrictions will not prevent the sender's message from reaching the recipient.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e3b2a-120">说明</span><span class="sxs-lookup"><span data-stu-id="e3b2a-120">Remarks</span></span>

<span data-ttu-id="e3b2a-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e3b2a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3b2a-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="e3b2a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3b2a-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="e3b2a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e3b2a-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="e3b2a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e3b2a-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="e3b2a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="e3b2a-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="e3b2a-126">Validation File</span></span>  <br/> |<span data-ttu-id="e3b2a-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e3b2a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e3b2a-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="e3b2a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3b2a-129">False</span><span class="sxs-lookup"><span data-stu-id="e3b2a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3b2a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3b2a-130">See also</span></span>

- [<span data-ttu-id="e3b2a-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e3b2a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

