---
title: SID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: SID 元素表示用于模拟或代理访问的帐户的安全标识符（SID）的安全描述符定义语言（SDDL）形式。
ms.openlocfilehash: 0e3f740e9a056f7c0042049d97757b5f2d3c441d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468045"
---
# <a name="sid"></a><span data-ttu-id="dfdf8-103">SID</span><span class="sxs-lookup"><span data-stu-id="dfdf8-103">SID</span></span>

<span data-ttu-id="dfdf8-104">**SID**元素表示用于模拟或代理访问的帐户的安全标识符（SID）的安全描述符定义语言（SDDL）形式。</span><span class="sxs-lookup"><span data-stu-id="dfdf8-104">The **SID** element represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation or delegate access.</span></span> 
  
```xml
<SID/>
```

 <span data-ttu-id="dfdf8-105">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="dfdf8-105">**SIDType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dfdf8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dfdf8-106">Attributes and elements</span></span>

<span data-ttu-id="dfdf8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dfdf8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dfdf8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dfdf8-108">Attributes</span></span>

<span data-ttu-id="dfdf8-109">无。</span><span class="sxs-lookup"><span data-stu-id="dfdf8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dfdf8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dfdf8-110">Child elements</span></span>

<span data-ttu-id="dfdf8-111">无。</span><span class="sxs-lookup"><span data-stu-id="dfdf8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dfdf8-112">父元素</span><span class="sxs-lookup"><span data-stu-id="dfdf8-112">Parent elements</span></span>

|<span data-ttu-id="dfdf8-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="dfdf8-113">**Element**</span></span>|<span data-ttu-id="dfdf8-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="dfdf8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfdf8-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="dfdf8-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="dfdf8-116">表示在使用 ExchangeImpersonation SOAP 标头时要模拟的帐户。</span><span class="sxs-lookup"><span data-stu-id="dfdf8-116">Represents an account to impersonate when using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="dfdf8-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="dfdf8-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="dfdf8-118">UserId</span><span class="sxs-lookup"><span data-stu-id="dfdf8-118">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="dfdf8-119">标识代理用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="dfdf8-119">Identifies a delegate user or a user with folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dfdf8-120">文本值</span><span class="sxs-lookup"><span data-stu-id="dfdf8-120">Text value</span></span>

<span data-ttu-id="dfdf8-121">文本值是 SID 的字符串表示形式。</span><span class="sxs-lookup"><span data-stu-id="dfdf8-121">The text value is a string representation of a SID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfdf8-122">备注</span><span class="sxs-lookup"><span data-stu-id="dfdf8-122">Remarks</span></span>

<span data-ttu-id="dfdf8-123">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dfdf8-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dfdf8-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="dfdf8-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dfdf8-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="dfdf8-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dfdf8-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="dfdf8-126">Schema Name</span></span>  <br/> |<span data-ttu-id="dfdf8-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="dfdf8-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="dfdf8-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="dfdf8-128">Validation File</span></span>  <br/> |<span data-ttu-id="dfdf8-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dfdf8-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dfdf8-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="dfdf8-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="dfdf8-131">False</span><span class="sxs-lookup"><span data-stu-id="dfdf8-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dfdf8-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dfdf8-132">See also</span></span>



- [<span data-ttu-id="dfdf8-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dfdf8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

