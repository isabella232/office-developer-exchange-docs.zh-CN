---
title: 名称（EmailAddress）
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
ms.openlocfilehash: 2c6b29f1b069f9cc72ac84e7aebfff99437e630a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466953"
---
# <a name="name-emailaddress"></a><span data-ttu-id="d5078-103">名称（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="d5078-103">Name (EmailAddress)</span></span>

<span data-ttu-id="d5078-104">**Name**元素表示邮箱用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="d5078-104">The **Name** element represents the display name of the mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="d5078-105">**String**</span><span class="sxs-lookup"><span data-stu-id="d5078-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d5078-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d5078-106">Attributes and elements</span></span>

<span data-ttu-id="d5078-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d5078-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5078-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d5078-108">Attributes</span></span>

<span data-ttu-id="d5078-109">无。</span><span class="sxs-lookup"><span data-stu-id="d5078-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5078-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d5078-110">Child elements</span></span>

<span data-ttu-id="d5078-111">无。</span><span class="sxs-lookup"><span data-stu-id="d5078-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d5078-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d5078-112">Parent elements</span></span>

|<span data-ttu-id="d5078-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d5078-113">**Element**</span></span>|<span data-ttu-id="d5078-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d5078-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5078-115">电子邮件（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="d5078-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="d5078-116">表示 GetUserAvailability 查询的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="d5078-116">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> <br/><span data-ttu-id="d5078-117">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="d5078-117">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="d5078-118">邮箱（可用性）</span><span class="sxs-lookup"><span data-stu-id="d5078-118">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="d5078-119">表示 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="d5078-119">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="d5078-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="d5078-120">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d5078-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d5078-121">Text value</span></span>

<span data-ttu-id="d5078-122">如果使用此元素，则需要一个 text 值。</span><span class="sxs-lookup"><span data-stu-id="d5078-122">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5078-123">备注</span><span class="sxs-lookup"><span data-stu-id="d5078-123">Remarks</span></span>

<span data-ttu-id="d5078-124">此元素最多可在[电子邮件（EmailAddressType）](email-emailaddresstype.md)元素中出现一次。</span><span class="sxs-lookup"><span data-stu-id="d5078-124">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="d5078-125">此元素不是必需的。</span><span class="sxs-lookup"><span data-stu-id="d5078-125">This element is not required.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d5078-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d5078-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d5078-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="d5078-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5078-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="d5078-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5078-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="d5078-129">Schema Name</span></span>  <br/> |<span data-ttu-id="d5078-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="d5078-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5078-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="d5078-131">Validation File</span></span>  <br/> |<span data-ttu-id="d5078-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d5078-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5078-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="d5078-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5078-134">False</span><span class="sxs-lookup"><span data-stu-id="d5078-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5078-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d5078-135">See also</span></span>

- [<span data-ttu-id="d5078-136">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="d5078-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="d5078-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="d5078-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="d5078-138">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="d5078-138">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

