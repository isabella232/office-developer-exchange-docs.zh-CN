---
title: RoutingType (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 74d83198-0d9d-4c78-a2bc-9a671859ff37
description: RoutingType 元素表示收件人的路由协议。
ms.openlocfilehash: 2193e72c38c687669f6e052b4d2526029aa89d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459032"
---
# <a name="routingtype-emailaddress"></a><span data-ttu-id="422f0-103">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="422f0-103">RoutingType (EmailAddress)</span></span>

<span data-ttu-id="422f0-104">**RoutingType**元素表示收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="422f0-104">The **RoutingType** element represents the routing protocol for the recipient.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="422f0-105">**string**</span><span class="sxs-lookup"><span data-stu-id="422f0-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="422f0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="422f0-106">Attributes and elements</span></span>

<span data-ttu-id="422f0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="422f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="422f0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="422f0-108">Attributes</span></span>

<span data-ttu-id="422f0-109">无。</span><span class="sxs-lookup"><span data-stu-id="422f0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="422f0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="422f0-110">Child elements</span></span>

<span data-ttu-id="422f0-111">无。</span><span class="sxs-lookup"><span data-stu-id="422f0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="422f0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="422f0-112">Parent elements</span></span>

|<span data-ttu-id="422f0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="422f0-113">**Element**</span></span>|<span data-ttu-id="422f0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="422f0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="422f0-115">电子邮件（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="422f0-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="422f0-116">指定 MailboxData 对象的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="422f0-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="422f0-117">此元素在[GetUserAvailability 操作](getuseravailability-operation.md)中使用。</span><span class="sxs-lookup"><span data-stu-id="422f0-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/><br/> <span data-ttu-id="422f0-118">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="422f0-118">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="422f0-119">邮箱（可用性）</span><span class="sxs-lookup"><span data-stu-id="422f0-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="422f0-120">表示 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="422f0-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="422f0-121">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="422f0-121">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="422f0-122">文本值</span><span class="sxs-lookup"><span data-stu-id="422f0-122">Text value</span></span>

<span data-ttu-id="422f0-123">文本值是可选的。</span><span class="sxs-lookup"><span data-stu-id="422f0-123">A text value is optional.</span></span> <span data-ttu-id="422f0-124">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="422f0-124">The following are the possible values:</span></span>

* <span data-ttu-id="422f0-125">SMTP</span><span class="sxs-lookup"><span data-stu-id="422f0-125">SMTP</span></span>
* <span data-ttu-id="422f0-126">EX</span><span class="sxs-lookup"><span data-stu-id="422f0-126">EX</span></span>

<span data-ttu-id="422f0-127">如果未提供任何值，则使用 SMTP 的默认值。</span><span class="sxs-lookup"><span data-stu-id="422f0-127">If no value is provided, the default value of SMTP is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="422f0-128">备注</span><span class="sxs-lookup"><span data-stu-id="422f0-128">Remarks</span></span>

<span data-ttu-id="422f0-129">此元素最多可在[电子邮件（EmailAddressType）](email-emailaddresstype.md)元素中出现一次。</span><span class="sxs-lookup"><span data-stu-id="422f0-129">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="422f0-130">此元素不是必需的。</span><span class="sxs-lookup"><span data-stu-id="422f0-130">This element is not required.</span></span> <span data-ttu-id="422f0-131">此元素存在，以包含将来的协议。</span><span class="sxs-lookup"><span data-stu-id="422f0-131">This element exists for the inclusion of future protocols.</span></span> <span data-ttu-id="422f0-132">另一个**RoutingType**元素用于访问用户邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="422f0-132">Another **RoutingType** element is used for accessing items in a user's mailbox.</span></span> 
  
<span data-ttu-id="422f0-133">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="422f0-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="422f0-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="422f0-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="422f0-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="422f0-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="422f0-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="422f0-136">Schema Name</span></span>  <br/> |<span data-ttu-id="422f0-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="422f0-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="422f0-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="422f0-138">Validation File</span></span>  <br/> |<span data-ttu-id="422f0-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="422f0-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="422f0-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="422f0-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="422f0-141">False</span><span class="sxs-lookup"><span data-stu-id="422f0-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="422f0-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="422f0-142">See also</span></span>

- [<span data-ttu-id="422f0-143">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="422f0-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="422f0-144">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="422f0-144">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="422f0-145">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="422f0-145">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

