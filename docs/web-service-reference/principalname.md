---
title: PrincipalName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PrincipalName
api_type:
- schema
ms.assetid: 88c142d4-0bc7-43ea-a997-d7200664d900
description: PrincipalName 元素表示要用于 Exchange 模拟的帐户的用户主体名称 (UPN)。
ms.openlocfilehash: d8557ce0435a11a5602372517db1f576028a9c97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826882"
---
# <a name="principalname"></a><span data-ttu-id="02f97-103">PrincipalName</span><span class="sxs-lookup"><span data-stu-id="02f97-103">PrincipalName</span></span>

<span data-ttu-id="02f97-104">**PrincipalName**元素表示要用于 Exchange 模拟的帐户的用户主体名称 (UPN)。</span><span class="sxs-lookup"><span data-stu-id="02f97-104">The **PrincipalName** element represents the user principal name (UPN) of the account to be used for Exchange impersonation.</span></span> 
  
```xml
<PrincipalName/>
```

 <span data-ttu-id="02f97-105">**PrincipalNameType**</span><span class="sxs-lookup"><span data-stu-id="02f97-105">**PrincipalNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02f97-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="02f97-106">Attributes and elements</span></span>

<span data-ttu-id="02f97-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="02f97-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02f97-108">属性</span><span class="sxs-lookup"><span data-stu-id="02f97-108">Attributes</span></span>

<span data-ttu-id="02f97-109">无。</span><span class="sxs-lookup"><span data-stu-id="02f97-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02f97-110">子元素</span><span class="sxs-lookup"><span data-stu-id="02f97-110">Child elements</span></span>

<span data-ttu-id="02f97-111">无。</span><span class="sxs-lookup"><span data-stu-id="02f97-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="02f97-112">父元素</span><span class="sxs-lookup"><span data-stu-id="02f97-112">Parent elements</span></span>

|<span data-ttu-id="02f97-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="02f97-113">**Element**</span></span>|<span data-ttu-id="02f97-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="02f97-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02f97-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="02f97-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="02f97-116">代表用于模拟使用 ExchangeImpersonation SOAP 标头时的帐户。</span><span class="sxs-lookup"><span data-stu-id="02f97-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="02f97-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="02f97-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="02f97-118">文本值</span><span class="sxs-lookup"><span data-stu-id="02f97-118">Text value</span></span>

<span data-ttu-id="02f97-119">文本值表示的用户的 UPN。</span><span class="sxs-lookup"><span data-stu-id="02f97-119">The text value represents the UPN of a user.</span></span> <span data-ttu-id="02f97-120">在 Active Directory 目录服务的用户对象上存在此值。</span><span class="sxs-lookup"><span data-stu-id="02f97-120">This value exists on the user object in the Active Directory directory service.</span></span> <span data-ttu-id="02f97-121">此部件包含用户登录名和域名标识所在的域中的用户帐户，采用以下格式： `someone@example.com`。</span><span class="sxs-lookup"><span data-stu-id="02f97-121">This contains the user logon name and a domain name that identifies the domain in which the user account is located, in the following format:  `someone@example.com`.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02f97-122">备注</span><span class="sxs-lookup"><span data-stu-id="02f97-122">Remarks</span></span>

<span data-ttu-id="02f97-123">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="02f97-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02f97-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="02f97-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02f97-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="02f97-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="02f97-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="02f97-126">Schema Name</span></span>  <br/> |<span data-ttu-id="02f97-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="02f97-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="02f97-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="02f97-128">Validation File</span></span>  <br/> |<span data-ttu-id="02f97-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="02f97-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="02f97-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="02f97-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="02f97-131">False</span><span class="sxs-lookup"><span data-stu-id="02f97-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02f97-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="02f97-132">See also</span></span>



- [<span data-ttu-id="02f97-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="02f97-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="02f97-134">EWS 中的服务器到服务器授权</span><span class="sxs-lookup"><span data-stu-id="02f97-134">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

