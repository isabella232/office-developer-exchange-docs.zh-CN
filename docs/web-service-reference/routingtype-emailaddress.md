---
title: RoutingType （电子邮件地址）
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
ms.openlocfilehash: a0a6cf312bcb1d4b4818a82bc8d8d3e3f33ad6f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827255"
---
# <a name="routingtype-emailaddress"></a><span data-ttu-id="928a4-103">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="928a4-103">RoutingType (EmailAddress)</span></span>

<span data-ttu-id="928a4-104">**RoutingType**元素表示收件人的路由协议。</span><span class="sxs-lookup"><span data-stu-id="928a4-104">The **RoutingType** element represents the routing protocol for the recipient.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="928a4-105">**string**</span><span class="sxs-lookup"><span data-stu-id="928a4-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="928a4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="928a4-106">Attributes and elements</span></span>

<span data-ttu-id="928a4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="928a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="928a4-108">属性</span><span class="sxs-lookup"><span data-stu-id="928a4-108">Attributes</span></span>

<span data-ttu-id="928a4-109">无。</span><span class="sxs-lookup"><span data-stu-id="928a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="928a4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="928a4-110">Child elements</span></span>

<span data-ttu-id="928a4-111">无。</span><span class="sxs-lookup"><span data-stu-id="928a4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="928a4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="928a4-112">Parent elements</span></span>

|<span data-ttu-id="928a4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="928a4-113">**Element**</span></span>|<span data-ttu-id="928a4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="928a4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="928a4-115">电子邮件 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="928a4-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="928a4-116">指定 MailboxData 对象的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="928a4-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="928a4-117">此元素使用[GetUserAvailability 操作](getuseravailability-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="928a4-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/><br/> <span data-ttu-id="928a4-118">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="928a4-118">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="928a4-119">邮箱 （可用性）</span><span class="sxs-lookup"><span data-stu-id="928a4-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="928a4-120">表示 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="928a4-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="928a4-121">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="928a4-121">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="928a4-122">文本值</span><span class="sxs-lookup"><span data-stu-id="928a4-122">Text value</span></span>

<span data-ttu-id="928a4-123">文本值是可选的。</span><span class="sxs-lookup"><span data-stu-id="928a4-123">A text value is optional.</span></span> <span data-ttu-id="928a4-124">唯一有效的值是 SMTP。</span><span class="sxs-lookup"><span data-stu-id="928a4-124">The only valid value is SMTP.</span></span> <span data-ttu-id="928a4-125">如果未提供值，使用 SMTP 的默认值。</span><span class="sxs-lookup"><span data-stu-id="928a4-125">If no value is provided, the default value of SMTP is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="928a4-126">注解</span><span class="sxs-lookup"><span data-stu-id="928a4-126">Remarks</span></span>

<span data-ttu-id="928a4-127">此元素可以发生最一次中的[电子邮件 (EmailAddressType)](email-emailaddresstype.md)元素。</span><span class="sxs-lookup"><span data-stu-id="928a4-127">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="928a4-128">此元素不是必需的。</span><span class="sxs-lookup"><span data-stu-id="928a4-128">This element is not required.</span></span> <span data-ttu-id="928a4-129">此元素存在包含将来的协议。</span><span class="sxs-lookup"><span data-stu-id="928a4-129">This element exists for the inclusion of future protocols.</span></span> <span data-ttu-id="928a4-130">另一个**RoutingType**元素用于访问用户的邮箱中的项。</span><span class="sxs-lookup"><span data-stu-id="928a4-130">Another **RoutingType** element is used for accessing items in a user's mailbox.</span></span> 
  
<span data-ttu-id="928a4-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="928a4-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="928a4-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="928a4-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="928a4-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="928a4-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="928a4-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="928a4-134">Schema Name</span></span>  <br/> |<span data-ttu-id="928a4-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="928a4-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="928a4-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="928a4-136">Validation File</span></span>  <br/> |<span data-ttu-id="928a4-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="928a4-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="928a4-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="928a4-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="928a4-139">False</span><span class="sxs-lookup"><span data-stu-id="928a4-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="928a4-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="928a4-140">See also</span></span>

- [<span data-ttu-id="928a4-141">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="928a4-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="928a4-142">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="928a4-142">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="928a4-143">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="928a4-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

