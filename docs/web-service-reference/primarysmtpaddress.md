---
title: PrimarySmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PrimarySmtpAddress
api_type:
- schema
ms.assetid: eee79904-9412-4e61-b9b8-aff0ce25fade
description: PrimarySmtpAddress 元素表示用于服务器到服务器授权或委派访问权限的帐户的主要简单邮件传输协议 (SMTP) 地址。
ms.openlocfilehash: d33bf22af4ddf6b2f6d8d8d434168264acfaea7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2018
ms.locfileid: "19826881"
---
# <a name="primarysmtpaddress"></a><span data-ttu-id="c399a-103">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="c399a-103">PrimarySmtpAddress</span></span>

<span data-ttu-id="c399a-104">**PrimarySmtpAddress**元素表示用于服务器到服务器授权或委派访问权限的帐户的主要简单邮件传输协议 (SMTP) 地址。</span><span class="sxs-lookup"><span data-stu-id="c399a-104">The **PrimarySmtpAddress** element represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization or delegate access.</span></span> 
  
```xml
<PrimarySmtpAddress/>
```

 <span data-ttu-id="c399a-105">**PrimarySmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="c399a-105">**PrimarySmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c399a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c399a-106">Attributes and elements</span></span>

<span data-ttu-id="c399a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c399a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c399a-108">属性</span><span class="sxs-lookup"><span data-stu-id="c399a-108">Attributes</span></span>

<span data-ttu-id="c399a-109">无。</span><span class="sxs-lookup"><span data-stu-id="c399a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c399a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c399a-110">Child elements</span></span>

<span data-ttu-id="c399a-111">无。</span><span class="sxs-lookup"><span data-stu-id="c399a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c399a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c399a-112">Parent elements</span></span>

|<span data-ttu-id="c399a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c399a-113">**Element**</span></span>|<span data-ttu-id="c399a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c399a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c399a-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="c399a-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="c399a-116">代表用于模拟使用 ExchangeImpersonation SOAP 标头时的帐户。</span><span class="sxs-lookup"><span data-stu-id="c399a-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="c399a-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="c399a-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="c399a-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="c399a-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="c399a-119">用于服务器到服务器身份验证中的令牌序列化的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="c399a-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span>  <br/> |
|[<span data-ttu-id="c399a-120">用户 Id</span><span class="sxs-lookup"><span data-stu-id="c399a-120">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="c399a-121">标识委派用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="c399a-121">Identifies a delegate user or a user who has folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c399a-122">文本值</span><span class="sxs-lookup"><span data-stu-id="c399a-122">Text value</span></span>

<span data-ttu-id="c399a-123">需要安装一个代表 SMTP 地址的文本值。</span><span class="sxs-lookup"><span data-stu-id="c399a-123">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c399a-124">注解</span><span class="sxs-lookup"><span data-stu-id="c399a-124">Remarks</span></span>

<span data-ttu-id="c399a-125">Exchange Web 服务需要邮箱由的邮箱的主 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="c399a-125">Exchange Web Services requires that mailboxes be identified by the primary SMTP address of the mailbox.</span></span> <span data-ttu-id="c399a-126">不接受代理地址或其他地址。</span><span class="sxs-lookup"><span data-stu-id="c399a-126">Proxy or alternative addresses are not accepted.</span></span>
  
<span data-ttu-id="c399a-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c399a-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c399a-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="c399a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c399a-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="c399a-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c399a-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="c399a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="c399a-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="c399a-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="c399a-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="c399a-132">Validation File</span></span>  <br/> |<span data-ttu-id="c399a-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c399a-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c399a-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="c399a-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="c399a-135">False</span><span class="sxs-lookup"><span data-stu-id="c399a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c399a-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c399a-136">See also</span></span>



- [<span data-ttu-id="c399a-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c399a-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c399a-138">EWS 中的服务器到服务器授权</span><span class="sxs-lookup"><span data-stu-id="c399a-138">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)
  
[<span data-ttu-id="c399a-139">使用代理访问</span><span class="sxs-lookup"><span data-stu-id="c399a-139">Working with Delegate Access</span></span>](http://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

