---
title: MailboxSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: MailboxSmtpAddress 元素均表示要检索或更新; 其收件箱规则的用户的 SMTP 地址或者是要检索其密码到期日期。
ms.openlocfilehash: 60b2c018f2a05e9630e92e28de1054a421b41e52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826303"
---
# <a name="mailboxsmtpaddress"></a><span data-ttu-id="91447-103">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="91447-103">MailboxSmtpAddress</span></span>

<span data-ttu-id="91447-104">**MailboxSmtpAddress**元素均表示要检索或更新; 其收件箱规则的用户的 SMTP 地址或者是要检索其密码到期日期。</span><span class="sxs-lookup"><span data-stu-id="91447-104">The **MailboxSmtpAddress** element represents the SMTP address of the user whose Inbox rules are to be retrieved or updated; or whose password expiration date is to be retrieved.</span></span> 
  
```XML
<MailboxSmtpAddress/>
```

<span data-ttu-id="91447-105">**string**</span><span class="sxs-lookup"><span data-stu-id="91447-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="91447-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="91447-106">Attributes and elements</span></span>

<span data-ttu-id="91447-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="91447-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91447-108">属性</span><span class="sxs-lookup"><span data-stu-id="91447-108">Attributes</span></span>

<span data-ttu-id="91447-109">无。</span><span class="sxs-lookup"><span data-stu-id="91447-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91447-110">子元素</span><span class="sxs-lookup"><span data-stu-id="91447-110">Child elements</span></span>

<span data-ttu-id="91447-111">无。</span><span class="sxs-lookup"><span data-stu-id="91447-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="91447-112">父元素</span><span class="sxs-lookup"><span data-stu-id="91447-112">Parent elements</span></span>

|<span data-ttu-id="91447-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="91447-113">**Element**</span></span>|<span data-ttu-id="91447-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="91447-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91447-115">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="91447-115">GetInboxRules</span></span>](getinboxrules.md) <br/> |<span data-ttu-id="91447-116">定义一个请求以获取对邮箱服务器存储区中的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="91447-116">Defines a request to get the Inbox rules on a mailbox in the server store.</span></span>  <br/> |
|[<span data-ttu-id="91447-117">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="91447-117">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md) <br/> |<span data-ttu-id="91447-118">定义一个请求以获取的电子邮件帐户的密码到期日期。</span><span class="sxs-lookup"><span data-stu-id="91447-118">Defines a request to get the password expiration date of an email account.</span></span>  <br/> |
|[<span data-ttu-id="91447-119">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="91447-119">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="91447-120">定义更新中的邮箱服务器存储区中的收件箱规则的请求。</span><span class="sxs-lookup"><span data-stu-id="91447-120">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="91447-121">文本值</span><span class="sxs-lookup"><span data-stu-id="91447-121">Text value</span></span>

<span data-ttu-id="91447-122">无。</span><span class="sxs-lookup"><span data-stu-id="91447-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91447-123">注解</span><span class="sxs-lookup"><span data-stu-id="91447-123">Remarks</span></span>

<span data-ttu-id="91447-124">**MailboxSmtpAddress**元素是一个可选的元素。</span><span class="sxs-lookup"><span data-stu-id="91447-124">The **MailboxSmtpAddress** element is an optional element.</span></span> <span data-ttu-id="91447-125">如果省略**MailboxSmtpAddress**元素，则使用登录用户的地址。</span><span class="sxs-lookup"><span data-stu-id="91447-125">If the **MailboxSmtpAddress** element is omitted, the address of the logged on user is used.</span></span> 
  
<span data-ttu-id="91447-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="91447-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91447-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="91447-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91447-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="91447-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="91447-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="91447-129">Schema Name</span></span>  <br/> |<span data-ttu-id="91447-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="91447-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="91447-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="91447-131">Validation File</span></span>  <br/> |<span data-ttu-id="91447-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="91447-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="91447-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="91447-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="91447-134">True</span><span class="sxs-lookup"><span data-stu-id="91447-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91447-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="91447-135">See also</span></span>

- [<span data-ttu-id="91447-136">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="91447-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)
- [<span data-ttu-id="91447-137">GetPasswordExpirationDate 操作</span><span class="sxs-lookup"><span data-stu-id="91447-137">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="91447-138">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="91447-138">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="91447-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="91447-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

