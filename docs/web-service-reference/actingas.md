---
title: ActingAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ActingAs
api_type:
- schema
ms.assetid: 3896afff-5c2c-4eaf-8621-c70e0371ea78
description: ActingAs 元素标识呼叫者发送的人。
ms.openlocfilehash: 175a03018ee3529ec595dbe9afb7dc61ad6afc35
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529698"
---
# <a name="actingas"></a><span data-ttu-id="7e9fe-103">ActingAs</span><span class="sxs-lookup"><span data-stu-id="7e9fe-103">ActingAs</span></span>

<span data-ttu-id="7e9fe-104">**ActingAs**元素标识呼叫者发送的人。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-104">The **ActingAs** element identifies who the caller is sending as.</span></span> 
  
```xml
<ActingAs>
   <EmailAddress/>
   <RoutingType/>
</ActingAs>
```

 <span data-ttu-id="7e9fe-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="7e9fe-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e9fe-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7e9fe-106">Attributes and elements</span></span>

<span data-ttu-id="7e9fe-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e9fe-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7e9fe-108">Attributes</span></span>

<span data-ttu-id="7e9fe-109">无。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e9fe-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7e9fe-110">Child elements</span></span>

|<span data-ttu-id="7e9fe-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7e9fe-111">**Element**</span></span>|<span data-ttu-id="7e9fe-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e9fe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e9fe-113">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="7e9fe-113">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="7e9fe-p101">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-p101">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7e9fe-116">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="7e9fe-116">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="7e9fe-p102">定义用于邮箱路由。默认值为 SMTP。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-p102">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7e9fe-120">父元素</span><span class="sxs-lookup"><span data-stu-id="7e9fe-120">Parent elements</span></span>

|<span data-ttu-id="7e9fe-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="7e9fe-121">**Element**</span></span>|<span data-ttu-id="7e9fe-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e9fe-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e9fe-123">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e9fe-123">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="7e9fe-124">定义**GetServiceConfiguration**请求。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-124">Defines a **GetServiceConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e9fe-125">说明</span><span class="sxs-lookup"><span data-stu-id="7e9fe-125">Remarks</span></span>

<span data-ttu-id="7e9fe-126">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-126">This element is optional.</span></span> <span data-ttu-id="7e9fe-127">如果此元素不存在，则假定已通过身份验证的用户成为发件人。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-127">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="7e9fe-128">若要请求发件人提示，必须包含**ActingAs**元素。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-128">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="7e9fe-129">如果**ActingAs**元素缺失、不包含路由类型、不包含电子邮件地址、包含无效的电子邮件地址、不会解析为 Active Directory 域服务（AD ds）中的用户或解析为 AD ds 中的多个用户，则会在响应中返回**ErrorInvalidArgument**错误。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-129">An **ErrorInvalidArgument** error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span> 
  
<span data-ttu-id="7e9fe-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7e9fe-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e9fe-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="7e9fe-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e9fe-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="7e9fe-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7e9fe-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="7e9fe-133">Schema Name</span></span>  <br/> |<span data-ttu-id="7e9fe-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="7e9fe-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7e9fe-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="7e9fe-135">Validation File</span></span>  <br/> |<span data-ttu-id="7e9fe-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7e9fe-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7e9fe-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="7e9fe-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="7e9fe-138">False</span><span class="sxs-lookup"><span data-stu-id="7e9fe-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e9fe-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7e9fe-139">See also</span></span>

- [<span data-ttu-id="7e9fe-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7e9fe-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

