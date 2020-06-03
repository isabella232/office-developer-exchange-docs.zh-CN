---
title: ExchangeImpersonation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExchangeImpersonation
api_type:
- schema
ms.assetid: d8cbac49-47d0-4745-a2a7-545d33f8da93
description: 在请求的 SOAP 标头中使用 ExchangeImpersonation 元素。 存在此元素时，调用方将尝试模拟 ExchangeImpersonation 元素中包含的帐户。
ms.openlocfilehash: 188219d95453dc45378c6ca65ab93c2de7db4eac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463347"
---
# <a name="exchangeimpersonation"></a><span data-ttu-id="11f00-104">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="11f00-104">ExchangeImpersonation</span></span>

<span data-ttu-id="11f00-105">在请求的 SOAP 标头中使用**ExchangeImpersonation**元素。</span><span class="sxs-lookup"><span data-stu-id="11f00-105">The **ExchangeImpersonation** element is used in the SOAP header of a request.</span></span> <span data-ttu-id="11f00-106">存在此元素时，调用方将尝试模拟**ExchangeImpersonation**元素中包含的帐户。</span><span class="sxs-lookup"><span data-stu-id="11f00-106">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span> 
  
[<span data-ttu-id="11f00-107">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="11f00-107">ExchangeImpersonation</span></span>](exchangeimpersonation.md)
  
```xml
<ExchangeImpersonation>
   <ConnectingSID/>
</ExchangeImpersonation>
```

 <span data-ttu-id="11f00-108">**ExchangeImpersonationType**</span><span class="sxs-lookup"><span data-stu-id="11f00-108">**ExchangeImpersonationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11f00-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="11f00-109">Attributes and elements</span></span>

<span data-ttu-id="11f00-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="11f00-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11f00-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="11f00-111">Attributes</span></span>

<span data-ttu-id="11f00-112">无。</span><span class="sxs-lookup"><span data-stu-id="11f00-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11f00-113">子元素</span><span class="sxs-lookup"><span data-stu-id="11f00-113">Child elements</span></span>

|<span data-ttu-id="11f00-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="11f00-114">**Element**</span></span>|<span data-ttu-id="11f00-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="11f00-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11f00-116">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="11f00-116">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="11f00-117">表示在使用 ExchangeImpersonation SOAP 标头时要模拟的帐户。</span><span class="sxs-lookup"><span data-stu-id="11f00-117">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="11f00-118">父元素</span><span class="sxs-lookup"><span data-stu-id="11f00-118">Parent elements</span></span>

<span data-ttu-id="11f00-119">无。</span><span class="sxs-lookup"><span data-stu-id="11f00-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11f00-120">说明</span><span class="sxs-lookup"><span data-stu-id="11f00-120">Remarks</span></span>

<span data-ttu-id="11f00-121">对于包含要模拟的邮箱的邮箱数据库或 Active Directory User/Contact 对象，呼叫帐户必须在客户端访问服务器上和**ms-exch-MayImpersonate**权限中直接具有**exch-模拟**权限。</span><span class="sxs-lookup"><span data-stu-id="11f00-121">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory User/Contact object.</span></span> 
  
<span data-ttu-id="11f00-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="11f00-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11f00-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="11f00-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11f00-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="11f00-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="11f00-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="11f00-125">Schema name</span></span>  <br/> |<span data-ttu-id="11f00-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="11f00-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="11f00-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="11f00-127">Validation file</span></span>  <br/> |<span data-ttu-id="11f00-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="11f00-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="11f00-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="11f00-129">Can be empty</span></span>  <br/> |<span data-ttu-id="11f00-130">False</span><span class="sxs-lookup"><span data-stu-id="11f00-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11f00-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="11f00-131">See also</span></span>



[<span data-ttu-id="11f00-132">EWS 中的服务器到服务器授权</span><span class="sxs-lookup"><span data-stu-id="11f00-132">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

