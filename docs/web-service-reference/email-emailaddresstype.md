---
title: 电子邮件 (EmailAddressType)
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
ms.openlocfilehash: 0e7848d7c4f5001ed86b06d11af1d7623b4bf1f0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754037"
---
# <a name="email-emailaddresstype"></a><span data-ttu-id="fa4f9-103">电子邮件 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="fa4f9-103">Email (EmailAddressType)</span></span>

<span data-ttu-id="fa4f9-104">**Email**元素表示 GetUserAvailability 查询的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="fa4f9-104">The **Email** element represents the mailbox user for a GetUserAvailability query.</span></span> 
  
- [<span data-ttu-id="fa4f9-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="fa4f9-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)  
- [<span data-ttu-id="fa4f9-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="fa4f9-106">MailboxDataArray</span></span>](mailboxdataarray.md) 
- [<span data-ttu-id="fa4f9-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="fa4f9-107">MailboxData</span></span>](mailboxdata.md) 
- [<span data-ttu-id="fa4f9-108">电子邮件 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="fa4f9-108">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
  
```xml
<Email>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Email>
```

 <span data-ttu-id="fa4f9-109">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="fa4f9-109">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa4f9-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa4f9-110">Attributes and elements</span></span>

<span data-ttu-id="fa4f9-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa4f9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa4f9-112">属性</span><span class="sxs-lookup"><span data-stu-id="fa4f9-112">Attributes</span></span>

<span data-ttu-id="fa4f9-113">无。</span><span class="sxs-lookup"><span data-stu-id="fa4f9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa4f9-114">子元素</span><span class="sxs-lookup"><span data-stu-id="fa4f9-114">Child elements</span></span>

|<span data-ttu-id="fa4f9-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa4f9-115">**Element**</span></span>|<span data-ttu-id="fa4f9-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa4f9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa4f9-117">名称 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="fa4f9-117">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="fa4f9-118">代表邮箱用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="fa4f9-118">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="fa4f9-119">地址 （字符串）</span><span class="sxs-lookup"><span data-stu-id="fa4f9-119">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="fa4f9-120">代表邮箱用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="fa4f9-120">Represents the e-mail address of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="fa4f9-121">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="fa4f9-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="fa4f9-122">代表邮件路由的协议。</span><span class="sxs-lookup"><span data-stu-id="fa4f9-122">Represents the routing protocol for the message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa4f9-123">父元素</span><span class="sxs-lookup"><span data-stu-id="fa4f9-123">Parent elements</span></span>

|<span data-ttu-id="fa4f9-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa4f9-124">**Element**</span></span>|<span data-ttu-id="fa4f9-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa4f9-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa4f9-126">MailboxData</span><span class="sxs-lookup"><span data-stu-id="fa4f9-126">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="fa4f9-127">代表单个邮箱用户和类型的数据的选项，将返回有关邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="fa4f9-127">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="fa4f9-128">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="fa4f9-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa4f9-129">注解</span><span class="sxs-lookup"><span data-stu-id="fa4f9-129">Remarks</span></span>

<span data-ttu-id="fa4f9-130">描述此元素的架构位于运行 MicrosoftExchange Server 2007 的安装了客户端访问服务器角色的计算机的 /EWS/ 目录中。</span><span class="sxs-lookup"><span data-stu-id="fa4f9-130">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa4f9-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa4f9-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa4f9-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa4f9-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa4f9-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa4f9-133">Schema Name</span></span>  <br/> |<span data-ttu-id="fa4f9-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="fa4f9-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa4f9-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa4f9-135">Validation File</span></span>  <br/> |<span data-ttu-id="fa4f9-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa4f9-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa4f9-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa4f9-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa4f9-138">False</span><span class="sxs-lookup"><span data-stu-id="fa4f9-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa4f9-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa4f9-139">See also</span></span>

- [<span data-ttu-id="fa4f9-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="fa4f9-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="fa4f9-141">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="fa4f9-141">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="fa4f9-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="fa4f9-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

