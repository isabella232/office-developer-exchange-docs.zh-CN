---
title: GroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIdentifier
api_type:
- schema
ms.assetid: bdc6fc1e-4979-42da-a35b-e3017988c7d3
description: GroupIdentifier 元素均表示一个安全标识符和 Active Directory 目录服务对象所在的组帐户成员属性。
ms.openlocfilehash: d73d72979762238ca09496cfbd6636b4ff44a969
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825767"
---
# <a name="groupidentifier"></a><span data-ttu-id="85235-103">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="85235-103">GroupIdentifier</span></span>

<span data-ttu-id="85235-104">**GroupIdentifier**元素均表示一个安全标识符和 Active Directory 目录服务对象所在的组帐户成员属性。</span><span class="sxs-lookup"><span data-stu-id="85235-104">The **GroupIdentifier** element represents a single security identifier and attribute for an Active Directory directory service object group of which the account is a member.</span></span> 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 <span data-ttu-id="85235-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="85235-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85235-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="85235-106">Attributes and elements</span></span>

<span data-ttu-id="85235-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="85235-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85235-108">属性</span><span class="sxs-lookup"><span data-stu-id="85235-108">Attributes</span></span>

|<span data-ttu-id="85235-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="85235-109">**Attribute**</span></span>|<span data-ttu-id="85235-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="85235-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85235-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="85235-111">**Attributes**</span></span> <br/> |<span data-ttu-id="85235-112">包含组属性。</span><span class="sxs-lookup"><span data-stu-id="85235-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85235-113">子元素</span><span class="sxs-lookup"><span data-stu-id="85235-113">Child elements</span></span>

|<span data-ttu-id="85235-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="85235-114">**Element**</span></span>|<span data-ttu-id="85235-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="85235-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85235-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="85235-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="85235-117">表示一个表示组的安全标识符 ([SID](sid.md)) 的安全描述符定义语言 (SDDL) 形式。</span><span class="sxs-lookup"><span data-stu-id="85235-117">Represents the security descriptor definition language (SDDL) form of a security identifier ([SID](sid.md)) that represents the group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="85235-118">父元素</span><span class="sxs-lookup"><span data-stu-id="85235-118">Parent elements</span></span>

|<span data-ttu-id="85235-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="85235-119">**Element**</span></span>|<span data-ttu-id="85235-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="85235-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85235-121">GroupSids</span><span class="sxs-lookup"><span data-stu-id="85235-121">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="85235-122">表示的 Active Directory 组对象安全标识符的令牌序列化帐户标记所组成的集合。</span><span class="sxs-lookup"><span data-stu-id="85235-122">Represents a collection of Active Directory group object security identifiers that make up an account token for token serialization.</span></span> <span data-ttu-id="85235-123">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="85235-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85235-124">备注</span><span class="sxs-lookup"><span data-stu-id="85235-124">Remarks</span></span>

<span data-ttu-id="85235-125">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="85235-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85235-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="85235-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85235-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="85235-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85235-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="85235-128">Schema Name</span></span>  <br/> |<span data-ttu-id="85235-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="85235-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="85235-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="85235-130">Validation File</span></span>  <br/> |<span data-ttu-id="85235-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85235-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85235-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="85235-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="85235-133">False</span><span class="sxs-lookup"><span data-stu-id="85235-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85235-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="85235-134">See also</span></span>



- [<span data-ttu-id="85235-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="85235-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

