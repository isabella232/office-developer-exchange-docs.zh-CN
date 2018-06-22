---
title: ConnectingSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: ConnectingSID 元素均表示用于模拟使用 ExchangeImpersonation SOAP 标头时的帐户。
ms.openlocfilehash: 6e0bb90e197ce22bcd982a6d51954a88f3a2cf03
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753488"
---
# <a name="connectingsid"></a><span data-ttu-id="a7a88-103">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="a7a88-103">ConnectingSID</span></span>

<span data-ttu-id="a7a88-104">**ConnectingSID**元素均表示用于模拟使用 ExchangeImpersonation SOAP 标头时的帐户。</span><span class="sxs-lookup"><span data-stu-id="a7a88-104">The **ConnectingSID** element represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span> 
  
[<span data-ttu-id="a7a88-105">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="a7a88-105">ExchangeImpersonation</span></span>](exchangeimpersonation.md)
  
[<span data-ttu-id="a7a88-106">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="a7a88-106">ConnectingSID</span></span>](connectingsid.md)
  
```xml
<ConnectingSID>
   <PrincipalName/>
</ConnectingSID>
```

 <span data-ttu-id="a7a88-107">**ConnectingSIDType**</span><span class="sxs-lookup"><span data-stu-id="a7a88-107">**ConnectingSIDType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7a88-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a7a88-108">Attributes and elements</span></span>

<span data-ttu-id="a7a88-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a7a88-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7a88-110">属性</span><span class="sxs-lookup"><span data-stu-id="a7a88-110">Attributes</span></span>

<span data-ttu-id="a7a88-111">无。</span><span class="sxs-lookup"><span data-stu-id="a7a88-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7a88-112">子元素</span><span class="sxs-lookup"><span data-stu-id="a7a88-112">Child elements</span></span>

|<span data-ttu-id="a7a88-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7a88-113">**Element**</span></span>|<span data-ttu-id="a7a88-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7a88-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7a88-115">PrincipalName</span><span class="sxs-lookup"><span data-stu-id="a7a88-115">PrincipalName</span></span>](principalname.md) <br/> |<span data-ttu-id="a7a88-116">代表要用于模拟使用的帐户的用户主体名称 (UPN)。</span><span class="sxs-lookup"><span data-stu-id="a7a88-116">Represents the user principal name (UPN) of the account to use for impersonation.</span></span> <span data-ttu-id="a7a88-117">这应该是的域用户帐户所在的 UPN。</span><span class="sxs-lookup"><span data-stu-id="a7a88-117">This should be the UPN for the domain where the user account exists.</span></span>  <br/> |
|[<span data-ttu-id="a7a88-118">SID</span><span class="sxs-lookup"><span data-stu-id="a7a88-118">SID</span></span>](sid.md) <br/> |<span data-ttu-id="a7a88-119">代表要用于模拟的帐户的安全描述符定义语言 (SDDL) 窗体的安全标识符 (SID)。</span><span class="sxs-lookup"><span data-stu-id="a7a88-119">Represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation.</span></span>  <br/> |
|[<span data-ttu-id="a7a88-120">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="a7a88-120">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="a7a88-121">代表要用于 Exchange 模拟的帐户的主要简单邮件传输协议 (SMTP) 地址。</span><span class="sxs-lookup"><span data-stu-id="a7a88-121">Represents the primary Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange impersonation.</span></span> <span data-ttu-id="a7a88-122">如果提供的主 SMTP 地址，则它将成本额外的 Active Directory 目录服务查找来获取用户的 SID。</span><span class="sxs-lookup"><span data-stu-id="a7a88-122">If the primary SMTP address is supplied, it will cost an extra Active Directory directory service lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="a7a88-123">我们建议您使用 SID 或 UPN 的它们是否可用。</span><span class="sxs-lookup"><span data-stu-id="a7a88-123">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
|[<span data-ttu-id="a7a88-124">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="a7a88-124">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="a7a88-125">代表要用于 Exchange 模拟的帐户的简单邮件传输协议 (SMTP) 地址。</span><span class="sxs-lookup"><span data-stu-id="a7a88-125">Represents the Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange Impersonation.</span></span> <span data-ttu-id="a7a88-126">如果提供的 SMTP 地址，则它将成本额外的 Active Directory 查找来获取用户的 SID。</span><span class="sxs-lookup"><span data-stu-id="a7a88-126">If the SMTP address is supplied, it will cost an extra Active Directory lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="a7a88-127">我们建议您使用 SID 或 UPN 的它们是否可用。</span><span class="sxs-lookup"><span data-stu-id="a7a88-127">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7a88-128">父元素</span><span class="sxs-lookup"><span data-stu-id="a7a88-128">Parent elements</span></span>

|<span data-ttu-id="a7a88-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7a88-129">**Element**</span></span>|<span data-ttu-id="a7a88-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7a88-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7a88-131">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="a7a88-131">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="a7a88-132">请求的 SOAP 标头中使用。</span><span class="sxs-lookup"><span data-stu-id="a7a88-132">Used in the SOAP header of a request.</span></span> <span data-ttu-id="a7a88-133">如果此元素存在，调用方尝试模拟**ExchangeImpersonation**元素中包含的帐户。</span><span class="sxs-lookup"><span data-stu-id="a7a88-133">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span>  <br/> <span data-ttu-id="a7a88-134">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="a7a88-134">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7a88-135">备注</span><span class="sxs-lookup"><span data-stu-id="a7a88-135">Remarks</span></span>

<span data-ttu-id="a7a88-136">调用帐户必须具有**ms exch 模拟**客户端访问服务器和**ms-exch MayImpersonate**上右右上也包含要模拟的邮箱的邮箱数据库或 Active Directory 用户或联系人对象。</span><span class="sxs-lookup"><span data-stu-id="a7a88-136">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory user or contact object.</span></span> 
  
<span data-ttu-id="a7a88-137">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a7a88-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7a88-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="a7a88-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7a88-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="a7a88-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7a88-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="a7a88-140">Schema name</span></span>  <br/> |<span data-ttu-id="a7a88-141">类型架构</span><span class="sxs-lookup"><span data-stu-id="a7a88-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7a88-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="a7a88-142">Validation file</span></span>  <br/> |<span data-ttu-id="a7a88-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a7a88-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7a88-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="a7a88-144">Can be empty</span></span>  <br/> |<span data-ttu-id="a7a88-145">False</span><span class="sxs-lookup"><span data-stu-id="a7a88-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7a88-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a7a88-146">See also</span></span>



[<span data-ttu-id="a7a88-147">EWS 中的服务器到服务器授权</span><span class="sxs-lookup"><span data-stu-id="a7a88-147">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

