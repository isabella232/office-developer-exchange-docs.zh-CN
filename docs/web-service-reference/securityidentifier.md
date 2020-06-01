---
title: SecurityIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SecurityIdentifier
api_type:
- schema
ms.assetid: f7656729-f2c9-41cc-b1ec-60f480fc4dab
description: SecurityIdentifier 元素表示安全标识符（SID）的安全描述符定义语言（SDDL）形式。
ms.openlocfilehash: c55e4a7f7f0b8f8a40e6fcaf8d18e253a6da2679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468801"
---
# <a name="securityidentifier"></a><span data-ttu-id="e6458-103">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="e6458-103">SecurityIdentifier</span></span>

<span data-ttu-id="e6458-104">**SecurityIdentifier**元素表示安全标识符（ [SID](sid.md)）的安全描述符定义语言（SDDL）形式。</span><span class="sxs-lookup"><span data-stu-id="e6458-104">The **SecurityIdentifier** element represents the security descriptor definition language (SDDL) form of a security identifier ( [SID](sid.md)).</span></span>
  
```xml
<SecurityIdentifier/>
```

 <span data-ttu-id="e6458-105">**string**</span><span class="sxs-lookup"><span data-stu-id="e6458-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6458-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e6458-106">Attributes and elements</span></span>

<span data-ttu-id="e6458-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e6458-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6458-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e6458-108">Attributes</span></span>

<span data-ttu-id="e6458-109">无。</span><span class="sxs-lookup"><span data-stu-id="e6458-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6458-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e6458-110">Child elements</span></span>

<span data-ttu-id="e6458-111">无。</span><span class="sxs-lookup"><span data-stu-id="e6458-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e6458-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e6458-112">Parent elements</span></span>

|<span data-ttu-id="e6458-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e6458-113">**Element**</span></span>|<span data-ttu-id="e6458-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6458-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6458-115">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="e6458-115">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="e6458-116">代表帐户所属的 Active Directory 对象组的单个安全标识符和属性。</span><span class="sxs-lookup"><span data-stu-id="e6458-116">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> <span data-ttu-id="e6458-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="e6458-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SerializedSecurityContext/GroupSids/GroupIdentifier[i]` <br/> |
|[<span data-ttu-id="e6458-118">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="e6458-118">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="e6458-119">代表用户令牌中的受限制组的组安全标识符和属性。</span><span class="sxs-lookup"><span data-stu-id="e6458-119">Represents the group security identifier and attributes for a restricted group within a user token.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6458-120">备注</span><span class="sxs-lookup"><span data-stu-id="e6458-120">Remarks</span></span>

<span data-ttu-id="e6458-121">此元素在简单对象访问协议（SOAP）标头中使用。</span><span class="sxs-lookup"><span data-stu-id="e6458-121">This element is used in the Simple Object Access Protocol (SOAP) header.</span></span>
  
<span data-ttu-id="e6458-122">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e6458-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6458-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="e6458-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6458-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="e6458-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e6458-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="e6458-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e6458-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="e6458-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="e6458-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="e6458-127">Validation File</span></span>  <br/> |<span data-ttu-id="e6458-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e6458-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e6458-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="e6458-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6458-130">False</span><span class="sxs-lookup"><span data-stu-id="e6458-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6458-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6458-131">See also</span></span>



- [<span data-ttu-id="e6458-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e6458-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

