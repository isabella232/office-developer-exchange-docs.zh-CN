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
description: SID 元素表示用于模拟或委派访问权限的帐户的安全描述符定义语言 (SDDL) 窗体的安全标识符 (SID)。
ms.openlocfilehash: efcea42c12ec1d26ea31fdb8de337c37a2338a96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827492"
---
# <a name="sid"></a><span data-ttu-id="e7217-103">SID</span><span class="sxs-lookup"><span data-stu-id="e7217-103">SID</span></span>

<span data-ttu-id="e7217-104">**SID**元素表示用于模拟或委派访问权限的帐户的安全描述符定义语言 (SDDL) 窗体的安全标识符 (SID)。</span><span class="sxs-lookup"><span data-stu-id="e7217-104">The **SID** element represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation or delegate access.</span></span> 
  
```xml
<SID/>
```

 <span data-ttu-id="e7217-105">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="e7217-105">**SIDType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7217-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e7217-106">Attributes and elements</span></span>

<span data-ttu-id="e7217-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e7217-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7217-108">属性</span><span class="sxs-lookup"><span data-stu-id="e7217-108">Attributes</span></span>

<span data-ttu-id="e7217-109">无。</span><span class="sxs-lookup"><span data-stu-id="e7217-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7217-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e7217-110">Child elements</span></span>

<span data-ttu-id="e7217-111">无。</span><span class="sxs-lookup"><span data-stu-id="e7217-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e7217-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e7217-112">Parent elements</span></span>

|<span data-ttu-id="e7217-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e7217-113">**Element**</span></span>|<span data-ttu-id="e7217-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e7217-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7217-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="e7217-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="e7217-116">代表用于模拟使用 ExchangeImpersonation SOAP 标头时的帐户。</span><span class="sxs-lookup"><span data-stu-id="e7217-116">Represents an account to impersonate when using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="e7217-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="e7217-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="e7217-118">用户 Id</span><span class="sxs-lookup"><span data-stu-id="e7217-118">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="e7217-119">标识委派用户与文件夹访问权限。</span><span class="sxs-lookup"><span data-stu-id="e7217-119">Identifies a delegate user or a user with folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e7217-120">文本值</span><span class="sxs-lookup"><span data-stu-id="e7217-120">Text value</span></span>

<span data-ttu-id="e7217-121">文本值的字符串表示形式 SID。</span><span class="sxs-lookup"><span data-stu-id="e7217-121">The text value is a string representation of a SID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7217-122">备注</span><span class="sxs-lookup"><span data-stu-id="e7217-122">Remarks</span></span>

<span data-ttu-id="e7217-123">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e7217-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7217-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="e7217-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7217-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="e7217-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7217-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="e7217-126">Schema Name</span></span>  <br/> |<span data-ttu-id="e7217-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="e7217-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="e7217-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="e7217-128">Validation File</span></span>  <br/> |<span data-ttu-id="e7217-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e7217-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7217-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="e7217-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="e7217-131">False</span><span class="sxs-lookup"><span data-stu-id="e7217-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7217-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7217-132">See also</span></span>



- [<span data-ttu-id="e7217-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e7217-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

