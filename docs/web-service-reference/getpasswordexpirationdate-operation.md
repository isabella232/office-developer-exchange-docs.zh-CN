---
title: GetPasswordExpirationDate 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: GetPasswordExpirationDate 操作提供当前用户的电子邮件帐户密码到期日期。
ms.openlocfilehash: 4184092cf98161e4c2f74446cef5439722ae71a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457891"
---
# <a name="getpasswordexpirationdate-operation"></a><span data-ttu-id="c90fe-103">GetPasswordExpirationDate 操作</span><span class="sxs-lookup"><span data-stu-id="c90fe-103">GetPasswordExpirationDate operation</span></span>

<span data-ttu-id="c90fe-104">**GetPasswordExpirationDate**操作提供当前用户的电子邮件帐户密码到期日期。</span><span class="sxs-lookup"><span data-stu-id="c90fe-104">The **GetPasswordExpirationDate** operation provides the email account password expiration date for the current user.</span></span> 
  
<span data-ttu-id="c90fe-105">此操作是在 Exchange Server 2010 Service Pack 1 （SP1）中引入的。</span><span class="sxs-lookup"><span data-stu-id="c90fe-105">This operation was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a><span data-ttu-id="c90fe-106">GetPasswordExpirationDate 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="c90fe-106">GetPasswordExpirationDate operation SOAP headers</span></span>

<span data-ttu-id="c90fe-107">**GetPasswordExpirationDate**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="c90fe-107">The **GetPasswordExpirationDate** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c90fe-108">**Header**</span><span class="sxs-lookup"><span data-stu-id="c90fe-108">**Header**</span></span>|<span data-ttu-id="c90fe-109">**元素**</span><span class="sxs-lookup"><span data-stu-id="c90fe-109">**Element**</span></span>|<span data-ttu-id="c90fe-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c90fe-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c90fe-111">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="c90fe-111">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="c90fe-112">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c90fe-112">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c90fe-113">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="c90fe-113">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="c90fe-114">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c90fe-114">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c90fe-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c90fe-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c90fe-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c90fe-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c90fe-117">标识操作请求的架构。</span><span class="sxs-lookup"><span data-stu-id="c90fe-117">Identifies the schema for the operation request.</span></span> <span data-ttu-id="c90fe-118">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c90fe-118">This is applicable to a request.</span></span> <span data-ttu-id="c90fe-119">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c90fe-119">This is applicable to a request.</span></span>  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a><span data-ttu-id="c90fe-120">GetPasswordExpirationDate 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="c90fe-120">GetPasswordExpirationDate operation request example</span></span>

### <a name="description"></a><span data-ttu-id="c90fe-121">说明</span><span class="sxs-lookup"><span data-stu-id="c90fe-121">Description</span></span>

<span data-ttu-id="c90fe-122">以下示例的**GetPasswordExpirationDate**操作请求显示如何获取电子邮件帐户的密码到期日期。</span><span class="sxs-lookup"><span data-stu-id="c90fe-122">The following example of a **GetPasswordExpirationDate** operation request shows how to get the password expiration date for an email account.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c90fe-123">代码</span><span class="sxs-lookup"><span data-stu-id="c90fe-123">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="c90fe-124">Request 元素</span><span class="sxs-lookup"><span data-stu-id="c90fe-124">Request elements</span></span>

<span data-ttu-id="c90fe-125">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="c90fe-125">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="c90fe-126">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="c90fe-126">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md)
    
- [<span data-ttu-id="c90fe-127">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="c90fe-127">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a><span data-ttu-id="c90fe-128">成功的 GetPasswordExpirationDate 操作响应</span><span class="sxs-lookup"><span data-stu-id="c90fe-128">Successful GetPasswordExpirationDate operation response</span></span>

<span data-ttu-id="c90fe-129">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="c90fe-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="c90fe-130">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="c90fe-130">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
    
- [<span data-ttu-id="c90fe-131">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="c90fe-131">PasswordExpirationDate</span></span>](passwordexpirationdate.md)
    

