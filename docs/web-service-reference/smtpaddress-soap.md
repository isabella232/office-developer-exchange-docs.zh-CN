---
title: SmtpAddress (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e833351c-4bd9-4937-8752-c743a7ce57ea
description: SmtpAddress 元素均表示备用邮箱的 SMTP 地址。
ms.openlocfilehash: a5ece8906d337f356126f1bcb2c349699f41831d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827508"
---
# <a name="smtpaddress-soap"></a><span data-ttu-id="78c3a-103">SmtpAddress (SOAP)</span><span class="sxs-lookup"><span data-stu-id="78c3a-103">SmtpAddress (SOAP)</span></span>

<span data-ttu-id="78c3a-104">**SmtpAddress**元素均表示备用邮箱的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="78c3a-104">The **SmtpAddress** element represents the alternate mailbox SMTP address.</span></span> 
  
```XML
<SmtpAddress/>
```

<span data-ttu-id="78c3a-105">**string**</span><span class="sxs-lookup"><span data-stu-id="78c3a-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="78c3a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="78c3a-106">Attributes and elements</span></span>

<span data-ttu-id="78c3a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="78c3a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78c3a-108">属性</span><span class="sxs-lookup"><span data-stu-id="78c3a-108">Attributes</span></span>

<span data-ttu-id="78c3a-109">无。</span><span class="sxs-lookup"><span data-stu-id="78c3a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78c3a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="78c3a-110">Child elements</span></span>

<span data-ttu-id="78c3a-111">无。</span><span class="sxs-lookup"><span data-stu-id="78c3a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="78c3a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="78c3a-112">Parent elements</span></span>

|<span data-ttu-id="78c3a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="78c3a-113">**Element**</span></span>|<span data-ttu-id="78c3a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="78c3a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78c3a-115">AlternateMailbox (SOAP)</span><span class="sxs-lookup"><span data-stu-id="78c3a-115">AlternateMailbox (SOAP)</span></span>](alternatemailbox-soap.md) <br/> |<span data-ttu-id="78c3a-116">代表一个备用的邮箱。</span><span class="sxs-lookup"><span data-stu-id="78c3a-116">Represents an alternate mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="78c3a-117">文本值</span><span class="sxs-lookup"><span data-stu-id="78c3a-117">Text value</span></span>

<span data-ttu-id="78c3a-118">**SmtpAddress**元素的文本值是邮箱的备用的 SMTP 电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="78c3a-118">The text value of the **SmtpAddress** element is the SMTP email address of the alternate mailbox.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="78c3a-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="78c3a-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78c3a-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="78c3a-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="78c3a-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="78c3a-121">Schema Name</span></span>  <br/> |<span data-ttu-id="78c3a-122">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="78c3a-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="78c3a-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="78c3a-123">Validation File</span></span>  <br/> |<span data-ttu-id="78c3a-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="78c3a-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="78c3a-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="78c3a-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="78c3a-126">True</span><span class="sxs-lookup"><span data-stu-id="78c3a-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78c3a-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="78c3a-127">See also</span></span>

- [<span data-ttu-id="78c3a-128">Exchange 的自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="78c3a-128">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="78c3a-129">SOAP Exchange 2013 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="78c3a-129">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

