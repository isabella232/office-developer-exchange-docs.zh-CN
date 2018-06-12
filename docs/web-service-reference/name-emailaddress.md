---
title: 名称 （电子邮件地址）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: c719c55f-d625-4e64-846f-50ac91881443
description: Name 元素表示邮箱用户的显示名称。
ms.openlocfilehash: 6d30f06c3bfd77d2715798349ab084cdf81f21a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826505"
---
# <a name="name-emailaddress"></a><span data-ttu-id="36a5a-103">名称 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="36a5a-103">Name (EmailAddress)</span></span>

<span data-ttu-id="36a5a-104">**Name**元素表示邮箱用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="36a5a-104">The **Name** element represents the display name of the mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="36a5a-105">**字符串**</span><span class="sxs-lookup"><span data-stu-id="36a5a-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="36a5a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="36a5a-106">Attributes and elements</span></span>

<span data-ttu-id="36a5a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="36a5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36a5a-108">属性</span><span class="sxs-lookup"><span data-stu-id="36a5a-108">Attributes</span></span>

<span data-ttu-id="36a5a-109">无。</span><span class="sxs-lookup"><span data-stu-id="36a5a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36a5a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="36a5a-110">Child elements</span></span>

<span data-ttu-id="36a5a-111">无。</span><span class="sxs-lookup"><span data-stu-id="36a5a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="36a5a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="36a5a-112">Parent elements</span></span>

|<span data-ttu-id="36a5a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="36a5a-113">**Element**</span></span>|<span data-ttu-id="36a5a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="36a5a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36a5a-115">电子邮件 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="36a5a-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="36a5a-116">表示 GetUserAvailability 查询的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="36a5a-116">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> <br/><span data-ttu-id="36a5a-117">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="36a5a-117">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="36a5a-118">邮箱 （可用性）</span><span class="sxs-lookup"><span data-stu-id="36a5a-118">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="36a5a-119">表示 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="36a5a-119">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="36a5a-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="36a5a-120">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36a5a-121">文本值</span><span class="sxs-lookup"><span data-stu-id="36a5a-121">Text value</span></span>

<span data-ttu-id="36a5a-122">如果使用此元素，则需要的文本值。</span><span class="sxs-lookup"><span data-stu-id="36a5a-122">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36a5a-123">备注</span><span class="sxs-lookup"><span data-stu-id="36a5a-123">Remarks</span></span>

<span data-ttu-id="36a5a-124">此元素可以发生最一次中的[电子邮件 (EmailAddressType)](email-emailaddresstype.md)元素。</span><span class="sxs-lookup"><span data-stu-id="36a5a-124">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="36a5a-125">此元素不是必需的。</span><span class="sxs-lookup"><span data-stu-id="36a5a-125">This element is not required.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="36a5a-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="36a5a-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="36a5a-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="36a5a-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36a5a-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="36a5a-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="36a5a-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="36a5a-129">Schema Name</span></span>  <br/> |<span data-ttu-id="36a5a-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="36a5a-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="36a5a-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="36a5a-131">Validation File</span></span>  <br/> |<span data-ttu-id="36a5a-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="36a5a-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="36a5a-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="36a5a-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="36a5a-134">False</span><span class="sxs-lookup"><span data-stu-id="36a5a-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36a5a-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36a5a-135">See also</span></span>

- [<span data-ttu-id="36a5a-136">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="36a5a-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="36a5a-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="36a5a-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="36a5a-138">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="36a5a-138">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

