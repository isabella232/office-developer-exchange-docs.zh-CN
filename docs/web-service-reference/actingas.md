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
description: ActingAs 元素标识谁将呼叫者发送为。
ms.openlocfilehash: 9c007ed45f85dba265261dd79a6fd846dbd9d2f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754278"
---
# <a name="actingas"></a><span data-ttu-id="d62d1-103">ActingAs</span><span class="sxs-lookup"><span data-stu-id="d62d1-103">ActingAs</span></span>

<span data-ttu-id="d62d1-104">**ActingAs**元素标识谁将呼叫者发送为。</span><span class="sxs-lookup"><span data-stu-id="d62d1-104">The **ActingAs** element identifies who the caller is sending as.</span></span> 
  
```xml
<ActingAs>
   <EmailAddress/>
   <RoutingType/>
</ActingAs>
```

 <span data-ttu-id="d62d1-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="d62d1-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d62d1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d62d1-106">Attributes and elements</span></span>

<span data-ttu-id="d62d1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d62d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d62d1-108">属性</span><span class="sxs-lookup"><span data-stu-id="d62d1-108">Attributes</span></span>

<span data-ttu-id="d62d1-109">无。</span><span class="sxs-lookup"><span data-stu-id="d62d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d62d1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d62d1-110">Child elements</span></span>

|<span data-ttu-id="d62d1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d62d1-111">**Element**</span></span>|<span data-ttu-id="d62d1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d62d1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d62d1-113">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="d62d1-113">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="d62d1-p101">定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d62d1-p101">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d62d1-116">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="d62d1-116">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="d62d1-p102">定义用于邮箱路由。默认值为 SMTP。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="d62d1-p102">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d62d1-120">父元素</span><span class="sxs-lookup"><span data-stu-id="d62d1-120">Parent elements</span></span>

|<span data-ttu-id="d62d1-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="d62d1-121">**Element**</span></span>|<span data-ttu-id="d62d1-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="d62d1-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d62d1-123">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d62d1-123">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="d62d1-124">定义**GetServiceConfiguration**请求。</span><span class="sxs-lookup"><span data-stu-id="d62d1-124">Defines a **GetServiceConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d62d1-125">备注</span><span class="sxs-lookup"><span data-stu-id="d62d1-125">Remarks</span></span>

<span data-ttu-id="d62d1-126">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="d62d1-126">This element is optional.</span></span> <span data-ttu-id="d62d1-127">如果此元素不存在，则假定为经过身份验证的用户为发件人。</span><span class="sxs-lookup"><span data-stu-id="d62d1-127">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="d62d1-128">**ActingAs**元素必须包含针对请求发件人提示。</span><span class="sxs-lookup"><span data-stu-id="d62d1-128">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="d62d1-129">如果**ActingAs**元素缺少，不包括路由类型，不包括电子邮件地址、 包含无效的电子邮件地址，不能解决 Active Directory 中的用户，可以在响应中返回**ErrorInvalidArgument**错误域服务 (AD DS) 或向 AD DS 中的多个用户解析。</span><span class="sxs-lookup"><span data-stu-id="d62d1-129">An **ErrorInvalidArgument** error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span> 
  
<span data-ttu-id="d62d1-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d62d1-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d62d1-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="d62d1-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d62d1-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="d62d1-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d62d1-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="d62d1-133">Schema Name</span></span>  <br/> |<span data-ttu-id="d62d1-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="d62d1-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d62d1-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="d62d1-135">Validation File</span></span>  <br/> |<span data-ttu-id="d62d1-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d62d1-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d62d1-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="d62d1-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="d62d1-138">False</span><span class="sxs-lookup"><span data-stu-id="d62d1-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d62d1-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d62d1-139">See also</span></span>

- [<span data-ttu-id="d62d1-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d62d1-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

