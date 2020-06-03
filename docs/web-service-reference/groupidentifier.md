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
description: GroupIdentifier 元素代表帐户所属的 Active Directory 目录服务对象组的单个安全标识符和属性。
ms.openlocfilehash: 8b427b9228cc5e66f46f70389acf2fa4bcd283b3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530801"
---
# <a name="groupidentifier"></a><span data-ttu-id="afdbc-103">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="afdbc-103">GroupIdentifier</span></span>

<span data-ttu-id="afdbc-104">**GroupIdentifier**元素代表帐户所属的 Active Directory 目录服务对象组的单个安全标识符和属性。</span><span class="sxs-lookup"><span data-stu-id="afdbc-104">The **GroupIdentifier** element represents a single security identifier and attribute for an Active Directory directory service object group of which the account is a member.</span></span> 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 <span data-ttu-id="afdbc-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="afdbc-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="afdbc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="afdbc-106">Attributes and elements</span></span>

<span data-ttu-id="afdbc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="afdbc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afdbc-108">属性</span><span class="sxs-lookup"><span data-stu-id="afdbc-108">Attributes</span></span>

|<span data-ttu-id="afdbc-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="afdbc-109">**Attribute**</span></span>|<span data-ttu-id="afdbc-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="afdbc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="afdbc-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="afdbc-111">**Attributes**</span></span> <br/> |<span data-ttu-id="afdbc-112">包含组属性。</span><span class="sxs-lookup"><span data-stu-id="afdbc-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="afdbc-113">子元素</span><span class="sxs-lookup"><span data-stu-id="afdbc-113">Child elements</span></span>

|<span data-ttu-id="afdbc-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="afdbc-114">**Element**</span></span>|<span data-ttu-id="afdbc-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="afdbc-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afdbc-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="afdbc-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="afdbc-117">表示表示组的安全标识符（[SID](sid.md)）的安全描述符定义语言（SDDL）形式。</span><span class="sxs-lookup"><span data-stu-id="afdbc-117">Represents the security descriptor definition language (SDDL) form of a security identifier ([SID](sid.md)) that represents the group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="afdbc-118">父元素</span><span class="sxs-lookup"><span data-stu-id="afdbc-118">Parent elements</span></span>

|<span data-ttu-id="afdbc-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="afdbc-119">**Element**</span></span>|<span data-ttu-id="afdbc-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="afdbc-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afdbc-121">GroupSids</span><span class="sxs-lookup"><span data-stu-id="afdbc-121">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="afdbc-122">表示用于组成令牌序列化帐户令牌的 Active Directory 组对象安全标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="afdbc-122">Represents a collection of Active Directory group object security identifiers that make up an account token for token serialization.</span></span> <span data-ttu-id="afdbc-123">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="afdbc-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afdbc-124">说明</span><span class="sxs-lookup"><span data-stu-id="afdbc-124">Remarks</span></span>

<span data-ttu-id="afdbc-125">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="afdbc-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afdbc-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="afdbc-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afdbc-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="afdbc-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="afdbc-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="afdbc-128">Schema Name</span></span>  <br/> |<span data-ttu-id="afdbc-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="afdbc-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="afdbc-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="afdbc-130">Validation File</span></span>  <br/> |<span data-ttu-id="afdbc-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="afdbc-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="afdbc-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="afdbc-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="afdbc-133">False</span><span class="sxs-lookup"><span data-stu-id="afdbc-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afdbc-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="afdbc-134">See also</span></span>



- [<span data-ttu-id="afdbc-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="afdbc-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

