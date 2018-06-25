---
title: GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4f958ed-9cf4-4ebf-9b01-e2df9a7cbd63
description: GetPasswordExpirationDate 元素定义一个请求以获取的电子邮件帐户的密码到期日期。 此元素是 GetPasswordExpirationDate 操作操作的基本元素。
ms.openlocfilehash: a9e0955566372f7b99c48c56e62ce2c5025f9f95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754645"
---
# <a name="getpasswordexpirationdate"></a><span data-ttu-id="5448c-104">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="5448c-104">GetPasswordExpirationDate</span></span>

<span data-ttu-id="5448c-105">**GetPasswordExpirationDate**元素定义一个请求以获取的电子邮件帐户的密码到期日期。</span><span class="sxs-lookup"><span data-stu-id="5448c-105">The **GetPasswordExpirationDate** element defines a request to get the password expiration date for an email account.</span></span> <span data-ttu-id="5448c-106">此元素是[GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md)操作的基本元素。</span><span class="sxs-lookup"><span data-stu-id="5448c-106">This element is the base element for the [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation.</span></span> 
  
```XML
<GetPasswordExpirationDate>
    <MailboxSmtpAddress/>
</GetPasswordExpirationDate>
```

 <span data-ttu-id="5448c-107">**GetPasswordExpirationDateType**</span><span class="sxs-lookup"><span data-stu-id="5448c-107">**GetPasswordExpirationDateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5448c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5448c-108">Attributes and elements</span></span>

<span data-ttu-id="5448c-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5448c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5448c-110">属性</span><span class="sxs-lookup"><span data-stu-id="5448c-110">Attributes</span></span>

<span data-ttu-id="5448c-111">无。</span><span class="sxs-lookup"><span data-stu-id="5448c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5448c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5448c-112">Child elements</span></span>

|<span data-ttu-id="5448c-113">**元素名**</span><span class="sxs-lookup"><span data-stu-id="5448c-113">**Element name**</span></span>|<span data-ttu-id="5448c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5448c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5448c-115">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="5448c-115">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="5448c-116">代表电子邮件帐户的密码到期日期要为其返回的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="5448c-116">Represents the email address of the email account for which the password expiration date is to be returned.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5448c-117">父元素</span><span class="sxs-lookup"><span data-stu-id="5448c-117">Parent elements</span></span>

<span data-ttu-id="5448c-118">无。</span><span class="sxs-lookup"><span data-stu-id="5448c-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5448c-119">备注</span><span class="sxs-lookup"><span data-stu-id="5448c-119">Remarks</span></span>

<span data-ttu-id="5448c-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5448c-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="5448c-121">Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5448c-121">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5448c-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="5448c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5448c-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="5448c-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5448c-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="5448c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="5448c-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="5448c-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5448c-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="5448c-126">Validation File</span></span>  <br/> |<span data-ttu-id="5448c-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5448c-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5448c-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="5448c-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="5448c-129">False</span><span class="sxs-lookup"><span data-stu-id="5448c-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5448c-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5448c-130">See also</span></span>



[<span data-ttu-id="5448c-131">GetPasswordExpirationDate 操作</span><span class="sxs-lookup"><span data-stu-id="5448c-131">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)


- [<span data-ttu-id="5448c-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5448c-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

