---
title: 地址 （字符串）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: a3cdfcbd-d0c5-46d6-8daa-52405fc63ff0
description: 在 Address 元素表示邮箱用户的电子邮件地址。
ms.openlocfilehash: 07c634d6166d88a8912bc66081a13671e600c801
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753125"
---
# <a name="address-string"></a><span data-ttu-id="1b58e-103">地址 （字符串）</span><span class="sxs-lookup"><span data-stu-id="1b58e-103">Address (string)</span></span>

<span data-ttu-id="1b58e-104">**在 Address**元素表示邮箱用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="1b58e-104">The **Address** element represents the e-mail address of the mailbox user.</span></span> 
  
```xml
<Address>...</Address>
```

 <span data-ttu-id="1b58e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="1b58e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b58e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1b58e-106">Attributes and elements</span></span>

<span data-ttu-id="1b58e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1b58e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b58e-108">属性</span><span class="sxs-lookup"><span data-stu-id="1b58e-108">Attributes</span></span>

<span data-ttu-id="1b58e-109">无。</span><span class="sxs-lookup"><span data-stu-id="1b58e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b58e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1b58e-110">Child elements</span></span>

<span data-ttu-id="1b58e-111">无。</span><span class="sxs-lookup"><span data-stu-id="1b58e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1b58e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1b58e-112">Parent elements</span></span>

|<span data-ttu-id="1b58e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1b58e-113">**Element**</span></span>|<span data-ttu-id="1b58e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1b58e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b58e-115">电子邮件 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="1b58e-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="1b58e-116">指定 MailboxData 对象的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="1b58e-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="1b58e-117">此元素使用[GetUserAvailability 操作](getuseravailability-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="1b58e-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span><br/><br/> <span data-ttu-id="1b58e-118">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="1b58e-118">The following is the XPath to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="1b58e-119">邮箱 （可用性）</span><span class="sxs-lookup"><span data-stu-id="1b58e-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="1b58e-120">表示 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="1b58e-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span><br/><br/>  <span data-ttu-id="1b58e-121">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="1b58e-121">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1b58e-122">文本值</span><span class="sxs-lookup"><span data-stu-id="1b58e-122">Text value</span></span>

<span data-ttu-id="1b58e-123">如果使用此元素，则需要的文本值。</span><span class="sxs-lookup"><span data-stu-id="1b58e-123">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b58e-124">注解</span><span class="sxs-lookup"><span data-stu-id="1b58e-124">Remarks</span></span>

<span data-ttu-id="1b58e-125">此元素可以发生在[电子邮件 (EmailAddressType)](email-emailaddresstype.md)元素和[邮箱 （可用性）](mailbox-availability.md)元素中最一次。</span><span class="sxs-lookup"><span data-stu-id="1b58e-125">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element and the [Mailbox (Availability)](mailbox-availability.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1b58e-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1b58e-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1b58e-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="1b58e-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b58e-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="1b58e-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1b58e-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="1b58e-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1b58e-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="1b58e-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="1b58e-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="1b58e-131">Validation File</span></span>  <br/> |<span data-ttu-id="1b58e-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1b58e-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1b58e-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="1b58e-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1b58e-134">False</span><span class="sxs-lookup"><span data-stu-id="1b58e-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b58e-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1b58e-135">See also</span></span>

- [<span data-ttu-id="1b58e-136">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="1b58e-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="1b58e-137">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="1b58e-137">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="1b58e-138">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="1b58e-138">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="1b58e-139">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="1b58e-139">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="1b58e-140">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="1b58e-140">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
- [<span data-ttu-id="1b58e-141">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="1b58e-141">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
- [<span data-ttu-id="1b58e-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="1b58e-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

