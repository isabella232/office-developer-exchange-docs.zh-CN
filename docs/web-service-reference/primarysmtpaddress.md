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
description: PrimarySmtpAddress 元素表示要用于服务器到服务器授权或代理访问的帐户的主要简单邮件传输协议（SMTP）地址。
ms.openlocfilehash: eea995b3e546d7e94e65cf9b230b639a781c4928
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467961"
---
# <a name="primarysmtpaddress"></a><span data-ttu-id="49b9e-103">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="49b9e-103">PrimarySmtpAddress</span></span>

<span data-ttu-id="49b9e-104">**PrimarySmtpAddress**元素表示要用于服务器到服务器授权或代理访问的帐户的主要简单邮件传输协议（SMTP）地址。</span><span class="sxs-lookup"><span data-stu-id="49b9e-104">The **PrimarySmtpAddress** element represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization or delegate access.</span></span> 
  
```xml
<PrimarySmtpAddress/>
```

 <span data-ttu-id="49b9e-105">**PrimarySmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="49b9e-105">**PrimarySmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49b9e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="49b9e-106">Attributes and elements</span></span>

<span data-ttu-id="49b9e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="49b9e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49b9e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="49b9e-108">Attributes</span></span>

<span data-ttu-id="49b9e-109">无。</span><span class="sxs-lookup"><span data-stu-id="49b9e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49b9e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="49b9e-110">Child elements</span></span>

<span data-ttu-id="49b9e-111">无。</span><span class="sxs-lookup"><span data-stu-id="49b9e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="49b9e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="49b9e-112">Parent elements</span></span>

|<span data-ttu-id="49b9e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="49b9e-113">**Element**</span></span>|<span data-ttu-id="49b9e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="49b9e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49b9e-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="49b9e-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="49b9e-116">表示在使用 ExchangeImpersonation SOAP 标头时要模拟的帐户。</span><span class="sxs-lookup"><span data-stu-id="49b9e-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="49b9e-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="49b9e-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="49b9e-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="49b9e-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="49b9e-119">在服务器到服务器身份验证中用于令牌序列化的 SOAP 标头中使用。</span><span class="sxs-lookup"><span data-stu-id="49b9e-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span>  <br/> |
|[<span data-ttu-id="49b9e-120">UserId</span><span class="sxs-lookup"><span data-stu-id="49b9e-120">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="49b9e-121">标识代理用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="49b9e-121">Identifies a delegate user or a user who has folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="49b9e-122">文本值</span><span class="sxs-lookup"><span data-stu-id="49b9e-122">Text value</span></span>

<span data-ttu-id="49b9e-123">需要一个代表 SMTP 地址的文本值。</span><span class="sxs-lookup"><span data-stu-id="49b9e-123">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49b9e-124">备注</span><span class="sxs-lookup"><span data-stu-id="49b9e-124">Remarks</span></span>

<span data-ttu-id="49b9e-125">Exchange Web 服务要求邮箱由邮箱的主 SMTP 地址标识。</span><span class="sxs-lookup"><span data-stu-id="49b9e-125">Exchange Web Services requires that mailboxes be identified by the primary SMTP address of the mailbox.</span></span> <span data-ttu-id="49b9e-126">不接受代理或备选地址。</span><span class="sxs-lookup"><span data-stu-id="49b9e-126">Proxy or alternative addresses are not accepted.</span></span>
  
<span data-ttu-id="49b9e-127">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="49b9e-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49b9e-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="49b9e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49b9e-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="49b9e-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49b9e-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="49b9e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="49b9e-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="49b9e-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="49b9e-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="49b9e-132">Validation File</span></span>  <br/> |<span data-ttu-id="49b9e-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="49b9e-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49b9e-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="49b9e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="49b9e-135">False</span><span class="sxs-lookup"><span data-stu-id="49b9e-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49b9e-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="49b9e-136">See also</span></span>



- [<span data-ttu-id="49b9e-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="49b9e-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="49b9e-138">EWS 中的服务器到服务器授权</span><span class="sxs-lookup"><span data-stu-id="49b9e-138">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)
  
[<span data-ttu-id="49b9e-139">使用代理访问</span><span class="sxs-lookup"><span data-stu-id="49b9e-139">Working with Delegate Access</span></span>](https://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

