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
description: MailboxSmtpAddress 元素表示要检索或更新其收件箱规则的用户的 SMTP 地址;或要检索其密码到期日期的或。
ms.openlocfilehash: 613e8098210257280bec47f2b22a2d29d04fa07c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530542"
---
# <a name="mailboxsmtpaddress"></a><span data-ttu-id="4b979-103">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="4b979-103">MailboxSmtpAddress</span></span>

<span data-ttu-id="4b979-104">**MailboxSmtpAddress**元素表示要检索或更新其收件箱规则的用户的 SMTP 地址;或要检索其密码到期日期的或。</span><span class="sxs-lookup"><span data-stu-id="4b979-104">The **MailboxSmtpAddress** element represents the SMTP address of the user whose Inbox rules are to be retrieved or updated; or whose password expiration date is to be retrieved.</span></span> 
  
```XML
<MailboxSmtpAddress/>
```

<span data-ttu-id="4b979-105">**string**</span><span class="sxs-lookup"><span data-stu-id="4b979-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4b979-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4b979-106">Attributes and elements</span></span>

<span data-ttu-id="4b979-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4b979-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b979-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4b979-108">Attributes</span></span>

<span data-ttu-id="4b979-109">无。</span><span class="sxs-lookup"><span data-stu-id="4b979-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b979-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4b979-110">Child elements</span></span>

<span data-ttu-id="4b979-111">无。</span><span class="sxs-lookup"><span data-stu-id="4b979-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4b979-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4b979-112">Parent elements</span></span>

|<span data-ttu-id="4b979-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4b979-113">**Element**</span></span>|<span data-ttu-id="4b979-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b979-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b979-115">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="4b979-115">GetInboxRules</span></span>](getinboxrules.md) <br/> |<span data-ttu-id="4b979-116">定义获取服务器存储中邮箱的收件箱规则的请求。</span><span class="sxs-lookup"><span data-stu-id="4b979-116">Defines a request to get the Inbox rules on a mailbox in the server store.</span></span>  <br/> |
|[<span data-ttu-id="4b979-117">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="4b979-117">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md) <br/> |<span data-ttu-id="4b979-118">定义获取电子邮件帐户的密码到期日期的请求。</span><span class="sxs-lookup"><span data-stu-id="4b979-118">Defines a request to get the password expiration date of an email account.</span></span>  <br/> |
|[<span data-ttu-id="4b979-119">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="4b979-119">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="4b979-120">定义更新服务器存储中的邮箱的收件箱规则的请求。</span><span class="sxs-lookup"><span data-stu-id="4b979-120">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4b979-121">文本值</span><span class="sxs-lookup"><span data-stu-id="4b979-121">Text value</span></span>

<span data-ttu-id="4b979-122">无。</span><span class="sxs-lookup"><span data-stu-id="4b979-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4b979-123">说明</span><span class="sxs-lookup"><span data-stu-id="4b979-123">Remarks</span></span>

<span data-ttu-id="4b979-124">**MailboxSmtpAddress**元素是一个可选元素。</span><span class="sxs-lookup"><span data-stu-id="4b979-124">The **MailboxSmtpAddress** element is an optional element.</span></span> <span data-ttu-id="4b979-125">如果省略**MailboxSmtpAddress**元素，则使用已登录用户的地址。</span><span class="sxs-lookup"><span data-stu-id="4b979-125">If the **MailboxSmtpAddress** element is omitted, the address of the logged on user is used.</span></span> 
  
<span data-ttu-id="4b979-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4b979-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b979-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="4b979-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b979-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="4b979-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4b979-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="4b979-129">Schema Name</span></span>  <br/> |<span data-ttu-id="4b979-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="4b979-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="4b979-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="4b979-131">Validation File</span></span>  <br/> |<span data-ttu-id="4b979-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4b979-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4b979-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="4b979-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b979-134">True</span><span class="sxs-lookup"><span data-stu-id="4b979-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b979-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b979-135">See also</span></span>

- [<span data-ttu-id="4b979-136">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="4b979-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)
- [<span data-ttu-id="4b979-137">GetPasswordExpirationDate 操作</span><span class="sxs-lookup"><span data-stu-id="4b979-137">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="4b979-138">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="4b979-138">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="4b979-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4b979-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

