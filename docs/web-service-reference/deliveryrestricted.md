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
description: DeliveryRestricted 元素指示传递限制是否将到达收件人阻止发件人的邮件。
ms.openlocfilehash: ba1c6e00b93c9e442a427fe98a5e15bf5fe1effd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753834"
---
# <a name="deliveryrestricted"></a><span data-ttu-id="dc2ce-103">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="dc2ce-103">DeliveryRestricted</span></span>

<span data-ttu-id="dc2ce-104">**DeliveryRestricted**元素指示传递限制是否将到达收件人阻止发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="dc2ce-104">The **DeliveryRestricted** element indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> 
  
```XML
<DeliveryRestricted>true | false</DeliveryRestricted>
```

 <span data-ttu-id="dc2ce-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc2ce-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc2ce-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc2ce-106">Attributes and elements</span></span>

<span data-ttu-id="dc2ce-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc2ce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc2ce-108">属性</span><span class="sxs-lookup"><span data-stu-id="dc2ce-108">Attributes</span></span>

<span data-ttu-id="dc2ce-109">无。</span><span class="sxs-lookup"><span data-stu-id="dc2ce-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc2ce-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dc2ce-110">Child elements</span></span>

<span data-ttu-id="dc2ce-111">无。</span><span class="sxs-lookup"><span data-stu-id="dc2ce-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc2ce-112">父元素</span><span class="sxs-lookup"><span data-stu-id="dc2ce-112">Parent elements</span></span>

|<span data-ttu-id="dc2ce-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc2ce-113">**Element**</span></span>|<span data-ttu-id="dc2ce-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc2ce-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc2ce-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="dc2ce-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="dc2ce-116">表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="dc2ce-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dc2ce-117">文本值</span><span class="sxs-lookup"><span data-stu-id="dc2ce-117">Text value</span></span>

<span data-ttu-id="dc2ce-118">此元素的文本值为**true** ，如果传递限制将会到达收件人阻止发件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="dc2ce-118">The text value of this element is **true** if delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> <span data-ttu-id="dc2ce-119">如果传递限制不会阻止发件人的邮件到达收件人，则值为**false** 。</span><span class="sxs-lookup"><span data-stu-id="dc2ce-119">The value is **false** if delivery restrictions will not prevent the sender's message from reaching the recipient.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dc2ce-120">备注</span><span class="sxs-lookup"><span data-stu-id="dc2ce-120">Remarks</span></span>

<span data-ttu-id="dc2ce-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dc2ce-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc2ce-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="dc2ce-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc2ce-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="dc2ce-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc2ce-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="dc2ce-124">Schema Name</span></span>  <br/> |<span data-ttu-id="dc2ce-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="dc2ce-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc2ce-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="dc2ce-126">Validation File</span></span>  <br/> |<span data-ttu-id="dc2ce-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc2ce-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc2ce-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="dc2ce-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc2ce-129">False</span><span class="sxs-lookup"><span data-stu-id="dc2ce-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc2ce-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc2ce-130">See also</span></span>

- [<span data-ttu-id="dc2ce-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dc2ce-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

