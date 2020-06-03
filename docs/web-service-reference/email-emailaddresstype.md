---
title: 电子邮件（EmailAddressType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Email
api_type:
- schema
ms.assetid: dfffa1d5-2c3c-4f56-af63-5853df462e58
description: Email 元素表示 GetUserAvailability 查询的邮箱用户。
ms.openlocfilehash: 2ed8de9c011a385ec6c4ebd2f8d1d47304343a0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459228"
---
# <a name="email-emailaddresstype"></a><span data-ttu-id="06ee8-103">电子邮件（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="06ee8-103">Email (EmailAddressType)</span></span>

<span data-ttu-id="06ee8-104">**Email**元素表示 GetUserAvailability 查询的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="06ee8-104">The **Email** element represents the mailbox user for a GetUserAvailability query.</span></span> 
  
- [<span data-ttu-id="06ee8-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="06ee8-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)  
- [<span data-ttu-id="06ee8-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="06ee8-106">MailboxDataArray</span></span>](mailboxdataarray.md) 
- [<span data-ttu-id="06ee8-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="06ee8-107">MailboxData</span></span>](mailboxdata.md) 
- [<span data-ttu-id="06ee8-108">电子邮件（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="06ee8-108">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
  
```xml
<Email>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Email>
```

 <span data-ttu-id="06ee8-109">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="06ee8-109">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="06ee8-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="06ee8-110">Attributes and elements</span></span>

<span data-ttu-id="06ee8-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="06ee8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06ee8-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="06ee8-112">Attributes</span></span>

<span data-ttu-id="06ee8-113">无。</span><span class="sxs-lookup"><span data-stu-id="06ee8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06ee8-114">子元素</span><span class="sxs-lookup"><span data-stu-id="06ee8-114">Child elements</span></span>

|<span data-ttu-id="06ee8-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="06ee8-115">**Element**</span></span>|<span data-ttu-id="06ee8-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="06ee8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06ee8-117">名称（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="06ee8-117">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="06ee8-118">表示邮箱用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="06ee8-118">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="06ee8-119">Address （string）</span><span class="sxs-lookup"><span data-stu-id="06ee8-119">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="06ee8-120">表示邮箱用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="06ee8-120">Represents the e-mail address of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="06ee8-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="06ee8-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="06ee8-122">表示邮件的路由协议。</span><span class="sxs-lookup"><span data-stu-id="06ee8-122">Represents the routing protocol for the message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="06ee8-123">父元素</span><span class="sxs-lookup"><span data-stu-id="06ee8-123">Parent elements</span></span>

|<span data-ttu-id="06ee8-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="06ee8-124">**Element**</span></span>|<span data-ttu-id="06ee8-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="06ee8-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06ee8-126">MailboxData</span><span class="sxs-lookup"><span data-stu-id="06ee8-126">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="06ee8-127">代表单个邮箱用户以及有关邮箱用户要返回的数据类型的选项。</span><span class="sxs-lookup"><span data-stu-id="06ee8-127">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="06ee8-128">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="06ee8-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06ee8-129">备注</span><span class="sxs-lookup"><span data-stu-id="06ee8-129">Remarks</span></span>

<span data-ttu-id="06ee8-130">描述此元素的架构位于运行 MicrosoftExchange Server 2007 且安装了客户端访问服务器角色的计算机的/EWS/目录中。</span><span class="sxs-lookup"><span data-stu-id="06ee8-130">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06ee8-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="06ee8-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06ee8-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="06ee8-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06ee8-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="06ee8-133">Schema Name</span></span>  <br/> |<span data-ttu-id="06ee8-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="06ee8-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="06ee8-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="06ee8-135">Validation File</span></span>  <br/> |<span data-ttu-id="06ee8-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="06ee8-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="06ee8-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="06ee8-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="06ee8-138">False</span><span class="sxs-lookup"><span data-stu-id="06ee8-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06ee8-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="06ee8-139">See also</span></span>

- [<span data-ttu-id="06ee8-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="06ee8-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="06ee8-141">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="06ee8-141">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="06ee8-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="06ee8-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

