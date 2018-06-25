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
description: SecurityIdentifier 元素均表示安全描述符定义语言 (SDDL) 窗体的安全标识符 (SID)。
ms.openlocfilehash: c18d7d4505c618792497c32c7499eab9ac82989e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827314"
---
# <a name="securityidentifier"></a><span data-ttu-id="f74a5-103">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="f74a5-103">SecurityIdentifier</span></span>

<span data-ttu-id="f74a5-104">**SecurityIdentifier**元素均表示安全描述符定义语言 (SDDL) 窗体的安全标识符 ( [SID](sid.md))。</span><span class="sxs-lookup"><span data-stu-id="f74a5-104">The **SecurityIdentifier** element represents the security descriptor definition language (SDDL) form of a security identifier ( [SID](sid.md)).</span></span>
  
```xml
<SecurityIdentifier/>
```

 <span data-ttu-id="f74a5-105">**string**</span><span class="sxs-lookup"><span data-stu-id="f74a5-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f74a5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f74a5-106">Attributes and elements</span></span>

<span data-ttu-id="f74a5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f74a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f74a5-108">属性</span><span class="sxs-lookup"><span data-stu-id="f74a5-108">Attributes</span></span>

<span data-ttu-id="f74a5-109">无。</span><span class="sxs-lookup"><span data-stu-id="f74a5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f74a5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f74a5-110">Child elements</span></span>

<span data-ttu-id="f74a5-111">无。</span><span class="sxs-lookup"><span data-stu-id="f74a5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f74a5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f74a5-112">Parent elements</span></span>

|<span data-ttu-id="f74a5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f74a5-113">**Element**</span></span>|<span data-ttu-id="f74a5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f74a5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f74a5-115">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="f74a5-115">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="f74a5-116">代表单个安全标识符和 Active Directory 对象所在的组帐户成员属性。</span><span class="sxs-lookup"><span data-stu-id="f74a5-116">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> <span data-ttu-id="f74a5-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="f74a5-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SerializedSecurityContext/GroupSids/GroupIdentifier[i]` <br/> |
|[<span data-ttu-id="f74a5-118">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="f74a5-118">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="f74a5-119">表示组安全标识符和用户令牌内受限制的组的属性。</span><span class="sxs-lookup"><span data-stu-id="f74a5-119">Represents the group security identifier and attributes for a restricted group within a user token.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f74a5-120">注解</span><span class="sxs-lookup"><span data-stu-id="f74a5-120">Remarks</span></span>

<span data-ttu-id="f74a5-121">简单对象访问协议 (SOAP) 标头中使用此元素。</span><span class="sxs-lookup"><span data-stu-id="f74a5-121">This element is used in the Simple Object Access Protocol (SOAP) header.</span></span>
  
<span data-ttu-id="f74a5-122">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f74a5-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f74a5-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f74a5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f74a5-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f74a5-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f74a5-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f74a5-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f74a5-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="f74a5-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="f74a5-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f74a5-127">Validation File</span></span>  <br/> |<span data-ttu-id="f74a5-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f74a5-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f74a5-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f74a5-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="f74a5-130">False</span><span class="sxs-lookup"><span data-stu-id="f74a5-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f74a5-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f74a5-131">See also</span></span>



- [<span data-ttu-id="f74a5-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f74a5-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

